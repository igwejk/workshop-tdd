# :octicons-mark-github-16: Test Driven Development

<!-- markdownlint-disable MD033 -->

!!! quote "Definition"

    > _Test-Driven Development (TDD) is a technique for building software that guides software development by writing tests. It was developed by Kent Beck in the late 1990's as part of Extreme Programming.[^1]_

In this workshop, we will often say TDD for brevity rather _Test Driven Development_.

## Test Driven Development Workflow

![SVG image of Test Driven Development workflow](./tdd.excalidraw.svg){ width="900" }

Martin Fowler further summarises the test driven development workflow into three simple steps[^1] that are repeatedly executed until the fulfillment of done criteria.

> - _Write a test for the next bit of functionality you want to add._
> - _Write the functional code until the test passes._
> - _Refactor both new and old code to make it well structured._

### TDD in Testing Strategy

What type or level of testing is relevant in test-driven development? -- The Wikipedia entry on test-driven development suggests that the test cases should be written at the unit-level[^2].

So, when we write functional tests to drive the development of our site, as we will do shortly, would our effort represent a correct application of the TDD technique? Here are the thoughts of some experts in the topic on that bit of introspection:

!!! quotes "Who cares?"

    > _Who cares? Was it an effective way to develop? Did you feel confident in the stability of the results when you were done? Were you able to take small steps?_
    >
    > _Also yes, that was TDD.[^5]_
    >
    > ~ Kent Beck

Kent Beck is credited with rediscovering test-driven development and making it a mainstream practice in the software development community.

!!! quotes "It doesn’t matter."

    > _It doesn’t matter._
    >
    > _Do you follow the process, Red ~> Green~> Refactor?_
    >
    > _Do you feel confident enough refactoring your system/site?_
    >
    > _Are your feedback cycles short enough for effective work?_
    >
    > _If you can answer all of these with a yes you do it right.[^6]_
    >
    > ~ Waldemar Kindler

Although a detailed discourse on test strategy is not in our focus, it is interesting to highlight the concept of test levels to bring consciousness to the approach we are adopting in this workshop and to keep us aware of alternative means.

??? abstract "Test strategy[^3]"

    > _A **test strategy** is an outline that describes the testing approach of the software development cycle. The purpose of a test strategy is to provide a rational deduction from organizational, high-level objectives to actual test activities to meet those objectives from a quality assurance perspective._

??? abstract "The different types of tests[^4]"

    > - **Unit tests**
    >
    >     Unit tests are very low level and close to the source of an application. They consist in testing individual methods and functions of the classes, components, or modules used by your software. Unit tests are generally quite cheap to automate and can run very quickly by a continuous integration server.
    >
    > - **Integration tests**
    >
    >     Integration tests verify that different modules or services used by your application work well together. For example, it can be testing the interaction with the database or making sure that microservices work together as expected. These types of tests are more expensive to run as they require multiple parts of the application to be up and running.
    >
    > - **Functional tests**
    >
    >     Functional tests focus on the business requirements of an application. They only verify the output of an action and do not check the intermediate states of the system when performing that action.
    >
    >     There is sometimes a confusion between integration tests and functional tests as they both require multiple components to interact with each other. The difference is that an integration test may simply verify that you can query the database while a functional test would expect to get a specific value from the database as defined by the product requirements.
    >
    > - **End-to-end tests**
    >
    >     End-to-end testing replicates a user behavior with the software in a complete application environment. It verifies that various user flows work as expected and can be as simple as loading a web page or logging in or much more complex scenarios verifying email notifications, online payments, etc...
    >
    >     End-to-end tests are very useful, but they're expensive to perform and can be hard to maintain when they're automated. It is recommended to have a few key end-to-end tests and rely more on lower level types of testing (unit and integration tests) to be able to quickly identify breaking changes.
    >
    > - **Acceptance testing**
    >
    >     Acceptance tests are formal tests that verify if a system satisfies business requirements. They require the entire application to be running while testing and focus on replicating user behaviors. But they can also go further and measure the performance of the system and reject changes if certain goals are not met.
    >
    > - **Performance testing**
    >
    >     Performance tests evaluate how a system performs under a particular workload. These tests help to measure the reliability, speed, scalability, and responsiveness of an application. For instance, a performance test can observe response times when executing a high number of requests, or determine how a system behaves with a significant amount of data. It can determine if an application meets performance requirements, locate bottlenecks, measure stability during peak traffic, and more.
    >
    > - **Smoke testing**
    >
    >     Smoke tests are basic tests that check the basic functionality of an application. They are meant to be quick to execute, and their goal is to give you the assurance that the major features of your system are working as expected.
    >
    >     Smoke tests can be useful right after a new build is made to decide whether or not you can run more expensive tests, or right after a deployment to make sure that they application is running properly in the newly deployed environment.

## Workshop

### :octicons-goal-16:{ style="color: pink" } Learning Objectives

- [x] Understand test driven development
- [x] Distinguish among different types of tests, and testing strategies
- [x] Apply test driven development

[^1]: :material-web: Martin Fowler, December 2023, [Test Driven Development](https://martinfowler.com/bliki/TestDrivenDevelopment.html)
[^2]: :simple-wikipedia: Wikipedia, May 2024, [Test-driven development](https://en.wikipedia.org/wiki/Test-driven_development)
[^3]: :simple-wikipedia: Wikipedia, October 2023, [Test strategy](https://en.wikipedia.org/wiki/Test_strategy)
[^4]: :simple-atlassian: Sten Pittet, [The different types of software testing](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
[^5]: :simple-x: Post by @igwejk, [Does any test count or just unit tests?](https://x.com/KentBeck/status/1795518645113933905)
[^6]: :simple-x: Post by @igwejk, [Is TDD actually unit test driven?](https://x.com/WaldemarKindler/status/1795211502787375285)
