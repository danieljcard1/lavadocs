# Always be Documenting: Effective Technical Writing in a Continuous Integration (CI) Environment
## Erik Rask
*Team Coordinator/Information Architect - Paligo*

**Contributed by Mary Frances Hull**

## Overview
In this presentation, you will learn:
1. How to adapt when product development changes processes.
2. Useful terms and concepts that will help you understand and contribute to the development conversation.
3. An example of how to leverage metadata from the source code of products.

Erik describes how for a long time, technical writers have been able to share a starting point and a deadline when
working in parallel with development teams. With the evolution of a more agile product release cycle though, working in parallel is no longer the norm. This may
create stress if the technical writers try to stick to a waterfall process for their documentation while development is using an agile method.

The following terms are used to identify decisions in an agile environment. For example, a product is usually built on a branch or a tag. Understanding these terms can be helpful for writers as they interact with developers and the devops teams.

**Key Terms**
+ **continuous integration** - getting new changes into the product quickly.
+ **continuous deployment** - rolling out changes as they happen.
+ **agile** - continuous integration, deployment, and release.
+ **release** - a stamped and approved version, bundled and ready to be used.
+ **commits** - small changes to code.
+ **repository** - consists of a bunch of files, organized as on a file system with a series of commits that detail what changed, when and by whom. In short, a history of changes.
+ **branches** - are similar to parallel histories; the code exists in different states at different times. One branch may be the main branch.
and another branch may be a feature branch where a bug is being worked on without disturbing the main branch.
+ **merges** - the difference between the two branches are reconciled and the merged branch contains everything that was in both branches.
+ **tags** - are labeling points in Git history. Tagging is generally used to capture a point in history that is used for a marked version release.
+ **pipelines** - events that are triggered when code is committed.

Erik demonstrated how metadata can be used in projects and how a workflow pipeline can then be created to pick up the correct metadata at the correct time. In this example, Erik used yang2doc to create DocBook content yang files. The code used in this presentation can be reviewed here: https://gitlab.com/lifeunleaded/yang2doc

Erik showed how updating and committing a file in GitLab, triggered a CI pipeline to convert the yang files to DocBooks and finally publish the HTML to the GitLab hosted pages.



## Key Takeaways

This presentation shows you how technical writers can create documentation to align with the CI working environment without having to go to the engineers all the time for information. It gives you an idea of what kind of manual work
can be offloaded by building documentation into the existing devops processes. It provides you with a set of key concepts and words that allows you to lead a conversation with the development and engineering teams.

To recap, to create the documentation pipeline, you will need three key pieces:
1. Find the metadata and/or ask the developers if there is a spot for it in their code.
2. Once you have the metadata, you can build XML out of it. Oftentimes, developers will provide the XML for you if they know what you want.
3. Now that you have the XML metadata, agree on where it will be stored and how it will be named so you can build a documentation pipeline to utilize it.

You might be used to documentation as a fixed process where user documentation is created after the product or feature is released. However, now technical writers can utilize
the automation process from the devops world. By utilizing this automation process, documentation can be delivered to the end-user on time versus after the fact.


## Reflection
I found this presentation to be very relevant in today's agile development world. Knowing the terms used in the agile environment will make it easier to
have discussions with the development teams. Having worked with CI pipelines before, it was easy for me to follow along with Erik's presentation, but he
also did an excellent job of stepping through a real-world example. It was interesting to see the process using pipelines to create real-time documentation as quickly as a feature is changed. Having a documentation pipeline, allows for automated documentation to be available at all times and up-to-date without any manual steps other than the initial setup of the pipeline. I look forward to using this process myself in the near future.
