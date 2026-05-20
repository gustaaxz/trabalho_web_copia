# Documentação do Projeto - Biografia de Gustavo "Sacy" Rossi

Esta documentação serve como snapshot detalhado da estrutura de arquivos HTML, CSS e ativos digitais (assets) antes das modificações planejadas. Ela registra a finalidade de cada página, os estilos associados, esquemas de cores e layouts.

---

## 📂 Estrutura de Diretórios Atual

```
trabalho_web/
├── index.html                   # Página principal (Biografia)
├── README.md                    # Esta documentação
├── css/                         # Folhas de estilo (CSS)
│   ├── contato.css
│   ├── lol.css
│   ├── loud.css
│   ├── pagina_inicio.css
│   ├── sacy.css
│   ├── sen.css
│   ├── valorant.css
│   └── vks.css
├── html/                        # Páginas secundárias (HTML)
│   ├── contato.html
│   ├── lol.html
│   ├── loud.html
│   ├── sacy.html
│   ├── sen.html
│   ├── valorant.html
│   └── vks.html
└── assets/                      # Imagens e logotipos do site
```

---

## 🌐 Mapeamento das Páginas HTML

### 1. `index.html` (Raiz)
* **Objetivo:** Página principal que apresenta a biografia geral de Gustavo "Sacy" Rossi.
* **Estilo Associado:** `css/sacy.css`
* **Layout / Seções:**
  - `.topo`: Cabeçalho com imagem (`assets/sacy_teste.jfif`), título em destaque "SACY" e subtítulo "Gustavo 'Sacy' Rossi".
  - `.times`: Menu de navegação superior contendo os logotipos dos quatro principais times (RED Canids, Vikings, LOUD, Sentinels) que levam às páginas na pasta `html/`.
  - `.biografia`: Texto narrando a trajetória geral, conquistas e retorno em 2026.
  - `.oque_e_valorant`: Banner inferior com link para a explicação do jogo VALORANT.

### 2. `html/sacy.html`
* **Objetivo:** Cópia interna da página de biografia principal, estruturada para navegação interna dentro de `/html`.
* **Estilo Associado:** `../css/sacy.css`
* **Links Internos:** Todos relativos à pasta `/html` (ex: `lol.html`, `vks.html`).

### 3. `html/lol.html`
* **Objetivo:** Detalha a história do jogador no League of Legends defendendo a RED Canids.
* **Estilo Associado:** `../css/lol.css`
* **Layout / Seções:**
  - Botão Voltar (`../assets/botao_volta.png`) que aponta para `../index.html`.
  - Cabeçalho com banner da RED Canids (`../assets/lol1.jpeg`).
  - `.times`: Navegador rápido de times.
  - `.grid-container`: Grid de 2 colunas alternando imagens históricas (`lol3.jpeg`, `lol2.jpeg`, `corinthians.jpg`) com blocos explicativos de texto.

### 4. `html/vks.html`
* **Objetivo:** Detalha a transição do jogador para o VALORANT na Team Vikings.
* **Estilo Associado:** `../css/vks.css`
* **Layout / Seções:**
  - Botão Voltar para a Home.
  - Cabeçalho com banner da Team Vikings (`../assets/vk.jpeg`).
  - `.grid-container`: Exibe imagens (`vkscam.jpg`, `viking.jpg`, `branco.webp`, `sacy-vikings-valorant-vks-removebg-preview.png`) e textos sobre a parceria de sucesso com o argentino Saadhak.

### 5. `html/loud.html`
* **Objetivo:** Apresenta o ápice da carreira de Sacy, onde conquistou o título mundial de VALORANT Champions em 2022 pela LOUD.
* **Estilo Associado:** `../css/loud.css`
* **Layout / Seções:**
  - Cabeçalho temático em tons de verde com logo da LOUD (`../assets/loud.jpeg`).
  - `.grid-container`: Estrutura de grid alternando imagens da estreia, taça do mundial e formação do time (`loudcam.jpg`, `sacy-loud-masters-reykjavik-2022-valorant.jpg`, `LOUD-Sacy-VCT-2022.jpeg`, `sacy-loud.jpg`) com narrativas históricas.

### 6. `html/sen.html`
* **Objetivo:** Descreve a transferência internacional para a Sentinels, título do Masters Madrid 2024 e o anúncio de sua aposentadoria.
* **Estilo Associado:** `../css/sen.css`
* **Layout / Seções:**
  - Cabeçalho com banner temático (`../assets/sen.jpeg`).
  - `.grid-container`: Textos explicativos e imagens memoráveis da trajetória norte-americana (`53053710949-4dbae23264-k.webp`, `rolon.png`, `dedo.jpg`, `feliz.jpeg`).

### 7. `html/valorant.html`
* **Objetivo:** Uma página simples de suporte que introduz o jogo VALORANT.
* **Estilo Associado:** `../css/valorant.css`
* **Conteúdo:** Apenas logotipo do jogo (`../assets/valorant_logo1.jpg`) e cabeçalho.

### 8. `html/contato.html`
* **Objetivo:** Página de captura / newsletter do site.
* **Estilo Associado:** `../css/contato.css`
* **Conteúdo:** Formulário estilizado para entrada de e-mail e botão de inscrição.

---

## 🎨 Fichas Técnicas dos Arquivos CSS

### 🎨 `sacy.css`
* **Cor de Fundo:** `#111` (Preto/Grafite escuro)
* **Cor do Texto:** `white` e `#ccc` / `#ddd` (Cinza claro para parágrafos)
* **Tipografia:** `Arial, sans-serif`
* **Layouts Principais:**
  - `.topo`: Bloco de altura fixa (`500px`) com sobreposição gradiente linear (`linear-gradient(to bottom, transparent, black)`) e posicionamento absoluto do título.
  - `.times`: Flexbox (`display: flex`) com espaçamento (`gap: 5px`) e cores de fundo específicas para cada link de time (vermelho, dourado, verde e cinza).
  - `.times a img`: Efeito hover com `scale(1.12)` em `0.2s`.
  - `.oque_e_valorant`: Box centralizado com efeito hover de zoom e opacidade na imagem do link.

### 🎨 `lol.css`
* **Cor de Fundo:** `black`
* **Layouts Principais:**
  - `.grid-container`: Layout Grid de 2 colunas (`grid-template-columns: 1fr 1fr`) com espaçamento (`gap: 20px`), centralizando imagens e textos explicativos.
  - `.topo h1`: Letras em tom vermelho vibrante (`rgb(236, 24, 24)`) com sombra cinza (`text-shadow: 2px 2px 10px rgb(112, 105, 105)`).
  - `.grid-item3`: Flexbox com posicionamento absoluto para fixar o botão de voltar no topo esquerdo.

### 🎨 `vks.css` / `loud.css` / `sen.css`
* **Cores de Fundo:** Seguem a identidade escura (`black` ou `#111`).
* **Layouts:** Utilizam a mesma base estrutural do `lol.css` com `.grid-container` (`grid-template-columns: 1fr 1fr`) e botões de voltar estilizados.

### 🎨 `contato.css`
* **Cor de Fundo:** Baseada em imagem de fundo desfocada (`url('../assets/LOUD-Sacy-VCT-2022.jpeg')`) com overlay gradiente escuro.
* **Layouts Principais:**
  - `.subscribe-box`: Caixa centralizada de vidro opaco (`rgba(240, 248, 255, 0.95)`) com bordas arredondadas (`16px`) e sombra suave.
  - Formulário e botões estilizados de forma responsiva com media queries (`@media (max-width: 768px)` e `@media (max-width: 480px)`).

---

## 📷 Detalhamento do Uso de Ativos (Assets)

A tabela abaixo lista os arquivos de imagem na pasta `assets/` e onde estão sendo utilizados de fato no HTML:

| Nome do Arquivo | Descrição | Utilizado em |
| :--- | :--- | :--- |
| `sacy_teste.jfif` | Foto principal do Sacy | `index.html`, `html/sacy.html` |
| `red.png` | Logotipo RED Canids | Todos os cabeçalhos de navegação de times |
| `vks.png` | Logotipo Team Vikings | Todos os cabeçalhos de navegação de times |
| `loud.png` | Logotipo LOUD | Todos os cabeçalhos de navegação de times |
| `sentinels.png` | Logotipo Sentinels | Todos os cabeçalhos de navegação de times |
| `botao_volta.png` | Ícone de seta para voltar | `html/lol.html`, `html/loud.html`, `html/sen.html`, `html/vks.html` |
| `lol1.jpeg` | Foto Sacy na RED Canids | `html/lol.html` |
| `lol2.jpeg` | Foto da RED Canids levantando taça | `html/lol.html` |
| `lol3.jpeg` | Foto Sacy RED Canids em jogo | `html/lol.html` |
| `corinthians.jpg` | Foto da RED Canids Corinthians | `html/lol.html` |
| `vk.jpeg` | Foto Sacy na Team Vikings | `html/vks.html` |
| `vkscam.jpg` | Foto da Team Vikings no palco | `html/vks.html` |
| `viking.jpg` | Arte promocional Team Vikings | `html/vks.html` |
| `branco.webp` | Foto Sacy Vikings na Islândia | `html/vks.html` |
| `sacy-vikings-valorant-vks-removebg.png` | Render sem fundo Sacy Vikings | `html/vks.html` |
| `loud.jpeg` | Sacy LOUD segurando bandeira | `html/loud.html` |
| `loudcam.jpg` | LOUD na estreia internacional | `html/loud.html` |
| `sacy-loud-masters-reykjavik-2022-valorant.jpg` | Sacy com uniforme LOUD no palco | `html/loud.html` |
| `LOUD-Sacy-VCT-2022.jpeg` | Sacy levantando a taça do Champions | `html/loud.html`, `css/contato.css` (Background) |
| `sacy-loud.jpg` | Foto promocional LOUD | `html/loud.html` |
| `sen.jpeg` | Sacy segurando bandeira dos EUA | `html/sen.html` |
| `53053710949-4dbae23264-k.webp` | Time da Sentinels no palco principal | `html/sen.html` |
| `rolon.png` | Sacy jogando pela Sentinels | `html/sen.html` |
| `dedo.jpg` | Foto Sacy apontando indicador | `html/sen.html` |
| `feliz.jpeg` | Sacy feliz com troféu da Sentinels | `html/sen.html` |
| `valorant.jpg` | Banner link Valorant | `index.html`, `html/sacy.html` |
| `valorant_logo1.jpg` | Logotipo Valorant | `html/valorant.html` |

---

## ✅ Melhorias e Atualizações Realizadas

1. Adicionado `css/style.css` em todas as páginas HTML para aplicar estilos globais compartilhados.
2. Importado o Font Awesome em todos os arquivos HTML usando `cdnjs.cloudflare.com`.
3. Atualizada a classe `container` em imagens principais de todas as páginas para melhorar a exibição responsiva e o layout.
4. Convertidos todos os `h1` para `h2` nas páginas HTML, mantendo apenas os títulos principais dentro da `div.topo` como `h1`.
5. Ajustados os caminhos relativos dos links de CSS e imagens onde necessário para garantir que todos os arquivos funcionem corretamente dentro de `html/`.
6. Verificado que não há links HTML apontando para `html/sacy.html` no projeto; sua referência existe apenas no `README.md`.
7. Organizado o conteúdo de navegação em todas as páginas para manter consistência visual entre as rotas internas.

> Essas alterações foram feitas para melhorar a consistência de estilo, a semântica dos títulos, a responsividade de imagens e a compatibilidade de ícones com Font Awesome.
