# **Spring**<br/>
  Spring Boot is built on top of Spring framework. It is used for building enterprise level applications.We can work with dbs,ORM,Hibernate within Spring to build entire application.<br/>
    Spring is light weight framework that is build using plain old java objects. Spring when initially introduced was used for dependency injection as it contained one module. Later on Spring got lot of improvemnts and mainly projects within that got introduced. Spring is combo of multiple things. Spring is ecosystem.<br/>
    Spring involves lot of configurations like creating projects,configuring XML file, creating the beans but Sping Boot just runs in a go. 
## Inversion of Control
Inversion of Control maily refers to inverting control that is transferring control. Programmers mainly handle the role of both flow of program and managing objects that involve creating objects, destroying objects, maintaining objects. But how? <br/>
![IOC Container](https://github.com/user-attachments/assets/f79b932c-e962-48be-9083-4fc2423bf6de)<br/>
By using this IOC Container, this is the priciple that is followed to store objects the entire managememt of objects is done by Spring that is stored in IOC Container.<br/>
## Dependency Injection
Dependency Injection is the one that takes objects that are stores in IOC Container and gives it to the one that requires it. 

## Spring Boot Configuration
In Spring Boot if you need to change port you can do it by changing the port no in application properties as server.port = port no ( for ex: 8081)


## Spring framework
In Spring framework generally we dont create and manage objects , everything is taken care by Spring. So here we use Application Context that is used to get the objects from container , previously Bean factories were used.
To use Application Context we need Spring Context
Application Context is a super set of Bean factory.
In Application Context while we load the xml file the objects get created. and in getBean we just use the bean.
Only mentioned bean in xml file is created. How many times you mention that many times bean will be created. 

## Scope in Spring framework
In Spring framework generally we use two scopes Singleton and Prototype. In Singleton when the xml file is loaded the objects get created. where as in Prototype when we call getBean at that time objects will be created. 

## Setter Injection
If we want to set some values to the variables we use the property name inside the bean tag in xml. we specify name of variable and its value. This calls setter methods to set the value so it is known as Setter Injection.

<property name ="" class=""/>

## Ref Attribute
Ref Attribute is used to assign the reference object of one class to another class. 

## Constructor Injection
Constructor is mainly used to intialize the values the objects. We can use Constructor-arg to initialize the values. 
We can assign the values to the variables by using value. it usually works based on sequence and if we dont want according to sequence then we can use the index along with value . and we also have another option type that specifies type but if there multiple then it leads to problem.
