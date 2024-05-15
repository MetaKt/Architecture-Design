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
|Kevin|**Architecture Documentation and Visualization** <li>Responsible for writing the architecture documentation and creating architecture diagrams based on the recovered architecture information.</li>  <li>Clearly define the target audience and purpose of the documentation, and use standardized architecture description languages and visualization tools, such as UML, to describe the system architecture.</li> |
|Meta |**Project Management and Coordination** <li>Responsible for the overall planning, coordination, and management of the architecture recovery project, ensuring the timely and successful completion of the project.</li>  <li>Define project goals and scope, create a timeline, assign tasks, monitor progress, organize meetings, and handle issues. Verification and Feedback</li> <li>Test and Evaluation Team: Responsible for verifying that the recovered architecture accurately reflects the actual structure and behavior of the system, and meets the initially set goals.</li> <li>Tasks: Design and execute architecture evaluation activities, such as case studies and performance tests, collect feedback and make necessary adjustments based on the feedback. </li>|
|Julieta|**Documentation Collection and Analysis** <li>Responsible for gathering all relevant documents and materials, including technical documents, user manuals, and development guides.</li> <li> Organize and analyze the collected materials to provide necessary background information for the architecture recovery.</li>|
|Parkin| **Code Analysis** <li>Analyze the system's structure, components, and dependencies through code reviews and static analysis tools.</li> <li>Understand the runtime behavior and component interactions using test cases, log analysis, and performance monitoring.</li> <li> Combine automated tools and manual inspection to recover the software architecture from the codebase.</li>|


## Abstract
This research paper delves into the software architecture of React Native, a prominent open-source framework for building mobile applications. Renowned for its cross-platform compatibility and efficiency, React Native empowers developers to create native-like experiences across iOS and Android platforms using a single codebase. 
This study focuses on analyzing the architectural design of React Native, exploring its core components, data flow mechanisms, and integration with native APIs. By examining React Native's architecture, this paper aims to provide insights into its underlying principles of maintainability, scalability, and security for diverse mobile application development scenarios.

## 1 Introduction
### 1.1 Purpose of the Documentation
This documentation is created to provide a comprehensive understanding of the React Native framework's architecture. The goal is to equip developers, project managers, and stakeholders with in-depth knowledge of the structural and operational aspects of React Native, enabling them to effectively build, maintain, and enhance mobile applications using this technology. Additionally, this document aims to serve as an educational tool for those new to React Native, offering a detailed guide to its core components and operational mechanics.
<br>

### 1.2 File organization
**The file structure of this document will be organized into the following chapters:**
"Chapter 2: Stakeholders & Requirement Analysis"...
"Chapter 3: Overview of the Architecture "...
"Chapter 4: React Native Architecture Patterns and Tactics"...
"Chapter 5: Conclusion"...
<br>

### 1.3 Overview of React Native
React Native is an open-source mobile application framework created by Meta (Facebook), enabling developers to build mobile apps using JavaScript and React. It aims to combine the best parts of native development with React, a best-in-class JavaScript library for building user interfaces. The framework allows for the development of applications for Android and iOS platforms with a single codebase, promoting code reuse, and speeding up the development process. It enables developers to create large web applications that can change data, without reloading the page. Emphasizes declarative programming, making the code more predictable and easier to debug.
As React Native has been rapidly evolving and widely adopted, the complexity of its software architecture is also increasing. Software architecture recovery can help to gain a deeper understanding of the framework's design and implementation and improve its maintainability, Extensibility, and security.
<br>

**1.3.1 What is the story of React Native?**
React Native was created by Jordan Walke, a software engineer at Facebook. It was first deployed on Facebook's News Feed in 2011 and later on Instagram.com in 2012. React was open-sourced at JSConf US in May 2013. It has since become one of the most popular JavaScript libraries for web development, with a large community and ecosystem. Meta Platforms, Inc. (formerly known as Facebook) is still the owner of the React Native framework.
<br>

**1.3.2 What is the importance of React Native in the Modern Web Development?**
React's component-based architecture not only helps in building scalable applications but also makes it easier to maintain and update them. It's used by many large companies and startups alike, proving its capability to handle complex applications efficiently. React's ecosystem includes tools like Create React App, Next.js, and Gatsby, which help developers start projects quickly and incorporate best practices.

React fundamentally changed the way developers build web applications by introducing an efficient and flexible model for constructing user interfaces. Its emphasis on component reusability, the virtual DOM, and a vibrant ecosystem makes it a cornerstone technology for modern web development.

**1.3.3 Relationship between React and React Native**
|Properties|Descriptions|
| :------: | :--------: |
| Shared Principles | React Native adopts the same basic principles of React, such as declarative components and a component-driven architecture. This means developers can apply the same method of creating interfaces in React to structure mobile applications. |
| Platform-Specific Extensions | While React targets browser environments, translating JSX into DOM updates, React Native extends this by mapping JSX to native platform components. It uses a bridge to communicate between the native platform and JavaScript code, rendering native application components instead of web components.|
| Unified Development Experience | Both React and React Native aim to streamline and unify the development experience. Developers can use similar patterns and techniques across web and mobile platforms, facilitating a more cohesive development process.|

React Native's architecture is designed to allow developers to leverage the expressive power and flexibility of JavaScript while retaining the performance and feel of native applications. This combination has made React Native a popular choice among developers looking to create cross-platform applications with a single codebase.

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

The early design decisions of the React Native framework can be directly linked to key quality attributes, showcasing how each decision impacts the framework's usability, performance, maintainability, and other aspects critical to its success. These decisions and their impacts underline the strategic thinking behind React Native's architecture, focusing on creating a powerful yet user-friendly cross-platform mobile development environment. Each decision not only addresses specific technical challenges but also strategically aligns with broader goals such as enhancing developer engagement and ensuring high-performance application delivery.

Here are some key early architectural decisions:
| Early Architectural Decisions | Impact | Key Quality Attributes
| ------------------------------------ | ------------------------------------ | ------------------------------------|
| **1. Use of JavaScript:** To leverage JavaScript and the React library for building mobile apps. This choice was driven by the success of React in the web ecosystem and the growing popularity of JavaScript as a versatile programming language.| <li>**Positive impact:** This decision allowed web developers to use their existing JavaScript knowledge to build mobile applications, thereby reducing the learning curve and accelerating mobile development. <li>**Negative impact:** JavaScript's dynamic nature can introduce security vulnerabilities, such as injection attacks or other JavaScript-specific risks, requiring developers to be vigilant and implement additional security measures.| **Usability & Portability:** By leveraging JavaScript and React, React Native taps into the existing skill set of web developers, making it more accessible and reducing the learning curve. This decision enhances usability for developers and allows for code portability between web and mobile platforms.|
| **2. The Bridge:** Implementing a bridge that allows JavaScript code to communicate asynchronously with native code. This architecture enables the JavaScript thread to interact with native modules without blocking UI animations and responses.| <li> **Positive impact:** The bridge became a fundamental part of React Native’s architecture, ensuring smooth communication between JavaScript and native environments. However, it also introduced complexity and became a focus for performance optimization in later versions <li>**Negative impact:** The bridge, while enabling asynchronous communication between JavaScript and native code, introduces an additional layer of complexity and can become a performance bottleneck due to the serialization and deserialization of data as it crosses the bridge.| **Usability &  Portability:** By leveraging JavaScript and React, React Native taps into the existing skill set of web developers, making it more accessible and reducing the learning curve. This decision enhances usability for developers and allows for code portability between web and mobile platforms.|
| **3. Native Components:** React Native components compile to native components, using native UI controllers instead of web views.| <li>**Positive impact:** This approach ensures that applications not only feel native but also perform efficiently by utilizing the inherent capabilities of the underlying platform. <li> **Negative impact:** Although compiling to native components provides a high-quality user experience, it increases the complexity of the architecture, as developers need to understand both the JavaScript and the native side of the application.| **Performance& Reliability:** Compiling to native components ensures that the applications perform efficiently and reliably, leveraging the maximum potential of the underlying hardware and operating system. This decision directly impacts the performance and feel of the applications, making them indistinguishable from native apps in terms of user experience.|
| **4. Modular and Plugin-friendly Architecture:** Designing React Native to be modular and plugin-friendly, allowing third-party plugins and custom native code to be integrated easily.| <li>**Positive impact:** This greatly enhanced the flexibility and extensibility of React Native, enabling developers to add features that are not supported out of the box. <li>**Negative impact:** Relying on third-party plugins can introduce variability in quality and performance, as not all plugins are maintained to the same standard or updated regularly.| **Flexibility& Maintainability:** A modular and plugin-friendly architecture enhances flexibility, allowing developers to extend the framework’s capabilities without waiting for those features to be available natively within React Native. This architectural choice also supports maintainability by enabling updates and additions without impacting existing functionality.|
| **5. Live and Hot Reloading:** Incorporating features like Live Reloading and Hot Reloading to improve the development workflow.| <li> **Positive impact:** Developers could see changes almost instantly without rebuilding their apps, significantly speeding up the development process. <li> **Negative impact:** While live and hot reloading improve development speed by allowing instant updates, they can sometimes lead to loss of application state if not handled carefully.| **Usability:** Live and Hot Reloading significantly improve developer productivity by allowing instant feedback during the development process. This feature enhances usability for developers, making the iteration process faster and more efficient.|

### 3.2 Viewpoints (Overview Architecture of React)

#### 3.2.1 Moduel View
#### 3.2.2 





