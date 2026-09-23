# Do jogo ao ativo — Pokémon TCG

Apresentação em página única sobre o mercado de cartas Pokémon como fenômeno de consumo,
com a antropóloga **Lívia Barbosa** como eixo teórico.

Trabalho da disciplina **Sociedade, Cultura e Consumo** — Fatec Sebrae, 2026.

**No ar em:** https://joaoluzdesign.github.io/pokemon-tcg-do-jogo-ao-ativo/

---

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | A apresentação inteira — 28 telas, com imagens e vídeos embutidos no próprio arquivo. É o único arquivo necessário para o site funcionar. |
| `og-cover.png` | Imagem que aparece na pré-visualização quando o link é compartilhado no WhatsApp, Slack ou LinkedIn. |
| `.nojekyll` | Diz ao GitHub Pages para publicar os arquivos como estão, sem passar pelo Jekyll. Pode ficar vazio. |
| `.gitignore` | Evita subir lixo do sistema (`.DS_Store`, `Thumbs.db`). |
| `README.md` | Este arquivo. |

O `index.html` é autocontido: todas as imagens, o logo e os dois vídeos estão embutidos em
base64. Não existe pasta de assets, e nada quebra se o arquivo for movido de lugar.

---

## Publicar no GitHub Pages

O GitHub Pages é gratuito em **repositórios públicos**. Em repositório privado ele exige
plano pago, então crie o repositório como público.

### 1. Criar o repositório

Em https://github.com/new:

- **Repository name:** `pokemon-tcg-do-jogo-ao-ativo`
- **Visibility:** Public
- Não marque "Add a README file" — o README já está nesta pasta.

### 2. Subir os arquivos

**Pelo navegador (mais simples):** na tela do repositório recém-criado, clique em
*uploading an existing file* e arraste **o conteúdo desta pasta** — os arquivos soltos,
não a pasta em si. O `index.html` precisa ficar na raiz do repositório.

> O Chrome não arrasta arquivos que começam com ponto. Se o `.nojekyll` não subir junto,
> crie-o direto no GitHub: **Add file → Create new file**, nome `.nojekyll`, deixe o corpo
> vazio e confirme.

**Pelo terminal, se preferir:**

```bash
cd "C:\Users\João Luz\Downloads\2. Fatec\2026\Sociedade e cultura\pokemon-tcg-do-jogo-ao-ativo"
git init -b main
git add .
git commit -m "Apresentação: Do jogo ao ativo"
git remote add origin https://github.com/joaoluzdesign/pokemon-tcg-do-jogo-ao-ativo.git
git push -u origin main
```

### 3. Ligar o Pages

No repositório: **Settings → Pages**

- **Source:** Deploy from a branch
- **Branch:** `main` · pasta `/ (root)`
- **Save**

A primeira publicação leva de 1 a 2 minutos. Acompanhe pela aba **Actions**; quando o
check ficar verde, o endereço está no ar.

---

## Detalhes que podem te pegar

- **Nome do repositório vira parte da URL.** Se você usar outro nome, o endereço muda e as
  duas linhas `og:` com URL absoluta no `<head>` do `index.html` precisam ser ajustadas —
  senão a pré-visualização do link fica sem imagem.
- **Repositório `joaoluzdesign.github.io`.** Esse nome é reservado para o seu site
  principal e serve na raiz do domínio. Como você já usa esse espaço, mantenha este
  trabalho em um repositório próprio.
- **Peso da página:** 4,7 MB, quase tudo vídeo e imagem em base64. Abre rápido no Wi-Fi da
  faculdade; em 4G fraco a primeira carga pode levar alguns segundos. Depois fica em cache.
- **Cache do navegador.** Ao atualizar o `index.html`, o GitHub pode continuar servindo a
  versão antiga por alguns minutos. Um *hard refresh* (Ctrl+Shift+R) resolve.
- **Apresentar em tela cheia:** a própria página aceita a tecla `F`. As setas, `Espaço` e
  `Page Down` passam de tela.

---

## Atualizar depois

Basta substituir o `index.html` no repositório (**Add file → Upload files**, ou
`git add . && git commit && git push`). O Pages republica sozinho a cada commit na `main`.
