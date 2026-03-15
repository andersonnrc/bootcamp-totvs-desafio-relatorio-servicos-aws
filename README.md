# ☁️ Relatório de Implementação de Serviços AWS

![AWS](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-FF9900?style=for-the-badge)
![Empresa](https://img.shields.io/badge/Empresa-Abstergo_Industries-232F3E?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

**Data:** 15/03/2026  
**Empresa:** Abstergo Industries  
**Responsável:** Anderson Ribeiro de Carvalho  

---

## 📌 Introdução
Este relatório apresenta o processo de implementação de arquitetura em nuvem na empresa **Abstergo Industries**, liderado por Anderson Ribeiro de Carvalho. O objetivo principal deste projeto foi elencar e estruturar 3 serviços da Amazon Web Services (AWS) focados na otimização de infraestrutura e **redução imediata de custos** operacionais.

---

## 🔎 Planejamento e Assessment (Fase Zero)
Antes de realizar a movimentação de qualquer carga de trabalho para a nuvem e definir as três ferramentas principais, é estritamente necessário analisar a infraestrutura local atual. Para isso, utilizamos o **AWS Migration Evaluator**.

Esta ferramenta permite:
* Rastrear e basear a tomada de decisão com uma avaliação personalizada, visando reduzir os custos em até **50%**.
* Descobrir instâncias superprovisionadas *on-premises*.
* Obter recomendações para alternativas econômicas nativas da AWS.
* Planejar a migração de forma eficiente, identificando licenças existentes e comparando custos de execução.

> **💡 Nota sobre Licenciamento:** Durante a avaliação, consideramos os modelos **BYOL** (*Bring Your Own License* - Traga sua Própria Licença) e **LI** (*License Included* - Licença Incluída). Eles definem quem é o proprietário da licença do software e como ela é paga no ambiente de nuvem, sendo essenciais para a estratégia de redução de custos.

---

## 🏗️ Arquitetura e Serviços Implementados
O projeto de implementação foi dividido em 3 etapas estratégicas, cada uma focada em modernizar um pilar da infraestrutura da empresa:

### Etapa 1: Banco de Dados
* **Nome da Ferramenta:** Amazon Relational Database Service (Amazon RDS)
* **Foco da Ferramenta:** Serviço de banco de dados relacional gerenciado.
* **Descrição do Caso de Uso:** O Amazon RDS é a escolha ideal para substituir a infraestrutura local de bancos de dados que possuem licenciamento de alto custo (como Oracle ou SQL Server). A migração otimiza o uso de licenças através do modelo BYOL ou do pagamento por hora. Imediatamente, podemos utilizar o *AWS Schema Conversion Tool (SCT)* para converter esses bancos para alternativas de código aberto (PostgreSQL ou Amazon Aurora), eliminando custos pesados de licenciamento.

**Principais Benefícios:**
* **Alta Disponibilidade:** Suporte nativo a implantações Multi-AZ.
* **Gerenciamento Simplificado:** Elimina tarefas administrativas (como provisionamento e manutenção de software).
* **Flexibilidade:** Liberdade para escolher, implantar e escalar o mecanismo relacional de preferência.
* **Segurança e Inovação:** Utilização das melhores práticas operacionais consolidadas pela AWS.

### Etapa 2: Armazenamento (Data Lake)
* **Nome da Ferramenta:** Amazon Simple Storage Service (Amazon S3)
* **Foco da Ferramenta:** Serviço de armazenamento de objetos altamente escalável.
* **Descrição do Caso de Uso:** Substituição de storages locais caros (SAN/NAS) e fitas de backup físicas, trazendo uma redução drástica no custo por gigabyte. É o ambiente perfeito para atuar como um *Data Lake*, recebendo grandes volumes de dados brutos para processos de modelagem de dados, backups de servidores ou servindo de repositório para scripts em Python voltados a análises de Big Data.

**Estratégia de Custos (Classes de Armazenamento):**
* `S3 Standard` / `S3 Express One Zone`: Para dados de produção e acesso frequente.
* `S3 Standard-IA` / `S3 One Zone-IA`: Economia para dados acessados com pouca frequência.
* `S3 Glacier (Instant, Flexible, Deep Archive)`: Para arquivamento de longo prazo com o menor custo possível.

### Etapa 3: Capacidade Computacional
* **Nome da Ferramenta:** Amazon Elastic Compute Cloud (Amazon EC2)
* **Foco da Ferramenta:** Fornecimento de capacidade computacional segura, escalável e redimensionável.
* **Descrição do Caso de Uso:** Redução de custos com hardware físico para desenvolvimento e implantação de aplicações. Para cargas de trabalho que não exigem tempo real (como processamento em lote, treinamento de modelos de dados ou rotinas de extração de ETL para alimentar dashboards de Business Intelligence), a adoção de **Instâncias Spot** permite alugar capacidade ociosa da AWS com até 90% de desconto.

**Dinâmica de Escalabilidade:**
* Aumento de escala vertical/horizontal sob demanda para lidar com tarefas pesadas (fechamentos mensais ou picos de tráfego).
* Redução automática de capacidade quando o processamento diminui, garantindo que a empresa pague apenas pelo que consome.

---

## 🎯 Conclusão
A implementação arquitetônica na **Abstergo Industries** atingiu os benefícios esperados através da tríade **Amazon RDS, Amazon S3 e Amazon EC2**. A estratégia adotada garante um ambiente escalável, altamente disponível e com custos otimizados, o que aumentará diretamente a eficiência e a produtividade da empresa. 

Recomenda-se a continuidade do monitoramento dos serviços implementados e a busca contínua por novas tecnologias *Cloud Native* que possam acelerar ainda mais os processos internos de dados e infraestrutura.

---

## 🧑‍💼 Contato

[Linkedin](https://www.linkedin.com/in/anderson-ribeiro-carvalho)
