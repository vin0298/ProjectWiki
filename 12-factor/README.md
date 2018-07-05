# 12 Factor App Manifesto
Read full blog [here](https://12factor.net)
## 1. Codebase
> One codebase tracked in revision control, many deploys

A twelve-factor app always track a codebase in a version control system (git is recommended). One app can only have one code base, if app have multiple codebase then it's a *distributed system*, and each component is a app that could comply with twelve-factor. One app can have many *deploy*, which is an instance of running app.
## 2. Dependencies
> Explicitly declare and isolate dependencies

**A twelve-factor app never relies on implicit existence of system-wide packages.** Always declare explicitly in dependencies manifest like `Gemfile` or `pom.xml` or `build.gradle` or `package.json`, it would simplifies the setup as the new developer can just checkout code and run install command.

## 3. Config
> Store config in the environment

Config file are most likely differ between deploys, like *development*, *staging* or *production* usually contain like backing service credential like database host, username and password. This shouldn't be saved as constant in program which are the violation of twelve-factor. Each app required to have strict separation between config and code.
## 4. Backing Service
> Treat backing services as attached resources

**The code for a twelve-factor app makes no distinction between local and third party services.** Always treat backing services as a attached resource that accessed via url declared in **config**, so that resources can be attached to and detached from deploys at will. 

## 5. Build, Release, run
> Strictly separate build and run stages

**The twelve-factor app uses strict separation between the build, release, and run stages.** For example, it is impossible to make changes to the code at runtime, since there is no way to propagate those changes back to the build stage. Each release should have an identifier

## 6. Processes
> Execute the app as one or more stateless processes

**Twelve-factor processes are stateless and share-nothing.** All data that need to be persist should be stored in a stateful backing service typically database. Some web usually use sticky-session, this violate the twelve-factor manifesto and session should be stored in a datastore such as memcache or Redis.  

## 7. Port Binding
> Export services via port binding

The twelve-factor app is completely self-contained and does not rely on runtime injection of a webserver into the execution environment to create a web-facing service. The web app exports HTTP as a service by binding to a port, and listening to requests coming in on that port.


## 8. Concurrency
![1](https://12factor.net/images/process-types.png)

In the twelve-factor app, processes are a first class citizen.
## 9. Disposability
## 10. Dev/Prod parity
## 11. Logs
## 12. Admin Event
