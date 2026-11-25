# Desafio 02 — Análise Exploratória: E-commerce Sales Performance

> Análise de dados de vendas de um e-commerce, investigando receita, lucro e comportamento de compra por categoria.

**Equipe:** Mário Henrique Bezerra Rocha (Substitua pelos seus nomes/nomes dos colegas)

## Perguntas
1. Quais categorias de produtos geram mais receita (Sales) e mais lucro (Profit)?
2. Existe relação entre a quantidade vendida (Quantity) e o lucro (Profit) por pedido?
3. Produtos da categoria "Electronics" têm um lucro médio por pedido maior do que produtos da categoria "Accessories"? (teste de hipótese)

## Principais conclusões
*(Nota: Substitua os textos abaixo pelos resultados reais que os seus gráficos e testes mostrarem no notebook)*
- A categoria **Electronics** lidera tanto em volume de receita quanto em lucro total gerado, impulsionada por produtos de maior valor agregado (como Laptops e Tablets).
- Foi observada uma correlação positiva fraca entre a quantidade de itens comprados e o lucro final do pedido, indicando que comprar mais volumes não garante necessariamente uma margem de lucro proporcionalmente maior.
- **Teste de Hipótese:** O teste t de Student revelou um valor-p menor que 0,05 (ex: p = 0.002). Isso significa que rejeitamos a hipótese nula; portanto, há evidências estatísticas de que os produtos da categoria Electronics realmente possuem um lucro médio por pedido significativamente maior do que os da categoria Accessories.

## Tratamento de Dados
A partir da base original, realizamos a limpeza e o enriquecimento dos dados no Python:
- Conversão da coluna de data (`Order Date`) para o formato datetime.
- Criação de novas colunas para facilitar a análise temporal: `Year`, `Month`, `Day_of_Week` e `Quarter`.
- Criação de métricas de negócio: `Unit_Price` (preço unitário) e `Profit_Margin_%` (margem de lucro percentual).

## Arquivos
- `analise_ecommerce.ipynb`: notebook com a análise completa, gráficos e teste de hipótese.
- `dados/ecommerce_sales_data_original.csv`: base original, sem alterações.
- `dados/ecommerce_sales_data_tratado.csv`: base após a conversão de datas e criação das novas colunas.
- `requirements.txt`: bibliotecas necessárias para rodar o notebook.

## Como rodar

### Só para ver
Clique em `analise_ecommerce.ipynb` aqui no GitHub. O notebook aparece com todas as tabelas e gráficos renderizados, sem precisar instalar nada.

### No seu computador
Você precisa do [Python](https://www.python.org/downloads/) 3.10 ou mais novo instalado.

1. Baixe o repositório: botão **Code → Download ZIP** (e descompacte), ou abra o terminal e clone:
   ```bash
   git clone https://github.com/mariohenrique2908-beep/desafio-2-trilhas.git
2. Abra o terminal dentro da pasta do projeto e instale as bibliotecas necessárias:
  pip install -r requirements.txt

3. Abra o Jupyter Lab:
   python -m jupyter lab

4. No navegador, clique em analise_ecommerce.ipynb e use Run → Run All Cells.
Aviso: O notebook precisa estar na mesma pasta que a pasta dados/. Se mover o arquivo .ipynb sozinho, ele não encontrará a base de dados.

Google Colab (sem instalar nada)

Vá em colab.research.google.com.
Escolha a aba GitHub, cole o link do seu repositório e abra o notebook.
Use Ambiente de execução → Executar tudo.
(Lembre-se de subir os arquivos CSV para o Colab ou descomentar a célula de código que baixa os dados do próprio GitHub, caso o professor decida rodar por lá).
