📝 Análise de Churn - TelecomX
Este projeto apresenta uma análise profunda sobre o fenômeno de evasão de clientes (Churn) na TelecomX. O objetivo é entender por que os clientes estão cancelando seus serviços e fornecer recomendações baseadas em dados para aumentar a retenção.

📌 Objetivos
Identificar padrões de comportamento de cancelamento.

Traçar perfis de clientes propensos à evasão.

Detectar falhas em serviços e condições contratuais.

Propor ações estratégicas para fidelização.

🛠️ O Fluxo de Dados (Pipeline)
O projeto foi estruturado seguindo o fluxo ETL e EDA:

1. Extração e Estruturação
Os dados foram consumidos de uma API em formato JSON.

Normalização: Utilização do json_normalize para transformar estruturas aninhadas em tabelas relacionais.

2. Limpeza e Sanetização
Auditoria: Inspeção de valores nulos, duplicados e caracteres especiais (?).

Filtragem Crítica: Remoção de registros sem a confirmação de Churn para evitar ruídos na análise.

3. Engenharia de Dados (Tratativa)
Limpeza de Labels: Padronização dos nomes das colunas após o aninhamento JSON.

Consistência Financeira: Recálculo do faturamento total (Tenure × MonthlyCharges) para garantir a integridade dos valores.

Codificação: Transformação de variáveis categóricas ("Yes"/"No") em binárias (1/0).

📊 Insights Principais (EDA)
Durante a análise exploratória, cruzamos dados financeiros e comportamentais, resultando nas seguintes descobertas:

Ticket Médio de Alto Risco: Clientes que entram em Churn possuem, em média, faturas mais caras que clientes retidos.

O Problema da Fibra: Usuários de Fibra Óptica evadem mais, possivelmente pela falta de serviços agregados de segurança e suporte.

Contratos Frágeis: O modelo Month-to-month (mensal) é o principal canal de saída de clientes.

🚀 Recomendações Estratégicas
Downselling Preventivo: Oferecer planos mais baratos para clientes de alto valor com sinais de insatisfação.

Combos de Suporte: Incentivar a contratação de pacotes de suporte técnico e segurança para estabilizar a experiência na Fibra Óptica.

Fidelização Contratual: Criar incentivos financeiros para migração de planos mensais para anuais.

📂 Como executar o projeto
Clone o repositório:

Bash
git clone https://github.com/seu-usuario/telecomx-churn-analysis.git
Instale as dependências:

Bash
pip install pandas plotly matplotlib seaborn
Abra o arquivo .ipynb no Google Colab ou Jupyter Notebook.

Autor
Lucas Gabriel Marques Rodrigues - https://www.linkedin.com/in/lucas-gabriel-marques-rodrigues/
