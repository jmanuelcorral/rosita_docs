# Configuration
The main Configuration file in Rosita is AppSettings.json
Here you have a brief sample:
```
{
  "Logging": {
    "IncludeScopes": false,
    "LogLevel": {
      "Default": "Verbose",
      "System": "Information",
      "Microsoft": "Information"
    }
  },
  "Smtp": {
    "Server": "0.0.0.1",
    "User": "user@company.com",
    "Pass": "123456789",
    "Port": "25"
  },
  "Databases": {
    "MainConnectionString": "data source=.\\sqlexpress;initial catalog=Invoices;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework",
    "LogsConnectionString": "FakeDb2",
    "MailConnectionString": "FakeDb3"
  }
}
```
This file is included in the project `Rosita.Invoice.Api.Service` and every time you build the project, the file is copied with the output. 

##Database section

if the `MainConnectionString` is not set, the aplication works in Memory Mode, and no need database.