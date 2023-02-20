Se siguio el procedimiento indicado en README.md
Se trabajo en el sistem a WSL2 de Windows con VSCode.
Paquetes y versiones utilizados (conforme README.md):
*Ubuntu 20.04.2 LTS
*Rush Multi-Project Build Tool 5.40.5 - https://rushjs.io
*Node.js version is 14.21.2 (LTS)
*Docker version 20.10.12, build 20.10.12-0ubuntu2~20.04.1

Se procedio a compilar un subconjunto de paquetes habilitados en rush.json["projects"] correspondinetes al modulo "Traceability"
para trabajar exclusivamente con el SDK Traceability siguiendo la orientacion de la documentacion de Energy Web:
https://energy-web-foundation-origin.readthedocs-hosted.com/en/latest/

El comando: "rush update" funciono correctamente.

El Comando: "rush build" arroja el siguiente:
marcelo@Marcelo:/mnt/c/Users/Lenovo/Documents/Energy Web/origin$ rush build


Rush Multi-Project Build Tool 5.40.5 - https://rushjs.io
Node.js version is 14.21.2 (LTS)


Starting "rush build"

Executing a maximum of 8 simultaneous processes...

==[ @energyweb/origin-backend-core ]==============================[ 1 of 11 ]==     
@energyweb/origin-backend-core was skipped.

==[ @energyweb/utils-general ]====================================[ 2 of 11 ]==     
@energyweb/utils-general was skipped.
@energyweb/issuer-api was skipped.

==[ @energyweb/issuer-irec-api ]==================================[ 8 of 11 ]==      
@energyweb/issuer-irec-api was skipped.

==[ @energyweb/issuer-api-client ]================================[ 9 of 11 ]==      
error Command failed with exit code 1.
Returned error code: 1
"@energyweb/issuer-api-client" failed to build.

==[ @energyweb/origin-backend-irec-app ]=========================[ 10 of 11 ]==
"@energyweb/origin-backend-irec-app" completed successfully in 3 minutes 58.0 seconds.

==[ @energyweb/issuer-irec-api-client ]==========================[ 11 of 11 ]==
(node:1353) UnhandledPromiseRejectionWarning: Error: Nest can't resolve dependencies of the TypeOrmCoreModule (TypeOrmModuleOptions, ?). Please make sure that the argument ModuleRef at index [1] is available in the TypeOrmCoreModule context.

Potential solutions:
- If ModuleRef is a provider, is it part of the current TypeOrmCoreModule?
- If ModuleRef is exported from a separate @Module, is that module imported within TypeOrmCoreModule?
  @Module({
    imports: [ /* the Module containing ModuleRef */ ]
  })

    at Injector.lookupComponentInParentModules (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:201:19)
    at Injector.resolveComponentInstance (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:156:33)
    at resolveParam (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:108:38)
    at async Promise.all (index 1)
    at Injector.resolveConstructorParams (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:123:27)
    at Injector.loadInstance (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:52:9)
    at Injector.loadProvider (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:74:9)
    at async Promise.all (index 0)
    at InstanceLoader.createInstancesOfProviders (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/instance-loader.js:44:9)
    at /mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/instance-loader.js:29:13
(Use `node --trace-warnings ...` to show where the warning was created)
(node:1353) UnhandledPromiseRejectionWarning: Unhandled promise rejection. This error originated either by throwing inside of an async function without a catch block, or by rejecting a promise which was not handled with .catch(). To terminate the node process on unhandled promise rejection, use the CLI flag `--unhandled-rejections=strict` (see https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode). (rejection id: 1)
(node:1353) [DEP0018] DeprecationWarning: Unhandled promise rejections are deprecated. In the future, promise rejections that are not handled will terminate the Node.js process with a non-zero exit code.
[Nest] 1353  - 02/20/2023, 5:50:04 PM   ERROR [AuthGuard] In order to use "defaultStrategy", please, ensure to import PassportModule in each place where AuthGuard() is being used. Otherwise, passport won't work correctly.
[error] The spec file is not found: src/schema.yaml
[error] Check the path of the OpenAPI spec and try again.
error Command failed with exit code 1.
error Command failed with exit code 1.
error Command failed with exit code 1.
Returned error code: 1
"@energyweb/issuer-irec-api-client" failed to build.



==[ SKIPPED: 8 projects ]======================================================      

These projects were already up to date:
  @energyweb/issuer
  @energyweb/issuer-api
  @energyweb/issuer-irec-api
  @energyweb/issuer-irec-api-wrapper
  @energyweb/origin-backend-core
  @energyweb/origin-backend-utils
  @energyweb/origin-organization-irec-api
  @energyweb/utils-general

==[ SUCCESS: 1 project ]=======================================================      

These projects completed successfully:
  @energyweb/origin-backend-irec-app    3 minutes 58.0 seconds

==[ FAILURE: 2 projects ]======================================================      

--[ FAILURE: @energyweb/issuer-api-client ]---------[ 8 minutes 1.7 seconds ]--      

error Command failed with exit code 1.

--[ FAILURE: @energyweb/issuer-irec-api-client ]----[ 8 minutes 1.7 seconds ]--      

(node:1353) UnhandledPromiseRejectionWarning: Error: Nest can't resolve dependencies of the TypeOrmCoreModule (TypeOrmModuleOptions, ?). Please make sure that the argument ModuleRef at index [1] is available in the TypeOrmCoreModule context.

Potential solutions:
- If ModuleRef is a provider, is it part of the current TypeOrmCoreModule?
- If ModuleRef is exported from a separate @Module, is that module imported within TypeOrmCoreModule?
  @Module({
    imports: [ /* the Module containing ModuleRef */ ]
  })

    at Injector.lookupComponentInParentModules (/mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/injector.js:201:19)
  ...8 lines omitted...
    at /mnt/c/Users/Lenovo/Documents/Energy Web/origin/common/temp/node_modules/.pnpm/@nestjs/core@8.1.1_13adf4c855eac18d5ece2d7b1023f678/node_modules/@nestjs/core/injector/instance-loader.js:29:13
(Use `node --trace-warnings ...` to show where the warning was created)
(node:1353) UnhandledPromiseRejectionWarning: Unhandled promise rejection. This error originated either by throwing inside of an async function without a catch block, or by rejecting a promise which was not handled with .catch(). To terminate the node process on unhandled promise rejection, use the CLI flag `--unhandled-rejections=strict` (see https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode). (rejection id: 1)
(node:1353) [DEP0018] DeprecationWarning: Unhandled promise rejections are deprecated. In the future, promise rejections that are not handled will terminate the Node.js process with a non-zero exit code.
[Nest] 1353  - 02/20/2023, 5:50:04 PM   ERROR [AuthGuard] In order to use "defaultStrategy", please, ensure to import PassportModule in each place where AuthGuard() is being used. Otherwise, passport won't work correctly.
[error] The spec file is not found: src/schema.yaml
[error] Check the path of the OpenAPI spec and try again.
error Command failed with exit code 1.
error Command failed with exit code 1.
error Command failed with exit code 1.


Projects failed to build.

rush build (8 minutes 27.9 seconds)
