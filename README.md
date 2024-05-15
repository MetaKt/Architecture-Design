# Architecture-Design
### Draft Document

This document is for gathering the information we have researched, in order to keep it in one place. 
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
<br>
React Native was created by Jordan Walke, a software engineer at Facebook. It was first deployed on Facebook's News Feed in 2011 and later on Instagram.com in 2012. React was open-sourced at JSConf US in May 2013. It has since become one of the most popular JavaScript libraries for web development, with a large community and ecosystem. Meta Platforms, Inc. (formerly known as Facebook) is still the owner of the React Native framework.
<br>

**1.3.2 What is the importance of React Native in the Modern Web Development?**
<br>
React's component-based architecture not only helps in building scalable applications but also makes it easier to maintain and update them. It's used by many large companies and startups alike, proving its capability to handle complex applications efficiently. React's ecosystem includes tools like Create React App, Next.js, and Gatsby, which help developers start projects quickly and incorporate best practices.

React fundamentally changed the way developers build web applications by introducing an efficient and flexible model for constructing user interfaces. Its emphasis on component reusability, the virtual DOM, and a vibrant ecosystem makes it a cornerstone technology for modern web development.

**1.3.3 Relationship between React and React Native**
|Properties|Descriptions|
| :------: | :--------: |
| Shared Principles | React Native adopts the same basic principles of React, such as declarative components and a component-driven architecture. This means developers can apply the same method of creating interfaces in React to structure mobile applications. |
| Platform-Specific Extensions | While React targets browser environments, translating JSX into DOM updates, React Native extends this by mapping JSX to native platform components. It uses a bridge to communicate between the native platform and JavaScript code, rendering native application components instead of web components.|
| Unified Development Experience | Both React and React Native aim to streamline and unify the development experience. Developers can use similar patterns and techniques across web and mobile platforms, facilitating a more cohesive development process.|

React Native's architecture is designed to allow developers to leverage the expressive power and flexibility of JavaScript while retaining the performance and feel of native applications. This combination has made React Native a popular choice among developers looking to create cross-platform applications with a single codebase.

## 2 2.	Stakeholders & Requirement Analysis

**Stakeholders analysis**
|Stakeholders|Description|
| :------: | :--------: |
|Meta (formerly Facebook)|As the creator and primary maintainer of React Native, Meta is responsible for strategic direction, major updates, and maintaining the framework's integrity. They ensure the platform remains innovative and robust to serve a wide array of developers and companies.|
|Software| Developers are the primary users of React Native. They rely on it.|
|Developers|capabilities to build cross-platform mobile applications efficiently. Their needs influence feature development, usability improvements, and documentation quality.|
|Mobile App Development Companies|These companies utilize React Native to deliver mobile solutions to their clients. They are concerned with the framework's ability to integrate smoothly with other systems, its performance, and its long-term viability for maintaining and scaling mobile applications.|
|Project Managers|Project managers overseeing React Native projects focus on the framework's ability to meet project timelines, budgets, and quality standards. They are interested in features that improve manageability and predictability, such as reliable build tools and efficient deployment processes.|
|End Users|Although not directly interacting with the framework, end users are affected by the performance, stability, and usability of apps developed with React Native. Their satisfaction is crucial as it impacts the reputation and success of the applications built on this framework.|
|Open-Source Community|This includes individual contributors, third-party service providers, and educators who contribute to the React Native ecosystem through code contributions, plugins, tutorials, and support. This community helps drive the evolution of the framework, ensuring it remains relevant and effective.|
|Integrators and Technology Partners|Companies that provide tools, libraries, and APIs that integrate with React Native. They need the framework to be stable and extensible to support a broad range of functionalities and ensure seamless integration of their products.|
These stakeholders each have distinct roles and contributions toward the development, sustainability, and proliferation of React Native, reflecting a broad and dynamic ecosystem. Their diverse needs and feedback help shape the framework's features, documentation, and support structures.

**2.2 Requirement analysis**
<br>
**2.2.1 Functional Requirements for React Native**
|Functional Requirements|Description|
| :------: | :--------: |
|Cross-Platform Compatibility|React Native must enable the development of applications that function seamlessly across diverse operating systems such as iOS, Android, and potentially other platforms like Windows or web browsers. This involves using the same JavaScript codebase to deploy native applications across all platforms, ensuring that components adapt and perform well in each environment.|
|Component-Based Architecture|The framework should support a modular architecture where applications are built using discrete, encapsulated components that manage their own state and lifecycle. This architecture should facilitate the reuse of code and simplify the development process by allowing developers to update and maintain individual components without affecting the whole application.|
|Native Component Integration|React Native should provide robust support for integrating with native platform components and APIs. This includes accessing device-specific hardware features like cameras, accelerometers, and GPS, as well as software capabilities such as push notifications and platform-specific UI components.|
|Hot Reloading|The framework should provide comprehensive debugging tools that help developers identify and resolve issues efficiently. These tools should offer features like performance profiling, state and prop inspection, and visual layout debugging.|
|Third-Party Plugin Integration|React Native should allow for easy integration with third-party plugins and libraries to extend the functionality of applications. This includes support for a wide range of community-driven packages for additional UI elements, connectivity options, or backend integrations.|
|Debugging Tools|The framework should provide comprehensive debugging tools that help developers identify and resolve issues efficiently. These tools should offer features like performance profiling, state and prop inspection, and visual layout debugging.|
|Accessibility Support|React Native applications should support accessibility features that make apps usable by people with disabilities. This includes support for screen readers, keyboard navigation, and adherence to accessible design guidelines such as the Web Content Accessibility Guidelines (WCAG) and the Americans with Disabilities Act (ADA).|
|Performance Optimization|The framework should include optimization strategies for high performance, focusing on efficient network communication, responsive UI rendering, and minimal memory usage. Techniques might include lazy loading of components, efficient data fetching strategies, and optimized state management.|
|Push Notifications|React Native should provide a straightforward method to implement push notifications across different platforms, allowing apps to maintain engagement with users through timely alerts and messages.|

<br>

**2.2.2 Key Quality Attributes for React Native**
|Key Quality Attributes|Description|
| :------: | :--------: |
|Performance|The system must ensure high responsiveness and efficient resource utilization, particularly in terms of CPU usage and memory management, to handle complex operations and large datasets smoothly across different devices.|
|Usability|The framework should be easy to use for developers at all skill levels, featuring clear documentation, comprehensive error messages, and a straightforward setup process to facilitate a smooth development experience.|
|Reliability|React Native must provide a stable foundation that consistently performs well across various devices and operating systems, ensuring that applications are dependable and function correctly under diverse conditions.|

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

### 3.2.1 Module View
**QA: Maintainability, Testability**
**Description:** This view describes the organization and structure of the software in terms of code components and their relationships. In React Native, the module view helps illustrate how different JavaScript modules and native code modules interact, which is crucial for understanding dependencies and managing code changes efficiently.

**Architecture Model**
The basic architecture model is as follows:

![图片1](https://github.com/MetaKt/Architecture-Design/assets/131533232/88b021a8-e340-411e-936c-40a66e501c5d)

The Module View of the React Native framework provides an understanding of how different software modules interact within the architecture, focusing primarily on the organization of the codebase and the functionality of individual modules. This view is crucial for developers who are looking to integrate or modify components within the framework, or for those designing systems that will extend or interact with React Native. Here’s a detailed breakdown of the main modules in the React Native architecture:

Main Modules of React Native and their interaction between each other.
<li> <b>React Components Module:</b> This module contains all the React components that developers use to build their applications. It includes everything from basic components like View, Text, and Button, to more complex components like ScrollView and ListView. These components are what developers interact with directly in their JavaScript code. React Components interact directly with the JavaScript Runtime. </li>
<li><b>JavaScript Runtime Module: </b>The core of this module is the JavaScript engine (JavaScriptCore for iOS, V8 or Hermes for Android). This engine executes the JavaScript code written by developers. Within this module, you also have the React interpreter, which manages the lifecycle of React components and their state. This module executes code and uses the Bridge to communicate changes and commands to the Native Side. </li>
<li><b>Bridge Module:</b> This is perhaps the most critical module in React Native, acting as the communication layer between the JavaScript runtime and the native side of the application. The bridge handles message passing, serialization, and deserialization of commands and data between JavaScript and the native modules. It receives commands from the JavaScript Runtime and forwards them to Native Modules or Native Components. It also sends responses back to the JavaScript side.</li>
<li><b>Native Modules:</b> These modules expose native functionalities to JavaScript. For example, if an app needs to access the device’s camera or GPS, native modules for these capabilities will be invoked. Developers can also create their own native modules to expose additional native functions to JavaScript. It receives commands from the Bridge and executes native code, interfacing with the device's hardware and other native libraries. It may also utilize Native Components to render native UI elements or perform functions.</li>
<li><b>Native Components:</b> Similar to native modules, native components are actual UI elements built using native code that can be controlled from JavaScript. These are wrapped inside React components so that they can be composed into the React component hierarchy. It used to render UI components on the screen. These components are often direct representations of native views.</li>
<li><b>Utilities Module: </b> This includes a set of utility functions and helpers that support the functioning of the framework. For example, utilities for handling layout calculations (like Yoga, a layout engine that translates React's flexible box layout into native view layouts), network requests, image handling, and other backend operations. It may be utilized by any of the other modules (especially Native Modules and Components) to perform specific tasks that support the main functionality, like handling layouts (using Yoga for example), or managing asynchronous network calls.</li>
<li><b>Overall Flow From JavaScript to Native: </b>JavaScript code defining components and their behaviors is executed in the JavaScript Runtime. Changes that need native functionality pass through the Bridge to either Native Modules or directly to Native Components.
From Native to JavaScript: Native Modules might collect data or perform operations that need to update the JavaScript side. These updates pass back through the Bridge to the JavaScript Runtime, which then updates the React Components accordingly.</li>


![图片2](https://github.com/MetaKt/Architecture-Design/assets/131533232/b9bc15de-2196-4bd0-8b2f-560cdcfd552e)

In React Native, the distinction between these two types of arrows helps clarify the nature of communication:
<li>Solid arrows often illustrate the execution flow or direct command and control interactions. For example, when the JavaScript Runtime sends a command to the Bridge, or when the Bridge directly invokes Native Modules or Native Components. These interactions are typically synchronous or have a direct cause-and-effect relationship.</li>
<li>Dotted arrows used to indicate data being passed back, such as responses from Native Modules to the Bridge, or from the Bridge back to the JavaScript Runtime. These could also represent less direct interactions, such as the use of utilities or services provided by the Utilities Module that support the main functions but do not directly control them.</li>


### 3.2.2 Component and Connector View
**QA: Performance, Extensibility, Reliability**
**Description:** This view focuses on the components involved in execution and data processing, including runtime components like the JavaScript Engine (like JavaScriptCore or Hermes), the Bridge, and native components. It illustrates how data flows between these components and how they communicate, which is vital for optimizing performance and ensuring reliable data handling.


![图片3](https://github.com/MetaKt/Architecture-Design/assets/131533232/09213d5d-c145-43b6-8a4e-101dc4d03ed6)


The Component and Connector View (C&C View) of the React Native framework provides an architectural perspective focusing on the runtime components and the interactions (connectors) between them. This view is particularly useful for understanding how different parts of the system interact with each other, which is crucial for both system integration and troubleshooting. Here’s a detailed breakdown of the components and connectors within the React Native architecture:

**Components:**
<li><b>React Components:</b> These are the building blocks of a React Native application. React components define the UI and manage the state and lifecycle of the views they represent. Each component corresponds to a native view, but the definition and logic are written in JavaScript using React's declarative syntax.</li>
<li><b>JavaScript Runtime:</b> This is the environment where the JavaScript code executes. In the context of React Native, this often refers to JavaScriptCore on iOS or V8/JavaScriptCore on Android (depending on configuration and version).</li>
<li><b>Native Modules:</b> These modules bridge React Native applications with the device's native capabilities such as camera access, GPS, accelerometer, etc. Native modules are custom Objective-C, Swift, Java, or Kotlin classes that expose their methods to JavaScript.</li>
<li><b>Native Components:</b>These are actual platform-specific UI components (like views, text inputs, images) that are ultimately rendered on the screen. They are controlled via the JavaScript written by developers but are fully native, which helps in achieving near-native performance.</li>


**Connectors:**
<li><b>Bridge:</b> The bridge is a critical architectural element in React Native. It is responsible for asynchronous communication between the JavaScript runtime and the native side. The bridge serializes messages using a JSON-like format, passing them between the two sides. This mechanism allows the JavaScript code to invoke native methods, subscribe to native events, and vice versa.</li>
<li><b>Events:</b> Events are a form of connector that facilitate communication from the native components back to JavaScript. For example, a touch event on a native button can trigger a callback in JavaScript, which can then execute some logic like updating the UI or changing the application state.</li>
<li><b>Commands: </b>Commands are instructions sent from JavaScript to control native components. For example, a command might tell a native video player component to pause or play. These are typically implemented as serialized messages that pass through the bridge.</li>
<li><b>Callbacks and Promises:</b> Callbacks and promises are used for handling asynchronous operations in React Native. JavaScript can initiate an action on the native side, which performs its operation and then calls back to JavaScript to signal completion, error, or return results. Promises offer a more modern approach to handling asynchronous responses, providing better syntax and error handling compared to traditional callbacks.</li>

### 3.2.3 Process View
**QA: Performance, Reliability**
**Description:** This view details the system’s runtime processing and is crucial for understanding how React Native applications execute within a device. It includes the execution of React components, the operation of the Bridge, and interactions with the native platform, all critical for diagnosing performance bottlenecks and ensuring application reliability.


The Process View of the React Native framework focuses on the dynamic behavior and runtime operations that manage the execution of processes within the application. This view is crucial for understanding how different parts of the application interact over time, how data flows between these parts, and how tasks are handled asynchronously. Let's delve into the key aspects of this view in the React Native architecture:


**Key Threads in React Native**
<li><b>JavaScript Thread:</b>
This thread is where your JavaScript code runs. It handles the React component lifecycle, state management, and event handling. The JavaScript thread interprets and executes the JS code, including API calls, touch events, and any other user interaction that drives the application logic.</li>
<li><b>Main Thread (UI Thread):</b>
The main thread, often referred to as the UI thread, is primarily responsible for rendering the native components and managing the UI updates on the screen. It is critical for maintaining a smooth user interface. Any blocking operations on this thread can lead to UI jank and poor user experience.</li>
<li><b>Shadow Thread (Layout Thread):</b>
This thread is responsible for calculating the layout using the Yoga layout engine. The layout calculations are based on the Flexbox algorithm, which determines the size and position of UI components. Once computed, the layout information is sent back to the main thread to update the UI accordingly.</li>


![图片4](https://github.com/MetaKt/Architecture-Design/assets/131533232/8477f945-8e01-4fb8-b21d-624330ebfaa1)

<li> <b>User Interaction:</b>Starts with the user interacting with the application (e.g., touches, gestures).</li>
<li> <b>JavaScript Thread (JST):</b> Handles most of the application logic, including event processing and state management. It sends data and commands to the bridge.</li>
<li> <b>Bridge:</b> Serves as the communication layer between JavaScript and the native side, serializing data and commands.</li>
<li> <b>Native Thread (NT):</b> Executes native code and handles operations that require direct interaction with the device's operating system and hardware.</li>
<li> <b>Shadow Thread (ST):</b> Specifically responsible for layout calculations which are then passed to the UI thread for rendering.</li>
<li> <b>UI Thread:</b> Directly responsible for rendering the UI elements onto the device screen. Ensures that the user interface remains responsive and smooth.</li>


<br>
<b>Core Processes</b>
<li> <b>Initialization:</b> During the app launch, the React Native environment is set up. This includes loading the JavaScript bundle into the JavaScript engine and initializing the bridge and native modules.
<li> <b>Event Handling:</b> User interactions or system events are captured in the JavaScript thread, where event handlers and responses are processed. The results might require updating the state of components or triggering actions in native modules.</li>
<li><b>Data Flow and Bridge Communication:</b> The bridge plays a pivotal role in communicating between the JavaScript thread and the native side. When JavaScript needs to access native capabilities, it sends serialized data across the bridge to the native modules. Similarly, responses from native modules are sent back to the JavaScript thread via the bridge.</li>
<li><b>Rendering Process:</b>React components define their views which are translated into native views by the bridge. The layout is calculated in the shadow thread, and the main thread then renders these native components onto the screen. Updates to the UI are managed through a batching and diffing process that optimizes performance by minimizing the number of native manipulations required.</li>
<li><b>Asynchronous Operations:</b>Network requests, data storage, and other heavy computations are handled asynchronously to avoid blocking the UI. These operations are initiated from the JavaScript thread and often managed by native modules that can perform background tasks.</li>
<br>




![图片5](https://github.com/MetaKt/Architecture-Design/assets/131533232/bbaaf628-c994-4841-b10f-3d19b415e4c4)

This sequence diagram illustrates how a typical interaction flows through the React Native architecture, highlighting the importance of each thread and the role of the bridge in facilitating communication between JavaScript and native components. This visualization helps in understanding the asynchronous nature of React Native and the separation of concerns which is crucial for maintaining smooth UI performance


<li><b>User Interaction:</b> Starts with the user interacting with the application (like pressing a button). JavaScript Thread: Handles the user event, processes it, and might change the state or call a native module. It sends commands or data across the bridge.</li>
<li><b>Bridge:</b>Acts as an intermediary, serializing JavaScript commands and data to the native modules and vice versa.</li>
<li><b>Shadow Thread:</b>Receives requests for layout calculations from native modules. It uses the Yoga engine to compute the layout of UI components.</li>
<li><b>Main Thread (UI Thread):</b>Receives the computed layout from the shadow thread and is responsible for rendering the native components onto the screen.</li>
<li><b>Native Modules:</b>Handle more complex functionalities that require native capabilities, such as accessing hardware features or performing background tasks.</li>



### 3.2.4 New Architecture
In June 2018, Facebook announced a plan to refactor the RN architecture. The new architecture is designed to address the limitations of the existing architecture and provide a number of benefits, including:

**Improved performance:** The new architecture uses a new rendering engine called Fabric that is designed to be more performant than the old engine.

**Better maintainability:** The new architecture is modular and easier to maintain.

**Increased flexibility:** The new architecture makes it easier for developers to add new native features.




![图片6](https://github.com/MetaKt/Architecture-Design/assets/131533232/d11df95d-b353-4898-b44c-7907dbf2c333)



**Main Changes in the New Architecture:**
<li><b>JavaScript Layer:</b> Supports enhanced features of React 16+. JavaScript static type checking (CodeGen). Introduction of JSI (JavaScript Interface), allowing for the replacement of different JavaScript engines. This supports direct communication between JavaScript and Native.</li>
<li><b>Bridge Layer:</b> Divided into two parts: Fabric and TurboModules, which are responsible for UI management and native modules, respectively. Without bridge, the performance will improve a lot.</li>
<li><b>Native Layer:</b> Streamlined core modules, with non-core parts separated out as community modules for independent updates and maintenance. Enhanced type checking.</li>


### 3.3 Relationship Between The Architecture and QA


The architecture of React Native significantly impacts several key quality attributes that are crucial for the development and performance of mobile applications. React Native's architecture brings several advantages in terms of development speed, user experience, and platform coverage. However, it also requires careful consideration, particularly regarding performance and security, to ensure that the benefits are fully realized without compromising the quality of the mobile application. Here's how React Native's architecture affects performance, reliability, Extensibility, maintainability, and security:

**1. Performance**
React Native's architecture, which includes the use of a bridge to communicate between the JavaScript code and the native components, has both benefits and challenges regarding performance:
- JavaScript to Native Bridge: This architecture allows React Native to utilize the native components of each platform (iOS, Android), providing near-native performance. However, the bridge itself can become a bottleneck because each interaction between JavaScript and the native side involves serialization and deserialization, which can be costly in terms of performance, especially for high-volume, real-time interactions.
- Asynchronous Execution: React Native's non-blocking, asynchronous execution model helps maintain smooth UI performance by preventing JavaScript operations from blocking the UI thread.

**2. Reliability**
- Component-Based Architecture: React Native's use of components facilitates reliability. Each component can be isolated, making it easier to manage faults and updates without affecting other parts of the application.
- Mature Ecosystem: Leveraging React's ecosystem, React Native benefits from a robust set of tools and community-tested libraries, which enhance the reliability of applications built with the framework.

**3. Extensibility**
- Code Reusability: The ability to use the same code for both iOS and Android platforms makes it easier to scale applications to multiple platforms. This reduces the complexity and resources required to maintain separate codebases.
- Third-Party Plugins and Modules: React Native's architecture supports integration with third-party modules, allowing developers to extend the functionality of applications as they scale without having to build all features from scratch.

**4. Maintainability**
- Modular Architecture: The modular nature of components in React Native not only simplifies updates and bug fixes but also enhances the overall maintainability of the code by promoting cleaner and more organized code structure.

**5. Security**
- JavaScript Environment: Since React Native apps execute JavaScript code, they inherit both the strengths and weaknesses of JavaScript with regards to security. Proper security measures must be implemented to handle JavaScript-specific security issues, such as injection attacks.
- Native Modules: While React Native uses native modules that can potentially offer better security than web-based interfaces, each native integration must be secured appropriately, as these can also introduce vulnerabilities if not correctly handled.



