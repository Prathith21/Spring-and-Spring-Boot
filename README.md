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

## Lazy Initialization
Lazy Initialization is used mainly when we want object to be created only when we call it and not when the context loads. It is singleton, this will be useful when we want objects to be created only when we call it. lazy-init="true" to make bean a lazy initialization.

## GetBeanByType
GetBeanByType is used to get the bean by specifying the class name. Usually when get the bean by using context it returns the object. So to get the bean in its type we have to specify classname.class of bean type so that context returns the bean in that format.

## Java Based Configration
In Java Based Configration we use java file inside config pacakage. Instead of xml file we used java file for configration purpose. We have to create a class and mention annotation @configration to mention it as configration class and methods within that are beans that must be created at top we mention @Bean.

## Bean Name
Usually bean name will be by default as method name but if we want to change the name of the bean we can use @Bean(name="") to change the name of the bean.

## Bean Scope 
If we want to change the scope then we can use @Scope("prototype")

## Autowired Annotation
If you want to have wire between two beans then you can pass the bean that you want assign to the method. The bean then can be passed using setter. Mainly Autowired is used to get the beans from container and assign it to reference variable that is injecting the bean.

There are three types:
Field Injection : We write @Autowired on top of field.<br/>
Setter Injection : We write @Autowired on top of setter. But this is recommended.<br/>
Constructor Injection : We write @Autowired on top of constructor.

## Qualifier and Primary
Qualifier is used to specify exactly which bean to inject when multiple beans of the same type exist.@Qualifier("bean name") and @Primary tells Spring which bean to use by default when multiple candidates are available for autowiring. @Qualifer has more priority then @Primary

## Component Stereotype Annotation
@Component is used replace all the beans in configration file of Java. We dont need to create all those beans. We just need to specify @Component on top of class for those where objects has to be created. and we use @ComponentScan on top of Configration file to indicate which package to scan for components.

## Value Annotation
Value Annotation is mainly used to assign the values to the variables. We can also directly assign values like int age = 20 but its not a good practice and its hardcoding . So we use @Value("21") and here we can also get the values from properties file.
