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

---

## 📋 Briefing — responder ao abrir a sessão nova (pra construir o app)

Quando o Luizão abrir a sessão nova nesta pasta, é só responder estas perguntas que o
app sai do jeito certo (o Claude usa isto como ponto de partida):

1. **Tipo de medição de vazão** — qual(is)?
   - [ ] Placa de orifício / pressão diferencial (ΔP)
   - [ ] Coriolis
   - [ ] Turbina
   - [ ] Ultrassônico
   - [ ] Vortex
   - [ ] Rotâmetro / área variável
   - [ ] Pitot / Annubar · V-cone
   - [ ] Outro: __________

2. **O que o app precisa CALCULAR?** (ex.: vazão a partir do ΔP; dimensionar a placa /
   furo (β); faixa do transmissor 4–20 mA; converter unidades…)
   - __________

3. **Entradas que o técnico tem em campo** (ex.: ΔP, diâmetro da tubulação D, diâmetro do
   furo d (ou β), densidade/temperatura/pressão, tipo de fluido, unidade do Tx…)
   - __________

4. **Saídas desejadas** (ex.: vazão mássica (kg/h) e/ou volumétrica (m³/h, L/min),
   LRV/URV/span, sinal em mA…) e **unidades** padrão.
   - __________

5. **Norma/padrão** a seguir? (ex.: ISO 5167 p/ placa de orifício, AGA 3, etc.) ou "tanto faz".
   - __________

6. **Precisa de desenho/esquema na tela?** (como o arranjo do app de nível) — sim/não e o quê.
   - __________

7. **Salvar pontos/medições** no aparelho (como os "vasos salvos" do nível)? — sim/não.
   - __________

8. **Nome e ícone** do app (por enquanto chama "Vazão" e usa ícone provisório do nível).
   - __________

> Dica: não precisa responder tudo de uma vez — pode ir conversando. O Claude pergunta o
> que faltar conforme for construindo.
