# Contribution
Hereby the complete contributions of Team Guava.

## Target Issues
Although Google Guava is an open source project, the maintainers of Guava do not encourage external contributions.[[1](#ec)] Since Guava is in wide usage among Googlers and external developers' understanding of the relation between Guava and whole Google's codebase is limited. We also learned how strict merge decision strategies are from issues and pull requests analysis. Based on above observations, we decided to select some potential issues that we were able to handle with from the issues posted by Guava team. Finally, we targeted at Guava's [issue 2365](https://github.com/google/guava/issues/2365). And we also contacted the person [@cpovirk](https://github.com/cpovirk) who posted the issue and asked him for help.

## Problem Specification
Guava's [Issue 2365](https://github.com/google/guava/issues/2365) is a **variable point** under two modules, `guava` and `guava-gwt`. From the codebase of Guava, this project has a core library `guava` and a separate module called `guava-gwt`. The module `guava` serves as the fundamental toolkit among the projects in Google while the module `guava-gwt` mainly focuses on Google Web Toolkit (GWT). The two modules have different dependencies thus leading to some conflicts. The annotation `@GwtIncompatible` is especially introduced to solve conflict issues between `guava` and `guava-gwt`.

The method `Stopwatch.toString` is one of the `@GwtIncompatible` examples (details refer to issue [#35](https://github.com/delftswa2016/team-guava/issues/35)). The cause of `@GwtIncompatible` of the method `Stopwatch.toString`is that `guava` uses `String.format()` from one Java standard library `java.util.concurrent.TimeUnit`; while this date and number formatting class is not available in `GWT` [2]. The only compatible date and number formatting classes are `com.google.gwt.i18n.client.NumberFormat` and `com.google.gwt.i18n.client.DateTimeFormat`.

## Contribution Specification
### Minor Contribution (Guava's issue [#24](https://github.com/delftswa2016/team-guava/issues/24))
#### Summary
We indirectly updated outdated information on Guava's  Wiki documentation `ContributorSetUp`.

#### Specification
When we set up our local clone repository, we found that there was a mismatch between guava GitHub repository and Google provided repository link. So we soon addressed this mismatch problem under Guava's [issue 2365](https://github.com/google/guava/issues/2365). [@cpovirk](https://github.com/cpovirk) replied that their `ContributorSetUp` page was outdated, and then he created [issue #2405](https://github.com/google/guava/issues/2365) under Guava project to address this mismatch problem. He also did some initial change in `ContibutionSetUp` page: changed Repositories URI from https://code.google.com/p/guava-libraries/ to https://github.com/google/guava.git.

### Stopwatch implementation under GWT (Guava's pr [#2437](https://github.com/google/guava/pull/2437/))
#### Summary
We implemented the `Stopwatch.toString()` method under GWT using a platform-specific method, and submitted a pull request to Guava's repository. The status now is waiting to be merged.

#### Specification
[@cpovirk](https://github.com/cpovirk) addressed the right file to modify which was `Platform.java` under `guava-gwt`; this method can solve the variable point between `guava` and `guava-gwt` elegantly.

What we did is following [@cpovirk](https://github.com/cpovirk) suggestions. (detailed solution refers to [delftswa2016/guava@276ed4c](https://github.com/delftswa2016/guava/commit/276ed4c757f69a7e098f16f555ccb30c3ecab305)). The main idea is as follows:

- convert `Stopwatch.toString` method to platform specified method `Platform.stopwatchToString`
- implement `stopwatchToString` under `guava-gwt` using `com.google.gwt.i18n.client.NumberFormat`
- keep two different versions of `stopwatchToString` methods via independent `Platform.java` classes under `guava` and `guava-gwt` packages.

After we had implemented the solution, we tested it under OS X El Capitan and Linux operation system. The all the tests passed. Finally, we posted our pull request to Guava's repository ([pr #2437](https://github.com/google/guava/pull/2437)).


## Reference
1. <div id="ec">K. Bourrillion, "The story with #guava and your patches", Plus.google.com, 2011. [Online]. Available: https://plus.google.com/113026104107031516488/posts/ZRdtjTL1MpM. [Accessed: 29-Mar-2016].

2. <div id="gwt">"GWT Project Formatting", Gwtproject.org. [Online]. Available: http://www.gwtproject.org/doc/latest/DevGuideCodingBasicsFormatting.html. [Accessed: 29-Mar-2016].
