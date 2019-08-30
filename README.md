# Install in local repo
mvn install:install-file -Dfile=http://jaspersoft.jfrog.io/jaspersoft/third-party-ce-artifacts/com/lowagie/itext/2.1.7.js6/itext-2.1.7.js6.jar  -DgroupId=com.lowagie -DartifactId=itext -Dversion=2.1.7.js6 -Dpackaging=jar

# Download and Install in Nexus
mvn compile deploy:deploy-file -Durl=http://xyz:8081/nexus/content/repositories/thirdparty/ -Dfile=itext-2.1.7.js6.jar -DgroupId=com.lowagie -DartifactId=itext -Dversion=2.1.7.js6 -Dpackaging=jar -DrepositoryId=nexus

