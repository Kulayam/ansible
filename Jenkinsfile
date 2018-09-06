#!groovy 

node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh 'npm install'

   stage 'Setup'
        sh 'npm install mocha@2.5.3 --save-dev'

   stage 'Setup'
        sh 'npm install zombie@5.0.3 --save-dev'

   stage 'Mocha test'
        sh './node_modules/mocha/bin/mocha'

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh 'npm prune'
        sh 'rm node_modules -rf'
}
