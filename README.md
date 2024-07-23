# Aplicativo de Probabilidade de Falhas em Equipamentos

Este aplicativo foi desenvolvido utilizando a biblioteca Streamlit, e tem como objetivo calcular e visualizar a probabilidade de falhas em equipamentos. A seguir, vamos detalhar o funcionamento do código e sua importância.

## Funcionalidades do Aplicativo

### 1. Configurações na Barra Lateral

- **Tipo de Cálculo**: O usuário pode selecionar entre três tipos de cálculos:
  - **Prob. Exata**: Calcula a probabilidade exata de um determinado número de ocorrências.
  - **Menos que**: Calcula a probabilidade acumulada de um número de ocorrências menor ou igual ao valor especificado.
  - **Mais que**: Calcula a probabilidade acumulada de um número de ocorrências maior que o valor especificado.
- **Ocorrência Atual**: Permite ao usuário inserir o número de ocorrências para as quais deseja calcular a probabilidade. O valor pode variar entre 1 e 99, com um valor padrão de 2.
- **Botão de Processar**: Inicia o cálculo e a visualização das probabilidades com base nos parâmetros fornecidos.

### 2. Cálculo e Visualização  

O aplicativo utiliza a distribuição de Poisson para calcular as probabilidades. A distribuição de Poisson é ideal para modelar o número de eventos que ocorrem em um intervalo de tempo fixo.

- Com base no valor de ocorrência fornecido, o aplicativo define um intervalo de valores para calcular as probabilidades.
- Dependendo do tipo de cálculo selecionado, o aplicativo usa as funções `pmf` (função de massa de probabilidade), `cdf` (função de distribuição cumulativa) ou `sf` (função de sobrevivência) da biblioteca `scipy.stats`.
- Os resultados são apresentados em um gráfico de barras, com as probabilidades para cada valor de ocorrência dentro do intervalo definido. As barras são rotuladas com os valores de ocorrência e suas respectivas probabilidades arredondadas.

## Relevância e Importância

A capacidade de calcular e visualizar probabilidades de falhas em equipamentos é extremamente útil em várias áreas, incluindo manutenção preditiva, gestão de riscos e planejamento operacional. Com este aplicativo, os usuários podem:

- **Analisar Riscos**: Determinar a probabilidade de falhas e tomar decisões informadas sobre manutenção e substituição de equipamentos.
- **Planejamento**: Alocar recursos de maneira eficiente, prevenindo paradas inesperadas e minimizando custos operacionais.
- **Monitoramento Contínuo**: Implementar uma abordagem proativa na gestão de equipamentos, aumentando a confiabilidade e a segurança das operações.

Em suma, este aplicativo oferece uma ferramenta poderosa e intuitiva para profissionais que lidam com a manutenção e a gestão de equipamentos, permitindo uma melhor tomada de decisão baseada em dados probabilísticos.

## Exemplo de Uso

- **Seleção de Configurações**: O usuário escolhe o tipo de cálculo desejado (por exemplo, "Prob. Exata") e insere o número de ocorrências (por exemplo, 5).
- **Processamento**: Ao clicar no botão "Processar", o aplicativo calcula e exibe um gráfico de barras mostrando as probabilidades de 3 a 7 ocorrências.
- **Interpretação dos Resultados**: O usuário pode interpretar visualmente as probabilidades e tomar decisões baseadas nos resultados apresentados.
 
​## Distribuição de Poisson

### Definição

A distribuição de Poisson é uma distribuição de probabilidade discreta que expressa a probabilidade de um número dado de eventos ocorrer em um intervalo fixo de tempo ou espaço, se esses eventos ocorrerem com uma taxa média constante e independentemente do tempo desde o último evento.

### Fórmula

A probabilidade de ocorrer exatamente \( k \) eventos em um intervalo é dada por:

\[ P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!} \]


![Imagem](https://media.licdn.com/dms/image/D4D12AQFW3LFuZNjtSw/article-inline_image-shrink_400_744/0/1703546673858?e=1726704000&v=beta&t=OrUCDFIqsZ0SXry819qxpf9Xh9E0PIOo1gfBlWnEQLs)

Onde:
- \( P(X = k) \) é a probabilidade de ocorrer exatamente \( k \) eventos em um intervalo.
- \( \lambda \) é a taxa média de ocorrências (média esperada de eventos por intervalo).
- \( e \) é a base do logaritmo natural (aproximadamente 2.71828).
- \( k \) é o número de eventos.
- \( k! \) é o fatorial de \( k \).

### Propriedades da Distribuição de Poisson

- **Média e Variância**: Para uma distribuição de Poisson com parâmetro \( \lambda \), tanto a média quanto a variância são iguais a \( \lambda \).
- **Independência**: Os eventos são independentes, ou seja, a ocorrência de um evento não afeta a probabilidade de ocorrência de outro evento.
- **Intervalos de Tempo/Área**: A distribuição de Poisson é frequentemente utilizada para modelar o número de eventos em intervalos de tempo ou áreas fixas.

### Aplicações da Distribuição de Poisson

A distribuição de Poisson é amplamente utilizada em várias áreas, incluindo:

- **Engenharia e Manutenção**: Para modelar a probabilidade de falhas em equipamentos ou sistemas.
- **Telecomunicações**: Para modelar o número de chamadas recebidas por uma central telefônica em um determinado período.
- **Saúde Pública**: Para modelar a incidência de doenças raras em uma população.
- **Economia e Finanças**: Para modelar o número de reivindicações de seguros ou eventos de mercado.

### Conclusão

A distribuição de Poisson é uma ferramenta poderosa para modelar e entender a probabilidade de eventos discretos em intervalos fixos. No contexto do aplicativo, ela permite calcular e visualizar a probabilidade de falhas em equipamentos, fornecendo insights valiosos para a manutenção e gestão de riscos.

 
