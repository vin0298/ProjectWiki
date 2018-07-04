# 12 Factor App Manifesto
Read full blog [here](https://12factor.net)
## 1. Codebase
> One codebase tracked in revision control, many deploys

A twelve-factor app always track a codebase in a version control system (git is recommended). One app can only have one code base, if app have multiple codebase then it's a *distributed system*, and each component is a app that could comply with twelve-factor. One app can have many *deploy*, which is an instance of running app.
## 2. Dependencies
> Explicitly declare and isolate dependencies

**A twelve-factor app never relies on implicit existence of system-wide packages.** Always declare explicitly in dependencies manifest like `Gemfile` or `pom.xml` or `build.gradle` or `package.json`, it would simplifies the setup as the new developer can just checkout code and run install command.

## 3. Config
## 4. Backing Service
## 5. Build, Release, run
## 6. Processes
## 7. Port Binding
## 8. Concurrency
## 9. Disposability
## 10. Dev/Prod parity
## 11. Logs
## 12. Admin Event
