# Object-Oriented JavaScript
*Object*: An object is a container for values in the form of _properties_ and functionality in the form of _methods_.
*What they do:*
  -Provide functionality through methods. Methods may or may not return values.
  -Provides data storage in properties
  -The name of the property is a key
  -The contents of a property is known as a value.

*Native Objects in JavaScript*
  -Number
  -String
  -Array
  -Boolean
  -Object

*Host Objects in the Browser*
  -document
  -console
  -Element

*Your Own Objects*
  -Anything you like (contacts, songs, guests)

## Object Literals
-It holds the state of a thing.
*Object Literal Ex.*
```
var person = {
  name: "Lauren",
  treeHouseStudent: true
}
person.name;
person.treeHouseStudent;
```
## Adding a Method to Objects
*Syntax Ex.*
```
var contact = {
  fullName(object): function () {
    var firstName = "Andrew";
    var lastName = "Cenci";
  }
}
```
## Understanding "this"
-"this" is the object that owns the method being called.

## Returning Values
-`return` prevents any additional lines of code from being executed.

## Modifying Objects with Methods
-within objects use commas not semi-colons

## Creating Multiple Instances with Constructors
*Constructor Functions*
-Describe how an object should be created
-Create similar objects
-Each object created is known as an instance of that object type.

*Syntax Example*
```
function Contact(name, email) {

  this.name = name;
  this.email = email;

}
var contact = new Contact("Andrew", "andrew@teamtreehouse.com");
var contact2 = new Contact("Dave", "dave@teamtreehouse.com");
```
-`new` turns it into a constructor function.
-Lets you create as many objects of the same type.

## Methods with Prototypes
-Prototypes are templates for objects, with values and behaviors to be shared between objects.

## Prototype Chains
`Object.create` to form prototype chains.
