# Estratégia de Negociação com Médias Móveis e Filtro de Vela #

Este repositório contém um código que implementa uma estratégia de negociação para o mercado financeiro. A estratégia utiliza médias móveis de 9, 20 e 50 períodos para identificar sinais de compra e venda. Além disso, inclui um filtro de vela que garante que as negociações só ocorram se a vela atual passar pela média de 20 períodos, mas sem tocá-la.

## Visão Geral

A estratégia é implementada em linguagem NTSL (NinjaTrader Scripting Language) e é projetada para ser utilizada na plataforma NinjaTrader para negociação em diversos mercados financeiros.

## Funcionamento

A estratégia é baseada em várias condições que devem ser atendidas para acionar sinais de compra e venda:

### Condições de Compra

Para acionar um sinal de compra, as seguintes condições devem ser atendidas:

- A média móvel de 9 períodos deve ser maior que a média móvel de 20 períodos.
- A média móvel de 20 períodos deve ser maior que a média móvel de 50 períodos.
- O preço mínimo (Low) da vela atual deve estar abaixo da média móvel de 20 períodos.
- O preço máximo (High) da vela atual deve estar acima da média móvel de 20 períodos.
- O preço de abertura (Open) da vela atual deve ser maior ou igual à média móvel de 20 períodos.
- O preço de fechamento (Close) da vela atual deve ser maior que a média móvel de 9 períodos.
- A vela atual não deve tocar a média móvel de 20 períodos.
- O corpo da vela atual deve ser maior que 75% do tamanho total da vela.

Se todas essas condições forem atendidas, a estratégia acionará um sinal de compra.

### Condições de Venda

Para acionar um sinal de venda, as seguintes condições devem ser atendidas:

- A média móvel de 9 períodos deve ser menor que a média móvel de 20 períodos.
- A média móvel de 20 períodos deve ser menor que a média móvel de 50 períodos.
- O preço mínimo (Low) da vela atual deve estar abaixo da média móvel de 20 períodos.
- O preço máximo (High) da vela atual deve estar acima da média móvel de 20 períodos.
- O preço de abertura (Open) da vela atual deve ser maior ou igual à média móvel de 20 períodos.
- O preço de fechamento (Close) da vela atual deve ser menor que a média móvel de 9 períodos.
- A vela atual não deve tocar a média móvel de 20 períodos.
- O corpo da vela atual deve ser maior que 75% do tamanho total da vela.

Se todas essas condições forem atendidas, a estratégia acionará um sinal de venda.

## Uso

Para utilizar esta estratégia, você precisará da plataforma NinjaTrader e inserir o código no editor de scripts. Certifique-se de configurar os parâmetros de médias móveis de acordo com suas preferências antes de utilizar a estratégia em um ambiente de negociação real.

## Nota Importante

Lembre-se de que esta estratégia é apenas uma implementação de exemplo e não deve ser considerada como um conselho de investimento. Antes de utilizar qualquer estratégia de negociação em um ambiente real, é altamente recomendável conduzir uma análise completa, considerar o gerenciamento de riscos e, se necessário, buscar aconselhamento de um profissional financeiro.

**Aviso de Risco:** Negociar em mercados financeiros envolve riscos significativos e pode resultar na perda de capital. Certifique-se de entender completamente os riscos antes de iniciar qualquer negociação.

## Contribuições

Contribuições são bem-vindas! Se você tiver sugestões de melhorias ou correções para este código, sinta-se à vontade para criar um pull request.

## Licença

Este código é fornecido sob a [Licença MIT](LICENSE), o que significa que você pode usá-lo livremente em seus próprios projetos, mas sem garantias de qualquer tipo.
