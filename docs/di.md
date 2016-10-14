# Dependency Injection

For this development we have choose SimpleInjector as IoC Framework. It's elegant, simple and have a good performance.

## Composition

Every project of the solution have a Composition.cs with a Setup Method, that configures the Dependecy Injection Container. 
Also, in the Crosscutting layer we have a Service Locator Antipattern implemented. This Service locator is used only for two things:
  - Resolve some dependencies in Tests Projects (for pragmatical reasons).
  - Resolve some dependencies in Mapping Process.

## LifeStyles

There are 3 main Lifestyles configured in the aplication:
   - AspNetRequestLifestyle 
   - Transient
   - Singleton

   We only use singleton for mapping factories (combined with a flyweight pattern like an object mapping cache).
   The AspNetRequestLifeStyle is the most common lifestyle configuration in the application (is the best approach in an Asp.Net application for thread-safe and garbagecollector reasons).
   Transient is commonly used in Testing, and we have tuned the dependency registration process avoiding the warnings in DbContext and UnitOfWork disposable events.
    