# Builder Patter - from Gang of Four : GoF
**intent**: "Separate the construction of a complex object from its preresentation so that the same 
construction process can create different representations."

## Telescoping Constructor Promblem
**example**: 

const BillTheManager = new Account('Bill', true, true, true, true, 15)
- ? What does true, true, true, true, 15 mean?

### Builder example
var bill = new PersonBuilder('bill').makeEmployee().makeManager().makePartTime().giveMoney(200)

Review the code folder to see how you can implement a builder.