## Maven

### Instalação

1. Fazer download do arquivo compactado do [Maven](https://maven.apache.org/download.cgi) (versão no momento do tutorial: **apache-maven-3.6.3**)

2. Descompactar o arquivo no diretório de sua preferência, por exemplo: `~/desenvolvimento/maven`

3. editar o arquivo `~/.profile` e incluir as linhas abaixo no final do arquivo:

   ```shell
   export M3_HOME=<diretorio-instalacao-maven>/apache-maven-3.6.3
   export MAVEN_HOME=<diretorio-instalacao-maven>/apache-maven-3.6.3
   export PATH=${M3_HOME}/bin:${PATH}
   ```

4. Carregar as configurações acima:

   ```shell
   source ~/.profile
   ```

5. Verificar a versão instalada

   ```shell
   mvn --version
   ```





----
voltar ao [README](README.md)
