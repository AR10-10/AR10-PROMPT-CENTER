# AGENTS.md — AR10-PROMPT-CENTER

Este repositório é a gaveta oficial da **Central NEBULA PromptOps**.

## Missão do repositório

Finalizar e manter uma página principal estática, premium, rápida e publicável via GitHub Pages para uso no iPad/Safari.

## Regras obrigatórias

1. `index.html` é a entrada principal oficial da página.
2. Se surgir outro HTML principal, consolidar a versão publicável em `index.html`.
3. Não recriar o projeto do zero: evoluir in-place sobre o HTML existente.
4. Preservar o visual premium **NEBULA / Siriform**.
5. Preservar as abas: **Início**, **Biblioteca**, **Ferramentas**, **Voz**, **Handoff/QA** e **Clean Room**.
6. Preservar Siriform Voice e compatibilidade com iPad/Safari.
7. Não criar backend obrigatório.
8. Não adicionar API key, token, segredo, `.env` real ou credencial.
9. Manter o projeto simples, estático, rápido e publicável.
10. Não remover conteúdo útil sem justificar no commit/PR.
11. Não adicionar complexidade desnecessária, frameworks ou build obrigatório sem necessidade explícita.
12. Preparar sempre para GitHub Pages em branch `main` / root.

## Padrão técnico

- Preferir HTML/CSS/JavaScript estático no próprio `index.html`.
- Manter PWA progressivo simples com `manifest.webmanifest`, `service-worker.js`, `assets/nebula-icon.svg` e `.nojekyll`, sem build obrigatório.
- Evitar dependências externas obrigatórias.
- Manter funcionamento aceitável se aberto diretamente no navegador.
- Usar recursos compatíveis com Safari/iPadOS sempre que possível.
- Para voz, manter controles visíveis de parar, pausar e continuar; lembrar que iPad/Safari pode exigir gesto do usuário para liberar áudio/voz.

## Segurança

- Nunca commitar segredos, tokens, chaves privadas, credenciais ou `.env` real.
- Não transformar a Central PromptOps em runtime operacional ou executor financeiro.
- Manter postura READ_ONLY / Clean Room para conteúdo sensível.

## Validação recomendada

Antes de finalizar mudanças:

```bash
git status --short
python3 -m http.server 8000
```

Abrir `http://localhost:8000/` ou `index.html` no navegador e validar abas principais, busca, modal, cópia e voz quando disponível.
