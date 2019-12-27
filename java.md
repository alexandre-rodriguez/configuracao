## Java
### Instalação
1. Fazer download do arquivo compactado do [java JDK](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html?ssSourceSiteId=otnpt) (versão no momento do tutorial: **jdk1.8.0_231**)
2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/java`
### Configuração
1. Configurar o java
   ```shell
   sudo update-alternatives --install /usr/bin/java java <diretorio-instalacao-java>/jdk1.8.0_231/bin/java 1000

   sudo update-alternatives --install /usr/bin/javac javac <diretorio-instalacao-java>/jdk1.8.0_231/bin/javac 1000
   ```
2. Para verificar a versão instalada
   ```shell
   java -version
   ```





----
voltar ao [README](README.md)
