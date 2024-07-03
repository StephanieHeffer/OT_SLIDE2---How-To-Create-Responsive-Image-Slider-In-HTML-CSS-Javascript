https://www.youtube.com/watch?v=_0mkCrQsOOw&list=PLV8UqTQmhTnFEu709oUyEfuq8J4Od-uIS&index=17&t=1s&ab_channel=OnlineTutorials

CSS
.container: Define um contêiner para o slider e os pontos de navegação.

position: absolute;: Define a posição absoluta do contêiner.
display: flex; justify-content: center; align-items: center;: Usa um layout flexível para centralizar o conteúdo horizontalmente e verticalmente.
height: 100vh; width: 100vw;: Define a altura como 100% da altura da janela e a largura como 100% da largura da janela.
background: #222;: Define o fundo do contêiner como cinza escuro.
.container input: Estiliza os inputs dentro do contêiner.

appearance: none;: Remove os estilos padrão dos inputs.
.container .dots: Estiliza os pontos de navegação.

position: absolute; bottom: 70px;: Define a posição dos pontos na parte inferior do contêiner.
z-index: 10000;: Define uma ordem de empilhamento alta para garantir que os pontos fiquem sobrepostos a outros elementos.
display: flex; gap: 6px;: Usa um layout flexível para os pontos com um espaçamento de 6px entre eles.
.container .dots label: Estiliza cada ponto de navegação.

width: 20px; height: 20px;: Define as dimensões dos pontos.
background: #fff;: Define o fundo dos pontos como branco.
cursor: pointer;: Altera o cursor do mouse para indicar que os pontos são clicáveis.
border-radius: 50%;: Aplica bordas arredondadas aos pontos.
opacity: 0.5;: Define a opacidade inicial dos pontos como 0.5.
border: 2px solid #222;: Adiciona uma borda sólida aos pontos.
.container input:nth-child(1):checked ~ .dots label:nth-child(1), ...: Estiliza os pontos quando os inputs correspondentes são marcados.

Altera a opacidade dos pontos para 1 quando o input correspondente está marcado.
.container .slider: Estiliza o slider.

position: absolute; top: 0; left: 0; width: 100%; height: 100%;: Define a posição e as dimensões do slider para ocupar todo o contêiner.
.container .slider .slide: Estiliza cada slide dentro do slider.

position: absolute; top: 0; left: 0; width: 100%; height: 100%;: Define a posição e as dimensões dos slides para ocupar todo o slider.
background: var(--img);: Define a imagem de fundo dos slides usando uma variável CSS (--img) que é definida inline no HTML.
clip-path: circle(0% at 0% 50%);: Define uma máscara circular que controla a forma como a imagem de fundo é exibida.
transition: 1.5s; transition-delay: 0s;: Adiciona uma transição suave para alterações de estilo.
background-position: left;: Define a posição inicial da imagem de fundo como à esquerda.
display: flex; justify-content: flex-start; align-items: flex-end;: Alinha o conteúdo dos slides na parte inferior.
.container .slider .slide:nth-child(even): Estiliza os slides pares.

Altera a posição da máscara circular e a posição da imagem de fundo para os slides pares.
.container input:nth-child(1):checked ~ .slider .slide:nth-child(1), ...: Estiliza os slides quando os inputs correspondentes são marcados.

Altera a máscara circular para revelar a imagem de fundo e a posição da imagem de fundo quando o input correspondente está marcado.
HTML
Dentro do <body>, há um <div> com a classe .container, que contém os inputs para controlar o slider, os pontos de navegação e os slides.
Os inputs são representados por <input> com ids slide1 a slide5.
Os pontos de navegação são representados por <label> associados aos inputs.
Os slides são representados por <div> com a classe .slide, e cada um possui seu próprio conteúdo (título e parágrafo) dentro de uma <div> com a classe .content.
