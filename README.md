# Machine Learning com Pyspark

## Sobre o respositório

Este repositório contém 4 projetos de Machine Learning com Pyspark. Um destes projetos é uma aplicação de Regressão Linear. Há dois projetos de Classificação, um utilizando Regressão Logística e outro Random Forest. Por fim, tem-se uma aplicação de Clusterização.

Esses projetos fazem parte do curso "Spark and Python for Big Data with PySpark" da Udemy.

## Regressão Linear - Estimando o número de tripulantes de um navio

Neste projeto (desenvolvido no notebook "linear_regression_pyspark.ipynb")temos um conjunto de dados com informações sobre navios de Cruzeiro e o nosso objetivo é desenvolver uma análise capaz de prever a quantidade de membros da tripulação necessária em cada situação.

Os dados apresentam colunas com as seguintes informações:
 
 - Nome do navio
 
 - Nome da companhia
 
 - Idade do navio 
 
 - Capacidade de carregamento (Tonnage)
 
 - N. de passegeiros
 
 - Comprimento
 
 - Cabines
 
 - Densidade de passageiros
 
 - Tripulação

![correlation](https://user-images.githubusercontent.com/88217999/168405819-bf1e257c-fa3d-47fb-9a3e-413361925d9b.png)

O número de tripulantes é fortemente correlacionado com as variáveis: "Tonnage", "passengers", "length" e "cabins". Isso faz com que o modelo de regressão linear forneça bons resultados.

## Regressão Logística - Previsão de churn de clientes

O objetivo desse projeto (desenvolvido no notebook "logistic_regression_pyspark.ipynb") é utilizar informações sobre clientes de uma empresa para identificar os clientes mais propensos ao churn (cancelamento). Essa análise permite que a empresa direcione gerentes para tais clientes e não de forma aleatória. 

As informações sobre os clientes são as seguintes:
 
 - Nome 
 - Idade
 - Compra total
 - Gerente de conta (se possuí ou não possui)
 - Anos (tempo como cliente)
 - N. de sites que utilizam o serviço
 - Data que o último contato foi integrado ("Onboard" date)
 - Endereço do cliente
 - Nome da empresa do cliente
 - Churn (Sim ou Não)

O modelo de Regressão Logística ajustado aos dados apresenta uma área sob a curva ROC de 0.75. 

## Random Forest - Identificando o conservante que leva alguns lotes da ração de uma empresa estragarem  

Alguns lotes das rações para cachorro de uma empresa têm estragado precocemente e aparentemente um dos conservantes usados pode ser a causa. Na composição da ração são utilizados 4 conservantes, chamados de A, B, C, e D, e as quantidades desses podem variar nos diferentes lotes.  

A base de dados da empresa contém informações sobre as quantidades dos conservantes utilizados em cada lote e indica se o lote estragou ou não. 

O objetivo dessa análise é utilizar técnicas de Machine Learning para prever os lotes que irão estragar e pelo resultado da modelagem identificar o conservante que está relacionado com o apodrecimento dos lotes.

O algorítmo Random Forest foi utilizado na classificação e o principal componente na determinação do apodrecimento da ração foi o conservante C.
