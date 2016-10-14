# Wellcome to Rosita

Rosita is a microservice sample project done in dot net core.

## How to Work with Rosita

Rosita is designed with the clean architecture philosophy in mind. 

The tech stack used for build this solution:
  - Asp.net core
  - EntityFramework core

## Solution layout

    /API
        Rosita.Invoice.API.Service      # The Rest API endpoint
        Rosita.Invoice.API.DtoMessages  # The Request/Response Messages for the Rest API
    /Core
        Rosita.Invoice.Core             # The Bussiness Logic of the application.
        Rosita.Invoice.Framework        # Base classess and Clean Architecture guidance patterns.
    /Infrastructure
        Rosita.Infrastructure.Database  # All the plumbing related Database/Entity Framework code.
    Rosita.XCutting                     # A set of CrossCutting concerns needed for the application design.

## Testing
Rosita has been built with Testing in mind, at the moment, whe have test the first UseCase. 
All the testing is doing with the EntityFramework InMemory Database.
