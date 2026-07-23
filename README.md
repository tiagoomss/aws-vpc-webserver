# AWS VPC + Web Server

![AWS](https://img.shields.io/badge/AWS-Cloud-orange)
![EC2](https://img.shields.io/badge/Amazon-EC2-orange)
![VPC](https://img.shields.io/badge/Amazon-VPC-blue)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

## 📌 Sobre o projeto

Este projeto demonstra a criação de uma infraestrutura de rede na AWS utilizando o Amazon VPC.

Foi construída uma arquitetura contendo sub-redes públicas e privadas, regras de segurança, tabelas de rotas e uma instância Amazon EC2 configurada como servidor web acessível pela Internet.

O laboratório foi realizado durante o programa AWS re/Start da Escola da Nuvem com o objetivo de desenvolver conhecimentos práticos em redes na nuvem.

## 🎯 Objetivos

- Criar uma Amazon VPC personalizada.
- Configurar sub-redes públicas e privadas.
- Configurar Internet Gateway.
- Configurar Route Tables.
- Criar Security Group.
- Implantar um servidor web em uma instância Amazon EC2.
- Validar o acesso ao servidor através do navegador.

## 🏗️ Arquitetura

```
Internet
    │
Internet Gateway
    │
───────────────
Amazon VPC
───────────────
│
├── Public Subnet 1
│      │
│      └── EC2 Web Server
│
├── Public Subnet 2
│
├── Private Subnet 1
│
└── Private Subnet 2
```

## ☁️ Serviços AWS utilizados

| Serviço | Finalidade |
|----------|------------|
| Amazon VPC | Criar uma rede privada na AWS. |
| Amazon EC2 | Hospedar o servidor web. |
| Security Groups | Controlar o tráfego permitido para a instância. |
| Internet Gateway | Permitir comunicação entre a VPC e a Internet. |
| Route Tables | Definir as rotas de tráfego da rede. |
| Subnets | Separar a infraestrutura em segmentos públicos e privados. |

## ⚙️ Implementação

A implementação foi realizada utilizando os serviços de rede da AWS para construir uma infraestrutura capaz de hospedar um servidor web de forma organizada e segura.

Inicialmente foi criada uma Amazon VPC utilizando o bloco CIDR `10.0.0.0/16`, servindo como rede principal da aplicação.

Em seguida foram criadas sub-redes públicas e privadas. As sub-redes públicas foram utilizadas para disponibilizar recursos acessíveis pela Internet, enquanto as sub-redes privadas ficaram preparadas para receber recursos internos da aplicação.

Foi configurado um Internet Gateway e associadas Route Tables para permitir o roteamento correto do tráfego entre as sub-redes e a Internet.

Na camada de segurança foi criado um Security Group permitindo conexões HTTP provenientes da Internet para que o servidor web pudesse ser acessado.

Por fim foi lançada uma instância Amazon EC2 baseada em Amazon Linux 2, utilizando um script de User Data para instalar automaticamente o Apache HTTP Server e publicar uma página web.

## 📸 Evidências

## 📚 Conceitos aprendidos

Durante este laboratório foi possível compreender conceitos importantes relacionados à infraestrutura de rede na AWS, como:

- Diferença entre VPC e Subnets.
- Função do Internet Gateway.
- Papel das Route Tables no roteamento do tráfego.
- Funcionamento dos Security Groups como firewall da instância.
- Processo de inicialização de uma instância EC2.
- Utilização do User Data para automatizar configurações durante o provisionamento.

## 🚀 Possíveis melhorias

Caso este projeto fosse utilizado em um ambiente de produção, poderiam ser implementadas as seguintes melhorias:

- Distribuição das instâncias em múltiplas Zonas de Disponibilidade.
- Utilização de um Application Load Balancer.
- Configuração de um Auto Scaling Group.
- Implantação utilizando AWS CloudFormation ou Terraform.
- Monitoramento com Amazon CloudWatch.
- Registro de logs utilizando AWS CloudTrail.

## 👨‍💻 Autor

**Antonio Tiago Moura da Silva**

Projeto desenvolvido durante o programa **AWS re/Start** da **Escola da Nuvem**, sendo posteriormente documentado e organizado como parte do meu portfólio de estudos em Cloud Computing e DevOps.
