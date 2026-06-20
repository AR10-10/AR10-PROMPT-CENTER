# AR10-PROMPT-CENTER

Central premium **NEBULA PromptOps AR10**: uma página estática para organizar prompts, gavetas, voz Siriform, ferramentas de resumo, Handoff/QA e Clean Room.

## Status

- **Entrada principal:** `index.html`
- **Tipo:** site estático, sem backend obrigatório
- **Build:** não requer build, bundler, servidor Node ou dependências externas
- **Publicação-alvo:** GitHub Pages via branch `main` / pasta root (`/`)
- **Link público esperado:** `https://ar10-10.github.io/AR10-PROMPT-CENTER/`
- **Modo aplicativo:** PWA progressivo com `manifest.webmanifest`, `service-worker.js`, ícone NEBULA e suporte a “Adicionar à Tela de Início”
- **Compatibilidade-alvo:** Safari/iPadOS, Safari/macOS e navegadores modernos
- **Segurança:** não usar API keys, tokens, segredos, `.env` real ou credenciais no front-end

## Arquivos principais

- `index.html` — página oficial da Central NEBULA PromptOps para abrir localmente ou publicar no GitHub Pages.
- `AR10_NEBULA_PROMPTOPS_CENTRAL_V10_2_PRO_LITE_FINAL_SIRIFORM.html` — HTML base preservado como artefato histórico/original da versão V10.2 Pro Lite.
- `AGENTS.md` — regras oficiais de manutenção para agentes e futuras evoluções.
- `manifest.webmanifest` — manifesto PWA para instalação progressiva como aplicativo.
- `service-worker.js` — cache estático simples para abertura rápida/offline após primeira visita.
- `assets/nebula-icon.svg` — ícone NEBULA/Siriform para navegador, PWA e tela inicial.
- `.nojekyll` — garante publicação direta dos arquivos estáticos no GitHub Pages.
- `README.md` — instruções de uso e publicação.


## Link direto

Quando o GitHub Pages estiver ativo, abra diretamente:

```text
https://ar10-10.github.io/AR10-PROMPT-CENTER/
```

## Instalar como aplicativo

### iPad / Safari

1. Abra `https://ar10-10.github.io/AR10-PROMPT-CENTER/` no Safari.
2. Toque no botão **Compartilhar**.
3. Toque em **Adicionar à Tela de Início**.
4. Confirme o nome **NEBULA PromptOps**.

### Desktop / Chrome / Edge

1. Abra o link público no navegador.
2. Use o ícone **Instalar** na barra de endereço quando aparecer.
3. Se o ícone não aparecer, use o menu do navegador e escolha instalar/salvar como aplicativo quando disponível.

> Observação: o modo aplicativo depende das regras do navegador. No iPad/Safari, a instalação é feita pelo menu Compartilhar. A voz Siriform pode exigir um toque do usuário antes de falar.

## Como abrir localmente

### Opção simples

Abra `index.html` diretamente no navegador.

### Opção com servidor estático local

Na raiz do repositório, execute:

```bash
python3 -m http.server 8000
```

Depois acesse:

```text
http://localhost:8000/
```

No iPad, publique no GitHub Pages ou sirva pela rede local para testar com Safari/iPadOS.

## Como publicar no GitHub Pages

1. Envie este repositório para o GitHub com `index.html` na raiz.
2. Abra **Settings** do repositório.
3. Entre em **Pages**.
4. Em **Build and deployment**, selecione:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Salve e aguarde o GitHub gerar a URL pública.

Como o projeto é estático, não há etapa obrigatória de instalação ou build.

## Regras de manutenção segura

- Evoluir sempre em cima do HTML existente; não recriar do zero.
- Preservar visual premium NEBULA / Siriform.
- Preservar as abas: **Início**, **Biblioteca**, **Ferramentas**, **Voz**, **Handoff/QA** e **Clean Room**.
- Preservar Siriform Voice e controles de parar/pausar/continuar voz.
- Manter compatibilidade com iPad/Safari: viewport correto, botões tocáveis, fonte mínima segura em campos e sem dependência de APIs privadas.
- Não adicionar backend obrigatório.
- Não adicionar chaves, tokens, segredos ou credenciais.
- Manter o projeto simples, rápido e publicável no GitHub Pages.

## Próximos passos seguros

- Testar no Safari/iPadOS após publicar no GitHub Pages.
- Validar a voz Siriform com interação manual, pois navegadores móveis podem exigir toque do usuário antes de liberar `speechSynthesis`.
- Manter qualquer integração futura como opcional e sem segredo embutido no HTML.
