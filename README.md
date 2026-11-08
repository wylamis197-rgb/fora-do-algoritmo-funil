# FORA DO ALGORITMO — Pós-compra

Este repositório contém **somente as páginas exibidas depois da compra**. A página de vendas fica em outro endereço/projeto e não faz parte deste repositório. O aplicativo de membros também permanece separado em `foraalgoritmo-2`.

## Páginas de pós-compra

- `/obrigado/essencial` — confirmação da compra Essencial e oferta de upgrade por +R$ 10.
- `/downsell` — última oferta de upgrade por +R$ 7,90.
- `/completo-confirmado` — confirmação da compra Completa, com link para o aplicativo.

A raiz `/` não é uma página de vendas e não deve ser usada nos botões dos anúncios ou da Cakto. Use diretamente as rotas acima.

## Checkouts

- Essencial: https://pay.cakto.com.br/5yg4tn3_1291919
- Completo: https://pay.cakto.com.br/5ghcqku_1292155
- Upsell (+R$ 10): https://pay.cakto.com.br/7x3i4sk
- Downsell (+R$ 7,90): ainda precisa ser criado na Cakto.

## Redirecionamentos da Cakto

1. Após pagamento do Essencial: `/obrigado/essencial`.
2. Após pagamento direto do Completo: `/completo-confirmado`.
3. Após pagamento do checkout de Upsell: `/completo-confirmado`.
4. Após pagamento do checkout de Downsell: `/completo-confirmado`.
5. A recusa do Upsell leva a `/downsell`.
6. A recusa do Downsell leva a `https://foraalgoritmo-2.vercel.app/acesso/essencial`.

## Publicação

Projeto estático independente na Vercel, ligado à branch `main`. O arquivo `vercel.json` mantém as rotas amigáveis.

**Atenção:** antes de ativar o Downsell, crie na Cakto um checkout do upgrade por +R$ 7,90 (total R$ 27,80 somando a compra Essencial) e substitua o botão desativado em `downsell/index.html` pelo link gerado.
