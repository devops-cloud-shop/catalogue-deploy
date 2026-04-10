@Library('jenkins-shared-library') _

properties([
  parameters([
    string(name: 'APP_VERSION', defaultValue: ''),
    string(name: 'DEPLOY_TO', defaultValue: 'dev')
  ])
])

def configMap [
    PROJECT : "roboshop",
    COMPONENT: "catalogue",
    APP_VERSION: (params.APP_VERSION),
    DEPLOY_TO: (params.DEPLOY_TO)
]

EKSPipelineDeploy(configMap)
