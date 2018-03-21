# Continuous Integration/Continuous Delivery (CI/CD)

## What

Continuous Integration (CI) is the practice where engineers integrate code into a shared repository regularly, typically several times a day. To ensure CI, a team should utilize a version control tool and check in code to one single branch (ex: the master branch) at least daily. Each check-in should trigger an automated build pipeline where the code gets compiled and tested. The build pipeline should then provide a red/green result in a short amount of time. If the build goes red, it should be fixed and brought back to green as the top priority for the team. Status of the build pipeline should be easily visible by the whole team.

Continuous Delivery (CD) refers to the frequent and fast deployment of tested software into all environments (non-production and production). The product should always be in a state where it's ready for a production deployment.  Deployment should be a simple, straightforward process that is automated.  Continuous Integration is a prerequisite of Continuous Delivery.  

*Note* : Continuous Delivery is sometimes confused with Continuous Deployment.  Continuous _Deployment_ which means that every code check-in results in an automated _production_ deployment.  Continuous Deployment is like the highest level of Continuous Delivery.

## How

- Every code check-in is on the same branch
- A test suite provides high test coverage and high confidence in the software so that it is always in a deployable state
- A build pipeline that is highly visible, stable and relatively fast 
  - Code integration, testing, publication and deployment should all be part of the pipeline
  - Deployment to all environments should be automatic or 'push-button'

## Why

- Continuous Integration
  - Faster feedback on code changes
    - By integrating small batches of code, builds and tests are fast and frequent.  Integration issues can be resolved quickly.
    - When integration is delayed, complex merge conflicts ("merge hell") can result that take signicant time and effort to resolve 
    
- Continuous Delivery
    - Lower risk
      - There is a higher risk when a large number of changes are released at the same time. Releasing frequently means smaller batches (smaller changes) wheich in turn means less risk
    - Reduce human errors
      - A deployment process is not automated is prone to human error. An automated deployment makes sure the same procedure is carried out each and every time. It also eliminates knowledge silos and manual process bottlenecks, so that the team is not dependent on certain members to perform the deployment
    - Faster feedback from user
      - A fast deployment makes sure that we deliver new features to the users as fast as possible. So we would know quickly how valuable it is to the users

- Automated build pipeline
  - Ensures CI/CD
    - A stable build pipeline makes CI/CD possible
  - Ensures code quality
    - Having tests as part of the pipeline that runs against every check-in ensures code quality
  - Prevent regression
    - Engineers might not be aware when their change has broken some previously working features. Running a full regression test suite as part of the build surfaces any regression quickly. 
  - Provides visibility 
    - When the build pipeline is highly visible to the whole team, everyone is aware when the build is broken so team can prioritize fixing the build. Non-engineers (PM, PD, etc.) on the team are aware of deployment progress or if any testing environments are broken. 
  - Provides traceability 
    - Publishing software artifact as part of pipeline saves a copy of the software executable as history of deployment for future use
