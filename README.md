
![Iron Hack](https://raw.githubusercontent.com/lemerodrigo/cv-workshop/master/img/ih.png)

# Currículo by Ironhack

O objetivo deste tutorial é montar um currículo simples para passar os conceitos básicos do HTML e CSS.

### Configurando o ambiente

Recomendamos a utilização do editor [Visual Studio Code](https://code.visualstudio.com/Download) para fazer esse exercício porém, qualquer editor pode ser utilizado.

Vamos começar montando o esquelto da nossa página:

1. Crie um diretório com o nome cv no seu desktop;

2. Dentro desse diretório, crie 2 arquivos (index.html e style.css) e um diretório (images);

![Structure](https://raw.githubusercontent.com/lemerodrigo/cv-workshop/master/img/structure.png)

3. Clique com o botão direito do mouse na imagem do Homer abaixo, escolha a opção "Salvar imagem como..." e grave a imagem com o nome profile.jpg dentro do diretório images do seu projeto;

![Homer Simpson](https://raw.githubusercontent.com/lemerodrigo/cv-workshop/master/img/profile.jpg "Homer Simpson")

4. Agora vamos pegar o código abaixo e colocar no arquivo index.html que está na raiz do nosso projeto:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Homer J. Simpson</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body>
  <!-- Main container -->
  <div id="container">
    <!-- Main info -->
    <section id="main-info">
      <img src="images/profile.jpg" alt="Homer Simpson profile picture" />
      <h1>Homer Jay Simpson</h1>
      <h2>Versitile employee, currently working at Springfield's Power Plant</h2>
      <p>This can be a longer description about the person's goals adipiscing elit. Aenean sit amet egestas ligula. Sed tincidunt urna erat, sit amet vehicula est imperdiet quis. Fusce a ullamcorper ex. Sed et lacus tristique, commodo nulla ac, fermentum arcu. Aliquam facilisis mauris mauris, eu volutpat tellus vehicula sit amet. Duis nisl elit, tempus vitae.</p>
    </section>
    <!-- /Main info -->
        
    <!-- Contact info -->
    <section id="contact-info">
      <h2>Contact Info</h2>
      <div>
        <ul>
          <li><a href="#">homer.simpson@gmail.com</a></li>
          <li><a href="#">Springfield, OR - USA</a></li>
          <li><a href="#">@homersimpson_official</a></li>
        </ul>
        <ul>
          <li><a href="#">+1 503-655-2393</a></li>
          <li><a href="#">May 12, 1956</a></li>
          <li><a href="#">linkedin.com/in/homersimpson</a></li>
        </ul>
      </div>
    </section>
    <!-- /Contact info -->
  
    <!-- Education -->
    <section id="education">
      <h2>Education</h2>
      <div>
        <h3>Master Degree</h3>
        <h4>ACME University</h4>
        <p>Jan, 2007 - Dez, 2010</p>
        <p>Los Angeles, USA</p>
      </div>
      <div>
        <h3>High School Degree</h3>
        <h4>Springfield High</h4>
        <p>Jan, 2001 - Dez, 2006</p>
        <p>Springfield, USA</p>
      </div>
    </section>
    <!-- /Education -->

    <!-- Skills -->
    <section id="skills">
      <h2>Skills</h2>
      <ul>
        <li>Math</li>
        <li>Jibberish</li>
        <li>Art</li>
        <li>Biology</li>
        <li>Enrolation</li>
        <li>Gardening</li>
      </ul>
    </section>
    <!-- /Skills -->

    <!-- Credits -->
    <footer>Thanks to Matt Groening for creating me!</footer>
    <!-- /Credits -->
  </div>
  <!-- /Container -->
</body>
</html>
```

Obs.: para cada alteração que você fizer no arquivo index.html ou no style.css, lembre-se de validar essa alteracão voltando para a janela do navegador e recarregando a página.

**IMPORTANTE!**

Antes de continuar, abra o navegador, clique em arquivo -> abrir e escolha o arquivo index.html que você criou e que está na raiz do seu projeto (diretório cv que está no desktop).

Como pode-se notar, neste ponto já temos uma página mas, com pouca ou nenhuma apresentação.

### Font Awesome

1. Acrescente a linha abaixo dentro da tag **head** do seu arquivo index.html sem excluir as linhas que já estavam por lá.

```css
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.0/css/all.css" integrity="sha384-lKuwvrZot6UHsBSfcMvOkWwlCMgc0TaWr+30HWe3a4ltaBwTZhyTEggF5tJv8tbt" crossorigin="anonymous">
```

2. Agora vamos modificar o conteúdo da seção Contact Info acrescentando alguns ícones nos nossos itens:

```html
<!-- Contact info -->
<section id="contact-info">
  <h2>Contact Info</h2>
  <div>
    <ul>
      <li><a href="#"><i class="far fa-envelope"></i>homer.simpson@gmail.com</a></li>
      <li><a href="#"><i class="fas fa-map-marker-alt"></i>Springfield, OR - USA</a></li>
      <li><a href="#"><i class="fab fa-instagram"></i>@homersimpson_official</a></li>
    </ul>

    <ul>
      <li><a href="#"><i class="fas fa-mobile-alt"></i>+1 503-655-2393</a></li>
      <li><a href="#"><i class="far fa-calendar-alt"></i>May 12, 1956</a></li>
      <li><a href="#"><i class="fab fa-linkedin"></i>linkedin.com/in/homersimpson</a></li>
    </ul>
  </div>
</section>
<!-- /Contact info -->
```

### Folhas de estilo/CSS

1. Vamos colocar a folha de estilo que irá deixar a aparência do currículo do Homer muito mais amigável. Para fazer isso, edite o arquivo style.css e coloque todo o conteúdo abaixo:

```css
@import url('https://zfonts.googleapis.com/css?family=Roboto:400,500,500i,900');

* {
  font-family: 'Roboto-Mono', monospace;
  padding: 0;
  margin: 0;
}

body {
  font-size: 16px;
}

h1 {
  font-size: 2.5em;
  font-weight: bold;
}

#container {
  margin: 0 auto 0 auto;
  padding-bottom: 50px;
}

section {
  padding: 35px;
}

section h2 {
  margin-bottom: 20px;
}

/********** MAIN INFO **********/
#main-info {
  color: white;
  flex-wrap: nowrap;
  background-color: #181B23;
}

#main-info h2 {
  color: #2DC5FA;
  font-size: 1.2em;
  margin: 10px 0 10px 0;
  line-height: 1.5em;
}

#main-info p {
  line-height: 1.5em;
}

#main-info img {
  width: 20%;
  border: 6px solid #2DC5FA;
  border-radius: 50%;
  margin: 0 0 25px 25px;
  float: right;
}
/********** /MAIN INFO **********/

/********** CONTACT INFO **********/
#contact-info > div {
  display: flex;
  justify-content: flex-start;
  flex-direction: row;
  flex-wrap: wrap;
}

#contact-info > div > ul {
  width: 300px;
}

#contact-info ul li a {
  color: #181B23;
  text-decoration: none;
}

#contact-info ul li a:hover {
  color: #2DC5FA;
}

#contact-info ul li {
  list-style-type: none;
  line-height: 2.0em;
}

#contact-info ul li i {
  margin-right: 10px;
}
/********** /CONTACT INFO **********/

/********** EDUCATION ***********/
#education {
  background-color: #efefef;
}

#education > div {
  margin-top : 25px;
}
/********** /EDUCATION ***********/

/********** SKILLS ***********/
#skills li {
  list-style-type: none;
  display: inline;
  line-height: 3.0em;
  border: 2px solid #2DC5FA;
  border-radius: 5px;
  padding: 5px 10px 5px 10px;
}

#skills li:hover {
  background-color: #181B23;
  color: #ffffff;
  border: 2px solid #2DC5FA;
}
/********** SKILLS ***********/

/********** CREDITS **********/
footer {
  text-align: center;
  padding: 10px;
}
/********** /CREDITS **********/
```

2. Agora que já temos nosso arquivo de estilo, vamos dizer que nosso HTML deve utilizá-lo. Para isso, basta acrescentar mais uma linha no head conforme indicação abaixo:

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```

3. Agora volte no navegador e atualize a página!

![MEME](https://raw.githubusercontent.com/lemerodrigo/cv-workshop/master/img/meme.gif)

4. Pronto, o currículo do Home Simpson está pronto, com uma boa apresentação e responsivo! \o/

### Processo de publicação

Existem várias formas de deixar uma página pública na internet. Vamos mostrar como é possível utilizando o Google Drive.

1. Abra seu Google Drive, crie uma pasta, vá na opção de compartilhamento e selecione a opção: qualquer um na internet pode achar e ver.

![Google drive](https://raw.githubusercontent.com/lemerodrigo/cv-workshop/master/img/drive-hosting.png)

2. Acesse o [DriveToWeb](https://drv.tw/), escolha a opção Google Drive.

![DRVTW](https://raw.githubusercontent.com/lemerodrigo/cv-workshop/master/img/drvtw.png)

3. Faça o login com a sua conta e permita o acesso aos seus arquivos (caso se sinta desconfortável com isso, crie uma conta Gmail apenas para armazenar seus arquivos públicos).

4. Pronto, já está publicado! No painel de administração, selecione o link que corresponde ao seu CV e é isso. :)
