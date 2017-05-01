node {
stage 'checkout'
git url: 'c:\\Software\\repos\\simpleGreeting.git'

stage 'Maven Build'
bat 'mvn install'

stage 'Archive test results'
step([$class: 'JUnitResultArchiver',
testResults:'**/target/surefire-reports/TEST-*.xml'])

}