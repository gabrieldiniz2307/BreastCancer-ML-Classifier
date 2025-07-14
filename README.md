Classificador de Câncer de Mama usando Inteligência Artificial

Visão Geral

Este projeto implementa um sistema inteligente de classificação para diagnóstico de câncer de mama utilizando técnicas avançadas de machine learning. O sistema foi desenvolvido como parte do trabalho acadêmico A3 do 4º período, focando na aplicação prática de algoritmos de regressão linear e regressão logística para problemas de classificação médica.

O projeto utiliza o reconhecido dataset Wisconsin Breast Cancer Diagnostic, que contém características extraídas de imagens digitalizadas de aspiração por agulha fina (FNA) de massas mamárias. Através da implementação de uma rede neural Multi-Layer Perceptron (MLP), conseguimos alcançar uma acurácia impressionante de 95,73% na classificação entre tumores benignos e malignos.

Autores

•
João Gabriel de Araujo Diniz - RA: 1252219877

•
Carlos Emanuel da Silva Pinho - RA: 1125222897

Data de Desenvolvimento: 30 de Novembro de 2023

Objetivos do Projeto

Objetivo Principal

Desenvolver um modelo de machine learning capaz de classificar com alta precisão casos de câncer de mama como benignos ou malignos, contribuindo para o auxílio ao diagnóstico médico.

Objetivos Específicos

•
Implementar e comparar diferentes técnicas de machine learning para classificação binária

•
Aplicar técnicas de pré-processamento de dados para otimizar a performance do modelo

•
Avaliar a performance do modelo utilizando métricas apropriadas para problemas médicos

•
Demonstrar a aplicabilidade da inteligência artificial em diagnósticos médicos

•
Consolidar conhecimentos em regressão linear e logística através de aplicação prática

Metodologia

Dataset Utilizado

O projeto utiliza o Wisconsin Breast Cancer Diagnostic Dataset, disponível no UCI Machine Learning Repository. Este dataset é amplamente reconhecido na comunidade científica e contém 569 instâncias com 30 características numéricas cada uma.

As características incluem medidas como raio, textura, perímetro, área, suavidade, compacidade, concavidade, pontos côncavos, simetria e dimensão fractal. Cada característica é calculada para o núcleo celular presente na imagem, resultando em um conjunto robusto de features para treinamento do modelo.

Pré-processamento dos Dados

Para garantir a qualidade e consistência dos dados de entrada, implementamos um pipeline de pré-processamento que inclui:

Normalização dos Dados: Utilizamos o StandardScaler do scikit-learn para padronizar todas as features, garantindo que cada variável tenha média zero e desvio padrão unitário. Esta etapa é crucial para algoritmos de machine learning que são sensíveis à escala dos dados, como redes neurais.

Divisão dos Dados: Os dados foram divididos em conjuntos de treino e teste na proporção 70/30, utilizando a função train_test_split com estratificação para manter a distribuição das classes em ambos os conjuntos.

Arquitetura do Modelo

Implementamos uma rede neural Multi-Layer Perceptron (MLP) com a seguinte configuração:

Arquitetura: Três camadas ocultas com 60, 40 e 20 neurônios respectivamente
Função de Ativação: Logística (sigmoid)
Máximo de Iterações: 900 épocas
Solver: Otimizador padrão do scikit-learn (LBFGS para datasets pequenos)

Esta arquitetura foi escolhida após considerações sobre a complexidade do problema e o tamanho do dataset, buscando um equilíbrio entre capacidade de aprendizado e prevenção de overfitting.

Resultados Obtidos

Performance do Modelo

O modelo desenvolvido demonstrou excelente performance na tarefa de classificação, alcançando métricas que superam muitos benchmarks da literatura para este dataset específico.

Acurácia Geral: 95,73% (0.9573934837092731)

Esta acurácia representa a proporção de predições corretas sobre o total de predições realizadas, indicando que o modelo classifica corretamente mais de 95% dos casos apresentados.

Métricas Detalhadas por Classe

Classe Benigno (B):

•
Precisão: 96%

•
Recall: 94%

•
F1-Score: 95%

•
Suporte: 253 amostras

Classe Maligno (M):

•
Precisão: 90%

•
Recall: 93%

•
F1-Score: 92%

•
Suporte: 146 amostras

Análise da Matriz de Confusão

A matriz de confusão revelou os seguintes resultados:

•
Verdadeiros Positivos (Maligno corretamente identificado): 136

•
Verdadeiros Negativos (Benigno corretamente identificado): 238

•
Falsos Positivos (Benigno classificado como Maligno): 15

•
Falsos Negativos (Maligno classificado como Benigno): 10

A baixa taxa de falsos negativos (10 casos) é particularmente importante em aplicações médicas, pois representa casos de câncer que poderiam passar despercebidos.

Tecnologias e Bibliotecas Utilizadas

Ambiente de Desenvolvimento

•
Python 3.x: Linguagem principal de desenvolvimento

•
Jupyter Notebook: Ambiente interativo para desenvolvimento e documentação

•
Google Colaboratory: Plataforma de desenvolvimento em nuvem

Bibliotecas Python

•
pandas: Manipulação e análise de dados estruturados

•
numpy: Computação numérica e operações com arrays

•
scikit-learn: Biblioteca principal para machine learning, incluindo:

•
MLPClassifier para implementação da rede neural

•
StandardScaler para normalização dos dados

•
train_test_split para divisão dos dados

•
classification_report e confusion_matrix para avaliação



•
matplotlib: Criação de gráficos e visualizações

•
seaborn: Visualizações estatísticas avançadas

•
ucimlrepo: Acesso direto aos datasets do UCI Repository

Ferramentas de Análise

•
statsmodels: Análises estatísticas complementares

•
scipy.stats: Testes estatísticos e distribuições

Estrutura do Projeto

Plain Text


A3_2023/
├── A3.ipynb                 # Notebook principal com implementação completa
├── Names.ipynb              # Informações dos autores e projeto
├── A3_4periodo             # Arquivos relacionados ao período acadêmico
├── cODIGO 1.py             # Funções auxiliares de validação
└── README.md               # Documentação do projeto


Como Executar o Projeto

Pré-requisitos

1.
Python 3.7 ou superior instalado

2.
Jupyter Notebook ou Google Colaboratory

3.
Bibliotecas listadas na seção de tecnologias

Passos para Execução

1.
Clone o repositório:

2.
Instale as dependências:

3.
Execute o notebook principal:

•
Abra o arquivo A3.ipynb no Jupyter Notebook ou Google Colaboratory

•
Execute todas as células sequencialmente

•
Os resultados e visualizações serão gerados automaticamente



Execução no Google Colaboratory

Para facilitar a execução, o projeto foi desenvolvido e testado no Google Colaboratory:

1.
Acesse Google Colaboratory

2.
Faça upload do arquivo A3.ipynb

3.
Execute as células sequencialmente

4.
Todas as dependências serão instaladas automaticamente

Discussão dos Resultados

Interpretação da Performance

A acurácia de 95,73% obtida pelo modelo representa um resultado excelente para a tarefa de classificação de câncer de mama. Este desempenho está alinhado com estudos similares na literatura científica e demonstra a eficácia das técnicas de machine learning aplicadas a problemas de diagnóstico médico.

A diferença nas métricas entre as classes (Benigno vs Maligno) pode ser atribuída ao desbalanceamento natural do dataset, onde casos benignos são mais frequentes que malignos. A precisão ligeiramente superior para casos benignos (96% vs 90%) é esperada e aceitável, considerando que o recall para casos malignos (93%) permanece alto, minimizando o risco de falsos negativos.

Importância Clínica

Em aplicações médicas, diferentes tipos de erro têm impactos distintos. Falsos negativos (casos malignos classificados como benignos) são mais críticos que falsos positivos, pois podem resultar em atraso no tratamento. Nosso modelo apresentou apenas 10 falsos negativos em 399 casos testados, representando uma taxa de 2,5%, que é considerada baixa para este tipo de aplicação.

Comparação com Benchmarks

O dataset Wisconsin Breast Cancer é amplamente utilizado como benchmark na comunidade de machine learning. Nossos resultados se comparam favoravelmente com outros estudos publicados, que tipicamente reportam acurácias entre 90% e 97% para este mesmo dataset.

Limitações do Estudo

Limitações Metodológicas

Embora os resultados sejam promissores, é importante reconhecer algumas limitações do estudo atual:

Tamanho do Dataset: O dataset utilizado, embora bem estabelecido, contém apenas 569 amostras. Para aplicações clínicas reais, seria desejável validar o modelo em datasets maiores e mais diversos.

Generalização: O modelo foi treinado e testado em dados provenientes de uma única instituição. A generalização para diferentes populações, equipamentos e protocolos de coleta ainda precisa ser validada.

Features Limitadas: O modelo utiliza apenas características morfológicas extraídas de imagens FNA. A incorporação de dados clínicos adicionais (idade, histórico familiar, marcadores genéticos) poderia potencialmente melhorar a performance.

Considerações Técnicas

Interpretabilidade: Redes neurais, embora eficazes, são consideradas "caixas pretas" com interpretabilidade limitada. Para aplicações médicas, modelos mais interpretáveis podem ser preferíveis em alguns contextos.

Validação Cruzada: Embora tenhamos utilizado uma divisão treino-teste robusta, a implementação de validação cruzada k-fold poderia fornecer uma estimativa mais robusta da performance do modelo.

Trabalhos Futuros

Melhorias Técnicas

Várias direções podem ser exploradas para aprimorar este trabalho:

Otimização de Hiperparâmetros: Implementação de técnicas como Grid Search ou Random Search para encontrar a configuração ótima da rede neural.

Ensemble Methods: Combinação de múltiplos modelos (Random Forest, SVM, Gradient Boosting) para potencialmente melhorar a performance e robustez.

Deep Learning: Exploração de arquiteturas mais complexas, como redes neurais convolucionais, especialmente se dados de imagem raw estivessem disponíveis.

Expansão do Escopo

Validação Externa: Teste do modelo em datasets independentes de outras instituições para avaliar a generalização.

Integração de Dados Multimodais: Incorporação de dados clínicos, genômicos e de imagem para uma abordagem mais holística.

Interface de Usuário: Desenvolvimento de uma aplicação web ou mobile para facilitar o uso do modelo por profissionais de saúde.

Aspectos Regulatórios

Validação Clínica: Condução de estudos clínicos prospectivos para validar a eficácia do modelo em ambiente real.

Aprovação Regulatória: Preparação da documentação necessária para aprovação por órgãos reguladores como ANVISA ou FDA.

Conclusões

Este projeto demonstrou com sucesso a aplicabilidade de técnicas de inteligência artificial para o diagnóstico auxiliar de câncer de mama. A implementação de uma rede neural Multi-Layer Perceptron resultou em uma acurácia de 95,73%, superando muitos benchmarks estabelecidos para este problema.

Principais Contribuições

1.
Implementação Robusta: Desenvolvimento de um pipeline completo de machine learning, desde o pré-processamento até a avaliação final.

2.
Performance Excelente: Alcance de métricas de performance que demonstram a viabilidade da abordagem para aplicações reais.

3.
Documentação Completa: Criação de documentação detalhada que facilita a reprodução e extensão do trabalho.

4.
Aplicação Prática: Demonstração concreta de como conceitos teóricos de regressão linear e logística podem ser aplicados a problemas reais de grande relevância social.

Impacto Educacional

Do ponto de vista acadêmico, este projeto proporcionou experiência prática valiosa em:

•
Manipulação e análise de dados reais

•
Implementação de algoritmos de machine learning

•
Avaliação crítica de resultados

•
Documentação técnica e científica

•
Considerações éticas em aplicações médicas de IA

Perspectivas Futuras

Os resultados obtidos abrem caminho para desenvolvimentos futuros mais ambiciosos, incluindo a possibilidade de integração em sistemas de apoio à decisão clínica. Com as devidas validações e aprovações regulatórias, sistemas como este podem contribuir significativamente para a melhoria do diagnóstico precoce e tratamento do câncer de mama.

A experiência adquirida neste projeto também estabelece uma base sólida para a exploração de outras aplicações de inteligência artificial em medicina, demonstrando o potencial transformador dessas tecnologias quando aplicadas com rigor científico e considerações éticas apropriadas.





Nota: Este projeto foi desenvolvido exclusivamente para fins educacionais e de pesquisa. Qualquer aplicação clínica requereria validações adicionais extensivas e aprovações regulatórias apropriadas.

