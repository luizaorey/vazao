# Conceito do app de Vazão (rascunho — a confirmar com o Luizão)

> Origem: foto de um cálculo à mão feito em campo (2026-10-15), medindo num equipamento
> com **placa de orifício**.

## Ideia central
Ferramenta de campo (PWA, igual à Régua de Nível): o técnico **joga o range** e o app
monta **na hora uma tabela** relacionando o que aparece **no campo (ΔP)** com o que o
operador vê **no painel (vazão)** — porque com placa de orifício a vazão é proporcional à
**raiz quadrada do ΔP**, então precisa da **extração de raiz quadrada**.

## Fórmula (relação ΔP ↔ vazão)
    Vazão% = 10 · √(ΔP%)        (equivalente a 100 · √(ΔP%/100))

Pontos padrão:

| ΔP% (campo) | Vazão% (painel) |
|------------:|----------------:|
| 0           | 0               |
| 25          | 50,0            |
| 50          | 70,7            |
| 75          | 86,6            |
| 100         | 100             |

(No papel: 70,1 e 86,3 — arredondamento manual; correto 70,7 e 86,6.)

## Do papel (interpretação)
- Coluna esquerda: ΔP% (0,25,50,75,100) e o resultado 10·√ΔP% = vazão%.
- Coluna direita (0 / 312,5 / 625 / 937,5 / 1250): parece ΔP mapeado LINEARMENTE no range 0–1250.
- Bloco "Painel" (0→0%, 1200→25%, 2400→50% [circulado], 3600→75%, 4800→100%): range 0–4800 linear.
  → provável segundo range (talvez a vazão em unidade de engenharia, ou o range do painel).

## Perguntas em aberto (CONFIRMAR antes de construir)
1. O range 0–1250 é a VAZÃO (painel)? E o 0–4800 é o quê (outro exemplo? range do ΔP/transmissor?).
2. Onde a raiz é extraída: transmissor manda ΔP linear e o painel/DCS faz a raiz? (define qual
   lado é "campo" e qual é "painel").
3. Quer colunas de mA (4–20) e/ou % além da unidade de engenharia?
4. Unidade do range (m³/h, t/h, kg/h, L/min…)? Passos da tabela (0/25/50/75/100 ou de 10 em 10%)?
5. Além da tabela fixa, quer um "modo calculadora" (digita um valor de campo e vê o convertido)?
6. Salvar pontos/tags no aparelho (como os "vasos salvos" do nível)?
