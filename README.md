# Icecream Sales Prediction

Este projeto tem como objetivo analisar a relação entre as vendas de sorvetes e as temperaturas registradas. Utilizando Machine Learning, aplicamos um modelo preditivo para estimar o volume de vendas com base na temperatura.

## Dataset

O arquivo `icecream_sales.csv` contém os seguintes campos:

- **Date**: Data da observação.
- **Temperature_C**: Temperatura registrada no dia.
- **IceCream_Sales**: Quantidade de sorvetes vendidos no dia.

## Treinamento do Modelo usando Azure Machine Learning Designer

Para treinar o modelo preditivo utilizando o Azure Machine Learning Designer, siga os passos abaixo:

### 1. Acesse o Azure Machine Learning Studio

Entre na sua conta do Azure e acesse o **Azure Machine Learning Studio**.

### 2. Crie um novo pipeline no Designer

No menu lateral, selecione **Designer** e clique em **+ Criar novo pipeline**.

### 3. Importe os dados

Arraste o componente **Import Data** e configure para carregar o dataset `icecream_sales.csv` da pasta `input/`.

### 4. Pré-processamento dos dados

- Utilize **Select Columns in Dataset** para selecionar as colunas `Temperature_C` e `IceCream_Sales`.

### 5. Divisão dos dados

Adicione o componente **Split Data** e configure para dividir os dados em **80% para treino** e **20% para teste**.

### 6. Escolha um modelo de regressão

- Arraste o componente **Train Model** e selecione um modelo de **Regressão Linear**.
- Conecte o **Train Model** aos dados de treino.

### 7. Avaliação do modelo

- Utilize o componente **Score Model** para testar o modelo.
- Conecte o **Evaluate Model** para verificar métricas como:
  - **Erro Médio Absoluto (MAE)**
  - **Erro Quadrático Médio (MSE)**

### 8. Publicação do modelo

Após validar os resultados, publique o modelo como um **endpoint** para previsões futuras.