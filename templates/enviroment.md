# Deployment Enviroments
###### There are two deployment enviroments
1. Integration (For testing purpose)
2. Production.

###### Your workflow should be.
1. Deploy to Integration
2. Quality Testing on Intergation
3. Deployment to Production.

#### Setting Enviroment
-  Enviroment is determined by your pipelines branch.
-  Branches that start with `INTEG` will publish to intergation.
    -  Example: `integ-1.2.3`
-  Branches that start with `PROD` will publish to production.
    -  Example: `prod-1.2.3`
-  Branches starting with any other names will fail.
    -  Example: `incorrect-integ-1.2.3`
