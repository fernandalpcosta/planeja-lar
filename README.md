# Planeja Lar

Simulador para planejar a independência financeira de uma família no Brasil: parte da situação de hoje e desenha um plano para viver de renda, com filhos em escola particular, no litoral ou interior de São Paulo.

É uma única página HTML, sem build e sem servidor. Basta abrir o `index.html` no navegador ou publicar com GitHub Pages.

## O que você informa

1. **Situação hoje:** idades, renda líquida do casal, gastos, financiamento, patrimônio, reserva, dívidas e quanto investe por mês.
2. **Filhos:** ano de nascimento, escola (pública, particular ou bilíngue) e faculdade.
3. **O sonho:** cidade de destino (com custos de referência editáveis), em quantos anos quer viver de renda e se terá casa própria ou aluguel.
4. **Premissas:** rendimento real, taxa de retirada segura, aumento real da renda e INSS.

## O que o app devolve

- Meta de patrimônio e quanto dela o ritmo atual alcança
- Aporte mensal necessário, antes e depois da chegada dos filhos
- Chance de sucesso (simulação Monte Carlo)
- Gráfico do patrimônio com os eventos da família
- Plano de ação em ordem de prioridade
- Sugestão de carteira conforme o prazo
- Alavancas: aportar mais, adiar, reduzir o custo de vida ou buscar mais rendimento
- Tabela ano a ano

## Como a conta funciona

Tudo é calculado em reais de hoje, já descontada a inflação.

- **Meta** = custo mensal do casal × 12 ÷ taxa de retirada segura + valor presente do custo dos filhos depois da data de viver de renda + parcelas restantes do financiamento − valor presente do INSS.
- **Projeção:** a cada ano, o patrimônio rende a taxa real e recebe a parte da sobra (renda − gastos − filhos − financiamento) que vocês investem hoje.
- **Custo dos filhos:** custo extra mensal até os 17 anos, mensalidade escolar × 13 por fase (infantil, fundamental, médio) e 5 anos de faculdade.

Os dados ficam salvos apenas no navegador de quem usa (localStorage).

> Estudo educativo com premissas simplificadas. Não é recomendação de investimento.
