Análise de Algoritmos e Resolução de Problemas
Este repositório contém soluções para diversos desafios de lógica e programação. Cada solução é apresentada com explicações claras e código Python, oferecendo uma visão de como resolver problemas práticos e teóricos.

Desafios Resolvidos
1. Cálculo de Soma em um Laço
Descrição: O programa calcula o valor final de uma variável SOMA ao somar progressivamente valores inteiros até atingir um limite.

Código:

Utiliza um laço while para calcular a soma dos números inteiros de 1 a 13.
Resultado: 91.
Execução:

python
Copiar código
I = 13
SOMA = 0
K = 0

while K < I:
    K += 1
    SOMA += K
print(SOMA)
2. Verificação de Pertinência à Sequência de Fibonacci
Descrição: O programa verifica se um número informado pertence à sequência de Fibonacci.

Características:

Implementação simples e interativa.
O número é verificado comparando-o aos elementos da sequência gerada dinamicamente.
Execução:

python
Copiar código
def pertence_fibonacci(numero):
    a, b = 0, 1
    while b < numero:
        a, b = b, a + b
    return b == numero
3. Análise de Faturamento Mensal
Descrição: O programa analisa o faturamento diário de uma distribuidora e responde:

Menor faturamento do mês.
Maior faturamento do mês.
Dias com faturamento acima da média mensal.
Características:

Aceita dados nos formatos JSON, CSV e XML.
Calcula valores considerando dias com faturamento positivo.
Execução:

python
Copiar código
import pandas as pd

def calcular_faturamento(df):
    menor_faturamento = df['valor'].min()
    maior_faturamento = df['valor'].max()
    media_faturamento = df['valor'].mean()
    dias_acima_media = len(df[df['valor'] > media_faturamento])
    print(f"Menor: R${menor_faturamento}, Maior: R${maior_faturamento}, Dias acima da média: {dias_acima_media}")
4. Percentual de Representação por Estado
Descrição: O programa calcula a contribuição percentual de cada estado no faturamento total de uma distribuidora.

Características:

Simples e direto.
Utiliza um dicionário para calcular os percentuais.
Execução:

python
Copiar código
faturamento = {
    'SP': 67836.43,
    'RJ': 36678.66,
    'MG': 29229.88,
    'ES': 27165.48,
    'Outros': 19849.53
}
5. Inversão de String
Descrição: O programa recebe uma string e retorna sua versão invertida.

Execução:

python
Copiar código
def inverter_string_iterativo(string_original):
    return string_original[::-1]
Como Executar
Clone o repositório:
bash
Copiar código
git clone https://github.com/seu-usuario/seu-repositorio.git
Instale as dependências (se necessário).
Execute os scripts desejados:
bash
Copiar código
python desafio_fibonacci.py
Tecnologias Utilizadas
Python 3.9+
Bibliotecas: pandas, xml.etree.ElementTree
