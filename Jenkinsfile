node ('master'){  
    //def app
    stage('Cloning Git') {
        /* Let's make sure we have the repository cloned to our workspace */
       checkout scm
    }  
      
    stage('Build-and-Tag') {
        sh 'echo Build-and-Tag'
    /* This builds the actual image; synonymous to
         * docker build on the command line 
        app = docker.build("amrit96/snake") */
    }
     stage('Scan with SNYK') {
        sh 'echo scan-with-snyk'
     /* docker.withRegistry('https://registry.hub.docker.com', 'training_creds') {
            app.push("latest")
        			} */
         }
     stage('Scan with OWASP ZAP') {
        sh 'echo scan-with-snyk'
     /* docker.withRegistry('https://registry.hub.docker.com', 'training_creds') {
            app.push("latest")
        			} */
         }
    
    stage('Post-to-dockerhub') {
        sh 'echo post-to-docker'
     /* docker.withRegistry('https://registry.hub.docker.com', 'training_creds') {
            app.push("latest")
        			} */
         }
      
    
    stage('Pull-image-server') {
    /*
         sh "docker-compose down"
         sh "docker-compose up -d"	*/
      }
    
  
}
