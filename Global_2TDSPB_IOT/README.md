
# Localização de Postos de Carregamento com KNN

Este projeto utiliza o modelo K-Nearest Neighbors (KNN) para localizar os postos de carregamento mais próximos, com base na latitude e longitude fornecidas pelo usuário.

## Etapas do Projeto

1. **Carregar os Dados**: O código carrega o arquivo CSV contendo informações de 20 postos de carregamento, incluindo localizações (latitude e longitude) e detalhes adicionais como capacidade de carga.

2. **Preparar os Dados**: Apenas as colunas de latitude e longitude são usadas para o treinamento do modelo.

3. **Treinar o Modelo KNN**: O modelo KNN é configurado para calcular distâncias geográficas usando a métrica de distância haversine, que é ideal para coordenadas geográficas.

4. **Fornecer a Localização do Usuário**: Um exemplo de localização (São Paulo) é fornecido como ponto de partida. Esta localização pode ser substituída por dados dinâmicos, como coordenadas GPS.

5. **Obter os Resultados**: O modelo retorna os 3 postos mais próximos com suas distâncias e capacidades de carga.

## Exemplo de Saída

Após executar o código, a saída será algo como:

```
Postos de carregamento mais próximos:
1. ChargePoint A - Rua A, 123 (São Paulo, SP)
   Distância: 0.00 km - Capacidade: 50 kW
2. ChargePoint Q - Rua Q, 112 (Taubaté, SP)
   Distância: 120.00 km - Capacidade: 120 kW
3. ChargePoint M - Rua M, 777 (Manaus, AM)
   Distância: 320.00 km - Capacidade: 85 kW
```

## Dependências

- Python 3.x
- Pandas
- NumPy
- scikit-learn

Para instalar as dependências, execute:
```
pip install pandas numpy scikit-learn
```

## Como Usar

1. Baixe o arquivo `locais_carregamento_expandido.csv`.
2. Coloque o arquivo na mesma pasta do código Python.
3. Execute o código fornecido.

Você pode substituir a localização do usuário na variável `user_location` para personalizar os resultados.
