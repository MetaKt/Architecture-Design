# Architecture-Design
### Draft Document

This document is for gathering the information we have researched, in order to keep in one place. 
https://docs.google.com/document/d/1ye1I2SVFl36FhlXH07YL651DnFitNfRkhsAFTA1BKFY/edit?usp=sharing

## Work Update
| Date | Week | Description |
| :----: | :---: | :------------------------------------: |
| 5/4/2024 | Week 6 | Description, Identify Stakeholders, Quality Concerns |
| 18/4/2024 | Week 8 | introduction, Identify Stakeholders, Quality Concerns |


## Abstract
This research paper delves into the software architecture of React Native, a prominent open-source framework for building mobile applications. Renowned for its cross-platform compatibility and efficiency, React Native empowers developers to create native-like experiences across iOS and Android platforms using a single codebase. 
This study focuses on analysing the architectural design of React Native, exploring its core components, data flow mechanisms, and integration with native APIs. By examining React Native's architecture, this paper aims to provide insights into its underlying principles maintability, scalability, and security for diverse mobile application development scenarios.

## 1 Introduction
### 1.1 Description
React Native is an open-source mobile application framework created by Facebook, enabling developers to build mobile apps using JavaScript and React. It aims to combine the best parts of native development with React, a best-in-class JavaScript library for building user interfaces. The framework allows for the development of applications for Android and iOS platforms with a single codebase, promoting code reuse, and speeding up the development process. It enables developers to create large web applications that can change data, without reloading the page. Emphasizes declarative programming, making the code more predictable and easier to debug.
<br>As React Native has been rapidly evolving and widely adopted, the complexity of its software architecture is also increasing. Software architecture recovery can help to gain a deeper understanding of the framework's design and implementation, and improve its maintainability, scalability, and security.
<br>
<br>**What is the story of React Native?**
<br>React Native was created by Jordan Walke, a software engineer at Facebook. It was first deployed on Facebook's News Feed in 2011 and later on Instagram.com in 2012.
React was open-sourced at JSConf US in May 2013. It has since become one of the most popular JavaScript libraries for web development, with a large community and ecosystem.
<br>
<br>**What is the importance of React Native in the Modern Web Development?**
<br>React's component-based architecture not only helps in building scalable applications but also makes it easier to maintain and update them.
It's used by many large companies and startups alike, proving its capability to handle complex applications efficiently.
React's ecosystem includes tools like Create React App, Next.js, and Gatsby, which help developers start projects quickly and incorporate best practices.
<br>
<br>React fundamentally changed the way developers build web applications by introducing an efficient and flexible model for constructing user interfaces.
Its emphasis on component reusability, the virtual DOM, and a vibrant ecosystem makes it a cornerstone technology for modern web development.
<br>

### 1.2 Proposed Architecture Recovery Steps
**1. Goal Setting and Requirement Gathering**
- Clearly define the purpose and requirements of the architecture recovery, including the specific problems to be solved and the target users (developers, project managers, etc.).
- Determine the types of architecture views to be recovered (e.g., module view, component-connector view, deployment view).

**2. Existing Documentation Collection**
- Gather all available documentation, including technical documents, development documents, and user manuals. Start with the official React Native documentation (https://reactnative.dev/docs/getting-started). It provides a solid foundation for understanding the framework's core concepts, architectural patterns, and best practices.
- Analyze the source code, especially the critical components and interfaces, to understand the system's structure and behavior. Dive into the React Native source code on GitHub (https://github.com/facebook/react-native). Look for comments, file structures, and module interactions to grasp how various parts collaborate. Consider using code navigation tools to explore the codebase efficiently.
- Search for existing architectural diagrams of React Native online. These can offer a high-level overview of the framework's components and their relationships.

**3. Tool and Method Selection**
- Select appropriate software architecture recovery tools for the React Native project, such as architecture recovery tools (e.g., Architexa, Lattix) and code analysis tools (e.g., SonarQube, CodeScene).
- Determine the suitable architecture recovery method for this project, such as the Scenario-based Architecture Analysis Method (SAAM), the Architecture Tradeoff Analysis Method (ATAM), or a combination of static and dynamic analysis.

**4. Architecture Recovery Implementation**
- Static Analysis: Recover the static architecture of the software by analyzing the source code, including module organization, class and component dependencies, etc.
- Dynamic Analysis: Understand the dynamic interaction and communication patterns between components by running the system and monitoring its behavior.
- Data Integration: Combine the results of static and dynamic analysis to build a comprehensive view of the architecture.

**5. Architecture Documentation**
- Create architecture documentation that describes the recovered architecture in detail, including architectural decisions, component descriptions, and interaction patterns.
- Use charts and models to visualize the architecture, such as UML diagrams.

**6. Verification and Feedback**
- Verify that the recovered architecture meets the initial goals and requirements.
- Present the recovered architecture and collect feedback from stakeholders, making necessary adjustments based on the feedback.

**7. Continuous Update**
- Software architecture is constantly evolving, so the results of the architecture recovery need to be regularly updated as the project progresses.

### 1.3 File structure
The file structure of this document will organized into the following chapters:

1. "Chapter 2: stakeholders Analysis"...
2. "Chapter 3: Viewpoints Analysis"...
3. "Chapter 4: Perspective Analysis"...


## 2 Stakeholders analysis
In this section we will analyze the stakeholders of React Native. 

### 2.1 Stakeholders
* **Meta (formerly Facebook):** They created React Native and are concerned with its long-term maintainability, performance across platforms, and fostering a healthy developer community.
* **Software Developers:** Developers using React Native are concerned with development speed, ease of learning, cross-platform compatibility, and access to a rich library of components and tools.
* **The Open-Source Community:** Contributors value code quality, adherence to best practices, modularity, and ease of contribution.
* **Mobile App Development Companies:** Companies using React Native prioritize development efficiency, app performance on target devices, and access to native functionalities.
* **End Users:** Users that use the applications developed with React Native.
* **Project Managers:** Oversee development projects using React Native.
* **Corporate Sponsors:** Companies that invest in React Native for their product development.
  
### 2.2 Quality Concerns from Each Type of Stakeholders
| Type of Stakeholders | Quality Concerns |
| :-------: | :------------------------------------: |
|Software Developers| Maintainanility & Performance & Cross-Platform Compatibility|
|Mobile APP Development Companies| Code Quality & Documentation quality & Ease of Contribution|
|Project Managers| Time-to-Market & Development Cost & Resource Efficiency|
|End Users| App Performance & Stability & Usability |
|Corporate Sponsors| Security & Scalability & Long-term Viability|
|Open-Source Community| Accessiblity of Contribution & Responsivenes to Community Feedback & Innovation and Feature Richness|

## Prioritizing Quality Concerns
**There are mainly 3 key quality(explained more into detail in the section) concerns are:**
1. Maintanability
2. Performance
3. Scalability
   
* **Performance and Stability:** Critical for end users, developers, and corporate sponsors.
* **Maintainability and Code Quality:** Essential for developers, contributors, and long-term viability.
* **Time-to-Market and Development Cost:** Important for project managers and corporate sponsors.
* **Security:** Non-negotiable for all stakeholders, especially corporate sponsors and end users.
* **Cross-platform Compatibility:** Key for developers and project managers to ensure wide reach

## Business Context 
* **Market Demand:**  The ever-growing demand for cross-platform mobile development tools that reduce development time and costs played a significant role in React Native's emergence. It allows companies to target both Android and iOS platforms with a single codebase, fostering faster development cycles and cost-efficiency.
* **Open-Source Model:**  React Native's open-source nature fosters rapid innovation and community engagement. This model allows developers worldwide to contribute to the framework's growth, identify and fix bugs, and create new features. This collaborative approach accelerates the development process and ensures the framework remains relevant in an ever-evolving mobile landscape.
* **Corporate Adoption:**  React Native's ability to streamline development processes and reduce costs has attracted numerous corporations. Companies can leverage a single codebase to target both Android and iOS users, saving development resources and time to market. This broader adoption by large corporations further fuels the growth and innovation within the React Native ecosystem.

## Technical Context
* **Cross-Platform Development:**  Maintaining consistent performance across different platforms with varying hardware capabilities can be challenging. Additionally, integrating native features specific to each platform requires careful implementation strategies.
* **Ecosystem Complexity:**  The vast array of available plugins and third-party libraries can be overwhelming. Careful management and selection of the appropriate libraries are crucial to ensure project stability and avoid compatibility issues.
* **Rapid Evolution:**  The React Native ecosystem, including the framework itself and its supporting libraries, evolves rapidly. Developers need to stay updated with these advancements to ensure their skills and applications remain relevant

## Programming Language used in React Native

React Native primarily uses JavaScript for building the user interface (UI) components of mobile apps. This allows developers to leverage their existing JavaScript knowledge for mobile development. React Native also utilizes XML-like syntax called JSX (JavaScript XML) to structure UI components within JavaScript code. While JavaScript is the main language for UI development, native languages like Java (Android) and Swift (iOS) are used for platform-specific functionalities.

## Early Architecture Design Decisions
| Decisions | :Descriptions: | :Rationales: |
|:------------------------------------:|:------------------------------------|:------------------------------------|
|Bridge-Based Communication|To facilitate communication between the JavaScript code running in the JavaScript engine (like V8 for Android or JavaScriptCore for iOS) and the native platform code (Objective-C for iOS, Java for Android), React Native uses a bridge.|This design allows for the development of applications using JavaScript while still accessing the full suite of native platform capabilities. It provides a flexible architecture that supports the React paradigm of declarative components while enabling high performance for native device features.|







