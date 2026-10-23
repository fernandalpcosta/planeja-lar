# Planeja Lar

Simulador para planejar a independência financeira de uma família no Brasil: parte da situação de hoje e desenha um plano para viver de renda, com filhos em escola particular, no litoral ou interior de São Paulo.

> ⚠️ **Aviso:** as projeções e recomendações deste app são simulações hipotéticas e não garantem nenhum resultado. Não são recomendação de investimento. Veja o [aviso legal](#aviso-legal).

É uma única página HTML, sem build e sem servidor. Basta abrir o `index.html` no navegador ou publicar com GitHub Pages.

## O que você informa

1. **Situação hoje:** idades, vínculo de cada um (CLT, PJ, autônomo ou servidor), renda líquida do casal, gastos, financiamento, patrimônio, reserva, dívidas e quanto investe por mês.
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

Para quem é PJ ou autônomo, o plano pede reserva de 12 meses, alerta que o INSS e a licença-maternidade seguem o pró-labore e indica seguros para proteger a renda.

## Como a conta funciona

Tudo é calculado em reais de hoje, já descontada a inflação.

- **Meta** = custo mensal do casal × 12 ÷ taxa de retirada segura + valor presente do custo dos filhos depois da data de viver de renda + parcelas restantes do financiamento − valor presente do INSS.
- **Projeção:** a cada ano, o patrimônio rende a taxa real e recebe a parte da sobra (renda − gastos − filhos − financiamento) que vocês investem hoje.
- **Custo dos filhos:** custo extra mensal até os 17 anos, mensalidade escolar × 13 por fase (infantil, fundamental, médio) e 5 anos de faculdade.

Os dados ficam salvos apenas no navegador de quem usa (localStorage).

## Aviso legal

- **Simulação hipotética.** Os números são estimativas feitas a partir dos dados informados e de premissas simplificadas: rendimento, inflação, custos de cidades e escolas, regras de impostos e do INSS. A realidade vai ser diferente.
- **Sem garantia.** Rentabilidade passada não garante rentabilidade futura. Todo investimento tem risco, inclusive de perda. Nada aqui garante que a meta será atingida.
- **Não é recomendação.** O plano de ação e a sugestão de carteira têm caráter educativo e genérico. Não são recomendação, oferta ou consultoria de investimento, contábil, tributária, jurídica ou previdenciária, e não consideram o perfil de investidor (suitability) de quem usa.
- **Regras mudam.** Leis de impostos, regras do INSS e produtos financeiros podem mudar. Confira as informações nas fontes oficiais.
- **Antes de decidir**, procure profissionais habilitados: um planejador financeiro certificado (CFP), um consultor de valores mobiliários registrado na CVM e um contador.
- **Responsabilidade.** As decisões tomadas com base neste app são de responsabilidade de quem o usa. Os autores não se responsabilizam por perdas ou danos decorrentes do uso dessas informações.
- **Privacidade.** Os dados digitados ficam só no navegador de quem usa e não são enviados a nenhum servidor.
