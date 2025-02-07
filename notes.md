# Theory notes:

## SOLID programming principles:

S: Single-responsibility principle

O: Open-closed principle

L: Liskov Substitution principle

I: Interface Segregation principle

D: Dependency Inversion principle

Recognized as one of the dominant and better practices when it comes to Object Oriented Programming (OOP).

It focuses on improving the scalability, ease of maintenance, and reusability of a codebase. It achieves this by creating clear and isolated sections that can be improved individually as well as together. It focuses on creating a decoupled and modular codebase.

#### Single Responsibility Principle (SRP):

SRP states that a class should only have one reason to change.

A class should have one purpose/responsibility. As more unrelated functions and tasks are given to any one class, the complexity starts to increase making it harder to maintain the code and keep track of what is going on when the code is running or troubleshooting and has an increased likelihood of error. If one class is performing multiple tasks, it may start limiting or affecting concurrent tasks it is responsible for.

#### Open/Closed Principle (OCP):

Entities within the code, such as classes, functions and modules [see dictionary] should be written in a manner that allows you to add new functionality to it, without having to change the existing code.

This could be done using inheritance in OOP or abstract classes and interfaces [see dictionary]. However, modifying existing code risks breaking code that already works and might affect the operations of the system.

This does not mean you are unable to go back to the previous code to optimize, bugfix and refactor it for ease of maintenance. It refers to maintaining stability within the codebase.

#### Liskov Substitution Principle (LSP):

A superclass can be replaced with objects its subclasses have.

A superclass should be able to take in parameters and values from subclasses that are inheriting from it without breaking or having any issues. If the subclasses cannot be used as a drop-in replacement it can lead to unexpected behavior and bugs within the code.

The subclasses should be able to handle and work with any operation/task expected of the parent class they are inheriting from. This principle makes it so fundamental behaviors stay consistent throughout the class tree. Subclasses will maintain the same behavior as its parent class.

An example would be having a Vehicle class, with speed, value, and passenger seating. Then there can be subclasses such as Car and Bus. The car takes in speed, value and passenger, and can have an additional parameter like a sports car (bool). Bus then can take speed, value, passengers, and the number of standing passengers. Both subclasses can be passed into the parent class and still have the main constructing parameters which would make them suitable for a drop-in.

#### Interface Segregation Principle (ISP):

Clients (classes, modules, functions) should not be forced to depend upon interfaces/functions they do not use.

The principle focuses on creating specific interfaces that will be used by the client, as opposed to having a general function that is not necessarily used fully. It encourages tailored and specific methods to achieve what is necessary.

As classes grow and depend on a large interface it doesn't directly interact with it becomes dependent on parts of the code that is not relevant to itself. Isolating and removing redundant dependencies makes the codebase easier to maintain and work with as well as less prone to interference from other sections of the code.

#### Dependency Inversion Principle (DIP):

This principle focuses on decoupling and logical dependencies.

High-level modules (ones that dictate behavior, rules, features etc) should not depend on low-level modules (data storage, basic utilities etc). Both depend separately on abstraction. Abstractions should not be dependent on details, but rather details depend on abstractions.

This prevents changes in any of the 3 influencing the other 2, meaning changes in low-level modules won't impact high-level and vice versa.

##

## KISS Concepts:

K - Keep

I - It

S - Simple

S - Silly/Stupid

In a broader sense, with no context, it refers to keeping solutions and problems simple, avoiding over complicating the task and what you have at hand. The benefit of this is you can handle smaller and simpler chunks of a solution/task.

Similar to its broader use, in software engineering it is a nearly identical concept. It focuses on keeping your designs and systems simple where possible. The aim is to reduce complexity, which makes it easier to interact with and improves the quality of the system.

A simpler codebase is always easier to maintain and build on which would tie into SOLID principles.

S - 'Simple' code would only have one task per relevant section, this would help keep complexity down and prevent interference with other areas as a software entity attempts to undertake multiple roles.

O - Open/closed principles would benefit as it is easier to extend the functionality and leave the main code without modifications if the said piece of code is designed simply and concisely, as it would be easier to understand and interact with.

L - Whilst it does not directly tie into Liskov's substitution, it would be easier to design classes and subclasses when they are designed to be easy to understand and work with, as it would require fewer modifications (tying again into open/closed principles).

I - Interface Segregation is directly tied into KISS, as it focuses on removing items that are not being utilized. This directly keeps software entities (classes, modules, functions etc) simpler and easier to work with.

D - Dependency inversion would be focused on creating a logical and less complicated set of dependencies that is easier to work with when looking at the hierarchy of a system in place. It keeps things simple by isolating high-level & low-level modules and details from each other and directly tying them to the objective, the abstract.

##

## DRY Concepts:

D - Don't

R - Repeat

Y - Yourself

The focus of DRY is to prevent redundancies within the system/codebase. It focuses on abstracting the problem/task at hand into smaller segments, and further breaking them down until they are one task/one problem at a time.

This allows you to recognize when tasks are similar or duplicates of one another, allowing you to create a solution that solves or handles them all at once as opposed to having a dedicated solution/code for each one. It reduces both redundancies in a process as you have seen which ones are repeated, as well as the redundancies in the logic, the solution that is being implemented.

This reduces redundant code within a system allowing for easier maintenance and alteration of the codebase. It focuses on automating repeat tasks/solutions as well as reducing overall lines of code being used as there isn't a need to have a unique solution to each repeat problem.

This heavily ties into KISS principles, as it encourages a simpler system to be used, reducing overall complexity and improving ease of maintenance and use for the system. As KISS ties into SOLID principles, DRY is also heavily related to that.

##

## React:

React is a JavaScript library that focuses on UI. Its main specialty is for single-page applications that can be updated without requiring a full reload of the webpage.

Here are the main features/points of React:

#### Component-based architecture:

React applications are built using components, which are reusable chunks of code contained within itself. You can use multiple components, such as a button component, a textbox component and an image component to create increasingly complex UIs. Components both dictate the structure and behavior, allowing for a more reusable and modular codebase.

#### Declarative Syntax:

It allows for code to be written telling what to have and what to do, as opposed to coding how that item is created and how it works. A better definition is available in the dictionary.

Developers need to define the UI they want and how they wish for it to appear and React will render it for them as opposed to having to render it manually each time.

#### Virtual DOM (Document Object Model):

It is a system in place that helps React webpages render state changes and alterations to elements faster.

When there is a state change of the UI, there is another Virtual DOM created, with the changes in place to the elements. The differences between Virtual DOMs are compared, and then only the necessary updates are re-rendered and shown on the Real DOM.

This prevents unnecessary re-rendering of elements that do not require it. And as the Virtual DOMs are not rendered at all, it is a very lightweight task to do.

#### JavaScript XML (JSX):

JSX allows DOMs to be created and managed directly within the JavaScript code. It makes it easier to declare the UI structure in React as it is a syntax extension for JavaScript.

It does require an interpreter (i.e. Babel) for browsers to understand as it does not do so naturally.

It allows for directly creating expressions in JavaScript, which can be used to create dynamic content, manipulate data and create conditions when rendering the UI.

It facilitates the logic of JavaScript whilst being able to use HTML-like scripting (making it more familiar to web developers) to manipulate DOMs

#### Unidirectional Data Flow:

Dataflow is not restricted directionally. It allows for communication between parents and children, by directly passing data to them via props, and from children to parents using callback functions.

#### React Hooks:

Introduced in early 2019. React hooks allow for functional components to also manage states, life cycle methods and other React features without relying on class components.

Hooks simplify the structure of functional components improving the ease of reading and maintenance.

It is one of the standout features of React as it contributes directly to the simplicity and flexibility React applications have. It allows for the handling of states and side effects for functional components.

#### React Router:

A popular React library that is used for navigation and routing in React applications. It allows for the creation of dynamic single-page applications that have multiple views.

With the use of JSX, the application's navigation structure can be defined in a declarative manner. It also allows for the use of nested navigation and route parameters, which allow for data to be routed within the application as well.

React Router also utilizes programmatic navigation by using the history object, allowing for redirection dynamically based on previous navigation and interactions within the application.

#### Ecosystem and Community:

React has a wide set of libraries and tools. These range from state management (i.e. Redux) and testing libraries (i.e. Jest).

Due to the widespread use and the active community, the codebase directly as well as the libraries are maintained and updated. This also results in a variety of third-party sources to learn from such as online courses and books.

##

## Message Queuing Telemetry Transport (MQTT):

MQTT is a lightweight and open messaging protocol that is designed to be used within small sensors and high latency/unreliable network mobile devices. It was developed by IBM in the 1990s and became an open standard later down the line. It is suitable for things such as home and industrial automation as well as transmitting telemetry data. It is also scalable if needed.

Key points and features:

#### Publish/subscribe model:

MQTT utilizes a publish/subscribe model. The entities are the publishers, the components that can send a message, and the subscribers, the ones that receive the message. Similar to YouTube content publishers and their subscribers.

There is a third component;

#### Broker:

Acts as a median between the publishers and subscribers, it is the component that relays the message between the two. It is essential in decoupling the other 2 entities. It receives the information from the publisher/s and relays it to relevant subscribers. Similar to stock brokers, acting as a median between you buying shares in a company and you.

#### Topics:

The messages that are published get categorized into channels or labels, these are referred to as topics. Subscribers follow (express interest) in these topics so they receive information from the topics when publishers post into them.

#### Quality of Service (QoS):

MQTT has 3 different message delivery assurance, acting as error detection/handling.

- QoS 0 (At most once)
  - The message is delivered at most one time, and delivery is not confirmed
- QoS 1 (At least once)
  - The message is delivered at least once and expects acknowledgement from the receiver
- QoS 2 (Exactly once)
  - It requires overhead when performing this type of communication
  - The message is delivered exactly once using a 4 step handshake:
  - Publish (PUB)
    - the publisher sends the message to the broker, the broker stores the message and acknowledges the receipt to the publisher
  - Publish received (PUBREC)
    - After receiving PUB acknowledgement from the broker, the publisher sends PUBREC to the broker
    - PUBREC message is an acknowledgement of the broker's receipt of the original message
  - Publish release (PUBREL)
    - After the broker receives PUBREC, it acknowledges it to the publisher
    - Broker stores PUBREC state and forwards the original message to the subscriber
  - Publish Complete (PUBCOMP)
    - after receiving PUBREC acknowledgement from the broker, the publisher sends a PUBCOMP message to the broker
    - PUBCOMP confirms the completion of QoS 2 handshake

#### Retained Messages:

MQTT has retained messages, almost acting as an archive. Messages can be marked as retained for a select topic. Retained messages are held by brokers, which are then passed on to any new subscribers to the topic.

#### Lightweight:

As mentioned, being lightweight is one of its key standouts. The communication protocol is designed to use minimal bandwidth and be efficient. It is designed to be suitable for restrictive environments such as IoT (Internet of Things) and networks with resource limitations.

## Object-Relational Mapping (ORM)

ORM is a programming technique that allows developers to interact with relational databases using OOP paradigms. Traditional databases utilize the data that is within tables, using them as foreign, composite and primary keys to define relations.

An ORM system has a higher level interface that allows developers to directly work with their choice of programming language as opposed to having to write SQL queries manually. ORM automatically takes care of the translation of objects and instructions.

#### Key concepts:

##### Object-Relational Mapping

The process of mapping objects and tables to one another within a relational database

##### Entities

In context of ORM's, they are the records within a databases tables

#### Mapping

Defining how objects and tables will be related "mapped" to one another

##### CRUD Operations

Create Read Update Delete operations, similar to basic/standard SQL

##### Relationships

Defining and managing relations between objects, one to many, many to one, many to many, one to one etc

##### Lazy Loading

ORM systems have some optimizations in place such as lazy loading - only loading data when explicitly requested

### About Sequelize

Iti s a popular ORM library for Node.JS and it is powerful and able to interact with multiple db types such as MySQL, PostgreSQL, SQLite, MSSQL. Simplifies db operations by allowing devs to work directly with JS objects and methods as opposed to using raw SQL queries

#### Key features:

##### Multiple DB Support

Sequelize supports multiple relational databases making it versatile and suitable for different projects and environments

##### Models and Migrations

Sequelize lets you define data models within the app, which represent tables in the db. Migrations aid in db schema changes over time

##### CRUD Operations

Sequelize provides methods for creating, reading, updating and deleting data records within the db using JS syntax

##### Associations

Has support for different types of relations between models, including one-one, many-one, one-many, many-many. MThis makes it easier to navigate and manipulate related data

##### Querying

Sequelize has a flexible and powerful querying API. Developers cam use methods to filter, sort, aggregate data without writing raw sql, but using JS syntax directly

##### Hooks

Sequelize allows you to define hooks, which are functions that are executed before or after certain events, such as creating or updating a record, this allows devs to customize how the system operates and responds. Hooks are functions to use in Sequelize, but similar to subscription methods and pipelines which is a broader version of it.

##### Transactions

Sequelize has support for transactions, allows you to group multiple database operations into a single transactions which allows database to be consistent and ensures atomicity

##### Validation

Allows for rules to be defined to validate the data and the database. Allows you to enforce constraints and adherence to them before committing them into the DB.

##

## DICTIONARY:

_Modules: a collection of related functions and code that can be used freely independent of its original use case, similar to libraries. It focuses on reusability in different scenarios independent of the different cases it is used for._

_Abstract Classes: the main blueprint for classes that will inherit from it. Dictates rough structure and properties._

_Interface: defining traits and parameters a class must obey and have. Not how they are done, but rather what should be done._

_Software entities: General way of referring to classes, modules and functions._

_Declarative syntax: Code that can be written procedurally. You tell what you want the code to do as opposed to telling it how to do it. i.e. create a 10px square vs draw 4 lines that are connecting at 90 deg angles each measuring 10px_

_Document Object Model (DOM): A structure representation of the HTML elements within the code. It is represented as a tree data structure, showing which top element has which sub elements._

_Real DOM: A type of Document Object Model that requires a full re-render of all elements within the DOM when there is any update of any component. It can be resource-intensive if there are a large number of elements to rerender_

_Virtual DOM: A lightweight version of Real DOM. It is a virtual representation of the real DOM without the ability to change the layout of a document directly._

_Extensible Markup Language (XML): It is a markup language and file format that allows for storing, transmitting and reconstructing data. It has a format that is both human/machine-readable._

_JavaScript XML (JSX): JSX is an extension of JavaScript that allows you to directly write HTML within the JavaScript code. It is translated into regular JavaScript at runtime. Not compulsory but used heavily._

_Props: The data type object where attributes about a tag are stored. Usually read-only components._

_Functional component: A JavaScript function that returns a React element. Takes in props as data entry, and are more refined way to define components vs class components._

_Class components: The older method of rendering and defining components. It is now treated as boilerplate code._

_Programmatic navigation: Redirection and/or dynamic routing based on prior interactions. Such as a login vs sign up action._

_Internet of Things (IoT): The network and communications between physical devices. Such as vehicles, appliances and other objects that have sensors or data to transmit. It uses the internet to achieve this. Summarized to 'smart' devices communicating without direct human involvement._

_Aggregating Data: Combining individual data to create a data that is a composition of the other types._

_Atomicity: A property of transactions in database systems, referred to via ACID acronym._

_ACID: Atomicity/All-or-nothing, consistency, isolation, durability_

_All-or-nothing: If a transaction has multiple steps and operations, they are all executed as one unit. If there is an error within any of the steps, i.e. transaction is unsuccessful, the entire transaction is rolled back and the database remains unchanged ensuring consistency through out the system._

_Consistency: Regardless of consistency provided by Atomicity/all-or-nothing, the database still needs to have consistency that allows it to transition from one consistent state to another at the end of a transaction._

_Isolation: This property allows transactions to be independent of one another. This prevents interference between multiple transactions to one another. Each transaction should be able to do its own thing without being dependent or influenced by another transaction._

_Durability: After a transaction is complete, the changes should be permanent and not be influenced by crashes or system failures. The state after transactions should not be volatile._
