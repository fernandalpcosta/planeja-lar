# Planeja Lar

Simulador de planejamento financeiro pessoal. Você escolhe o estilo de vida dos sonhos, conta onde está hoje e o app responde:

- **Quanto minha carreira precisa evoluir** para chegar lá no prazo, considerando reajustes, promoções e grandes saltos, inclusive para quem está sem emprego.
- **Onde colocar o meu dinheiro** para garantir o sonho.
- **O que fazer a partir deste mês.**

> ⚠️ **Aviso:** as projeções e recomendações deste app são simulações hipotéticas e não garantem nenhum resultado. Não são recomendação de investimento. Veja o [aviso legal](#aviso-legal).

É uma única página HTML, sem build e sem servidor. Basta abrir o `index.html` no navegador ou publicar com GitHub Pages.

## O que você informa

1. **O sonho:** 11 estilos de vida em cartões (Minimalista, Essencial, Interior tranquilo, Sítio ou chácara, Vida no litoral, Confortável, Cidade grande, Viajante, Nômade digital, Morar em Portugal, Alto padrão) ou um personalizado. Dá para somar extras (filho, pet, ajudar os pais, carro novo, viagem internacional, hobby, casa de temporada…), escolher entre comprar a casa, já ter a casa ou morar de aluguel, e definir em quantos anos quer viver de renda.
2. **Você hoje:** idade, situação de trabalho (CLT, servidor, PJ, empreendedor ou sem emprego), renda, gastos, viagens, patrimônio, reserva, dívidas e quanto da sobra você investe. Sem emprego, o primeiro degrau da carreira vira o primeiro emprego: em quantos meses você consegue e com que salário.
3. **Carreira:** reajuste anual acima da inflação, quanto de cada aumento vira gasto e os saltos que você planeja (promoção, troca de empresa, virar gestor, especialização, mudar de área, abrir empresa, trabalhar para fora), cada um com o ano e a nova renda em reais. O app mostra quanto cada salto representa de aumento.
4. **Premissas:** perfil de investidor, rendimento real, retirada segura, oscilação da carteira e INSS.

Cada campo tem um botão **i** com uma explicação simples.

## O que o app devolve

- **Veredito:** quanto do sonho o seu plano alcança.
- **Quanto sua carreira precisa evoluir:** os caminhos para fechar a conta.
  - **Salário-alvo:** quanto o primeiro emprego (ou um emprego a partir de hoje) precisa pagar para chegar ao sonho só com reajustes.
  - **Só com aumentos anuais:** o crescimento de renda necessário por ano.
  - **Um grande salto:** qual nova renda um salto no ano que você escolher precisa trazer.
  - **O seu plano:** quanto do sonho os seus saltos planejados alcançam.
  - Tudo traduzido em linguagem de carreira ("equivale a uma promoção de 20% a cada 3 anos"), com gráfico e marcos de renda ano a ano.
- **Onde colocar o seu dinheiro:** para onde vai cada real do aporte mensal, em ordem (dívidas, reserva de emergência, caixa de viagens, educação do filho, independência), e a carteira de longo prazo conforme o perfil e o prazo.
- **Caminho do patrimônio**, **plano de ação**, **outras alavancas** (investir mais, adiar a data, sonho que cabe no plano, cartão que já cabe) e **tabela ano a ano**.

## Compartilhar um plano

O botão **Compartilhar plano** gera um link protegido por senha:

1. Crie uma senha de pelo menos 8 caracteres e clique em **Gerar link**.
2. Envie o link para a outra pessoa e passe a senha por outro caminho (pessoalmente ou numa ligação).
3. Quem abrir o link digita a senha e vê o plano. Ela recebe uma cópia: o que mudar fica só no navegador dela.

O link guarda o plano como estava na hora. Se algo mudar, gere um link novo.

**Como funciona a proteção:** o plano é criptografado no navegador com AES-256-GCM, usando uma chave derivada da senha (PBKDF2, 250 mil iterações). Os dados vão depois do `#` no link, parte que o navegador nunca envia ao servidor. Nem o GitHub nem ninguém sem a senha consegue ler o plano. Quem tiver o link e a senha consegue, então guarde os dois com cuidado.

## Como a conta funciona

Tudo é calculado mês a mês, em reais de hoje, já descontada a inflação.

- **Meta** = custo mensal do sonho × 12 ÷ taxa de retirada segura + preço da casa (se for comprar) + valor presente do custo restante do filho − valor presente do INSS.
- **Renda:** parte da renda atual (ou do salário do primeiro emprego), muda para a nova renda em cada salto de carreira e cresce pelo reajuste anual desde o último salto.
- **Projeção:** a cada mês, a sobra (renda − gastos − viagens − filho − a parte dos aumentos que vira gasto) é investida no percentual informado. Se faltar dinheiro, ele sai do patrimônio. O patrimônio rende a taxa real.
- **Carreira necessária:** o app busca o salário inicial, o crescimento anual ou a nova renda do salto que faz a projeção alcançar a meta, mantendo o mesmo hábito de investir.
- **Chance de chegar lá:** simulação com anos bons e ruins de mercado.

Os dados ficam salvos apenas no navegador de quem usa.

## Aviso legal

- **Simulação hipotética.** Os números são estimativas feitas a partir dos dados informados e de premissas simplificadas: rendimento, inflação, custos de cidades e escolas, regras de impostos e do INSS. A realidade vai ser diferente.
- **Sem garantia.** Rentabilidade passada não garante rentabilidade futura. Todo investimento tem risco, inclusive de perda. Nada aqui garante que a meta será atingida.
- **Não é recomendação.** O plano de ação e a sugestão de carteira têm caráter educativo e genérico. Não são recomendação, oferta ou consultoria de investimento, contábil, tributária, jurídica ou previdenciária, e não consideram o perfil de investidor (suitability) de quem usa.
- **Regras mudam.** Leis de impostos, regras do INSS e produtos financeiros podem mudar. Confira as informações nas fontes oficiais.
- **Antes de decidir**, procure profissionais habilitados: um planejador financeiro certificado (CFP), um consultor de valores mobiliários registrado na CVM e um contador.
- **Responsabilidade.** As decisões tomadas com base neste app são de responsabilidade de quem o usa. Os autores não se responsabilizam por perdas ou danos decorrentes do uso dessas informações.
- **Privacidade.** Os dados digitados ficam só no navegador de quem usa e não são enviados a nenhum servidor. Links de compartilhamento levam os dados criptografados com a senha escolhida.
