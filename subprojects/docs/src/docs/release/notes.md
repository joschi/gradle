The Gradle team is excited to announce Gradle @version@.

This release continues on the series of performance improvements, particularly for incremental builds. File-system watching introduced in Gradle 6.5 is [now ready for production use](#file-system-watching-is-ready-for-production-use). You can expect up to 20% build speed improvements on large projects when turning this feature on. Additionally, the experimental [configuration cache](#configuration-cache-improvements) has been improved to make troubleshooting easier for early adopters.

This release introduces [Java toolchain APIs](#toolchains-for-jvm-projects) that make it much easier to build JVM projects using a different version of Java than the one Gradle is running on. Gradle itself can now run on [Java 15](#support-for-java-15). 

Gradle's dependency management includes support for [compile only API dependencies](#compile-only-api-dependencies-for-jvm-libraries), [version ranges in repository content filtering](#version-ranges-in-repository-content-filtering) and the ability to [ignore selected dependencies in dependency locking](#ignore-dependencies-in-dependency-lock-state). 

This release also includes additional guidance and new samples for [managing build complexity over time](#managing-build-complexity). When starting new projects, [`gradle init`](#gradle-init) now generates sample projects that follow our latest recommendations and best practices. 

We would like to thank the following community contributors to this release of Gradle:

<!-- 
Include only their name, impactful features should be called out separately below.
 [Some person](https://github.com/some-person)
-->

## Upgrade instructions

Switch your build to use Gradle @version@ by updating your wrapper:

`./gradlew wrapper --gradle-version=@version@`

See the [Gradle 6.x upgrade guide](userguide/upgrading_version_6.html#changes_@baseVersion@) to learn about deprecations, breaking changes and other considerations when upgrading to Gradle @version@. 

For Java, Groovy, Kotlin and Android compatibility, see the [full compatibility notes](userguide/compatibility.html).

<!-- Do not add breaking changes or deprecations here! Add them to the upgrade guide instead. --> 

<!-- 
Add release features here!
## 1

details of 1

## 2

details of 2

## n
-->

## Documentation and samples

### New samples

The [sample index](samples/index.html) includes new samples, with step-by-step instructions on how to get started with Gradle for different project types and programming languages:

- Building an application with libraries:
[Java](samples/sample_building_java_applications_multi_project.html),
[Groovy](samples/sample_building_groovy_applications_multi_project.html),
[Scala](samples/sample_building_scala_applications_multi_project.html),
[Kotlin](samples/sample_building_kotlin_applications_multi_project.html)
- Building a simple application:
[Java](samples/sample_building_java_applications.html),
[Groovy](samples/sample_building_groovy_applications.html),
[Scala](samples/sample_building_scala_applications.html),
[Kotlin](samples/sample_building_kotlin_applications.html),
[C++](samples/sample_building_cpp_applications.html),
[Swift](samples/sample_building_swift_applications.html)
- Building a single library:
[Java](samples/sample_building_java_libraries.html),
[Groovy](samples/sample_building_groovy_libraries.html),
[Scala](samples/sample_building_scala_libraries.html),
[Kotlin](samples/sample_building_kotlin_libraries.html),
[C++](samples/sample_building_cpp_libraries.html),
[Swift](samples/sample_building_swift_libraries.html)

### Authoring multi-project builds 

We've reworked our documentation for [authoring multi-project builds](userguide/multi_project_builds.html). We also have some [new guidance on how to share build logic between subprojects](userguide/sharing_build_logic_between_subprojects.html#sec:convention_plugins) with [convention plugins](samples/sample_convention_plugins.html).

## Promoted features
Promoted features are features that were incubating in previous versions of Gradle but are now supported and subject to backwards compatibility.
See the User Manual section on the “[Feature Lifecycle](userguide/feature_lifecycle.html)” for more information.

* [File system watching is now stable](#file-system-watching-is-ready-for-production-use)

## Fixed issues

## Known issues

Known issues are problems that were discovered post release that are directly related to changes made in this release.

## External contributions

We love getting contributions from the Gradle community. For information on contributing, please see [gradle.org/contribute](https://gradle.org/contribute).

## Reporting Problems

If you find a problem with this release, please file a bug on [GitHub Issues](https://github.com/gradle/gradle/issues) adhering to our issue guidelines. 
If you're not sure you're encountering a bug, please use the [forum](https://discuss.gradle.org/c/help-discuss).

We hope you will build happiness with Gradle, and we look forward to your feedback via [Twitter](https://twitter.com/gradle) or on [GitHub](https://github.com/gradle).
