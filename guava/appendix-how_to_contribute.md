## How to Contribute [441/500 words]

Know that we have explained what Guava is, how can you as a reader contribute? Here is our advice on how to start and what pitfalls to avoid.

### Practical Guide to Contributing [213/250 words]

The Guava wiki page [**add ref**]( https://github.com/google/guava/wiki/ContributorSetUp) about contributing to the project on GitHub is quite outdated. As a matter of fact, we raised the issue while trying to do a contribution ourselves.  
The first step in order to take part to the development and maintenance of Guava is to sign the CLA Agreement[**add ref**]( https://cla.developers.google.com/about/google-individual?csw=1) in order to clarify the intellectual property of the code.

Cloning the repository and setting up the development environment is pretty straightforward. After having made a local copy of the project, using Eclipse as IDE the contributor would need to import it as an existing Maven project.

In order to check whether everything is working as expected, is useful to run (from command line or from the Eclipse Run configuration) `mvn install`, which takes care about building and testing the whole project. In order to skip tests, that on average take about 20 minutes to run on a modern laptop, pass the parameter `-DskipTests=True` to the previous command. 

Once everything is correctly set-up, the outline in the project section to the developer would appear as follows:

-	`guava-parent`, the “parent” project 
-	`guava`, the main repository
-	`guava-gwt`, the additional GWT-compatible code
-	`guava-testlib`, containing the test suite builder
-	`guava-tests`, containing the tests for the project

### What to expect [200/250 words]

We have dealt with the initial mismatching about the cloned repository and the one present on GitHub, because the Contributor set-up page was outdated as previously mentioned.

After having commented on the issue we tried to solve, we started to try to make changes in order to fix some bugs in Guava.
We had a bit of work to do in order to get enough understandings on how the code was structured and what we could do.
The interaction with the Guava team (in particular, @cpovrik) has been quite minimal, although it helped a lot in addressing the right part of the project to modify.

Working with the project is not trivial, due to the fact that it has some particular platform choices. In particular, we are referring to the platform-specific code behind a method in the Platform classes, that don’t immediately make sense if a developer has never seen them.

Also changes, except for trivial wiki changes, are not immediately added to the codebase. Rather several pull-requests are waiting to be merged [**add ref**] simply because the code is first applied to the internal Google repository [**add ref**] and then mirrored out. Contributing to Guava takes time and some patience.