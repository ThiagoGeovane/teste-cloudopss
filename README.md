# teste-cloudopss

<h2>Teste CloudOpss</h2>

Tem como objetivo configurar um ambiente Docker criando um arquivo Dockerfile para Wordpress com MySQL.
O template do Wordpress deve ser de um site simples como Blog de notícias com fotos.

<b><i>Template no Wordpress</i></b>

Primeiramente realizar o download de dois componentes básico para a criação do Template no Wordpress no Computador
<ul>
  <li>Wordpress</li>
  Para o Wordpress, ir no seu navegador e pesquisar Wordpress Org</br>
  Utilizar o link a seguir:
  </br>
  <a href="https://br.wordpress.org/download/">Wordpress</a></br>
  Para Windows, selecionar <b>Baixar o WordPress versão</b>, para Linux selecionar <b>Baixar .tar.gz</b>. Realizar apenas o donwload, não precisa executar nada.</br>
  
  <li>Xampp</li>
  Para o Xampp, ir no seu navegador e pesquisar Xampp
  Utilizar o link a seguir:
  </br>
  <a href="https://www.apachefriends.org/pt_br/index.html">Xampp</a></br>
  Selecionar qual sistema Operacional deseja e realizar o download.</br>
</ul>

A instalação é bem simples para o Xampp, apenas ir avançando clicando em <i>Next.</i></br></br>

Para configurar o Wordpress, vamos precisar colar a pasta que fizemos download do site do Wordpress para o caminho: <b>c:\xampp\htdocs</b> </br></br>
Copiar a pasta Wordpress nesse caminho informado.</br></br>
Você pode nomear essa pasta para o nome do seu projeto. Nomeei como teste-cloudopss.</br></br>

Agora vamos iniciar a aaplicação para criar um Wordpress.</br></br>

Para isso devemos iniciar o Xampp.
<ul>
  <li>Ir na pasta onde foi instalada o Xampp. Normalmente é no caminho C:\xampp</li>
  <li>Inciar a aplicação <b>xampp.control</b></li>
  <li>Com a aplicação aberta, iniciar: Apache e MySQL</b></li>
  <li>Clicando em Start na opção Actions</b></li>
  Os dois serviços (Apache e MySQL) serão iniciados.
</ul>
</br>
Feito isso, vamos abrir qualquer navegador e digitar o seguinte caminho: <b>localhost</b></br></br>

Fazendo isso, ele vai abrir o servidor local do Xampp.</br></br>

Antes de instalar o banco de Dados para o projeto, vá em: localhost e vá na Opção: <b>phpMyAdmin</b></br>
Crie o banco de dados, indo na opção: </br>
<b>Novo</b></br>
<b>Digite o nome do banco de dados</b>. Clique em <b>Criar</b>.</br>
Feito isso, vamos abrir o projeto.</br></br>

Digite no navegador: <b>localhost/teste-cloudopss</b>. No meu caso o nome do meu projeto é esse.</br></br>
Ele vai iniciar nossa aplicação.</br></br>
Vai pedir para criar o banco de dados.</br></br>

Na próxima tela, clique em <b>Instalar</b>.</br>
Na próxima tela será feita a criação do banco de dados.</br>
<ul>
  <li>Nome do Banco de Dados: (Colocar o mesmo no phpMyAdmin. No meu caso foi wp_teste-cloudopss</li>
  <li>Nome do Usuário: (Pode deixar <b>root</b>)</li>
  <li>Senha: (Pode deixar em branco)</li>
  <li>Servidor do Banco de Dados: localhost</li>
  <li>Prefixo da Tabela: wp_</li>
  Clicar em Enviar</br>
  Clicar em Instalar</br>
  O que fizemos aqui foi a linkagem do Wordpress com o MySQL.
</ul>
</br></br>
Agora vamos criar o template do Wordpress.</b>
<ul>
  <li>Titulo do Site: Blog de Noticias</li>
  <li>Nome do Usuário: (Pode deixar <b>admin</b>)</li>
  <li>Senha: (Crie uma senha. Criei como <b>admin</b></li>
  <li>Flegar a opção de confirmação de senha</li>
  <li>E-mail: (Opcional)</li>
  Clicar em <b>Instalar o Wordpress</b></br>
  Clicar em <b>Instalar</b></br>
  Após isso, clicar em <b>Acessar</b></br></br>
  Na tela do Wordpress, vai pedir usuário e senha. Colocar usuário e senha que criou. (admin e admin).</br></br>
  O que fizemos aqui foi a criação do Wordpress.</br></br>
  Para testar: localhost/teste-cloudopss
</ul>
</br>
Para acessar o meu template conforme solicitado de um template de site simples como Blog de notícias com fotos.</br>
Acessar no meu git o arquivo: wordpress.zip</br>
Link: <a href="https://github.com/ThiagoGeovane/teste-cloudopss/blob/main/Wordpress.zip">Wordpress</a></br>

<h3>Intregação Docker e Wordpress</h3>
Primeiramente precisa instalar o Docker e Docker Compose.</br></br>
<ul>
  <li>Instalar o Docker, só seguir esse link: <a href="https://docs.docker.com/get-docker/">Docker</a></li>
  <li>Instalar o Docker Compose, só seguir esse link: <a href="https://docs.docker.com/compose/install/">Docker Compose</a></li>
</ul>
Para criar o ambiente, abrir em uma IDE (No meu caso usei o Visual Studio Code) os arquivos do Docker.</br>
Você deve abrir uma Workspace. Buscar a pasta do projeto com os arquivos: <b> src, Dockerfile, docker-compose.yml</b></br>
Está no caminho: <a href="https://github.com/ThiagoGeovane/teste-cloudopss">Projeto</a></br></br>
Na IDE, executar o comando no terminal: <b><i>docker-compose up</b></i></br></br>
Quando você executar docker-compose up, o Docker analisará o seu arquivo docker-compose.yml e buscará tudo o que é necessário para subir o seu ambiente. Na primeira vez ele precisará baixar as imagens listadas no docker-compose, mas é só da primeira vez.</br></br>
O <b>docker-compose.yml</b>, O conteúdo deste arquivo é quase idêntico ao que consta na documentação oficial da imagem do WordPress. A única diferença é que aqui os volumes começam com ./, para que o Docker use as pastas que nós criamos no começo. Isto torna desnecessária a seção final volumes do arquivo original.</br></br>
Feito isso, foi criado o ambiente de integração Docker e Wordpress.
