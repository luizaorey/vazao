# Vazão

Ferramenta de campo (PWA) para cálculos de vazão. Mesmo padrão do projeto
[`regua-nivel`](https://github.com/luizaorey/regua-nivel): arquivo único,
funciona offline, instala no celular.

> Projeto iniciado em 2026-10-15. O escopo (que medição de vazão e quais cálculos)
> vai ser definido com o Luizão — ainda a construir.

## Estrutura
- `index.html` — o app inteiro (HTML + CSS + JS num arquivo só)
- `manifest.webmanifest` — nome, ícones, cores do PWA
- `sw.js` — service worker (cache offline)
- `icon-*.png` — ícones (temporários, copiados do nível; trocar pelos de vazão)

## Publicar no GitHub Pages
1. Crie um repositório novo, público, por exemplo `vazao`.
2. Envie todos os arquivos desta pasta para a raiz do repositório.
3. **Settings → Pages** → *Source*: **Deploy from a branch**, branch `main`, pasta `/ (root)`.
4. Em 1–2 min o endereço aparece: `https://luizaorey.github.io/vazao/`

## Instalar no iPhone
Abra o endereço no **Safari** → Compartilhar → **Adicionar à Tela de Início**.

## Onde ficam os dados salvos
Na memória do próprio navegador, no aparelho. Não sobem para lugar nenhum.
