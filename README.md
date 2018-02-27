# ePricer NEXTGEN Cloud Architecture

Reference architecture of ePricer using Angular and NetflixOSS microservice-based backend and deploying onto IBM Bluemix container, leveraging Bluemix DevOPS and other services.

## Architecture

  ![Application Architecture](static/imgs/epricer-nextgen-architecture.png?raw=true)

## Application Overview

ePricer is one of the largest enterprise's worldwide global tools that provides uniform and consistent pricing solutions for their produces and services. ePricer provides awesome UI to create quotation for end user customers quickly and effectively.
This architecture has been adopted to build ePricer from a Monolith to micro-service based by isolating each of the business components from the whole unit and expose them as  micro-services so that they can exist independently and deployed independently. 

##ePricer Components
UI Components:- The UI components are designed as Single Page Application using [Angular5](https://angular.io/) framework. It also uses [Angular Material Design] for various UI components, [NPM](https://github.com/npm/npm) as package manager, [TypeScript](https://github.com/Microsoft/TypeScript) and [Webpack](https://github.com/webpack/webpack) as module loader.

## Features - Technical
- [x] TypeScript
- [x] TSLint
- [x] @types
- [x] Webpack 3
- [x] Karma + Jasmine
- [x] Protractor
- [x] Styling using SASS
- [x] NPM
- [x] Code Coverage
- [x] Angular 5
- [x] Lazy-loading
- [x] Lazy reducers
- [x] LocalStorage ui state persistence
- [x] `@ngrx/effects` for API requests
- [x] Time travel debigging capability
- [x] angular-material and custom components in `SharedModule`
- [x] Production build containing chunks


Micro-service Components - There are several micro-services of ePricer and the individual microservices communicate to each other using the [Netflix OSS Framework](https://netflix.github.io/).

## Project Component Repositories

This project runs itself like a microservice project, as such each component in the architecture has its own Git Repository and tutorial listed below.  

Infrastructure Components:  

1. [ep-nextgen-eureka](https://git.ng.bluemix.net/epricer-pocs/ep-nextgen-eureka.git)  - Contains the Eureka application components for microservices foundation  
2. [ep-nextgen-zuul](
https://git.ng.bluemix.net/kiranchowdhury/ep-nextgen-zuul.git)  - Contains the Zuul application components for microservices foundation  
3. [ep-nextgen-cloud-config](https://git.ng.bluemix.net/epricer-pocs/ep-nextgen-cloud-config.git) - Contains the Config application components
4. [ep-pricing-services](https://git.ng.bluemix.net/epricer-pocs/ep-pricing-services.git) - Provides APIs for pricing methods.
5. [ep-configuration-services](https://git.ng.bluemix.net/epricer-pocs/ep-configuration-services.git) - Provides APIs for Product and Service managements.
6. [ep-promo-services](https://git.ng.bluemix.net/epricer-pocs/ep-promo-services.git) - Provides APIs for promotions and incentives.
7. [ep-prepricing-services](https://git.ng.bluemix.net/epricer-pocs/ep-prepricing-services.git) - Provides APIs to automatically perform pre pricing checks to meet compliance and legan requirements

Resiliency Components:

1. [ep-nextgen-hystrix](https://git.ng.bluemix.net/epricer-pocs/ep-nextgen-hystrix.git) - Contains the Hystrix Dashboard container version application component for microservices foundation
2. [ep-nextgen-turbine](https://git.ng.bluemix.net/epricer-pocs/ep-nextgen-turbine.git) - Contains the Turbine application component for microservices foundation

DevOps Components:
[IC Toolchain](https://git.ng.bluemix.net/epricer-pocs/ep-devops-container.git) - A one click full deployment process which will create a toolchain for the IBM Bluemix CKubernetes ontainers version of this architecture


