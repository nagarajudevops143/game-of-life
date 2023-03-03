node('MAVEN_JDK8'){
    stage('version control'){
        git url: 'https://github.com/nagarajudevops143/game-of-life.git',
            branch: 'scripted'
    }
stage('build the code'){
    sh 'export PATH="/vsr/lib/jvm/java-1.8.0-openjdk-amd64/bin:$PA'
}
stage('archive the artifacts'){
    archiveartifacts onlyIFsuccessful:true
       artifacts: '**target/gameoflife.war',
       allowemtyachive: false
    }
    stage('show the test results') {
        junit testResults: '**/surefire-reports/TEST-*.xml',
              allowEmptyResults: true
    }    
}

