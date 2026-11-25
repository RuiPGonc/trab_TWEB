---
tags: [tecnologias-web, trabalho-pratico, mwc, grupo]
uc: Tecnologias Web 2026/27
site: https://www.mwcbarcelona.com/
entrega: 2026-12-31 23:59
defesa: 2027-01-03 a 2027-01-06
peso: 40% (8 valores)
---

# TW — Trabalho Prático: réplica MWC Barcelona

> [!info] Resumo
> - **O quê:** replicar a página do **MWC Barcelona** (screenshot do Anexo 1, de 22/10/2026) só com **HTML + CSS**, e acrescentar uma **secção de compra de bilhetes** em **JavaScript**, antes do rodapé.
> - **Grupo:** 3 elementos.
> - **Entrega:** 31/12/2026, 23:59, no Nónio (.zip). Penalização de 2% por hora de atraso, só nas primeiras 24 h.
> - **Defesa:** 3 a 6/01/2027, parte em grupo + parte individual. **Cada um leva o seu portátil.**
> - **Nota:** `T × (0,4 + 0,6 × D)`. Se D < 40%, fica `T × D`. **A defesa conta muito: todos têm de saber explicar e alterar tudo.**

---

## 1. Regras obrigatórias (checklist)

- [ ] Só 3 ficheiros + pasta de imagens: `index.html`, `estilos.css`, `logica.js`, `img/`
- [ ] **Flexbox E Grid** usados no layout (os dois são obrigatórios)
- [ ] **Responsive com no máximo 3 media queries / breakpoints**
- [ ] **Menu hamburger** em ecrãs pequenos, **só HTML/CSS** (ex.: truque da checkbox), 1 nível, sem submenus
- [ ] **Submenus com hover** na barra de navegação (1 nível; podem ser inventados)
- [ ] **JavaScript SÓ na secção de bilhetes.** Tudo o resto em HTML/CSS, incluindo o carrossel "Past MWC speakers" (usar scroll horizontal + `scroll-snap`, ou similar)
- [ ] Proibido usar `alert()`, `confirm()` e `prompt()`: as mensagens aparecem na página
- [ ] Efeitos hover em links, botões, cartões e menus
- [ ] Sem subpáginas: os links apontam para `#`
- [ ] Proibido: frameworks (Bootstrap, Tailwind), SASS, jQuery e qualquer biblioteca, templates, **código copiado do site original** (dá 0% em T = chumbo) e cópia entre grupos
- [ ] Permitido: Google Fonts, Google Material Symbols **em SVG**, SVG de marcas/redes sociais de outras fontes, imagens e logótipo do site original
- [ ] **Comentário no início do HTML** a indicar as ferramentas de IA usadas e para quê
- [ ] Nomes de ficheiros e pastas sem espaços nem acentos; **caminhos relativos**
- [ ] Zip: `PrimeiroUltimo_nº_PrimeiroUltimo_nº_PrimeiroUltimo_nº`, entregue por **um só** elemento
- [ ] Se o site mudar entretanto, segue-se o **screenshot**, não o site atual

---

## 2. Critérios de avaliação

**T: trabalho entregue (nota de grupo)**

| Critério | Peso |
|---|---|
| Réplica visual (estrutura, cores, tipografia, imagens, hover) | 20% |
| Layout com Flexbox + Grid | 15% |
| Responsive (≤ 3 breakpoints) | 15% |
| Hamburger + submenus hover (só HTML/CSS) | 15% |
| Funcionalidades JS (formulário, programa, bilhetes, preço, confirmação) | **25%** |
| Qualidade do código (HTML semântico, CSS organizado, nomes claros) | 10% |

**D: defesa (nota individual)**

| Momento | Critério | Peso |
|---|---|---|
| Grupo | Apresentação e explicação das opções tomadas | 20% |
| Individual | Perguntas sobre o código | 30% |
| Individual | Alteração pedida em HTML/CSS | 25% |
| Individual | Alteração pedida em JavaScript | 25% |

> [!warning] Implicação para a divisão
> Na defesa individual, cada um faz **uma alteração em HTML/CSS e outra em JS**. Por isso **cada elemento tem de fazer as duas coisas**: não convém que uma pessoa fique só com o JS e as outras só com o CSS.

---

## 3. Breakdown das tarefas

### 3.1 Secções da página MWC (pela ordem do screenshot)

| # | Secção | Conteúdo | Layout sugerido | Pontos de atenção | Dificuldade |
|---|---|---|---|---|---|
| 1 | **Header / navegação** | Barra superior pequena (pesquisa, links, login), logo MWC, menu principal (Industries, Attend, Get involved, MWC27 highlights, About), logos 4YFN/GSMA | Flexbox | Submenus com hover; **hamburger só com CSS** em mobile | 🔴 Alta |
| 2 | **Hero** | Imagem de fundo com gradiente azul/rosa, título "Experience the power of connection", texto, datas e local, botão rosa | Flexbox | `background-image` + overlay em gradiente | 🟡 Média |
| 3 | **"Turn conversations into customers"** | Texto + botão à esquerda, imagem à direita | Grid (2 colunas) | Em mobile passa a 1 coluna | 🟢 Baixa |
| 4 | **"Connect Health launches"** | Imagem à esquerda, texto + botão à direita (invertido) | Grid (2 colunas) | Reaproveitar as classes da secção 3 | 🟢 Baixa |
| 5 | **Keynote speakers** | 5 cartões (foto, nome, cargo, descrição) em fundo azul escuro | Grid (5 colunas) | Hover nos cartões; 5 → 2 → 1 colunas | 🟡 Média |
| 6 | **Global connectivity ecosystem** | Elipses concêntricas com logos e "MWC" ao centro | Grid/posicionamento ou imagem | Pode ser feito com `border-radius` em elipses + logos posicionados, ou com imagem/SVG (mais simples) | 🔴 Alta (se for em CSS) |
| 7 | **"Make the numbers work"** | 7 caixas de estatísticas (5 + 2) + botão | Flexbox com `wrap` + `justify-content: center` | Com Flexbox, a linha de 2 fica centrada | 🟢 Baixa |
| 8 | **Our themes** | 6 logos de temas (Networks Reinvented, AI in Action…) + faixa de logos de parceiros + botão "Explore the themes" | Grid (6 colunas) + Flexbox | Hover nos temas | 🟡 Média |
| 9 | **The MWC experience** | 4 cartões (imagem, título, texto, link com seta) | Grid (4 colunas) | Hover; link com ícone SVG | 🟢 Baixa |
| 10 | **Event highlights** | Imagem/vídeo grande centrado | Flexbox | Pode ser imagem estática ou `<video>` | 🟢 Baixa |
| 11 | **Past MWC speakers** | Carrossel de oradores com setas | Flexbox + `overflow-x: auto` + `scroll-snap` | ⚠️ **Sem JS!** As setas podem ser decorativas ou âncoras `#` | 🔴 Alta |
| 12 | **Key headlines from MWC26** | 1 notícia grande à esquerda + 3 pequenas à direita (imagem, título, data, etiqueta rosa) | Grid (2 colunas) + Flexbox nas pequenas | Etiquetas em "pill" | 🟡 Média |
| 13 | **Newsletter** | Faixa azul com texto + input de email + botão "Subscribe" | Flexbox | Só visual: não há JS aqui | 🟢 Baixa |
| 14 | **Partners & Sponsors** | 11 logos (6 + 5) com legendas | Grid (6 colunas) | Hover nos logos | 🟢 Baixa |
| 15 | **🎟️ Compra de bilhetes (NOVA)** | Formulário + resultados + confirmação | Grid/Flexbox | Não existe no site: o design tem de seguir o estilo MWC | 🟡 Média (HTML/CSS) |
| 16 | **Footer** | Logo, texto, redes sociais, 4 colunas de links, badges das apps, copyright | Grid (5 colunas) | Ícones SVG de redes sociais | 🟡 Média |

### 3.2 Funcionalidades em JavaScript (secção de bilhetes, 25% de T)

| # | Tarefa | Detalhe | Dificuldade |
|---|---|---|---|
| J1 | **Formulário** | Tipo (Geral/VIP), nº de bilhetes (1–6, por omissão 1), data de início e de fim, checkbox "Incluir workshop", botão "Calcular preço" | 🟢 |
| J2 | **Validações** | Nº entre 1 e 6; datas entre **15 e 21/03/2027** (15 é segunda, 21 é domingo); fim ≥ início; erros mostrados **na página** | 🟡 |
| J3 | **Cálculo do preço** | Por dia e por bilhete: dias úteis 30€ (G) / 50€ (VIP); fim de semana 45€ (G) / 70€ (VIP). Desconto de 10% (2 dias) ou 20% (≥ 3 dias), **só sobre os bilhetes**. Workshop: +25€ por bilhete, **uma vez e sem desconto**. Duas casas decimais com vírgula | 🔴 |
| J4 | **Lista de bilhetes** | Formato `TIPO-X` (ex.: VIP-1, VIP-2, VIP-3) | 🟢 |
| J5 | **Programa** | Array de **8 sessões** (título, orador, data, hora), das quais se mostram **4 aleatórias sem repetição** (é a opção mais valorizada) | 🟡 |
| J6 | **Total + "ver detalhes"** | "Total: 354,00€ (ver detalhes)"; o clique mostra/esconde o cálculo | 🟡 |
| J7 | **Substituir resultados** | Um novo cálculo **substitui** o anterior, não acrescenta | 🟢 |
| J8 | **Confirmar** | Mostra um mini-formulário (nome + email); valida campos vazios e formato do email; mensagem "Obrigado, Ana! A sua compra de 354,00€ foi registada." | 🟡 |
| J9 | **Cancelar** | Apaga os resultados e repõe o formulário no estado inicial | 🟢 |

> [!example] Casos de teste obrigatórios
> - 2 VIP, 19 a 21/03, com workshop: (50+70+70)×2 = 380 → −20% = 304 + 50 = **354,00€**
> - 1 Geral, 19 a 20/03, sem workshop: 30+45 = 75 → −10% = **67,50€**

### 3.3 Tarefas transversais

| # | Tarefa | Quando |
|---|---|---|
| T1 | Confirmar a inscrição do tema no Nónio (fórum "Tema do Trabalho Prático", nome e número dos 3) | Já, se ainda não estiver feito |
| T2 | Criar repositório Git partilhado (GitHub) e combinar o fluxo de trabalho | Semana 1 |
| T3 | **Base comum de CSS**: reset, variáveis (cores, fontes, espaçamentos), fonte Google, classes reutilizáveis (`.container`, `.btn`, `.card`, títulos de secção) | Semana 1, **em conjunto** |
| T4 | Combinar os **3 breakpoints** (ex.: 1024px, 768px, 480px) e a convenção de nomes das classes (ex.: BEM) | Semana 1 |
| T5 | Recolher imagens, logos e ícones SVG para `img/` | Semana 1–2 |
| T6 | Comentário sobre o uso de IA no topo do HTML | Final |
| T7 | Validar no W3C Validator (HTML e CSS) e testar em vários tamanhos de ecrã | Final |
| T8 | **Code review cruzado**: cada um explica a sua parte aos outros dois | Contínuo + última semana |
| T9 | Simular a defesa: pedir alterações uns aos outros | 27–30/12 |
| T10 | Zip com o nome correto e entrega por um elemento | Até 30/12 (com margem) |

---

## 4. Divisão proposta pelos 3 elementos

**Princípio:** cada pessoa fica com **secções de HTML/CSS + uma parte do JS**, para que todos pratiquem os dois tipos de alteração pedidos na defesa. Os pesos ficam equilibrados.

| | 👤 Elemento A — "Navegação e topo" | 👤 Elemento B — "Conteúdo central" | 👤 Elemento C — "Fim da página e bilhetes" |
|---|---|---|---|
| **HTML/CSS** | 1. Header + **submenus hover** + **hamburger** · 2. Hero · 3. Conversations · 4. Connect Health · 16. Footer | 5. Keynote speakers · 6. Ecosystem · 7. Numbers · 8. Themes · 9. MWC experience | 10. Event highlights · 11. **Carrossel Past speakers (CSS)** · 12. Headlines · 13. Newsletter · 14. Partners · 15. **HTML/CSS da secção de bilhetes** |
| **JavaScript** | J1 + J2 **Validações** do formulário + J9 **Cancelar** (reset) | J3 **Cálculo do preço** + J4 Bilhetes `TIPO-X` + J6 Total/"ver detalhes" | J5 **Programa aleatório** + J7 Substituir resultados + J8 **Confirmação** (nome/email) |
| **Critério que "lidera"** | Hamburger/submenus (15%) | Grid/Flexbox + réplica visual | Responsive do fim da página + integração JS |
| **Responsive** | Das suas secções | Das suas secções | Das suas secções |

> [!tip] Como trabalhar em conjunto
> 1. **Semana 1 (até 20/11):** os 3 juntos fazem T1–T5: base de CSS, variáveis, breakpoints, estrutura HTML vazia com as 16 secções (`<header>`, `<main>` com `<section id="...">`, `<footer>`). Cada um passa a trabalhar só dentro das suas secções, o que evita conflitos no Git.
> 2. **Até 6/12:** HTML/CSS das secções em desktop.
> 3. **Até 15/12:** JS. O C cria primeiro a estrutura HTML do formulário (secção 15) e combina com os outros os `id` dos elementos, para que A e B possam avançar em paralelo.
> 4. **Até 22/12:** responsive + integração + testes dos casos de cálculo.
> 5. **23–30/12:** revisão cruzada, validação W3C, simulação da defesa, entrega **antes** de 31/12.

> [!important] Interfaces entre as partes do JS (combinar no início)
> - A expõe uma função `validarFormulario()` que devolve `true`/`false` e mostra os erros.
> - B expõe `calcularPreco(tipo, qtd, inicio, fim, workshop)`, que devolve `{ subtotal, desconto, workshop, total, detalhes }`.
> - C trata do clique em "Calcular preço": chama `validarFormulario()`, depois `calcularPreco()`, limpa os resultados anteriores e mostra programa, bilhetes, total e os botões Confirmar/Cancelar.

> [!warning] Lembrete
> A divisão serve só para **produzir**. Na defesa **todos respondem sobre tudo**. Reservar tempo para que cada um explique o seu código aos outros e para que cada um experimente alterar o código dos colegas.

---

## 5. Riscos e armadilhas

- **Carrossel com setas:** a tentação é usar JS, mas **não é permitido**. Fazer em CSS (`overflow-x` + `scroll-snap`).
- **Hamburger:** usar `<input type="checkbox">` + `<label>` + seletor `:checked ~ nav`.
- **Mais de 3 media queries** = penalização. Planear bem os breakpoints desde o início.
- **Datas em JS:** `new Date("2027-03-15")` é interpretado em UTC. Usar `new Date(2027, 2, 15)` ou `getUTCDay()` com consistência; `getDay()` devolve 0 (domingo) e 6 (sábado).
- **Arredondamentos:** usar `toFixed(2).replace(".", ",")` para mostrar "354,00€".
- **Ecosystem (elipses):** se demorar demasiado, uma imagem/SVG é aceitável. O que é avaliado é a fidelidade visual.
- **Código gerado por IA:** só vale se for defendido. Escrever código que se consiga explicar linha a linha.



| Fase | Datas | O que fica feito | Checkpoint |
|---|---|---|---|
| **0. Arranque** | 13 a 16/11 (sex. a seg.) | Inscrição no Nónio confirmada, repositório Git, base de CSS (variáveis, reset, fonte), os 3 breakpoints, esqueleto HTML com as 16 secções, imagens em `img/`, nomes das funções e `id` do JS combinados | Reunião na seg. 16/11 |
| **1. HTML/CSS em desktop** | 17 a 29/11 | Cada um faz as suas secções. O C faz primeiro o HTML do formulário de bilhetes (até 20/11) para desbloquear o JS | Dom. 22/11: metade das secções; dom. 29/11: todas |
| **2. JavaScript** | 23/11 a 6/12 (em paralelo com o fim da fase 1) | A: validações + Cancelar · B: cálculo do preço + bilhetes + detalhes · C: programa + confirmação + integração | Dom. 6/12: os dois casos de teste dão 354,00€ e 67,50€ |
| **3. Responsive e integração** | 30/11 a 9/12 | Media queries, hamburger, submenus, acertos visuais face ao screenshot | Qua. 9/12: página completa em mobile, tablet e desktop |
| **4. Revisão** | 10 a 13/12 | Validação W3C, limpeza do código, comentário sobre o uso de IA, revisão cruzada (cada um explica a sua parte aos outros) | Dom. 13/12: versão final congelada |
| **Entrega** | **Seg. 14/12** | Zip com o nome certo, submetido por um elemento | Fica um dia de margem até 15/12 |