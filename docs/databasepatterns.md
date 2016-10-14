#Database Patterns

We think one of the best approach working with databases is the combo Unit of Work / Generic Repository.

##Database Entities
All the database entities have an inheritance with the Base class BaseDao that defines a Standar convention of work with the primary key.

##Mapping Configuration
Each Entity has his mapping configuration in the `Mappings` folder. Every Mapping class is configured using the Entity framework FluentApi.

##Unit Of Work
We have a Unit Of Work Approach with the base contract IUnitOfWork.
Also we have a IBussinessUnitOfWork that group all the repositories that can participate in the context transaction.