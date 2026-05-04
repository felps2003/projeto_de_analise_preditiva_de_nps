📊 Case: NPS Preditivo em E-commerce
Projeto de Análise de Dados e Estratégia de Experiência do Cliente

Este projeto foi desenvolvido como parte do Tech Challenge (Fase 1). O objetivo central é transformar a gestão de satisfação de um e-commerce, saindo de uma postura reativa (esperar a nota do cliente) para uma proativa (antecipar a insatisfação com base em dados operacionais).

🎯 O Problema de Negócio
Atualmente, o NPS é coletado apenas após o encerramento da jornada de compra. Isso gera um "ponto cego": a empresa só descobre que o cliente está insatisfeito quando o dano à marca já aconteceu.

Objetivo: Identificar quais variáveis operacionais (logística, atendimento, financeiro) mais impactam o NPS e propor uma estratégia para prever potenciais detratores antes mesmo da pesquisa ser enviada.

📁 Estrutura do Repositório
data/: Base de dados contendo indicadores operacionais e notas de NPS.

notebooks/:

analise_eda_nps.ipynb: Análise Exploratória de Dados, limpeza e visualização de correlações.

modelo_preditivo_nps.ipynb: Desenvolvimento do modelo de Machine Learning para predição de comportamento.

models/: Modelos treinados salvos (arquivos .pkl).

PERGUNTAS.txt: Documentação das etapas de entendimento de negócio e respostas teóricas do desafio.

🔍 Principais Insights da Análise (EDA)
Durante a exploração dos dados, identifiquei os seguintes pontos críticos:

Logística como Detrator: O atraso na entrega (delivery_delay_days) é o fator com maior correlação negativa com a nota de satisfação.

Atrito no Atendimento: Clientes que precisam entrar em contato com o suporte mais de 2 vezes têm uma probabilidade 70% maior de se tornarem detratores.

Fator Valor: Curiosamente, o valor do desconto (discount_value) tem um impacto menor no NPS do que a eficiência da entrega, sugerindo que o cliente prioriza o serviço sobre o preço.

🤖 Solução Preditiva
Foi desenvolvido um modelo de Random Forest Classifier para categorizar clientes com risco de baixa satisfação.

Estratégia: O modelo utiliza dados de tentativas de entrega e contatos no SAC para gerar um alerta de "Risco de Detração".

Ação Proativa: Com esses nomes em mãos, o time de Customer Experience pode disparar cupons de desculpas ou priorizar o atendimento antes do produto ser entregue.

🛠️ Tecnologias Utilizadas
Python 3.10+

Pandas & Numpy: Manipulação de dados.

Seaborn & Matplotlib: Visualização de dados.

Scikit-Learn: Modelagem preditiva.

🚀 Como Executar
Clone este repositório.

Instale as dependências:

Bash
pip install pandas seaborn matplotlib scikit-learn
Execute o notebook analise_eda_nps.ipynb para visualizar os insights.
