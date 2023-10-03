# Proposta de solução de aprendizado contínuo num sistema conversacional.

## Introdução

Atualmente, nos sistemas conversacionais, dependemos amplamente de Modelos de Linguagem de Grande Escala pré-treinados. Esses modelos desempenham um papel vital em nossa capacidade de compreender e responder às consultas dos usuários, fornecendo respostas contextuais e relevantes. Eles são a espinha dorsal desses sistemas, permitindo-nos codificar e processar conhecimento do mundo em seus parâmetros.

No entanto, enfrentamos um desafio crítico: a rápida obsolescência do conhecimento armazenado nesses modelos de linguagem devido às mudanças constantes no mundo real. À medida que o mundo evolui, as informações armazenadas nesses modelos podem se tornar desatualizadas, levando a respostas imprecisas ou inadequadas aos usuários. Isso é conhecido como "concept drift" e representa uma preocupação central para a relevância contínua de aplicativos conversacionais.

Neste contexto, enfrentamos a tarefa crítica de superar o concept drift e manter a relevância do sistema conversacional. Esta proposta busca abordar esse desafio, introduzindo um sistema de Aprendizado Contínuo de Conhecimento (CKL) que permitirá a atualização constante dos modelos de linguagem pré-treinados, garantindo que o sistema continue fornecendo respostas precisas e contextualmente relevantes aos usuários, mesmo em face das mudanças rápidas do mundo real.

## Solução Proposta

Para abordar esse desafio, a proposta é um sistema de Atualização Contínua de Modelos de Linguagem. Este sistema permite a adaptação constante dos nossos modelos de linguagem às demandas em constante mudança dos usuários e ao conhecimento em constante evolução.

Nossa solução é composta por uma série de blocos interconectados, cada um desempenhando um papel crucial no processo de atualização contínua. Nesta seção, detalharemos cada um desses blocos, suas responsabilidades e como eles contribuem para manter nossos modelos de linguagem sempre atualizados e prontos para fornecer respostas precisas aos nossos usuários.

A seguir uma representação visual do diagrama dos blocos e após uma visão geral dos principais blocos da nossa solução acompanhado de sua descição e responsabilidades:

![diagrama_bruno](https://github.com/brun0meira/continual-knowledge-learning-of-language-models/assets/99202553/07037132-62a4-4f3a-930d-0cbd2c089adf)

### Bloco 1: Modelo de Linguagem Pré-treinado
- **Descrição:** Este é o ponto de partida do nosso sistema, onde usamos um modelo de linguagem pré-treinado como base para processar consultas de usuários.
- **Responsabilidades:**
    - Utilizar um modelo de linguagem pré-treinado como referência inicial para processar consultas dos usuários.
    - Fornecer respostas de acordo com o conhecimento atual do modelo.

### Bloco 2: Identificar o Concept Drift
- **Descrição:** Este bloco é responsável por monitorar e identificar o concept drift, ou seja, mudanças significativas nas consultas dos usuários e no conhecimento necessário para responder a essas consultas.
- **Responsabilidades:**
    - Analisar regularmente os dados de consultas dos usuários e compará-los com o conhecimento atual do modelo.
    - Identificar tendências de concept drift, como novos tópicos emergentes ou informações desatualizadas.

### Bloco 3: Coleta de Logs dos Chats
- **Descrição:** Este bloco é responsável por coletar e armazenar registros das conversas em tempo real entre os usuários e o sistema de chat do aplicativo.
- **Responsabilidades:**
    - Registrar todas as interações dos usuários, incluindo consultas, respostas, feedbacks e timestamps.
    - Armazenar esses registros em um repositório seguro e escalável para análise posterior.

### Bloco 4: Análise de Logs
- **Descrição:** Este bloco analisa os logs de chat coletados para identificar padrões e tendências nas consultas dos usuários.
- **Responsabilidades:**
    - Realizar análise exploratória dos dados de logs para identificar tópicos populares, mudanças no comportamento dos usuários e problemas recorrentes.
    - Gerar insights a partir dos dados de logs que serão usados para aprimorar o sistema.

### Bloco 5: Aprendizado Contínuo de Conhecimento (CKL)
- **Descrição:** Este bloco aplica o conceito de Aprendizado Contínuo de Conhecimento (CKL) para atualizar os modelos de linguagem de forma contínua com base nas informações identificadas na análise de logs.
- **Responsabilidades:**
    - Utilizar os insights da análise de logs para criar um conjunto de dados de referência específico para o CKL, incluindo informações desatualizadas, invariantes no tempo e novos conhecimentos.
    - Implementar métodos CKL, como regularização, repetição e expansão de parâmetros, para atualizar os modelos de linguagem.

### Bloco 6: Atualização de Conhecimento dos Modelos de Linguagem
- **Descrição:** Este bloco é responsável por integrar as novas informações adquiridas durante o CKL aos modelos de linguagem pré-treinados.
- **Responsabilidades:**
    - Atualizar os parâmetros do modelo de linguagem com base nas informações mais recentes adquiridas durante o CKL.
    - Garantir que o modelo esteja sempre atualizado e pronto para fornecer respostas precisas.

### Bloco 7: Retenção de Conhecimento não Aproveitável
- **Descrição:** Este bloco atua como um filtro que decide quais informações devem ser mantidas e quais podem ser descartadas antes de atualizar o modelo.
- **Responsabilidades:**
    - Verificar informações duplicadas, redundantes ou obsoletas antes de integrar os dados ao modelo.
    - Garantir que apenas conhecimento relevante e atualizado seja retido e utilizado na atualização dos modelos.

### Bloco 8: Banco de Dados
- **Descrição:** Este bloco é responsável por armazenar todas as informações, novas e antigas, que alimentam o processo de aprendizado contínuo.
- **Responsabilidades:**
    - Manter um banco de dados centralizado que contenha todos os dados relevantes para o sistema, incluindo informações atualizadas, invariantes no tempo e novos conhecimentos.
    - Fornecer acesso aos dados para o processo de aprendizado contínuo e atualização dos modelos de linguagem.

## Conclusão

A proposta de implementação do Aprendizado Contínuo de Conhecimento (CKL) em sistema conversacional é fundamental para lidar com o desafio do concept drift e garantir que nossos modelos de linguagem permaneçam atualizados. Isso permitirá que o sistema forneça respostas precisas e relevantes aos usuários, mesmo diante das mudanças constantes no mundo real.

É importante reconhecer que essa abordagem exigirá um esforço significativo em termos de desenvolvimento e recursos computacionais. No entanto, os benefícios de manter a relevância e a precisão do sistema conversacional justificam esse investimento. À medida que se avança nesse caminho, é crucial monitorar continuamente o desempenho do sistema, ajustar os métodos CKL conforme necessário e explorar oportunidades para otimização e escalabilidade.

O CKL não apenas permitirá que nosso aplicativo forneça respostas mais precisas aos usuários, mas também nos ajudará a entender melhor e treinar nossos modelos de linguagem em constante mudança. Com o tempo, essa abordagem nos permitirá melhorar continuamente a experiência do usuário e manter nosso aplicativo como uma fonte confiável de informações.

## Referências Bibliográficas.

Joel Jang, Seonghyeon Ye, Sohee Yang, Joongbo Shin, Janghoon Han, Gyeonghun Kim, Stanley Jungkyu Choi, Minjoon Seo, KAIST AI, LG AI Research. Towards Continual Knowlage Learning of Language Models. arXiv:2110.03215v4 [cs.CL] 24 May 2022
https://arxiv.org/pdf/2110.03215.pdf
