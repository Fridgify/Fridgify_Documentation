# Test plan

## 1.	Introduction
### 1.1	Purpose
The purpose of the Iteration Test Plan is to gather all of the information necessary to plan and control the test effort for a given iteration. 
It describes the approach to testing the software.
This Test Plan for **Fridgify** supports the following objectives:
-	Identifies the items that should be targeted by the tests.
-	Identifies the motivation for and ideas behind the test areas to be covered.
-	Outlines the testing approach that will be used.
-	Identifies the required resources and provides an estimate of the test efforts.

### 1.2	Scope
This document describes the used tests, as they are unit tests and functionality testing.

### 1.3	Intended Audience
This document is meant for internal use primarily.

### 1.4	Document Terminology and Acronyms
- **SRS**	Software Requirements Specification
- **n/a**	not applicable
- **tbd**	to be determined

### 1.5	 References
| Reference        | 
| ------------- |
| [SAD](https://github.com/Fridgify/Fridgify_Documentation/blob/master/planning/architecture/rup_sad.md) | 
| [Function Points](https://github.com/Fridgify/Fridgify_Documentation/tree/master/planning/analysis) |
| [Manage Account](https://github.com/Fridgify/Fridgify_Documentation/tree/master/use_cases/account/manageAccountUC.md) |
| [Login](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/authentication/login/login.md) |
| [Register](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/authentication/register/register.md) |
| [Create Fridge](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/createFridge/createFridgeUseCase.md) |
| [Add Content](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/fridgeContent/addContent/addContentUseCase.md) |
| [Change Content Volume](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/fridgeContent/changeContentVolume/changeContentVolume.md) |
| [Get Content](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/fridgeContent/getContent/getFridgeContentUseCase.md) |
| [Remove Content](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/fridgeContent/removeContent/removeContentUseCase.md) |
| [Get Fridges](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/getFridges/getFridgesUseCase.md) |
| [Join Fridge](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/joinFridge/joinFridgeUseCase.md) |
| [Fridge User Management](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/management/ManageFridgeUsersUC.md) |
| [Remove Fridge](https://github.com/Fridgify/Fridgify_Documentation/tree/master//use_cases/fridge_ucs/removeFridge/deleteFridgeUseCase.md) |   
            
## 2.	Evaluation Mission and Test Motivation
### 2.1	Background
By testing source code, we ensure our application to run smoothly. The goal is to make sure, that our application does not run into any unexpected errors.
### 2.2	Evaluation Mission
The mission of this test plan is to prevent errors in production and ensure an outstanding software quality.
### 2.3	Test Motivators
Our testing is motivated by 
- quality risks 
- technical risks, 
- use cases 
- functional requirements

## 3.	Target Test Items
The listing below identifies those test items (software, hardware, and supporting product elements) that have been identified as targets for testing. 
This list represents what items will be tested. 

Items for Testing:
- Python Backend
- Flutter Frontend

## 4.	Outline of Planned Tests
### 4.1	Outline of Test Inclusions
Unit Testing the backend as well as Integration (especially API testing) for the backend. <br/>
Unit Testing and functional Testing for the Frontend. <br/>
### 4.2	Outline of Other Candidates for Potential Inclusion
Stress Testing the application and its servers.
### 4.3 Outline of Test Exclusions
Simulating cyber attacks is currently not part of the test plan.

## 5.	Test Approach

General blog post about [testing](https://blog.fridgify.com/phase-2-week-4-testing-and-badges/).

### 5.1 Initital Test-Idea Catalogs and Other Reference Sources
**n/a**
### 5.2	Testing Techniques and Types
#### 5.2.1 Python Backend Testing
|| |
|---|---|
|Technique Objective  	| The backend should be started. Several request should be made to determine the correct functionality of the backend. |
|Technique 		|  Data should be mocked. A productive environment (same database technology) should be used. |
|Oracles 		| Endpoints return the correct and expected data as well as the expected response codes. |
|Required Tools 	| unittest (Python), Postgres, Docker, Django (Python), Postman |
|Success Criteria	| expected responses, passing tests |
|Special Considerations	|     -          |

#### 5.2.2 Flutter Frontend Testing
|| |
|---|---|
|Technique Objective  	| Every interaction with the frontend should function as intended. |
|Technique 		| Unit Tests and Gherkin tests should test the technology. For testing the frontend uses a mock backend first and then the develop backend.  |
|Oracles 		| backend returns expected data, information is shown as expected |
|Required Tools 	| Gherkin, Flutter Tests & Mocks |
|Success Criteria	| Expected behavior and passing tests |
|Special Considerations	|     -          |

#### 5.2.3 Business Cycle Testing
**n/a**

#### 5.2.4 User Interface Testing
Updated version of the [testing blog post](https://blog.fridgify.com/phase-2-week-4-testing-and-badges/)

#### 5.2.5 Performance Profiling 
**n/a**

#### 5.2.6 Load Testing
**n/a**

#### 5.2.7 Stress Testing
**n/a**

#### 5.2.8	Volume Testing
**n/a**

#### 5.2.9	Security and Access Control Testing
**n/a**

#### 5.2.10	Failover and Recovery Testing
**n/a**

#### 5.2.11	Configuration Testing
**n/a**

#### 5.2.12	Installation Testing
Test was performed by hopper. [Blog post](https://blog.fridgify.com/phase-2-week-9-installation/) for the installation.

## 6.	Entry and Exit Criteria
### 6.1	Test Plan
#### 6.1.1	Test Plan Entry Criteria
Building a new version of the software with DockerHub will execute the testprocess.
#### 6.1.2	Test Plan Exit Criteria
When all tests pass without throwing an exception.
#### 6.1.3 Suspension and Resumption Criteria
It will be possible to skip the tests for faster deployment during development.

## 7.	Deliverables
### 7.1	Test Evaluation Summaries
Test evaluation will be available online every time the tests are run in DockerHub. The code coverage is shown via badges inside of the GitHub repository of the respective branch.
### 7.2	Reporting on Test Coverage
Backend Coverage is reported by Django Nose. Frontend Coverage is reported by Darts lcov.
### 7.3	Perceived Quality Reports
tbd
### 7.4	Incident Logs and Change Requests
Parts of the above features are already integrated into the GitHub environment.
### 7.5	Smoke Test Suite and Supporting Test Scripts
Regressions are determined through new code coverage runs for each update.
### 7.6	Additional Work Products
#### 7.6.1	Detailed Test Results
tbd

#### 7.6.2	Additional Automated Functional Test Scripts
**n/a**
#### 7.6.3	Test Guidelines
In general all testable code should be tested. Due to time constraint this is of course not always possible. Therefore we set a bound of at least 80%.
#### 7.6.4	Traceability Matrices
**n/a**

## 8.	Testing Workflow
Developers should execute tests locally before pushing source code. When pushing to branches, tests are executed automatically.
## 9.	Environmental Needs
This section presents the non-human resources required for the Test Plan.
### 9.1	Base System Hardware
The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource | Quantity | Name and Type |
|---|---|---|
| Production "Server" (API) <br/> | 1 | Debian Buster Server |
| Server Name |  	| api.fridgify.com |
| <hr> | <hr> | <hr> |
| Development "Server" (API) | 1 | Debian Buster Server	|
| Server Name |  | api-dev.fridgify.com |
| <hr> | <hr> | <hr> |
| Database | 2 | PostgreSQL |
| Database Name |  | Production: PostgreSQL fridgify_backend_db |
| Database Name |  | Development: fridgify_backend_db_develop |
| Database Name |  | sqlite on localhost |

### 9.2	Base Software Elements in the Test Environment
The following base software elements are required in the test environment for this Test Plan.

| Software Element Name | Version | Type and Other Notes |
|---|---|---|
| Windows | 10 | Operating System |
| Python | 3.7 | Programming Language |
| Docker | | Container Software |
| PostgreSQL |  | Database |
| sqlite |  | Database |

### 9.3	Productivity and Support Tools
The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                              |
|-----------------------|----------------------------------------------|
| Code Hoster           | [github.com](https://github.com/fridgify/) |
| CI Service            | [TeamCity](https://fridgify-tc.donkz.dev) |
| Container Hub         | [DockerHub](https://hub.docker.com/repository/docker/fridgify/fridgify)

### 9.4	Test Environment Configurations
In order to be able to run the tests you need to have a database set up and running. Or you have docker, which would allow you to start a Docker container with the help of the appropriate Dockerfile.

## 10.	Responsibilities, Staffing, and Training Needs
### 10.1	People and Roles
This table shows the staffing assumptions for the test effort.

Human Resources


| Role | Minimum Resources Recommended (number of full-time roles allocated) |	Specific Responsibilities or Comments |
|---|---|---|
| Test Manager | 1 | Provides management oversight. <br> Responsibilities include: <br> planning and logistics <br> agree mission <br> identify motivators<br> acquire appropriate resources<br> present management reporting<br> advocate the interests of test<br>evaluate effectiveness of test effort |
| Test Designer | 1 | Defines the technical approach to the implementation of the test effort. <br> Responsibilities include:<br> define test approach<br> define test automation architecture<br> verify test techniques<br> define testability elements<br> structure test implementation|
| Tester | 1 |	Implements and executes the tests.<br> Responsibilities include:<br> implement tests and test suites<br> execute test suites<br> log results<br> analyze and recover from test failures<br> document incidents|
| Test System Administrator | 1 | Ensures test environment and assets are managed and maintained.<br> Responsibilities include:<br> 	administer test management system<br> install and support access to, and recovery of, test environment configurations and test labs | 
| Database Administrator, Database Manager | 1 | Ensures test data (database) environment and assets are managed and maintained.<br> Responsibilities include:<br> support the administration of test data and test beds (database). |
| Implementer | 3 | Implements and unit tests the test classes and test packages.<br> Responsibilities include:<br> creates the test components required to support testability requirements as defined by the designer |

### 10.2	Staffing and Training Needs
* Flutter Basics/Advanced knowledge (Dennis, Joschua)
* Django Basics/Advanced knowledge (Duc, Joschua)
* Docker and docker-compose Basics (Joschua, Duc)

## 11.	Iteration Milestones

| Milestone | Planned Start Date | Actual Start Date | Planned End Date | Actual End Date |
|---|---|---|---|---|
| Have Unit Tests | 01.04.2020 | since start of development | 4.6.2020 | 03.06.2020 |
| 70% coverage | 12.5.2020 | 12.05.2020   | 4.6.2020   | 3.06.2020   |
| Tests integrated in CI | 01.04.2020 | 01.04.2020 | 12.05.2020 | 12.05.2020 |


## 12.	Risks, Dependencies, Assumptions, and Constraints
| Risk | Mitigation Strategy	| Contingency (Risk is realized) |
|---|---|---|
| Unexpected failures in production | Cover as much scenarios as possible, Logging | Look into logs and fix the bug, Roll back version if necessary |
## 13. Management Process and Procedures
**n/a**
