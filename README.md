# 𝖡𝖺𝗋𝖻𝖾𝖺𝗋𝗂𝖺-𝖻𝗎𝗒𝗌
Site de modelo para barbearias, para todo o mundo!.👩‍💻


# Orlando Cortes · Landing Page de Barbearia

Landing page profissional, responsiva e animada para a barbearia **Orlando Cortes**. O visual segue um estilo grafite com dourado fosco, com animação de abertura, rolagem com revelação de conteúdo e integração com o **WhatsApp** para agendamentos.

O projeto é um **único arquivo HTML** (HTML + CSS + JavaScript puro), sem frameworks, sem build e sem dependências além das fontes do Google Fonts.

---

## Sumário

1. [Visão geral](#visão-geral)
2. [Funcionalidades](#funcionalidades)
3. [Seções da página](#seções-da-página)
4. [Tecnologias](#tecnologias)
5. [Como executar](#como-executar)
6. [Estrutura do projeto](#estrutura-do-projeto)
7. [Personalização](#personalização)
8. [Como o código funciona](#como-o-código-funciona)
9. [Animações](#animações)
10. [Integração com o WhatsApp](#integração-com-o-whatsapp)
11. [Responsividade](#responsividade)
12. [Acessibilidade](#acessibilidade)
13. [Desempenho](#desempenho)
14. [Publicação (deploy)](#publicação-deploy)
15. [Limitações conhecidas](#limitações-conhecidas)
16. [Próximos passos](#próximos-passos)
17. [Licença](#licença)

---

## Visão geral

| Item | Detalhe |
|---|---|
| **Cliente** | Barbearia Orlando Cortes |
| **Objetivo** | Apresentar a barbearia, mostrar serviços e preços e levar o visitante ao WhatsApp para agendar |
| **Estilo** | Grafite escuro, dourado fosco, tipografia condensada e uma abertura animada |
| **Idioma** | Português do Brasil |
| **Arquivo principal** | `barbearia-orlando-cortes-grafite.html` |
| **Tamanho** | Aproximadamente 20 KB, sem imagens externas |

A página foi pensada para um único caminho de conversão: **o visitante chega, vê os serviços e preços e chama no WhatsApp**. Por isso há botões de WhatsApp em vários pontos da página e um botão flutuante sempre visível.

---

## Funcionalidades

- **Animação de abertura (intro):** a tesoura da marca é desenhada traço a traço, o nome aparece, uma barra de carregamento avança e a tela se abre ao meio como uma cortina.
- **Hero animado:** título que sobe linha por linha, linhas decorativas que se expandem, botão e indicador de rolagem em sequência.
- **Revelação ao rolar:** os blocos entram suavemente conforme aparecem na tela.
- **Botão de WhatsApp flutuante** com pulso animado.
- **Lista de preços clicável:** cada serviço abre o WhatsApp já com uma mensagem pronta citando o serviço e o valor.
- **Carrossel "Nossos trabalhos"** com setas e rolagem por toque.
- **Depoimentos rotativos** que alternam sozinhos a cada 5 segundos, com indicadores.
- **Bloco de marca** com luzes desfocadas flutuando (efeito de bokeh).
- **Link "Como chegar"** que abre o endereço no Google Maps.
- **Layout responsivo** para celular, tablet e desktop.
- **Respeito a "movimento reduzido":** quem desativa animações no sistema não vê a abertura nem os movimentos.

---

## Seções da página

| Seção | Âncora | Conteúdo |
|---|---|---|
| Abertura | `#intro` | Overlay com a animação de entrada, some sozinho após cerca de 3,3 s |
| Hero | `#top` | Título "Conhecemos seu estilo melhor", rótulo "Barbearia premium" e botão de agendamento |
| Sobre + Contato | `#sobre` e `#contato` | Texto institucional à esquerda; localização, telefone e horários à direita |
| Trabalhos | `#trabalhos` | Carrossel de cartões com setas de navegação |
| Preços | `#precos` | Lista de serviços e valores, bloco da marca e depoimentos |
| Chamada final | (sem âncora) | Convite final e botão verde do WhatsApp |
| Rodapé | | Direitos autorais |

---

## Tecnologias

- **HTML5** semântico (`section`, `header`, `nav`, `footer`).
- **CSS3** puro: variáveis CSS, Flexbox, CSS Grid, `@keyframes`, `clip`/`overflow` para efeitos de revelação, `backdrop`-free (sem efeitos pesados), `@media` para responsividade e `prefers-reduced-motion`.
- **JavaScript (ES6+)** puro: `IntersectionObserver`, manipulação do DOM, `scrollBy`, `setInterval`, `encodeURIComponent`.
- **Google Fonts:** [Teko](https://fonts.google.com/specimen/Teko) para títulos e [Montserrat](https://fonts.google.com/specimen/Montserrat) para textos.
- **Ícones:** SVG inline, sem biblioteca externa.

Nenhum framework, gerenciador de pacotes ou etapa de build é necessário.

---

## Como executar

### Opção 1: abrir direto no navegador

1. Baixe o arquivo `barbearia-orlando-cortes-grafite.html`.
2. Dê dois cliques nele. A página abre no navegador.

### Opção 2: VS Code com Live Server (recomendado para editar)

1. Abra a pasta do projeto no **VS Code**.
2. Instale a extensão **Live Server**.
3. Clique com o botão direito no arquivo HTML e escolha **Open with Live Server**.
4. A cada salvamento, a página recarrega sozinha.

> Para ver as fontes corretas, é preciso estar **conectado à internet**, porque elas vêm do Google Fonts. Sem internet, o navegador usa as fontes de reserva (`Arial Narrow` e `system-ui`).

---

## Estrutura do projeto

O projeto inteiro cabe em um arquivo, organizado em três blocos:

```
barbearia-orlando-cortes-grafite.html
├── <head>
│   ├── meta viewport (com viewport-fit=cover)
│   ├── link das fontes (Teko e Montserrat)
│   └── <style> ...... todo o CSS
├── <body>
│   ├── #intro ........ animação de abertura
│   ├── .hero ......... cabeçalho + título + botão
│   ├── .sec .......... sobre + contato
│   ├── .works ........ carrossel de trabalhos
│   ├── .pr ........... preços + marca + depoimentos
│   ├── .final ........ chamada final
│   ├── footer
│   └── .fab .......... botão flutuante do WhatsApp
└── <script> ......... todo o JavaScript
```

Dentro do CSS, o código segue esta ordem: variáveis, estilos base, botões, intro, hero, sobre, trabalhos, preços, marca, depoimentos, chamada final, botão flutuante e, por último, as regras responsivas.

---

## Personalização

### 1. Número do WhatsApp (obrigatório)

No início do bloco `<script>`:

```js
const WA = "5511999999999"; // 55 + DDD + número, sem espaços, parênteses ou "+"
```

Exemplo: o número (19) 98888-7777 vira `"5519988887777"`.

### 2. Mensagem padrão

Os botões gerais usam o atributo `data-wa` no próprio HTML:

```html
<a class="btn" href="#" data-wa="Olá! Vim pelo site da Orlando Cortes e gostaria de agendar um horário.">Agendar horário</a>
```

Edite o texto do `data-wa` para mudar a mensagem enviada.

### 3. Serviços e preços

Cada linha da lista usa `data-s` (serviço) e `data-p` (preço) para montar a mensagem do WhatsApp. Ao mudar um valor, altere **os dois lugares**: o texto visível e o atributo.

```html
<a class="row" href="#" data-s="Corte de cabelo" data-p="R$ 50">
  Corte de cabelo <b>R$ 50</b>
</a>
```

Para adicionar um serviço, copie uma linha `.row` inteira e troque os valores.

### 4. Cores

Todas as cores ficam nas variáveis do `:root`:

| Variável | Valor | Uso |
|---|---|---|
| `--bg` | `#232323` | Fundo principal |
| `--bg2` | `#2b2b2b` | Fundo das seções alternadas |
| `--bg3` | `#1b1b1b` | Fundo do hero, da abertura e da chamada final |
| `--gold` | `#a99660` | Destaque principal (títulos, bordas, botões) |
| `--gold2` | `#cbb784` | Dourado claro (hover) |
| `--ivory` | `#efeae0` | Texto principal |
| `--mut` | `#8d8a83` | Texto secundário |
| `--line` | `#3d3d3b` | Linhas e divisórias |
| `--sage` | `#7fb596` | Preços e ícones de contato |

Trocar o valor da variável muda a cor em toda a página.

### 5. Fontes

As fontes são definidas em `--head` (títulos) e `--sans` (textos). Para trocar, altere o link do Google Fonts no `<head>` e os valores dessas duas variáveis.

### 6. Endereço, telefone e horários

Edite diretamente o HTML nas seções `#contato` e no link "Como chegar", cujo endereço está codificado na URL do Google Maps:

```
https://www.google.com/maps/search/?api=1&query=Rua+das+Estrelas+123+S%C3%A3o+Paulo
```

### 7. Fotos reais

A página usa blocos de cor no lugar de fotos. Para colocar imagens nos cartões do carrossel `.w`, troque a variável `--g` de cada cartão por uma imagem:

```html
<div class="w" style="--g:url('fotos/corte-classico.jpg') center/cover"><span>Corte clássico</span></div>
```

### 8. Depoimentos

Os três depoimentos (`.q`) são **exemplos**. Substitua por avaliações reais de clientes, com autorização, antes de divulgar. Se adicionar mais, inclua também um `<i></i>` em `.dots`.

---

## Como o código funciona

### Variáveis CSS

O `:root` guarda cores e fontes. Isso deixa o tema centralizado: mudar uma variável muda o site inteiro.

### Layout com Flexbox e Grid

- **Flexbox** organiza elementos em uma linha: logo e menu do cabeçalho, linhas de preço (nome à esquerda, valor à direita), botão flutuante e as filas do carrossel.
- **CSS Grid** divide as grandes seções em colunas: `.sec` (texto + contato), `.works` (carrossel + título) e `.pr` (preços + marca/depoimentos). No celular, essas grades passam para uma coluna só.

### Revelação ao rolar

Elementos com a classe `.rv` começam invisíveis e levemente deslocados para baixo. Um `IntersectionObserver` observa cada um e, ao entrar na tela, adiciona a classe `.vis`, que dispara a transição. Cada elemento é observado apenas uma vez:

```js
const io = new IntersectionObserver(es => es.forEach(x => {
  if (x.isIntersecting) { x.target.classList.add("vis"); io.unobserve(x.target); }
}), { threshold: .12 });
```

As linhas de preço recebem um atraso escalonado (`--dl`) para entrarem em cascata.

### Carrossel de trabalhos

A trilha `.track` usa `overflow-x: auto` e `scroll-snap-type`, então funciona por toque no celular sem JavaScript. As setas apenas chamam `scrollBy` para avançar ou voltar um cartão:

```js
tr.scrollBy({ left: 314, behavior: "smooth" });
```

### Depoimentos rotativos

Um `setInterval` de 5 segundos troca a classe `.on` entre os depoimentos e os indicadores. Só o depoimento com `.on` fica visível (`display:block`), com uma entrada suave.

### Cabeçalho

O cabeçalho é posicionado sobre o hero (`position:absolute`), por isso não ocupa espaço no fluxo e a imagem de fundo aparece atrás dele.

---

## Animações

### Linha do tempo da abertura

Tudo é feito com `@keyframes` e `animation-delay`, **sem JavaScript**, então não depende de scripts carregarem.

| Tempo | O que acontece |
|---|---|
| 0,2 s | A tesoura começa a ser desenhada (`stroke-dashoffset`) |
| 0,6 s | Os círculos da tesoura são desenhados |
| 1,1 s | O nome "Orlando Cortes" aparece |
| 1,4 s | O rótulo "Barbearia" aparece |
| 0,2 a 2,2 s | A barra de carregamento cresce |
| 2,1 s | O conteúdo central some |
| 2,3 s | As duas metades da tela deslizam para cima e para baixo (1 s) |
| 3,3 s | O overlay fica invisível e deixa de capturar cliques |

### Animações da página (depois da abertura)

| Elemento | Efeito | Início |
|---|---|---|
| Título (linha 1) | Sobe de dentro de uma máscara | 2,6 s |
| Título (linha 2) | Sobe de dentro de uma máscara | 2,8 s |
| Rótulo "Barbearia premium" | Fade + subida | 3,1 s |
| Linhas ao lado do rótulo | Expandem de 0 a 34 px | 3,2 s |
| Botão do hero | Fade + subida | 3,3 s |
| Indicador de rolagem | Linha com ponto que desce em loop | 3,5 s |
| Botão flutuante | Fade + subida, depois pulso contínuo | 3,6 s |
| Fundo do hero | Reflexos de luz que se movem lentamente | contínuo |
| Bokeh da marca | Círculos que flutuam | contínuo |

### Interações

- **Botões:** o fundo dourado preenche da esquerda para a direita ao passar o mouse.
- **Menu:** sublinhado dourado e mudança de cor no hover.
- **Linhas de preço:** deslocam para a direita e o valor aumenta levemente.
- **Cartões de trabalhos:** a imagem dá zoom suave.
- **Setas do carrossel:** deslocam na direção em que apontam.

---

## Integração com o WhatsApp

A página usa o link oficial `https://wa.me/NUMERO?text=MENSAGEM`, que abre o WhatsApp (app ou web) com a conversa e a mensagem já preenchida, **sem precisar de API, servidor ou conta comercial**.

```js
const wal = t => `https://wa.me/${WA}?text=${encodeURIComponent(t)}`;
```

- `encodeURIComponent` converte acentos, espaços e símbolos para o formato aceito em URLs.
- Os links são montados quando a página carrega: o script procura todo elemento com `data-wa` e define o `href`.
- Todos os links do WhatsApp abrem em nova aba (`target="_blank"`) com `rel="noopener"`.

### Pontos de contato com o WhatsApp

| Local | Mensagem enviada |
|---|---|
| Botão flutuante | Pedido geral de agendamento |
| Menu "Agendar" | Pedido geral de agendamento |
| Botão do hero | Pedido geral de agendamento |
| Link no painel de contato | Saudação simples |
| Cada linha de preço | Serviço e valor escolhidos, com pergunta sobre horários |
| Botão de preços e chamada final | Pedido geral de agendamento |

Exemplo de mensagem gerada pela linha "Barba à navalha":

> Olá! Vim pelo site da Orlando Cortes e gostaria de agendar: Barba à navalha (R$ 60). Quais horários estão disponíveis?

---

## Responsividade

| Largura | Comportamento |
|---|---|
| Acima de 860 px | Layout em colunas, menu completo no cabeçalho |
| Até 860 px | Seções em coluna única, menu escondido, carrossel com margem lateral, botão do WhatsApp só com o ícone |

Outros detalhes:

- O hero usa `100svh`, que respeita as barras do navegador no celular.
- A meta tag `viewport-fit=cover` e o `padding` com `env(safe-area-inset-*)` evitam que o conteúdo fique sob o "notch" ou a barra inferior de iPhones.
- Títulos usam `clamp()` para crescer e diminuir suavemente conforme a tela.

---

## Acessibilidade

- Foco visível em todos os elementos interativos (contorno dourado).
- Botões do carrossel com `aria-label`.
- Botão flutuante com `aria-label="Falar no WhatsApp"`.
- A abertura é marcada com `aria-hidden`, pois é apenas decorativa.
- Contraste alto entre texto claro e fundo escuro.
- **`prefers-reduced-motion`:** com animações reduzidas no sistema, a abertura é removida e todos os elementos aparecem imediatamente, sem movimento.

---

## Desempenho

- Um único arquivo, sem imagens externas, sem bibliotecas JavaScript e sem requisições além das fontes.
- Ícones em SVG inline.
- Animações usam `transform` e `opacity`, que são processadas pela GPU.
- O `IntersectionObserver` deixa de observar cada elemento após a primeira revelação.
- `preconnect` no Google Fonts acelera o carregamento da tipografia.

---

## Publicação (deploy)

Como é um site estático, qualquer hospedagem simples serve. Antes de publicar, **renomeie o arquivo para `index.html`**.

### GitHub Pages (gratuito)

1. Crie um repositório e envie o `index.html`.
2. Em **Settings → Pages**, escolha a branch `main` e a pasta raiz.
3. O site fica disponível em `https://seu-usuario.github.io/nome-do-repositorio/`.

### Netlify ou Vercel (gratuito)

Arraste a pasta com o `index.html` para o painel da Netlify, ou conecte o repositório na Vercel. O endereço sai em segundos, e é possível ligar um domínio próprio, como `orlandocortes.com.br`.

---

## Limitações conhecidas

- **Sem fotos reais:** o carrossel de trabalhos usa blocos de cor como placeholder.
- **Depoimentos de exemplo:** os textos e nomes são fictícios e devem ser trocados.
- **Número de WhatsApp de exemplo:** é preciso configurar o número real.
- **Preços e endereço de exemplo:** devem ser confirmados com o barbeiro.
- **Sem menu hambúrguer:** no celular o menu do cabeçalho fica escondido; a navegação é feita pela rolagem e pelos botões.
- **Telefone sem `tel:`:** o número aparece como texto; o contato clicável é o do WhatsApp.
- **Fontes dependem de internet:** sem conexão, entram as fontes de reserva.

---

## Próximos passos

- [ ] Substituir os blocos de cor por fotos reais da barbearia e dos barbeiros
- [ ] Trocar depoimentos de exemplo por avaliações reais
- [ ] Configurar o número real do WhatsApp e confirmar os preços
- [ ] Adicionar menu hambúrguer para celular
- [ ] Incluir meta tags de SEO e Open Graph (título, descrição e imagem de compartilhamento)
- [ ] Inserir dados estruturados `LocalBusiness` (Schema.org) para o Google
- [ ] Incorporar um mapa interativo do Google Maps
- [ ] Adicionar links de Instagram e outras redes sociais
- [ ] Criar uma seção com a equipe de barbeiros
- [ ] Integrar a um sistema de agendamento online, se necessário

---

## Variações de estilo

Durante o desenvolvimento foram criadas outras versões do mesmo conceito, que compartilham a mesma lógica de WhatsApp e animação:

| Versão | Estilo |
|---|---|
| Azul | Azul-marinho com agendador interativo completo (serviço, barbeiro, data e hora) |
| Clássica | Marrom-café e dourado latão, com poste de barbeiro animado |
| Vintage | Madeira escura e âmbar, inspirada na referência "Gentsbox" |
| **Grafite** | **Grafite e dourado fosco com animação de abertura (versão descrita neste README)** |

---

## Licença

Projeto desenvolvido sob medida para a barbearia Orlando Cortes. Defina aqui a licença de uso conforme o acordo entre as partes.

---

**Contato do projeto:** edite esta seção com o seu nome e forma de contato.
