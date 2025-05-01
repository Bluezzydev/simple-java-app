node{
    git branch: 'main', url: 'https://github.com/Bluezzydev/simple-java-app.git'
    stage('Build') {
        try{
        sh 'echo "clean package"' 
        }
        catch (Exception e) {
           sh 'echo "Build failed"'
            throw e
        }
    }
  stage('test') {
        if (env.BRANCH_NAME == 'feature') 
        sh 'echo "test"'
        else 
        sh 'echo "not test"'
}
