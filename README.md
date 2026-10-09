# Deck Diffs

**[Português](#português) · [English](#english)**

---

## Português

Mostre o que saiu e o que entrou no seu deck de Magic: The Gathering, carta por carta, com as artes lado a lado. Feito para compartilhar upgrades de precon, ajustes de Commander e listas de compras com o grupo.

### O que ele faz

- Mostra cada troca como **carta que sai → carta que entra**, com as artes oficiais do Scryfall.
- Calcula o **preço estimado** (USD) do que entrou e monta a **lista de compras**.
- Marque **"Já tenho"** nas cartas que você já possui: elas saem da lista e do total.
- Exporta em **PDF** (A4, 3 trocas por página, fundo escuro ou claro) e em **imagem PNG**, prontos para mandar no WhatsApp ou Discord.
- Gera um **link compartilhável** com as trocas dentro da própria URL.
- Interface em **português e inglês**. Em português, cada carta tem link para a Liga Magic; em inglês, para o TCGplayer.

### Como usar

Escreva uma troca por linha, no formato `carta que saiu --> carta que entrou`:

```
Mind Stone --> Fellwar Stone
Cancel --> Counterspell
1 Path of Ancestry (CMR) 350 -> 1 Command Tower
Opt -->
--> Sol Ring
```

- A seta pode ser `-->`, `->`, `=>` ou `→`.
- Se uma carta só saiu, deixe o lado direito vazio. Se só entrou, deixe o esquerdo vazio.
- Cada lado aceita quantidade, coleção e número de colecionador no formato do Moxfield, Archidekt ou MTGA (`1 Sol Ring (CMM) 395 *F*`). Coleção e número fixam a arte exata; sem eles, o site usa a impressão mais barata com preço.
- Use os nomes das cartas **em inglês**. Erros de digitação e acentos faltando são corrigidos automaticamente na maioria dos casos.

### Rodando localmente

Não há build nem dependências. O site inteiro é o arquivo `index.html`: baixe e abra no navegador.

### Publicando no GitHub Pages

1. Crie um repositório e suba o `index.html` para a branch `main`.
2. Vá em **Settings → Pages**.
3. Em **Source**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
4. Em um ou dois minutos o site fica disponível em `https://<seu-usuario>.github.io/<nome-do-repositorio>/`.

Para atualizar, basta fazer commit de uma nova versão do `index.html`.

### Como funciona

- HTML, CSS e JavaScript puros, num arquivo só. Não tem servidor nem banco de dados: cada visitante consulta a [API do Scryfall](https://scryfall.com/docs/api) direto do próprio navegador.
- As cartas são buscadas em lote (`/cards/collection`), com busca aproximada (`/cards/named?fuzzy=`) para nomes não encontrados.
- O PDF é gerado no navegador com [jsPDF](https://github.com/parallax/jsPDF), carregado só quando você clica em **Baixar PDF**.
- Preferências (idioma, tamanho das cartas, cartas marcadas como "já tenho") ficam salvas no `localStorage` do navegador.

---

## English

Show what went out and what came in to your Magic: The Gathering deck, card by card, with the art side by side. Made for sharing precon upgrades, Commander tweaks and shopping lists with your playgroup.

### Features

- Shows each swap as **card out → card in**, with official card images from Scryfall.
- Estimates the **price** (USD) of the incoming cards and builds a **shopping list**.
- Mark cards as **"I own it"** to drop them from the list and the total.
- Exports to **PDF** (A4, 3 swaps per page, dark or light background) and **PNG image**, ready to share on Discord or WhatsApp.
- Creates a **shareable link** with the swaps stored in the URL.
- **English and Brazilian Portuguese** interface. English links each card to TCGplayer; Portuguese links to Liga Magic.

### Usage

Write one swap per line, as `card out --> card in`:

```
Mind Stone --> Fellwar Stone
Cancel --> Counterspell
1 Path of Ancestry (CMR) 350 -> 1 Command Tower
Opt -->
--> Sol Ring
```

- The arrow can be `-->`, `->`, `=>` or `→`.
- For a card that was only cut, leave the right side empty. For one that was only added, leave the left side empty.
- Each side accepts quantity, set and collector number in Moxfield, Archidekt or MTGA format (`1 Sol Ring (CMM) 395 *F*`). Set and number pin the exact printing; without them, the site uses the cheapest printing that has a price.
- Use **English** card names. Most typos and missing accents are fixed automatically.

### Running locally

No build step and no dependencies. The whole site is `index.html`: download it and open it in your browser.

### Deploying to GitHub Pages

1. Create a repository and push `index.html` to the `main` branch.
2. Go to **Settings → Pages**.
3. Under **Source**, pick **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute or two the site is live at `https://<your-username>.github.io/<repository-name>/`.

To update it, commit a new version of `index.html`.

### How it works

- Plain HTML, CSS and JavaScript in a single file. No server or database: each visitor queries the [Scryfall API](https://scryfall.com/docs/api) straight from their own browser.
- Cards are fetched in batches (`/cards/collection`), with fuzzy search (`/cards/named?fuzzy=`) for names that aren't found.
- The PDF is built in the browser with [jsPDF](https://github.com/parallax/jsPDF), loaded only when you click **Download PDF**.
- Preferences (language, card size, cards marked as owned) are stored in the browser's `localStorage`.

---

## Créditos · Credits

Dados, imagens e preços das cartas: [Scryfall](https://scryfall.com). Card data, images and prices: [Scryfall](https://scryfall.com).

Este projeto não é afiliado, patrocinado nem endossado pela Wizards of the Coast. Magic: The Gathering, os nomes e as artes das cartas são propriedade da Wizards of the Coast LLC.

This project is not affiliated with, sponsored or endorsed by Wizards of the Coast. Magic: The Gathering, card names and card art are property of Wizards of the Coast LLC.
