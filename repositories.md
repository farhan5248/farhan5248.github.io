---
layout: page
title: Git Repositories & Maven Projects
permalink: /repositories/
---

There are 4 repositories
1. [**sheep-dog-ops**:][1] Contains deployment automation code for sheep-dog-* projects.
   - **sheep-dog-mgmt-maven-plugin**: The Maven release plug-in doesn't work for the xtext projects so I made this to mimic the behavior.

2. [**sheep-dog-qa**:][2] Contains the tests written in Asciidoc from which test automation is derived for the sheep-dog-local and sheep-dog-cloud projects. 
I think the tests should be in the Git repo as the code that is being tested so that I can run it easily. 
However if you have an end-to-end test which applies to several components, where do you keep them? For my QA team we kept the tests in one central repo. 
Also if you don't have end-to-end tests, where would you go to get a complete picture of the system if the tests serve as living documentation.
So to solve this problem, as is demonstrated with the code in these repos, tests applicable to a component can be queried via the API and transformed into test automation. 
That test automation is kept in the same repo as the code being tested but the specs are kept together.
   - **sheep-dog-specs**: Living documentation about the plug-ins. They are converted into test automation but also serve as documentation about what the plug-ins do.

3. [**sheep-dog-local**:][3] Eclipse and Maven plug-ins where all the code generation is done locally. 
This is what I had implemented for my team. That is, all the transformations were done on their laptops. 
I actually preferred to have them on a server but this approach allowed me to move without dependencies on external teams that controlled the infrastructure like the architecture teams. 
I think this approach is best in the beginning so testers can get started using the tools and only consider moving the code to the cloud when scaling up.
   - **sheep-dog-test**: Contains semantic validation rules. Used in the **sheepdogxtextplugin.parent** to demonstrate adding a dependency to the Xtext plug-in.
   - **sheepdogxtextplugin.parent**: Eclipse DSL plug-in that the testers use to write their test cases in the ubiquitous language.
   - **sheepdogxtextcukeplugin.parent**: Example of using Xtext to generate an API for a language like Cucumber feature files and Java code.
   - **sheep-dog-dev**: Converts the test cases into UML models and converts those into Cucumber and Java. It's all the transformation logic of converting docs to models to code and vice-versa.
   - **sheep-dog-maven-plugin**: Maven plug-in that's just a wrapper around **sheep-dog-dev**. 

4. [**sheep-dog-cloud**:][4] Eclipse and Maven plug-ins to help manual testers support developers adopting Deming driven testing. All the code generation is done remotely in k8s.
This project serves 2 purposes. One is to demonstrate how the code would be implemented as services. 
The second is to demonstrate how a monolithic code base is split into micro-services following an event-driven architecture. 
This was the original problem I was trying to solve, break up a large monolithic platform and have the QA tests executed earlier.
I'll document more about this in the [Specification By Prompt site][5]
   - **sheep-dog-dev-svc**: Currently wraps **sheep-dog-dev** as a Spring Boot service. This is going to be changed over the next few months to be several services and include **sheep-dog-test**.
   - **sheep-dog-dev-svc-maven-plugin**: Maven plug-in for **sheep-dog-dev-svc**.

[1]: https://github.com/farhan5248/sheep-dog-ops
[2]: https://github.com/farhan5248/sheep-dog-qa
[3]: https://github.com/farhan5248/sheep-dog-local
[4]: https://github.com/farhan5248/sheep-dog-cloud
[5]: /specificationbyprompt
