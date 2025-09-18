# Projeto Code Girl - Desafio Instâncias EC2

## Descrição do Projeto
Este projeto foi desenvolvido como parte do desafio do **Bootcamp Code Girl** na plataforma DIO. O objetivo é demonstrar uma arquitetura básica na AWS para disponibilizar uma aplicação web que pode ser acessada por pacientes de forma segura e escalável.

A aplicação contempla:
- Distribuição de conteúdo via CDN (CloudFront) para reduzir latência.
- Resolução de nomes e roteamento com Route 53.
- Balanceamento de carga com Application Load Balancer (ALB).
- Servidores de aplicação em EC2.
- Armazenamento de arquivos estáticos no S3.
- Banco de dados relacional RDS.

---

## Sobre as Instâncias EC2

- As Instâncias EC2 (Elastic Compute Cloud) são a base de computação desta arquitetura. Elas funcionam como servidores virtuais na nuvem da AWS, fornecendo o poder de processamento necessário para a aplicação web.

- Função no Projeto: No nosso projeto, as instâncias EC2 rodam o código da aplicação e interagem com o banco de dados (RDS) e o armazenamento de arquivos (S3).

- Papel na Arquitetura: Elas recebem as requisições que vêm do ALB e são o componente central que executa a lógica do nosso sistema. A flexibilidade do EC2 nos permite ajustar a capacidade de processamento em tempo real, garantindo que a aplicação seja capaz de lidar com picos de acesso de forma eficiente.

---
## Arquitetura

Descrição do fluxo:

1. **Paciente** acessa a aplicação via computador ou dispositivo móvel.
2. A requisição é enviada para o **CloudFront**, que atua como CDN e cache para melhorar o desempenho.
3. **Route 53** resolve o DNS e direciona a requisição para o **Application Load Balancer (ALB)**.
4. O **ALB** distribui a carga entre as instâncias **EC2**, garantindo alta disponibilidade.
5. As instâncias **EC2** podem acessar:
   - O **S3**, para armazenamento de arquivos estáticos.
   - O **RDS**, para gerenciar os dados da aplicação.

---

## Tecnologias Utilizadas
- **AWS CloudFront**: Distribuição de conteúdo.
- **AWS Route 53**: Gerenciamento de DNS.
- **AWS ALB (Application Load Balancer)**: Balanceamento de carga.
- **AWS EC2**: Servidores de aplicação.
- **AWS S3**: Armazenamento de arquivos.
- **AWS RDS**: Banco de dados relacional.

---

## Objetivo de Aprendizado
- Entender o fluxo de uma aplicação web na AWS.
- Aprender a integrar diferentes serviços AWS para escalabilidade e performance.
- Documentar e apresentar uma arquitetura de forma clara.

---

## Autor
**Karollyne Cabrau**  
Bootcamp Code Girl - DIO
