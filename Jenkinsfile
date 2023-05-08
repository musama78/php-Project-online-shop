node{

    stage('SCM Checkout')
    {
        git credentialsId: '9de2933e-475b-40fc-a2c8-ce9a957e0fbc', url: 'https://github.com/musama78/php-Project-online-shop.git'
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
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "muhammadusama7" -p "Usama1191" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push muhammadusama7/php-Project-online-shop-v1.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
