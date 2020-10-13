# HAPPY NWL#3

### AULA 01

- Início do Projeto:

#1
yarn create react-app web --template typescript
ou
npx create-react-app web --template typescript

#2
cd web/
code .

#3
Babel converte o JS para o Browser entender.

#4 
Limpar a estrutura(deletando arquivos desnecessários):
README.md,
pasta public deixar somente o arquivo index.html,

index.html -> Alterar o arquivo igual o exemplo abaixo:
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
 
    <title>Happy</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>

pasta src deixar somente os arquivos App.tsx, index.tsx e react-app-env.d.ts.

arquivo index.tsx dentro de src deixar o arquivo conforme o exemplo abaixo:
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

Arquivo App.tsx dentro de src alterar conforme o exemplo abaixo:
import React from 'react';

function App() {
  return (
    <div className="App">
      <h1>Hello World</h1>
    </div>
  );
}

export default App;

#5
Abrindo o terminal:
Ctrl + shift + p
>toggle integrated terminal

#6
yarn start -> Executa no browser.

#7
JSX - JavaScript XML

#8
Componentes são funções que retornam um JSX - HTML.

#9
Exemplo de Interface e Componentes:
import React from 'react';

// JSX - JavaScript XML

interface TitleProps {
  text: string;
}

function Title(props: TitleProps) {
  return (
    <h1>{props.text}</h1>
  )
}

function App() {
  return (
    <div className="App">
      <Title text="Título 1" />
      <Title text="Título 2" />
      <Title text="Título 3" />
      <Title text="Título 4" />
    </div>
  );
}

export default App;

#10
Criar a pasta images e salvar os arquivos.
Formato de vetor .svg

#11
Criar a pasta styles dentro de src
Criar o arquivo global.css dentro de styles

#12
Definindo o global.css:


#13
Fonte Nunito - tamanho semi-bold 600, bold 700 e extra-bold 800
Embed - Copiar o link - Adicionar no Head do index.html
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@600;700;800&display=swap" rel="stylesheet">

#14
Importa o arquivo global.css dentro do arquivo App.tsx
import './styles/global.css';

#15
Dentro de styles adicionar a pasta pages
Dentro de pages adicionar o arquivo landing.css

#16
Adicionando o pacote de icones:
yarn add react-icons

#17
importando dentro do arquivo App.tsx
import {} from 'react-icons/fi';

#18
Instalando Rotas:
yarn add react-router-dom

#19
Criar o arquivo routes.tsx dentro de src.

#20
yarn add @types/react-router-dom -D
-D significa como Desenvolvimento
Desenvolvimento só é necessário quando está desenvolvendo, online não precisa.

#21
Leaflet
React Leflet -> Bibioleta de Mapas dentro do React

yarn add leaflet react-leaflet
yarn add @types/react-leaflet -D

TileLayer -> Pegar/trazer as imagens do Mapa.
OpenStreetMap

#22
MapBox
