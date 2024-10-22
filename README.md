# Interview Prep

- [Interview Prep](#interview-prep)
  - [OOP Questions](#oop-questions)
    - [What is OOP?](#what-is-oop)
    - [What is the need for OOP?](#what-is-the-need-for-oop)
    - [What is Encapsulation?](#what-is-encapsulation)
      - [What is data hiding?](#what-is-data-hiding)
      - [What is data binding?](#what-is-data-binding)
    - [What is Abstraction?](#what-is-abstraction)
    - [What is Polymorphism?](#what-is-polymorphism)
      - [What is Compile Time Polymorphism?](#what-is-compile-time-polymorphism)
      - [What is Run Time Polymorphism?](#what-is-run-time-polymorphism)
    - [What is Inheritance?](#what-is-inheritance)
      - [What are some types of Inheritance?](#what-are-some-types-of-inheritance)
      - [What are some limitations of Inheritance?](#what-are-some-limitations-of-inheritance)
  - [Javascript Questions](#javascript-questions)
    - [Difference between null and undefined](#difference-between-null-and-undefined)
    - [What is the difference between var, let, and const](#what-is-the-difference-between-var-let-and-const)
    - [Is JS statically or dynamically typed?](#is-js-statically-or-dynamically-typed)
    - [Explain passed by value vs passed by reference?](#explain-passed-by-value-vs-passed-by-reference)
    - [What are the primitive data types in JavaScript?](#what-are-the-primitive-data-types-in-javascript)
    - [What is an Immediately Invoked Function Expression?](#what-is-an-immediately-invoked-function-expression)
    - [What is the difference between overloading and overriding?](#what-is-the-difference-between-overloading-and-overriding)
    - [What is an exception?](#what-is-an-exception)
    - [What is exception handling?](#what-is-exception-handling)
  - [Classes, Interfaces, and Objects](#classes-interfaces-and-objects)
    - [What is an interface?](#what-is-an-interface)
    - [What is an abstract class?](#what-is-an-abstract-class)
    - [What is the difference between an abstract class and an interface?](#what-is-the-difference-between-an-abstract-class-and-an-interface)
    - [How much memory does a class take up?](#how-much-memory-does-a-class-take-up)
    - [Is it necessary to create an object of a class to access its static members?](#is-it-necessary-to-create-an-object-of-a-class-to-access-its-static-members)
    - [What is a constructor?](#what-is-a-constructor)
    - [What is Dependency Injection?](#what-is-dependency-injection)
  - [SOLID Questions](#solid-questions)
    - [What is SOLID?](#what-is-solid)
    - [Why is SOLID important?](#why-is-solid-important)
    - [What is the Single Responsibility Principle?](#what-is-the-single-responsibility-principle)
    - [What is the Open/Closed Principle?](#what-is-the-openclosed-principle)
    - [What is the Liskov Substitution Principle?](#what-is-the-liskov-substitution-principle)
    - [What is the Interface Segregation Principle?](#what-is-the-interface-segregation-principle)
    - [What is the Dependency Inversion Principle?](#what-is-the-dependency-inversion-principle)
  - [Database Questions](#database-questions)
    - [What are the main 3 types of databases?](#what-are-the-main-3-types-of-databases)
    - [What is a SQL database?](#what-is-a-sql-database)
    - [What is a SQLite database?](#what-is-a-sqlite-database)
    - [What is a NoSQL database?](#what-is-a-nosql-database)
    - [What are the key differences between SQL and NoSQL databases?](#what-are-the-key-differences-between-sql-and-nosql-databases)
    - [What is indexing in databases?](#what-is-indexing-in-databases)
    - [What is the difference between indexing in SQL and NoSQL databases?](#what-is-the-difference-between-indexing-in-sql-and-nosql-databases)

## OOP Questions

### What is OOP?

<details>

<summary>Answer</summary>

Object Oriented Programming is a programming paradigm designed for solving complex problems and models real world examples. OOP consists of 4 major principles: `Encapsulation`, `Abstraction`, `Polymorphism`, & `Inheritance`.

</details>

### What is the need for OOP?

<details>

<summary>Answer</summary>

OOP is needed to help solve complex problems, make the code more readable, and make the code more maintainable.

</details>

### What is Encapsulation?

<details>

<summary>Answer</summary>

Encapsulation is the OOP principle that hides the data inside of the object and only allows access with pre-defined methods.

Example:

    ```javascript
    class Person {
        private _name: string;
        private _age: number;

        constructor(name: string, age: number) {
            this.name = name;
            this.age = age;
        }

        getAge() {
            return this.age;
        }

        setAge(age) {
            this.age = age;
        }
    }
    ```

</details>

#### What is data hiding?

<details>

<summary>Answer</summary>

Data hiding is the process of hiding the data inside of an object so that it cannot be accessed directly. This is done to prevent the data from being changed in an unexpected way.

</details>

#### What is data binding?

<details>

<summary>Answer</summary>

Data binding is the process of connecting the data inside of an object to the object itself. This is done to ensure that the data is always up to date and accurate.

</details>

### What is Abstraction?

<details>

<summary>Answer</summary>

Abstraction is the OOP principle of hiding characteristics inside an object that a user does not need to know about, but can still utilize.

Example:

    ```javascript
    class Car {
        private _make: string;
        private _model: string;
        private _year: number;
        private _speed: number;

        constructor(make: string, model: string, year: number) {
            this.make = make;
            this.model = model;
            this.year = year;
            this.speed = 0;
        }

        accelerate() {
            this.speed += 10;
        }

        brake() {
            this.speed -= 10;
        }
    }
    ```

</details>

### What is Polymorphism?

<details>

<summary>Answer</summary>

Polymorphism is the OOP principle of having a parent class or interface pass a method to child classes that will and are capable of being changed. This allows the same method to be used in different ways from the same parent class.

Example:

    ```javascript
    interface Shape(){
        area(): number;
    }

    class Circle implements Shape {
        private _radius: number;

        constructor(radius: number) {
            this.radius = radius;
        }

        area(): number {
            return Math.PI * this.radius * this.radius;
        }
    }

    class Rectangle implements Shape {
        private _width: number;
        private _height: number;

        constructor(width: number, height: number) {
            this.width = width;
            this.height = height;
        }

        area(): number {
            return this.width * this.height;
        }
    }
    ```

</details>

#### What is Compile Time Polymorphism?

<details>

<summary>Answer</summary>

Compile Time Polymorphism is when the method is decided at compile time. This is also known as method overloading.

Example:

    ```javascript
    class Math {
        add(a: number, b: number): number {
            return a + b;
        }

        add(a: number, b: number, c: number): number {
            return a + b + c;
        }
    }
    ```

</details>

#### What is Run Time Polymorphism?

<details>

<summary>Answer</summary>

Run Time Polymorphism is when the method is decided at runtime. This is also known as method overriding.

Example:

    ```javascript
    class Animal {
        makeSound() {
            console.log('Animal makes sound');
        }
    }

    class Dog extends Animal {
        makeSound() {
            console.log('Dog barks');
        }
    }
    ```

</details>

### What is Inheritance?

<details>

<summary>Answer</summary>

Inheritance is the OOP Principle where a subclass inherits from a superclass and uses the methods from the class while adding more personal methods.

Example:

    ```javascript
    class baseSpotify {
        private _user: string;
        private _pass: string;
        protected _song: string;

        constructor(user: string, pass: string) {
            this._user = user;
            this._pass = pass;
            this._song = 'Song Name';
        }

        playSong() {
            console.log(`Now playing: ${this._song}`);
        }
    }

    class premiumSpotify extends baseSpotify {
        private _premium: boolean;

        constructor(user: string, pass: string, premium: boolean) {
            super(user, pass);
            this._premium = premium;
        }

        chooseSong(song: string) {
            if (this._premium) {
                this._song = song;
            }
        }
    }
    ```

</details>

#### What are some types of Inheritance?

<details>

<summary>Answer</summary>

Single Inheritance, Multiple Inheritance, Multilevel Inheritance, Hierarchical Inheritance, & Hybrid Inheritance

</details>

#### What are some limitations of Inheritance?

<details>

<summary>Answer</summary>

Takes more time to process, tight coupling, and can be difficult to maintain.

</details>

## Javascript Questions

### Difference between null and undefined

<details>

<summary>Answer</summary>

Undefined is when a variable has been declared but doesn't have a value. Null is an assignable value that represents no value.

</details>

### What is the difference between var, let, and const

<details>

<summary>Answer</summary>

The `var` keyword can be globally scoped or function scoped and is mutable. The `let` keyword is block scoped and is mutable. The `const` keyword is block scoped and is immutable.

</details>

### Is JS statically or dynamically typed?

<details>

<summary>Answer</summary>

JavaScript is dynamically typed. This means that the type of a variable is determined at runtime. TypeScript is statically typed.

</details>

### Explain passed by value vs passed by reference?

<details>

<summary>Answer</summary>

Passed by value is when a copy of the variable is passed to the function. Passed by reference is when the memory address of the variable is passed to the function.

Examples:

Passed by value:

    ```javascript
    let a = 5;

    function changeValue(val) {
        val = 10;
    }

    changeValue(a);

    console.log(a); // 5
    ```

Passed by reference:

    ```javascript
    let obj = { a: 5 };

    function changeValue(val) {
        val.a = 10;
    }

    changeValue(obj);

    console.log(obj.a); // 10
    ```

</details>

### What are the primitive data types in JavaScript?

<details>

<summary>Answer</summary>

`number`, `string`, `boolean`, `null`, `undefined`, & `symbol`

</details>

### What is an Immediately Invoked Function Expression?

<details>

<summary>Answer</summary>

An IIFE is a function that is executed immediately after it is created. It is a design pattern that is used to prevent polluting the global scope.

</details>

### What is the difference between overloading and overriding?

<details>

<summary>Answer</summary>

Overloading is when a method has the same name but different parameters. Overriding is when a method has the same name and parameters but different implementations.

Example:

Overloading:

    ```javascript
    class Math {
        add(a: number, b: number): number {
            return a + b;
        }

        add(a: number, b: number, c: number): number {
            return a + b + c;
        }
    }
    ```

Overriding:

    ```javascript
    class Animal {
        makeSound() {
            console.log('Animal makes sound');
        }
    }

    class Dog extends Animal {
        makeSound() {
            console.log('Dog barks');
        }
    }
    ```

</details>

### What is an exception?

<details>

<summary>Answer</summary>

An exception is a special event raised during runtime that brings the runtime to a halt. The reason for the exception can be anything from a logical error to a runtime error.

</details>

### What is exception handling?

<details>

<summary>Answer</summary>

The method used for identifying, catching, and responding to exceptions is called exception handling. It is used to prevent the program from crashing when an exception is raised. The most common method used for exception handling is the try-catch block.

</details>

## Classes, Interfaces, and Objects

### What is an interface?

<details>

<summary>Answer</summary>

An interface is a blueprint of a class that has abstract methods that are not given definitions. It is used to provide a contract for the class that implements it.

</details>

### What is an abstract class?

<details>

<summary>Answer</summary>

An abstract class is a special class that contains abstract methods. These abstract methods are only declared and not implemented. The significance of an abstract class is that it cannot be instantiated, and it must be inherited by another class.

</details>

### What is the difference between an abstract class and an interface?

<details>

<summary>Answer</summary>

When an interface is implemented, all methods must be defined. When an abstract class is inherited, generally all methods must be defined unless the subclass is also abstract. An abstract class can also have both abstract and non-abstract methods. Also, only one abstract class can be inherited, but multiple interfaces can be implemented.

</details>

### How much memory does a class take up?

<details>

<summary>Answer</summary>

A class does not take up any memory until an object is created from it. Once an object is created, the memory taken up by the class is the sum of the memory taken up by all the variables and methods in the class.

</details>

### Is it necessary to create an object of a class to access its static members?

<details>

<summary>Answer</summary>

No, it is not necessary to create an object of a class to access its static members. Static members can be accessed using the class name itself.

Example:

    ```javascript
    class Math {
        static add(a: number, b: number): number {
            return a + b;
        }
    }

    console.log(Math.add(5, 10));
    ```

</details>

### What is a constructor?

<details>

<summary>Answer</summary>

A constructor is a special method that is called when an object is created from a class. It is used to initialize the object's state.

Example:

    ```javascript
    class Person {
        private _name: string;
        private _age: number;

        constructor(name: string, age: number) {
            this.name = name;
            this.age = age;
        }
    }

    let person = new Person('Spencer', 23);
    ```

</details>

### What is Dependency Injection?

<details>

<summary>Answer</summary>

Dependency Injection is a design pattern that is used to remove the dependency of a class on another class. It is used to inject the dependency of one class into another class.

Example:

    ```javascript
    class Database {
        save(data: any) {
            console.log('Data saved to database');
        }
    }

    class User {
        private _database: Database;

        constructor(database: Database) {
            this.database = database;
        }

        saveData(data: any) {
            this.database.save(data);
        }
    }

    let database = new Database();
    let user = new User(database);
    ```

</details>

## SOLID Questions

### What is SOLID?

<details>

<summary>Answer</summary>

SOLID is a set of five principles that are designed to make software designs more understandable, flexible, and maintainable. The five principles are: `Single Responsibility Principle`, `Open/Closed Principle`, `Liskov Substitution Principle`, `Interface Segregation Principle`, & `Dependency Inversion Principle`.

</details>

### Why is SOLID important?

<details>

<summary>Answer</summary>

The purpose of SOLID principles is to explore different design approaches that allow software engineers and developers to tackle problematic design patterns. By working with the SOLID principles, they can build software programs that are adaptive, agile and effective. While following the SOLID principles can increase the time and effort required for the software development, it can also ensure that the resulting code is easy to read, test, maintain and extend.

</details>

### What is the Single Responsibility Principle?

<details>

<summary>Answer</summary>

The Single Responsibility Principle states that a class should have only one reason to change. This means that a class should only have one responsibility.

Example:

Bad:

    ```javascript
    class User {
        private _name: string;
        private _email: string;
        private _theme: string;
        private _textSize: number;

        constructor(name: string, email: string) {
            this.name = name;
            this.email = email;
            this.theme = 'light';
            this.textSize = 12;
        }

        changeName(name: string) {
            this.name = name;
        }

        changeEmail(email: string) {
            this.email = email;
        }

        changeTheme(theme: string) {
            this.theme = theme;
        }

        changeTextSize(size: number) {
            this.textSize = size;
        }
    }
    ```

Good:

    ```javascript
    class User {
        private _name: string;
        private _email: string;

        constructor(name: string, email: string) {
            this.name = name;
            this.email = email;
        }

        changeName(name: string) {
            this.name = name;
        }

        changeEmail(email: string) {
            this.email = email;
        }
    }

    class Settings {
        private _theme: string;
        private _textSize: number;

        constructor() {
            this.theme = 'light';
            this.textSize = 12;
        }

        changeTheme(theme: string) {
            this.theme = theme;
        }

        changeTextSize(size: number) {
            this.textSize = size;
        }
    }
    ```

</details>

### What is the Open/Closed Principle?

<details>

<summary>Answer</summary>

The Open/Closed Principle states that a class should be open for extension but closed for modification. This means that a class should be able to be extended without changing the existing code.

Example:

Bad:

    ```javascript
    class Math {
        add(a: number, b: number): number {
            return a + b;
        }

        subtract(a: number, b: number): number {
            return a - b;
        }

        multiply(a: number, b: number): number {
            return a * b;
        }

        divide(a: number, b: number): number {
            return a / b;
        }
    }
    ```

Good:

    ```javascript
    interface Math {
        calculate(a: number, b: number): number;
    }

    class Add implements Math {
        calculate(a: number, b: number): number {
            return a + b;
        }
    }

    class Subtract implements Math {
        calculate(a: number, b: number): number {
            return a - b;
        }
    }

    class Multiply implements Math {
        calculate(a: number, b: number): number {
            return a * b;
        }
    }

    class Divide implements Math {
        calculate(a: number, b: number): number {
            return a / b;
        }
    }
    ```

</details>

### What is the Liskov Substitution Principle?

<details>

<summary>Answer</summary>

The Liskov Substitution Principle states that objects of a superclass should be replaceable with objects of a subclass without affecting the correctness of the program.

Example:

Bad:

    ```javascript
    class Rectangle {
        private _width: number;
        private _height: number;

        constructor(width: number, height: number) {
            this.width = width;
            this.height = height;
        }

        setWidth(width: number) {
            this.width = width;
        }

        setHeight(height: number) {
            this.height = height;
        }

        getArea(): number {
            return this.width * this.height;
        }
    }

    class Square extends Rectangle {
        setWidth(width: number) {
            this.width = width;
            this.height = width;
        }

        setHeight(height: number) {
            this.width = height;
            this.height = height;
        }
    }
    ```

Good:

    ```javascript
    interface Shape {
        getArea(): number;
    }

    class Rectangle implements Shape {
        private _width: number;
        private _height: number;

        constructor(width: number, height: number) {
            this.width = width;
            this.height = height;
        }

        getArea(): number {
            return this.width * this.height;
        }
    }

    class Square implements Shape {
        private _side: number;

        constructor(side: number) {
            this.side = side;
        }

        getArea(): number {
            return this.side * this.side;
        }
    }
    ```

</details>

### What is the Interface Segregation Principle?

<details>

<summary>Answer</summary>

The Interface Segregation Principle states that a client should not be forced to implement an interface that it does not use. This means that interfaces should be broken down into smaller, more specific interfaces.

Example:

Bad:

    ```javascript
    interface Worker {
        work(): void;
        eat(): void;
        manage(): void;
    }

    class Engineer implements Worker {
        work() {
            console.log('Engineer is working');
        }

        eat() {
            console.log('Engineer is eating');
        }

        manage() {
            console.log('Engineer does not manage');
        }
    }

    class Manager implements Worker {
        work() {
            console.log('Manager is working');
        }

        eat() {
            console.log('Manager is eating');
        }

        manage() {
            console.log('Manager is managing engineers');
        }
    }
    ```

Good:

    ```javascript
    interface Worker {
        work(): void;
        eat(): void;
    }

    interface Manager {
        manage(): void;
    }

    class Engineer implements Worker {
        work() {
            console.log('Engineer is working');
        }

        eat() {
            console.log('Engineer is eating');
        }
    }

    class Manager implements Worker, Manager {
        work() {
            console.log('Manager is working');
        }

        eat() {
            console.log('Manager is eating');
        }

        manage() {
            console.log('Manager is managing engineers');
        }
    }
    ```

</details>

### What is the Dependency Inversion Principle?

<details>

<summary>Answer</summary>

The Dependency Inversion Principle states that high-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend on details. Details should depend on abstractions.

Example:

Bad:

    ```javascript
    class Database {
        save(data: any) {
            console.log('Data saved to database');
        }
    }

    class User {
        private _database: Database;

        constructor() {
            this.database = new Database();
        }

        saveData(data: any) {
            this.database.save(data);
        }
    }
    ```

Good:

    ```javascript
    interface Storage {
        save(data: any): void;
    }

    class Database implements Storage {
        save(data: any) {
            console.log('Data saved to database');
        }
    }

    class User {
        private _storage: Storage;

        constructor(storage: Storage) {
            this.storage = storage;
        }

        saveData(data: any) {
            this.storage.save(data);
        }
    }
    ```

</details>

## Database Questions

### What are the main 3 types of databases?

<details>

<summary>Answer</summary>

MySQL, SQlite, and NoSQL

<details>

<summary>Disclaimer</summary>

There are many more types of databases, but these are the main 3 I have encountered in jobs and cover the most common types.

</details></details>

### What is a SQL database?

<details>

<summary>Answer</summary>

A relational database management system (RDBMS) that uses SQL syntax and a tabular design. SQL is good for multi-row transactions and applications with stable data requirements. It is vertically scalable and runs in memory.

</details>

### What is a SQLite database?

<details>

<summary>Answer</summary>

A serverless relational database management system (RDBMS) that uses SQL syntax and a file-based design. SQLite is good for small applications and mobile applications. It also only allows only one write operation at a time.

</details>

### What is a NoSQL database?

<details>

<summary>Answer</summary>

A non-relational database with a document-based design that uses flexible schemas. NoSQL is good for applications with large amounts of data and applications with changing data requirements. They are typically document-based, key-value, or graph-based.

</details>

### What are the key differences between SQL and NoSQL databases?

<details>

<summary>Answer</summary>

- SQL databases are relational databases that use SQL syntax and a tabular design. NoSQL databases are non-relational databases that use a document-based design and flexible schemas.
- SQL databases are good for multi-row transactions and applications with stable data requirements. NoSQL databases are good for applications with large amounts of data and applications with changing data requirements.
- SQL databases are vertically scalable, while NoSQL databases are horizontally scalable.
- SQL databases run in memory, while NoSQL databases run on disk/are file based.

</details>

### What is indexing in databases?

<details>

<summary>Answer</summary>

Indexing is the process of creating an index on a table in a database. This index is used to speed up the retrieval of rows from the table. Indexing is done on columns that are frequently used in queries.

</details>

### What is the difference between indexing in SQL and NoSQL databases?

<details>

<summary>Answer</summary>

SQL uses a B-tree index which employs a hierarchical structure to store data. In contrast, NoSQL uses a hash index, which stores data in a key-value store.

</details>
