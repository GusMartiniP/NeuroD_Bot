# NeuroD_Bot
## TCC Escola da Nuvem - Chatbot IA

| **Data de lançamento** | 6 de abril de 2025  | 
|--------|------------|
| **Descrição do projeto** | Desenvolver chatbot com Inteligente Artificial com Python e Amazon Bedrock, auxiliando pessoas com Transtorno de Déficit de Atenção e Hiperatividade e Transtorno do Espectro Autista, dando dicas de organização, bem estar emocional, sensorial e diferentes técnicas para variados cenários   | 
| **Lider técnico** | Gustavo Passos |
| **Scrum Masters** | Mariana Rouxinol; Aline Conchetta |
| **Equipe de desenvolvedores** | Python/Backend - Walbens Charles, Mariana Rouxinol, Aline Conchetta | 
| **Equipe de Infraestrutura nuvem AWS** | Gustavo Passos, Isabéli Januário |


🎯 Objetivos:

Este projeto possui o objetivo de, através da linguagem Python e utilizando o Amazon Bedrock da AWS para usar modelo de linguagem, construir uma solução de inteligência artificial, a fim de ajudar pessoas com Transtorno de Déficit de Atenção e Hiperatividade e Transtorno do Espectro Autista (TDAH e TEA) em seus quadros de crises ou organização no geral.

O principal objetivo com a solução é auxiliar pessoas com TDAH e TEA a se ajustarem com o dia-a-dia, tendo essa condição que pode tornar algo simples bem desafiador, através de dicas de técnicas e apps de organização, afim de estabelecer uma rotina para estudos e organização em geral. Ou, também, para quadro de crises, com as melhores dicas e soluções pensando no quadro, tais como ajustes sensoriais (ambiente, iluminação, sons, tato, cheiros) e como lidar com shutdowns e meltdowns. Também poderá trazer questões alimentares que possam causar mudanças positivas.

📌 Importante destacar que, a solução é apenas uma ferramenta de auxílio, e não uma substituição de tratamento psicológico/psiquiátrico.

O projeto abrange todo o ciclo de desenvolvimento, desde a definição de requisitos, passando por arquitetura e design thinking.

## 📊 Indicadores de missão cumprida:

### **Indicadores de Sucesso**

O chatbot deve ser capaz de:

- **Interagir com o usuário de forma simples e eficiente, com acessibilidade para ouvir o texto através de áudio;**
- **Armazenar os dados do usuário** para trazer informações personalizadas referente ao(s) transtorno(s) que for(em) mencionado(s);
- **De acordo com relato, solicitando também por comorbidades comumentes relacionadas aos transtornos, como ansiedade, depressão, bipolaridade, etc; e irá processar em sua base de dados para oferecer a melhor abordagem para a situação;**
- **Indicar ações imediatas que podem ser feitas (ajustes ambientais, sensoriais, mindfulness, etc)**
- **Fornecer dicas personalizadas para organização geral e de estudos e alimentação pensadas justamente para o(s) quadro(s) relatado(s)**
- **Possuir uma interface simples e descomplicada para facilitar e encorajar o uso** 
- **Escalabilidade e Uso da IA:** Integração funcional com o modelo Amazon Bedrock.**

 ## 📜 Premissas

- Utilização de Python e Amazon Bedrock para desenvolvimento.
- Aplicação de todo o ciclo de desenvolvimento de software.
- Organização de equipes com papéis bem definidos.
- Criação e uso de um documento de requisitos detalhado.
- Entregas incrementais com progresso contínuo.
- Implementação de uma arquitetura escalável e eficiente.
- Entrega de todas as etapas dentro dos prazos estabelecidos.

## 📑 Requisitos

### **Requisitos Funcionais**

- Serviço LEX - Serviço AWS que fornece a função de ChatBot;
- Serviço Via Back-end → Python, para estruturação e criação dos mecanismos internos de input/output da IA; uso de API; 
- Armazenamento e Segurança na infraestrutura AWS;
- Serviço CloudFront - Trabalha com otimização de entrega de conteúdo para usuário final, reduzindo latência e introduzindo segurança à aplicação web através do AWS WAF e Shield Standard, que são configurados juntos dele.
- Serviço AWS Lambda e DynamoDB - Para registrar interações, armazenar e melhorar o output de acordo com as informações do usuário X base de treinamento da IA;
- Serviço Amazon S3 e Bedrock, Integração dos dados que a IA utilizará e hospedagem do web app;
- Serviço OpenSearch, que irá osquestrar toda a comunicação da documentação do Bot no S3 e retornar de forma eficaz e rápida um resultado preciso.


### **Requisitos Não Funcionais**

**Desempenho**:

- O chatbot deve ser responsivo, com tempo de resposta rápido para as interações do usuário.

**Linguagem utilizada e Bibliotecas:**

- A linguagem utilizada será Python;
- Será utilizada a biblioteca Boto3 para interagir com os serviços da AWS e automatizar tarefas, como provisionar recursos e gerenciar dados. 
**Uso de um serviço de Inteligência Artificial para processamento e resposta:**

- Utilização do serviço Amazon Bedrock para geração das respostas personalizadas com base na documentação fornecida pelo Amazon S3;

## 📖 Histórias de Usuário

***R1 → Como um usuário, quero interagir com a aplicação através do chatbot para que possa obter informações sobre como lidar com questões envolvendo TDAH e/ou TEA***

- **Critérios de aceite:**
    - O chatbot deve responder enfaticamente e de forma tranquilizadora para aproximar o usuário
    - O usuário deve poder adicionar mais informações referentes a comorbidades (Depressão, ansiedade, bipolaridade, etc)

***R2 →Como um usuário, quero que a aplicação gere um plano emergencial para crises ou dicas para rotina/organização como um todo, além como alimentação***

- **Critérios de aceite:**
    - O plano deve ser adaptado aos objetivos do usuário (Qual a queixa, quais comorbidades, se é diagnosticado, etc.;
    - O plano deve ser apresentado de forma clara e intuitiva, porém não sendo um substituto à uma consulta médica ou psiquiátrica 
    

***R3 → Como um desenvolvedor, quero utilizar o DynamoDB e o CloudFront para que os dados dos usuários sejam armazenados de forma segura e escalável com um tempo de resposta rápido e satisfatório.***

- **Critérios de aceite:**
    - Os dados pessoais dos usuários devem ser armazenados de forma segura.
    - O tempo de resposta deve ser adequado para um uso eficiente da aplicação.

***R4 → Como um desenvolvedor, quero utilizar funções Lambda para realizar a análise dos dados dos usuários e para que seja feita a integração entre os serviços.***

- **Critérios de aceite:**
    - A função Lambda deve Armazenar os dados em um DynamoDB;
    - A  função Lambda deve utilizar o serviço do Amazon Bedrock para gerar respostas personalizadas com base nos dados do usuário.

***R5 → Como um desenvolvedor, quero integrar a aplicação com o OpenSearch para que o usuário possa realizar buscas por aplicativos mencionados ou se aprofundar em alguma técncia mencionada.***

- **Critérios de aceite:**
    - O OpenSearch deve indexar uma base de dados referente a crises em TDAH/TEA e ténicas ou apps de organização no geral.
    - Os resultados da busca devem ser relevantes e personalizados.

## 🧑‍💻🛠️ Tecnologias & Ferramentas

### Serviços Utilizados e suas Funcionalidades

- **IAM:** Garante a segurança da aplicação, controlando quem acessa quais recursos da AWS e com quais permissões.
- **Route 53:** Direciona o tráfego de internet para a aplicação, atuando como um DNS inteligente, otimizando a rota para o usuário.
- **CloudFront:** Acelera a entrega de conteúdo estático da aplicação, como imagens e scripts, para os usuários, melhorando a performance e assegurando a aplicação com Shield Standard e WAF.
- **AWS Lambda:** Executa códigos python necessários via back-end 
- **Lex:** Permite criar interfaces de conversação, como chatbots, para interagir com os usuários de forma natural e intuitiva.
- **DynamoDB:** Armazena dados de forma flexível e escalável, como informações dos usuários e suas interações com o chatbot.
- **S3:** Armazena arquivos de diversos tipos, como modelos de linguagem, resultados de análises e outros dados necessários para a aplicação.
- **OpenSearch:** Permite realizar buscas eficientes em grandes volumes de dados, como encontrar exercícios específicos ou informações relevantes para o usuário.
- **Bedrock:** Gera conteúdo personalizado, como texto, código e imagens, tornando as respostas do chatbot mais relevantes e personalizadas.

## 📌 Backlog | Melhorias

- Aperfeiçoar a precisão do chatbot para lidar com perguntas complexas ou não relacionadas.
- Ajustar a interface para fornecer feedback em tempo real sobre erros de entrada do usuário.
- Expandir as categorias de recomendações para incluir dietas ou hábitos saudáveis.
- Reduzir tempo de resposta das interações para menos de 5 segundos.
- Incluir suporte para múltiplos idiomas.
- Integrar métricas de uso para análise de dados e otimização do modelo.
- Incluir acessibilidade para que o texto gerado seja também audível.
