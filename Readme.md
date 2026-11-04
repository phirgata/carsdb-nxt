Title:
====================================================
CarsDBNxt

Architecture:
=====================================================
Clean architecture

Technologies:
=====================================================
- ASP.NET MVC Core
- MongoDB
- Bootstrap
- Bootstrap Icons
- Typescript
- Unit tests

Projects:
=====================================================
- CarsDBNxt.Web - holds the ASP.NET MVC Core application (so the UI, controlller and DI layers). Imports CarsDBNxt.Services, CarsDBNxt.Models and CarsDBNxt.Database.
- CarsDbNxt.Models - holds the application entities. Does not import any other project from the solution.
- CarsDbNxt.Services - holds the business use cases. Imports CarsDBNxt.Models.
	- folder Interfaces - holds the services as interfaces
	- folder Implementation - holds the implementation of the services
	- folder Repositories - holds the required respository interfaces for the application. Implementation for them will be found in the database layer
	- folder for DB data models?
- CarsDbNxt.Database - implements repositories for working with the MongoDB. Imports CarsDBNxt.Services (and CarsDBNxt.Models?).