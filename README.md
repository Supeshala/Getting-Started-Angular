# Getting-Started-Angular
This repository is created for with regard to the following blog of Getting Started with Angular.
http://supeshalamadushani.blogspot.com/2018/01/getting-started-with-angular.html

Nowadays Angular has become an outstanding web development framework because of the following reasons.
Provides improved application design architecture
Promotes code re usability
Consists of easy to remove components
Employs two way data binding

Angular contains the following core types of objects and components.
Modules
Controllers
Services
Directives

These core components can be injected into each other using Dependency Injection (DI) mechanism built in Angular. DI is a software design pattern that assigns dependencies to components instead of hard coding them within the component itself. Angular uses a feature called directives that allow to write HTML code, which then builds the HTML of the application instead of using templates to generate the user interface. The adoption of two-way data binding can be seen in Angular. It tightly bounds the values in your view to the data source. When a user interacts and updates a value, the model is updated dynamically as well.
When a web page is loaded, the browser creates a Document Object Model (DOM) of the page. Using the DOM, JavaScript can access and change all the elements of an HTML document. Angular can separate each component into a separate files because Angular is DOM-based. Due to its component structure, Angular offers speed and flexibility.

Introduction to Angular Modules

Let’s see what are Angular modules? Angular module is considered as a container for various parts of the app. Since an Angular app does not have a single point of entry like some environments, modules provides the means for defining how the application can be started. The components of Angular modules provide specific functionality via self-contained sections of code. Through the process called Dependency Injection, modules can share variables between one another without having to reuse code. Angular modules are organized by function rather than type. This modular concept helps you better understand the context of the different components, enables more direct access to the modules, and provides more streamlined testing of the modules. Modules provide a number of benefits including:
They may be reused in multiple applications
They can be loaded in any order (or in parallel)
Unit testing need only load the relevant modules, keeping the tests fast
 
Module is assigned to a variable called app in left side of the assignment. The right side of the statement specifies where the module is created. The empty array [], is for injecting other modules as necessary.
To add controllers or other components to the module, reference the variable that you had defined for the module (var App in this instance), and then add additional method calls, like so:

Bootstrapping Angular Modules
Bootstrapping your module starts Angular and initializes the module, binding it to a section of the HTML that you wish to transform into a dynamic view. "Binding" tells Angular that this piece of HTML will be controlled by Angular, which will allow it to transform the HTML as the data changes, thereby creating a "Dynamic View" instead of the "Static View" of plain HTML. 

Your Angular app can affect as much or as little HTML as you prefer. For example, if you are defining a Single Page App, you will want to bootstrap your module on the <html> element, so that Angular can control the entirety of the page.
If you want Angular to only control some of your page, for example, if you are implementing Angular in a website that was built mostly out of jQuery.

Introduction to Dependency Injection
Dependency Injection (DI) is a software design pattern that manages how components in a system obtain their dependencies. In Angular, Dependency Injection is responsible for:
Creating components
Maintaining a component's state
Providing components to other components, as required

In Angular, DI allows us to share variables and functions between self-contained modules without having to reuse code, and maintains the state of each component.DI employs the injector, the service object(s) to be used, the client object that is depending on the services it uses, and the interfaces. When Angular compiles the HTML, it processes the ng-controller directive, which, in turn, asks the injector to create an instance of the controller and its dependencies. The application code simply declares the dependencies it needs without having to deal with the injector. Angular invokes certain functions, such as service factories and controllers, via the injector. You annotate these functions so that the injector knows what services to inject into the function. These functions are injectable with dependencies, just like the factory functions. The factory methods are registered with the modules. Components such as services, directives, filters, and animations are defined by an injectable factory method or constructor function. These components can be injected with service and value components as dependencies.
DI allows a client the flexibility of being configurable. Only the client's behavior is fixed. The client may act on anything that supports the intrinsic interface the client expects. The client only needs to know about the intrinsic interfaces of the services since these define how the client may use the services. This separates the responsibilities of use and construction. The interfaces are the dependency types that the client expects. You use DI when defining components or when specifying functions to run at configuration and run time for a module by calling the config and run methods. The run method accepts a function, which can be injected with service, value, and constant components as dependencies. Note that you cannot inject providers into run blocks. The config method accepts a function, which can be injected with provider and constant components as dependencies. Note that you cannot inject service or value components into configuration.

One of the most commonly used dependencies in Angular is $scope. Controllers need access to the $scope object in order to bind values to the view. 

