node{

    stage('SCM Checkout')
    {
        git credentialsId: 'gitub', url: 'https://github.com/vvamzy/demo.git'
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
            sh "docker login -u vvamzy -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "vvamzy" -p "eac5d1f8-9333-4527-a2f2-245526a356c9" docker.io'
             //sh 'sudo docker push vvamzy/demo'
    }
}
