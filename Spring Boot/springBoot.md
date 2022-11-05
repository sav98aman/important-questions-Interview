### Spring Boot Important Questions 


<br>


*Q1.    What is loose coupling?*

    One of the most key aspects of a Java project is loose coupling. 

    In loose coupling, a method or class is almost independent, and they have less depended on each other. 
    In other words, the more knowledge one class or method has about another class or method, the more tightly coupled structure is developed. 
    If the classes or methods know less about each other, the more loosely coupled structure comes into existence.
    note:-achieve loose coupling, one should use abstract classes or interface while performing inheritance. 
   

*Q2.    What is a Dependency?*

    Spring-Boot framework is the most popular web development framework. No doubt, it provides an abundance of essential features and a convenient way to handle those features. At the heart of Spring-Boot, is the ‘Dependency Management’ feature. 

*Q3.    What is IOC (Inversion of Control)?*

    Spring IoC (Inversion of Control) Container is the core of Spring Framework. 
    It creates the objects, configures and assembles their dependencies, manages their entire life cycle. The Container uses Dependency Injection(DI) to manage the components that make up the application

    It gets the information about the objects from a configuration file(XML) or Java Code or Java Annotations and Java POJO class. These objects are called Beans. Since the Controlling of Java objects and their lifecycle is not done by the developers, hence the name Inversion Of Control.

    There are 2 types of IoC containers:
        BeanFactory 
        ApplicationContext

    That means if you want to use an IoC container in spring whether we need to use a BeanFactory or ApplicationContext. The BeanFactory is the most basic version of IoC containers, and the ApplicationContext extends the features of BeanFactory. The followings are some of the main features of Spring IoC,

    Creating Object for us,
    Managing our objects,
    Helping our application to be configurable,
    Managing dependencies

    Implementation: So now let’s understand what is IoC in Spring with an example. Suppose we have one interface named Sim and it has some abstract methods calling() and data().

*Q4.   Can you give few examples of Dependency*
    
  
    public interface Client {
        void doSomething();
    }
    
    public interface Service {
        String getInfo();
    }


    public class ServiceC implements Service {
        @Override
        public String getInfo() {
            return "ServiceC's Info";
        }
    }
 
    public class ServiceD implements Service {
        @Override
        public String getInfo() {
            return "ServiceD's Info";
        }
    }

*Q5     What is Auto Wiring?*

    Autowiring feature of spring framework enables you to inject the object dependency implicitly. 
    
    It internally uses setter or constructor injection.

    Autowiring can't be used to inject primitive and string values. It works with reference only.

    Autowiring Modes
    There are many autowiring modes:

| no   |  mode |    description     |
|   :---:   |   :---:   |   :---:   |
|   1   | no    |   It is the default autowiring mode. It means no autowiring bydefault.    |
|   2   | byName   |   IThe byName mode injects the object dependency according to name of the bean. In such case, property name and bean name must be same. It internally calls setter method.  |
|   3   | bytag TYpe   |  The byType mode injects the object dependency according to type. So property name and bean name can be different. It internally calls setter method    |
|   4   | constructor   | The constructor mode injects the dependency by calling the constructor of the class. It calls the constructor having large number of parameters.   |
|   5  | autodetect   | 	It is deprecated since Spring 3.   |


*Q 7.   What are the important roles of an IOC Container?*

    The IoC container is responsible to instantiate, configure and assemble the objects. 
    The IoC container gets informations from the XML file and works accordingly. The main tasks performed by IoC container are:

    to instantiate the application class
    to configure the object
    o assemble the dependencies between the objects

*      There are two types of IoC containers. They are:

    BeanFactory

    ApplicationContext
        
            The ClassPathXmlApplicationContext class is the implementation class of ApplicationContext interface. We need to instantiate the ClassPathXmlApplicationContext class to use the ApplicationContext as given below:

        ApplicationContext context =   new ClassPathXmlApplicationContext("applicationContext.xml");  

        The constructor of ClassPathXmlApplicationContext class receives string, so we can pass the name of the xml file to create the instance of ApplicationContext.

*Q 8.   What are Bean Factory and Application Context?*

    This interface is designed on top of the BeanFactory interface. The ApplicationContext interface is the advanced container that enhances BeanFactory functionality in a more framework-oriented style.

    While the BeanFactory provides basic functionality for managing and manipulating beans, often in a programmatic way, the ApplicationContext provides extra functionality like MessageSource, Access to resources, Event propagation to beans, Loading of multiple (hierarchical) contexts etc

    ApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");


*Q 9.   Can you compare Bean Factory with Application*

    This is the root interface for accessing a Spring bean container. 
    
    It is the actual container that instantiates, configures, and manages a number of beans. 

    These beans collaborate with one another and thus have dependencies between themselves. 

    These dependencies are reflected in the configuration data used by the BeanFactory. 

    This interface is implemented by the objects that hold a number of bean definitions, each uniquely identified by a String name. 

    The most common implementation class used for this BeanFactory is XmlBeanFactory available in org.springframework.beans.factory.xml package. 

    *Q 10.  How does Spring know where to search for*

        With Spring, we use the @ComponentScan annotation along with the @Configuration annotation to specify the packages that we want to be scanned. @ComponentScan without arguments tells Spring to scan the current package and all of its sub-packages.

        Note that the main application class is also a bean, as it's annotated with @Configuration, which is a @Component.

        We should also note that the main application class and the configuration class are not necessarily the same. If they are different, it doesn't matter where we put the main application class. Only the location of the configuration class matters, as component scanning starts from its package by default.


*Q 11.  What is a component scan?*

    When developing Spring Boot applications, you need to tell the Spring Framework where to look for Spring components. Using component scan is one method of asking Spring to detect Spring managed components. Spring needs the information to locate and register all the Spring components with the application context when the application starts.

    Spring can auto scan, detect, and instantiate components from pre-defined project packages. It can auto scan all classes annotated with the stereotype annotations @Component, @Controller, @Service, and @Repository


*Q 12.  How do you define a component scan in XML and*


*Q13. How is it done with Spring Boot?*
