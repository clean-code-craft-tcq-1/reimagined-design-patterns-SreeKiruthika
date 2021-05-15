# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.

# Adapter

- This method is a structural design pattern
- As in the name, this method helps in adapting incompatible functions or objects by providing adapting objects or functions
- The idea revolves around the fact of reusing  existing solution for extention of the software feature by easy interfacing thus reducing testing efforts and development time

**How it works**
- The adapting function helps in converting the  sender parameteres / objects  into form of receiver function / object using the desired adapter services 

**Use case**
- Already existing validated solution, if needs to be reused then adapter can be used in case of solving incompatiblity issues
- Also in case when a base class calculations are expected in different  formats by it's child classes, then adapter can be used for each child class instead of designing base class to suit / meet all needd

**Pros**
- Existing solutions cas be resued
- Modification scope is less, hence less validation time
- Easy extension of features of a program

**Cons**
- But incase of more paramaters / objects to be interfaced, then additional memory is consumed for the new interfacing objects created
- This method is not for a new developments, only applicable or useful for existing

**Real World use case**
- In case of SW sharing or 3rd party SW is avaialable for reuse while modification is time consuming. 
- Say in our previous assignments, we had a BMS system in which sensor was earlier measuring in celcius, while the same was then extended to support other temperature units  like fahrenheit where a "unit conversion" adapting function was used


# Observer 
- This method is behavioral design pattern
- Basic idea is to abide with open/close principle and resource optimisation (instead of polling / service switching)

**How it works**
- A subscription mechanism is designed to notify the classes about the change in state of the class which they are observing  / dependant (say notification via callbacks)
- Open/close principle is met as the main class / object is not  modified whenever a new object which demand the notification from main object is added, but the need of notifying is met through callbacks
- Also polling or the frequent check by the classess are not needed as they will be notified when ever state change occurs

**Use case**
- This implementation is used when changes to the state of one object may require changing other objects, and the actual set of objects is unknown beforehand or changes dynamically.
- Also in case of interrupt kind of implementation this pattern is the mostly used

**Pros**
- Open / close prinicple
- Avoiding polling mechanism which lead to resource optimisation

**Cons**
- But in this method , the priority cannot be set among the requesters as they are dynamically allocated
- Number of observers is restricted based on callback array size (hence needs to be taken care in design)

**Real World use case**
-In cases where a communication frame / data is needed,  only when requested from external sources and not to be transmitted periodically.


# State
- This method is behavioral design pattern
- This method can be used if the system behaviour / response is dependent on the current state of the system.

**How it works**
- The main idea is that, at any given moment, there’s a finite number of states which a system  can be in. 
- Hence the entire features of the system is divided based on the state at which it could be performed
- The trasnistion from one state to another state needs to have a cetain condition met and hence that serves a check for state transition of the system

**Use case**
- In systems where same input or condition needs unique reactions based on the current state of the system 
- Also to have a clear and defined restriction in state transition of the system.

**Pros**
-  It helps to reduce redundant / multiple condition check for system state change 
-  Avoiding unintended / unexpected system behaviour by restricting the features of the sytem in current state and have a clear control on state transition of the system.

**Cons**
- In case of very less number of states and no further enhancement expected, normal implementataion itself holds good and apllying this method id redundant
- In later point of time, introducing a new state needs to be done carefully.

**Real World use case**
- Net banking programs were each user actions / scope can be considered as states
- Engine state in an autombile, first key input is needed to start the engine, then it goes to cranking and then only running


# Bridge 
- This method is structural design pattern
- It is used in large cases where multi level split is feasible as objects turn out ot be combinations of sub levels

**How it works**
- In case the product is characteristed by 3 parameters say shape , colour and type , then the 3^3 = 27  comibinations are possible , hence it might need a lot of objects to be created. Incase if a new type is to be added, then many objects are to be created.
- Instead if a class for shape, clas for colour and class for type is created, then the classess can be combined with the needed parameter ffrom each class to create object

**Use case**
- It is used in cases where a larger number of class objects would be created / needed , but in which they turn out to be combination of objects that can be split into base objects
- Use the Bridge pattern when you want to divide and organize a monolithic class that has several variants of some functionality.
- Use the pattern when you need to extend a class in several orthogonal (independent) dimensions.

**Pros**
- Also this method can be used for prototype projects which is subject to further enhancement of base features
- In case of Platform independent implementation this method is significant.
- Easy to maintain and enhancement

**Cons**
- Becomes complex if multiple levels are to be realised

**Real World use case**
- Variant handing applications 
- Combination use case applications
