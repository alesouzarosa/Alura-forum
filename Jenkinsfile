
stages {

    stage('build') {
        steps {
            withMaven(maven: 'Maven-3.6.0') {
                sh "mvn clean package -DskipTests"
            }
        }
    }


    stage('build') {
        //builda o projeto
        sh 'mvn -B -DskipTests clean package'
    }
}


/*
builda a aplicação, compilação e empacotamento retona o jar
mvn clean package
rodar a apicação:
java -jar forum-0.0.1-SNAPSHOT.jar
java -jar -Dspring.profiles.active=prod forum.jar
java -jar -Dspring.profiles.active=prod -DFORUM_DATABASE_URL=jdbc:h2:mem:alura-forum -DFORUM_DATABASE_USERNAME=sa -DFORUM_DATABASE_PASSWORD= -DFORUM_JWT_SECRET=123456 forum.jar

*/


/*
Docker: criando a imagem
docker build -t alura/forum .

docker run -p 8080:8080 -e SPRING_PROFILES_ACTIVE='prod' -e FORUM_DATABASE_URL='jdbc:h2:mem:alura-forum' -e FORUM_DATABASE_USERNAME='sa' -e FORUM_DATABASE_PASSWORD='' -e FORUM_JWT_SECRET='123456' alura-forum

 */