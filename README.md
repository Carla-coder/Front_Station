# Homepage Front-Station

Front Station é um site educacional e interativo voltado para explorar as possibilidades do desenvolvimento front-end, especialmente em JavaScript. Este projeto inclui várias seções, como uma estação de música, uma estação de quiz e uma estação de jogos, todas projetadas para demonstrar as capacidades do desenvolvimento web moderno.


## Sumário

- Visão Geral

- Tecnologias Utilizadas

- Configuração do Projeto

- Estrutura de Arquivos

- Detalhes de Implementação

    - Autenticação com GitHub 

    - Estilização

    - Funcionalidades Interativas



## Visão Geral

Front Station é uma plataforma educativa destinada a profissionais que desejam aprofundar seus conhecimentos e habilidades em desenvolvimento web. O projeto demonstra a criação de interfaces dinâmicas e a implementação de lógica usando JavaScript.
## Tecnologias utilizadas

- **HTML5**

- **CSS3** 

- **JavaScript**

- **GitHub OAuth**
## Configurações do projeto

### Requisitos

- Conta no GitHub para configurar OAuth

- Clone este repositório para a sua máquina local.

```
git clone git clone https://github.com/yourusername/front-station.git`
```

- Abra o VSCode.

- Configuração do GitHub OAuth

```
Crie uma nova OAuth App em GitHub Developer Settings
```





## Estrutura de arquivos

```
front-station/
├── css/
│   └── styles.css
├── image/
│   └── logo.png
├── js/
│   └── main.js
├── song/
│   └── (arquivos relacionados à estação de música)
├── game.html
├── home.html
├── index.html
├── music.html
├── quiz.html
├── README.md

```

## Detalhes de Implementação

### Autenticação com GitHub

O projeto utiliza o fluxo OAuth do GitHub para autenticação. A função loginWithGitHub redireciona os usuários para a página de login do GitHub. Após a autenticação, o GitHub redireciona de volta para o nosso servidor, onde trocamos o código de autorização pelo token de acesso.

main.js

```
function loginWithGitHub() {
  window.location.href =
    "https://github.com/login/oauth/authorize?client_id=Ov23li7tNKGsZVBsVMYm&scope=user";
}

const urlParams = new URLSearchParams(window.location.search);
const error = urlParams.get("error");
if (error === "access_denied") {
  window.location.href = "home.html";
}

```

### Estilização

O projeto usa CSS para estilizar as páginas. Um exemplo de estilo de botão:

```

.button {
    background-color: #444;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.button:hover {
    background-color: #333;
}

```



### Funcionalidades Interativas

 O projeto inclui várias seções interativas, como:

- **Music Station**

- **Quiz Station**

- **Game Station**

Cada seção é projetada para proporcionar uma experiência única e educacional.

## Print da Tela

 ![home](https://github.com/Carla-coder/Front_Station/assets/128012862/8fc3f10b-adcd-4030-ad49-29a7e069537d)



## Autores

- [@Carla-coder](https://www.github.com/Carla-coder)


## Instituição de Ensino

- Escola Senai unidade Jaguariúna - Curso Técnico em Desenvolvimento de Sistemas FullStack - Segundo Semestre (2024)

- Professor responsável pelo Projeto: Robson B. Souza https://github.com/robsonbsouzaa
