# JS Objects Notes

 ### **EVERYTHING is an object**
### even the parts that aren’t— like strings or numbers— can still act like objects in some instances.
### JavaScript objects are containers storing related data and functionality
### Objects can be assigned to variables, just like any JavaScript
* Use curly braces to designate an **object literal { }**

```javascript
let spaceship = {}; // spaceship is an empty object
```
### This data is organized into key###value pairs
### A key’s value can be of any data type in the language
* **Including functions**
* Other objects
### We make key###value pair by giving the key a name
* It may have spaces and special characters
* It needs to be closed in quotation marks **“ ”**
### Separate each key###value pair in an object literal with a comma , 
* Except for the last one
* Don’t use a semicolon **;**
### **Keys are strings**
### two ways we can access an object’s property. Let’s explore the first way
* dot notation
### If we try to access a property that does not exist on that object, undefined will be returned.
```javascript
spaceship.favoriteIcecream; // Returns undefined
```
### The second way to access a key’s value is by using
* bracket notation **[ ].**
### To use bracket notation to access a objects property, we pass in the property name as a string
### We must use bracket notation when
* accessing keys that have numbers
* Spaces
* Special characters in them
```javascript
let spaceship = {
  'Fuel Type': 'Turbo Fuel',
  'Active Duty': true,
  homePlanet: 'Earth',
  numCrew: 5
};
spaceship['Active Duty'];   // Returns true
spaceship['Fuel Type'];   // Returns  'Turbo Fuel'
spaceship['numCrew'];   // Returns 5
spaceship['!!!!!!!!!!!!!!!'];   // Returns undefined
```
### With bracket notation you can also use a variable inside the brackets to select the keys of an object
* Can be helpful when working with functions
```javascript
let returnAnyProp = (objectName, propName) => objectName[propName];
returnAnyProp(spaceship, 'homePlanet'); // Returns 'Earth'
```
### If we tried to write out **returnAnyProp()**function with a dot notation, the computer would look for for a key of **“propName”**
* Not the value of propName parameter

