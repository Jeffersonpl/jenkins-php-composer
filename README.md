# jenkins-php-composer
Jenkin com Php 7.2 e composer

**PHP-FPM 7.2.18 ALPINE**

**JENKINS 2.178 ALPINE**

**INTRODUÇÃO**

Crie esse formato devido a minha necessidade de fazer deploy contínuo
com test units do php, procurei pegar todos os dados atualizado do
php-fpm alpine que tenho usado em outros projetos, e está bem
estável. Copiei o Dockerfile do php:7.2.18-fpm-alpine3.9
e introduzi dentro do meu Dockerfile que chama a imagem do
Jenkins, ao fazer isso utilizei o composer, para criar
um pipeline estável. Essa imagem está pronta para usar o
kubernetes, minha idéia é aplicar o conceito DevOps.

**Missão**
Deixar o jekins com pipeline pronto para o php, assim aplicar
CI/CD com kubernetes no conceito DevOps.

**Obs**

Deixarei o admin com a senha admin123, podendo ser mudado.
Também deixarei o host como jenkins:8080, por isso peço que observe o exemplo abaixo.
**Linux/MacOs**
`sudo vi /etc/hosts`
aperte i e insira como está baixo

`127.0.0.1 jenkins`

**Windows**
 abra notepad como adminstrador vá em abrir, e procure a pasta 
 windows>system32>drivers>etc>hosts e insira igual está escrito abaixo e depois salve .

`127.0.0.1 jenkins`

**Backup e Automatização**
Deixarei um backup automático, direto para uma pasta externa da imagem
com nome config_jenkins, por favor crie essa pasta. 

**Para iniciar o Jenkins**
Primeiramente antes de tudo você tem que ter o docker instalado em sua máquina,
não vou explicar como fazer isso.
Depois de clonar esse reposítório ou fazer um docker pull da imagem,
faça o seguinte comando.

` docker run --name jenkins -p 8080:8080  jeffersonpl/jenkins-php-composer:tagdaversão`

versão atual está assim

` docker run --name jenkins -p 8080:8080  jeffersonpl/jenkins-php-composer:1.0.0 `


