# Architecture-Design
### Draft Document

This document is for gathering the information we have researched, in order to keep in one place. 
https://docs.google.com/document/d/1ye1I2SVFl36FhlXH07YL651DnFitNfRkhsAFTA1BKFY/edit?usp=sharing

## Work Update
| Date | Week | Description |
| :----: | :---: | :------------------------------------: |
| 5/4/2024 | Week 6 | Description, Identify Stakeholders, Quality Concerns |
| 18/4/2024 | Week 8 | introduction, Identify Stakeholders, Quality Concerns |
| 21/4/2024 | Week 9 | Architecture-Design Document 1.0| 

## Task Allocation
| Team Member | Tasks |
|:----------:|------------------------------------|
|Kevin|**Architecture Documentation and Visualization** <li>Responsible for writing the architecture documentation and creating architecture diagrams based on the recovered architecture information.</li>  <li>Clearly define the target audience and purpose of the documentation, use standardized architecture description languages and visualization tools, such as UML, to describe the system architecture.</li> |
|Meta |**Project Management and Coordination** <li>Responsible for the overall planning, coordination, and management of the architecture recovery project, ensuring the timely and successful completion of the project.</li>  <li>Define project goals and scope, create a timeline, assign tasks, monitor progress, organize meetings, and handle issues. Verification and Feedback</li> <li>Test and Evaluation Team: Responsible for verifying that the recovered architecture accurately reflects the actual structure and behavior of the system, and meets the initially set goals.</li> <li>Tasks: Design and execute architecture evaluation activities, such as case studies and performance tests, collect feedback, and make necessary adjustments based on the feedback. </li>|
|Julieta|**Documentation Collection and Analysis** <li>Responsible for gathering all relevant documents and materials, including technical documents, user manuals, and development guides.</li> <li> Organize and analyze the collected materials to provide necessary background information for the architecture recovery.</li>|
|Parkin| **Code Analysis** <li>Analyze the system's structure, components, and dependencies through code reviews and static analysis tools.</li> <li>Understand the runtime behavior and component interactions using test cases, log analysis, and performance monitoring.</li> <li> Combine automated tools and manual inspection to recover the software architecture from the codebase.</li>|


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
| :-------: | ------------------------------------ |
|Software Developers| <li>Maintainanility <li>Performance <li>Cross-Platform Compatibility|
|Mobile APP Development Companies| <li>Code Quality <li>Documentation quality <li>Ease of Contribution|
|Project Managers| <li>Time-to-Market <li>Development Cost <li>Resource Efficiency|
|End Users| <li>App Performance <li>Stability <li>Usability |
|Corporate Sponsors| <li>Security <li>Scalability <li>Long-term Viability|
|Open-Source Community| <li>Accessiblity of Contribution <li>Responsivenes to Community Feedback <li>Innovation and Feature Richness|


## 3 Overview of The Architecture

### 3.1 Early Architecture Design Decisions
The early architecture design decisions of the React Native framework were crucial in shaping its development philosophy and operational functionality. These decisions highlight how React Native bridges the gap between web technologies and native mobile development. Here are some key early architectural decisions:
| Early Architectural Decisions | Impact | Key Quality Attributes
| ------------------------------------ | ------------------------------------ | ------------------------------------|
| **1. Use of JavaScript:** To leverage JavaScript and the React library for building mobile apps. This choice was driven by the success of React in the web ecosystem and the growing popularity of JavaScript as a versatile programming language.| <li>**Positive impact:** This decision allowed web developers to use their existing JavaScript knowledge to build mobile applications, thereby reducing the learning curve and accelerating mobile development. <li>**Negative impact:** JavaScript's dynamic nature can introduce security vulnerabilities, such as injection attacks or other JavaScript-specific risks, requiring developers to be vigilant and implement additional security measures.| **Usability & Portability:** By leveraging JavaScript and React, React Native taps into the existing skill set of web developers, making it more accessible and reducing the learning curve. This decision enhances usability for developers and allows for code portability between web and mobile platforms.|
| **2. The Bridge:** Implementing a bridge that allows JavaScript code to communicate asynchronously with native code. This architecture enables the JavaScript thread to interact with native modules without blocking UI animations and responses.| <li> **Positive impact:** The bridge became a fundamental part of React Native’s architecture, ensuring smooth communication between JavaScript and native environments. However, it also introduced complexity and became a focus for performance optimization in later versions <li>**Negative impact:** The bridge, while enabling asynchronous communication between JavaScript and native code, introduces an additional layer of complexity and can become a performance bottleneck due to the serialization and deserialization of data as it crosses the bridge.| **Usability &  Portability:** By leveraging JavaScript and React, React Native taps into the existing skill set of web developers, making it more accessible and reducing the learning curve. This decision enhances usability for developers and allows for code portability between web and mobile platforms.|





