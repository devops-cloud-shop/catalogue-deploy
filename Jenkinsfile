@Library('jenkins-shared-library') _

// parameters must be declared before the pipeline logic executes//
properties([
  parameters([
    string(name: 'APP_VERSION', defaultValue: ''),
    choice(name: 'DEPLOY_TO', choices: ['dev', 'qa', 'prod'], description: 'Target environment')
  ])
])

// build configMap from params (with safe defaults)//
def configMap = [
    PROJECT : "roboshop",
    COMPONENT: "catalogue",
    APP_VERSION: (params.APP_VERSION),
    DEPLOY_TO: (params.DEPLOY_TO)
]

EKSPipelineDeploy(configMap)
