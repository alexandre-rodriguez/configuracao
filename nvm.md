## NVM
### Instalação
1. Fazer o download e instalar o [NVM](https://github.com/nvm-sh/nvm) com o comando abaixo (versão no momento do tutorial: **v.35.2**):
   ```shell
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
   ```
2. Verificar a versão instalada
   ```shell
   nvm --version
   ```
### Uso
1. Instalar a última release do Node.js:
   ```shell
   nvm install node
   ```
2. Para listar as versões disponíveis do Node.js  para instalação:
   ```shell
   nvm ls-remote
   ```
3. Para listar as versões instaladas do Node.js:
   ```shell
   nvm ls
   ```
4. Definir uma versão padrão do Node.js:
   ```shell
   nvm alias default <versão>
   ```
5. Usar uma versão do Node.js:
	```shell
	nvm use <versão>
	```
6. Para saber qual a versão atual do Node.js
	```shell
	nvm current
	```
7. Para saber qual a versão sendo utilizada do Node.js
   ```shell
   node --version
   ```
8. Para saber qual a versão sendo utilizada do NPM
   ```shell
   npm --version
   ```





----
voltar ao [README](README.md)
