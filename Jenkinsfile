node{

    stage('SCM Checkout')
    {
        git credentialsId: '	d287b2af-baa4-411a-954b-8b94e00687de', url: 'https://github.com/SHRINIWASTIWARI/online-shopping-system.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u shriniwas34 -p ${DHPWD}"
        }
        sh 'docker push  shriniwas34/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u " shriniwas34" -p "shri12345" docker.io'
             //sh 'sudo docker push shriniwas34/mysql'
             //sh 'sudo docker push shriniwas34/job1_web1.0'
             sh 'sudo docker push shriniwas34/job1_web2.0'
            // sh 'docker push shriniwas34/mysql'
          
    }
}