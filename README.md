# Desafio - Implementando de Infraestrutura Automatizada com AWS CloudFormation

Este repositório contém anotações organizadas, exemplos e insights adquiridos durante o estudo e prática sobre a implementação de infraestrutura automatizada utilizando AWS CloudFormation.  
O objetivo é servir como material de referência para estudos futuros, criação de novas stacks e aprofundamento em infraestrutura como código.

---

## 1. O que é o AWS CloudFormation

AWS CloudFormation é um serviço que permite modelar, provisionar e gerenciar recursos da AWS de forma automatizada, segura e padronizada.  
Ele utiliza arquivos no formato JSON ou YAML chamados templates, que descrevem tudo o que será criado na AWS: instâncias EC2, redes, buckets S3, bancos de dados, políticas IAM e muito mais.

Ao enviar um template, o CloudFormation cria uma stack, ou seja, um conjunto de recursos que pode ser gerenciado, atualizado ou deletado como uma unidade.

---

## 2. Benefícios do AWS CloudFormation

### Automação
CloudFormation automatiza a criação, configuração e exclusão de recursos da AWS.  
Com isso, a infraestrutura pode ser criada rapidamente, com previsibilidade e menor chance de erro humano.

### Consistência e Padronização
Templates permitem criar múltiplas cópias idênticas de uma mesma infraestrutura.  
Isso garante que ambientes como desenvolvimento, homologação e produção sigam a mesma arquitetura.

### Economia de Custos
É possível reutilizar templates em vários ambientes, evitando recriação manual e diminuindo retrabalho.

### Segurança
CloudFormation aplica boas práticas de segurança da AWS, garantindo que os recursos sejam criados com configurações adequadas.

---

## 3. Formatos Aceitos para Templates

O AWS CloudFormation suporta dois formatos principais: JSON e YAML.

### Exemplo de Template em JSON

```
{
  "Resources": {
    "MyInstance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "InstanceType": "t2.micro",
        "ImageId": "ami-12345678"
      }
    }
  }
}

```

### Exemplo Equivalente em YAML

```
Resources:
  MyInstance:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      ImageId: ami-12345678
```
---
## 4. Diferenças entre AWS CloudFormation e Terraform

 - CloudFormation é focado na AWS

 - Terraform é voltado para múltiplos provedores de nuvem.

## 5. Insights e Aprendizados Durante a Prática

 - AWS CloudFormation é uma ferramenta poderosa para padronizar e automatizar ambientes.

 - Templates bem escritos podem ser reutilizados e versionados facilmente.

 - O Designer ajuda a visualizar arquiteturas e entender dependências entre recursos.

 - Utilizar parâmetros torna os templates flexíveis e reutilizáveis.

 - Validar os templates antes da criação evita erros e perda de tempo.

 - A criação de stacks facilita a replicação de ambientes complexos.


