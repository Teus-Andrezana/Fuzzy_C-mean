# Fuzzy_C-mean
Este repositório contém uma implementação do algoritmo de agrupamento desenvolvida do zero em Python, sem o uso de bibliotecas de aprendizado de máquina pré-construídas para o cálculo do modelo. 

O projeto foi validado inicialmente utilizando o clássico Iris Dataset, mas a lógica foi estruturada de forma genérica para ser reaproveitada em qualquer outro conjunto de dados numéricos multidimensionais.

---

## Funcionalidades

Implementação: Toda a lógica matemática — desde a inicialização da matriz de pertinência, cálculo dos centroides, até a atualização iterativa e normalização — foi codificada passo a passo.
Modelo Reutilizável: Código desacoplado do dataset original, permitindo que você altere o arquivo de entrada e configure o número de clusters desejado.

---

## Como Funciona o Algoritmo

O Fuzzy C-Means difere do K-Means tradicional, pois permite que um ponto de dado pertença a mais de um cluster com diferentes graus de pertinência (valores entre 0 e 1). 

O processo segue o fluxo clássico:
1. Inicialização: Criação da matriz de pertinência $U$ com valores aleatórios normalizados.
2. Cálculo dos Centroides: Determinação do centro de cada cluster com base nos graus de pertinência atuais.
3. Atualização da Matriz: Recálculo das distâncias e atualização dos graus de pertinência dos pontos em relação aos novos centroides.
4. Critério de Parada: Iteração contínua via laço de repetição até que a variação entre as matrizes $U$ de duas iterações consecutivas seja menor que um limiar predefinido.

---

## Como Reutilizar

Para aplicar este algoritmo no seu próprio conjunto de dados, certifique-se de que seus dados estão em formato numérico e siga a estrutura principal do script:

1. Substitua o carregamento do `Iris dataset` pelo seu arquivo (ex: CSV ou matriz NumPy).
2. Configure o número de clusters e o fator de fuzzificação.
3. Execute o script principal.
