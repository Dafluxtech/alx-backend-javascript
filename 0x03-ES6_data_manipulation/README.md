# ES6 data manipulation


This project contains tasks for learning to manipulate data in ECMAScript 2015 (ES6).


![](https://i.imgur.com/ZJT26qb.jpg)


-----------------------------

![](https://www.tutsmake.com/wp-content/uploads/2019/03/JavaScript-Array-Methods.jpeg)



An array is a special variable in all the languages that are used to store different elements. JavaScript array contains some built-in properties that every JavaScript developer should know how to use and when or where to use them. We can use them to add, remove, iterate, or manipulate data as per our requirements.

## Learning Objectives

- How to use map, filter and reduce on arrays
- Typed arrays
- The Set, Map, and Weak link data structures

## Learning Requiremnets

- All your files will be executed on `Ubuntu 18.04` LTS using `NodeJS 12.11.x`
- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`
- All your files should end with a new line
- A __README.md file__, at the root of the folder of the project, is mandatory
- Your code should use the `js extension`
- Your code will be tested using Jest and the command npm run test
- Your code will be verified against lint using `ESLint`
- Your code needs to pass all the tests and lint. You can verify the entire project running npm run full-test
- All of your functions must be exported


# :computer: Tasks To Complete

+ [x] 0. **You used to attend a place like this at some point**<br/>[0-classroom.js](0-classroom.js) contains a script that exports a class named `ClassRoom` with the following requirements:
  + Prototype: `export default class ClassRoom`.
  + It should accept one attribute named `maxStudentsSize` (Number) and assigned to `_maxStudentsSize`.

+ [x] 1. **Let's make some classrooms**<br/>[1-make_classrooms.js](1-make_classrooms.js) contains a script that meets the following requirements:
  + Import the `ClassRoom` class from [0-classroom.js](0-classroom.js).
  + Export a function named `initializeRooms`. It should return an array of 3 `ClassRoom` objects with the sizes 19, 20, and 34 (in this order).

+ [x] 2. **A Course, Getters, and Setters**<br/>[2-hbtn_course.js](2-hbtn_course.js) contains a script that exports a class named `HolbertonCourse` with the following requirements:
  + Constructor arguments:
    + `name` (String).
    + `length` (Number).
    + `students` (array of Strings).
  + Make sure to verify the type of attributes during object creation.
  + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
  + Implement a getter and setter for each attribute.

+ [x] 3. **Methods, static methods, computed methods names..... MONEY**<br/>[3-currency.js](3-currency.js) contains a script that exports a class named `Currency` with the following requirements:
  + Constructor arguments:
    + `code` (String).
    + `name` (String).
  + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
  + Implement a getter and setter for each attribute.
  + Implement a method named `displayFullCurrency` that will return the attributes in the format `name (code)`.

+ [x] 4. **Pricing**<br/>[4-pricing.js](4-pricing.js) contains a script that meets the following requirements:
  + Import the class `Currency` from [3-currency.js](3-currency.js).
  + Export a class named `Pricing` that meets the following requirements:
    + Constructor arguments:
      + `amount` (Number).
      + `currency` (Currency).
    + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
    + Implement a getter and setter for each attribute.
    + Implement a method named `displayFullPrice` that returns the attributes in the format `amount currency_name (currency_code)`.
    + Implement a static method named `convertPrice`. It should accept two arguments: `amount` (Number), `conversionRate` (Number). The function should return the amount multiplied by the conversion rate.

+ [x] 5. **A Building**<br/>[5-building.js](5-building.js) contains a script that exports a class named `Building` with the following requirements:
  + Constructor arguments:
    + `sqft` (Number).
  + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
  + Implement a getter for each attribute.
  + Consider this class as an abstract class. And make sure that any class that extends from it should implement a method named `evacuationWarningMessage`.
    + If a class that extends from it does not have a `evacuationWarningMessage` method, throw an error with the message `Class extending Building must override evacuationWarningMessage`.

+ [x] 6. **Inheritance**<br/>[6-sky_high.js](6-sky_high.js) contains a script that meets the following requirements:
  + Import `Building` from [4-building.js](4-building.js).
  + Export a class named `SkyHighBuilding` that extends from `Building` and meets the following requirements:
    + Constructor arguments:
      + `sqft` (Number) (must be assigned to the parent class `Building`).
      + `floors` (Number).
    + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
    + Implement a getter for each attribute.
    + Override the method named `evacuationWarningMessage` and return the following string `Evacuate slowly the NUMBER_OF_FLOORS floors`.

+ [x] 7. **Airport**<br/>[7-airport.js](7-airport.js) contains a script that exports a class named `Airport` with the following requirements:
  + Constructor arguments:
    + `name` (String).
    + `code` (String).
  + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
  + The default string description of the class should return the airport `code` (example below).

+ [x] 8. **Primitive - Holberton Class**<br/>[8-hbtn_class.js](8-hbtn_class.js) contains a script that exports a class named `HolbertonClass` with the following requirements:
  + Constructor arguments:
    + `size` (Number).
    + `location` (String).
  + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
  + When the class is cast into a `Number`, it should return the size.
  + When the class is cast into a `String`, it should return the location.

+ [x] 9. **Hoisting**<br/>[9-hoisting.js](9-hoisting.js) contains a fixed and working copy of the code below:
  ```js
  const class2019 = new HolbertonClass(2019, 'San Francisco');
  const class2020 = new HolbertonClass(2020, 'San Francisco');

  export class HolbertonClass {
    constructor(year, location) {
      this._year = year;
      this._location = location;
    }

    get year() {
      return this._year;
    }

    get location() {
      return this._location;
    }
  }

  const student1 = new StudentHolberton('Guillaume', 'Salva', class2020);
  const student2 = new StudentHolberton('John', 'Doe', class2020);
  const student3 = new StudentHolberton('Albert', 'Clinton', class2019);
  const student4 = new StudentHolberton('Donald', 'Bush', class2019);
  const student5 = new StudentHolberton('Jason', 'Sandler', class2019);

  export class StudentHolberton {
    constructor(firstName, lastName) {
      this._firstName = firstName;
      this._lastName = lastName;
      this._holbertonClass = holbertonClass;
    }

    get fullName() {
      return `${this._firstName} ${this._lastName}`;
    }

    get holbertonClass() {
      return this.holbertonClass;
    }

    get fullStudentDescription() {
      return `${self._firstName} ${self._lastName} - ${self._holbertonClass.year} - ${self._holbertonClass.location}`;
    }
  }


  export const listOfStudents = [student1, student2, student3, student4, student5];
  ```

+ [x] 10. **Vroom**<br/>[10-car.js](10-car.js) contains a script that exports a class named `Car` with the following requirements:
  + Constructor arguments:
    + `brand` (String).
    + `motor` (String).
    + `color` (String).
  + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
  + Add a method named `cloneCar`. This method should return a new object of the class.

+ [x] 11. **EVCar**<br/>[100-evcar.js](100-evcar.js) contains a script that meets the following requirements:
  + Import `Car` from [10-car.js](10-car.js).
  + Export a class named `EVCar` that extends the `Car` class and meets the following requirements:
    + Constructor arguments:
      + `brand` (String).
      + `motor` (String).
      + `color` (String).
      + `range` (String).
    + Each attribute must be stored in an "underscore" attribute version (ex: `name` is stored in `_name`).
    + For privacy reasons, when `cloneCar` is called on an `EVCar` object, the object returned should be an instance of `Car` instead of `EVCar`.
