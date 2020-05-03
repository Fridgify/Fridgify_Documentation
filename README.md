# fridgify-doc
This repository contains all files related to the documentation of Fridgify.

The following *README* will guide you through this repository as well as give you an overview of every important file.

This document is going to be maintained constantly.

### Structure
1. **Management Docs**
   1. [SRS](./planning/srs.md)
   2. [SAD](./planning/architecture/rup_sad.md)
   3. [Risk Management & Use Case Durations](./planning/risks/risk.md)
2. **Use Cases**
   1. **Overall Use Case Diagram**
      1. [Semester 1](./use_cases/overall_ucd.png)
      2. [Semester 2](./use_cases/overall_ucd_v2.png)
   2. **Use Case Collection**
      1. [Manage Account](./use_cases/account/manageAccountUC.md)
      2. **Authentication**
         1. [Login](./use_cases/authentication/login/login.md)
         2. [Register](./use_cases/authentication/register/register.md)
      3. **Fridges**
         1. [Create Fridge](./use_cases/fridge_ucs/createFridge/createFridgeUseCase.md)
         2. **FridgeContent**
            1. [Add Content](./use_cases/fridge_ucs/fridgeContent/addContent/addContentUseCase.md)
            2. [Change Content Volume](./use_cases/fridge_ucs/fridgeContent/changeContentVolume/changeContentVolume.md)
            3. [Get Content](./use_cases/fridge_ucs/fridgeContent/getContent/getFridgeContentUseCase.md)
            4. [Remove Content](./use_cases/fridge_ucs/fridgeContent/removeContent/removeContentUseCase.md)
         3. [Get Fridges](./use_cases/fridge_ucs/getFridges/getFridgesUseCase.md)
         4. [Join Fridge](./use_cases/fridge_ucs/joinFridge/joinFridgeUseCase.md)
         5. [Fridge User Management](./use_cases/fridge_ucs/management/ManageFridgeUsersUC.md)
         6. [Remove Fridge](./use_cases/fridge_ucs/removeFridge/deleteFridgeUseCase.md)
3. **Development Documentation**
   1. **API**
      1. [Endpoint Definition](./planning/api-doc/endpoint_definition.txt)
      2. **API-Workflows**
         1. [Authentication](./planning/workflows/authentication_system.md)
         2. [Register](./planning/api-doc/api-workflows/auth_register.md)
         3. [Create Fridge](./planning/api-doc/api-workflows/create_fridge.md)
         4. [Fridge Content](./planning/api-doc/api-workflows/fridge_content.md)
         5. [Get Fridges](./planning/api-doc/api-workflows/get_fridges.md)
         6. [Fridge Roles](./planning/api-doc/api-workflows/role_management.md)
   2. **Database**
      1. [Database Model](./planning/database/Fridgify_DBModel.png)
      2. [Table View](./planning/database/Fridgify_Tables.png)
      3. [ER-Diagram](./planning/database/Fridgify-ER.png)
      4. [Class Diagram (Django)](./planning/database/generatedClassDiagram.png)
      5. [Up to Date Models](./planning/database/models.md)
      6. [SQL](./planning/database/tablecreation.sql)
   3. **Continuous Integration / Continuous Delivery**
      1. [Deployment](planning/ci_cd/Fridgify_deployment.pdf)
4. **Hand-Ins**
   1. **Midterm**
      1. [Presentation](public/midterm/Fridgify-Midterm.pptx)
      2. [Handout](public/midterm/handout.pdf)
