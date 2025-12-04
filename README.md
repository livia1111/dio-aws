# Gerenciamento Básico de Instâncias EC2 na AWS 🚀

Este guia fornece uma introdução prática ao gerenciamento de instâncias **Amazon EC2 (Elastic Compute Cloud)**, ideal para quem está começando a explorar a AWS.

---

## 📌 O que é EC2?
O **Amazon EC2** é um serviço que permite criar e gerenciar máquinas virtuais na nuvem da AWS.  
Ele oferece escalabilidade, flexibilidade e controle sobre recursos computacionais.

![Logo EC2](images/aws-ec2-logo.png)

---

## 🔑 Conceitos Fundamentais
- **Instância**: máquina virtual criada na AWS.
- **AMI (Amazon Machine Image)**: imagem usada para inicializar a instância (ex.: Ubuntu, Amazon Linux).
- **Tipos de instância**: definem CPU, memória e rede (ex.: `t2.micro`, `m5.large`).
- **Security Groups**: regras de firewall que controlam tráfego de entrada e saída.
- **Key Pair**: par de chaves usado para acessar a instância via SSH.

![Tipos de instância](images/ec2-instance-types.png)

---

## ⚙️ Passos Básicos para Gerenciar uma Instância EC2
1. **Criar uma instância**
   - Acesse o console da AWS → EC2 → *Launch Instance*.
   - Escolha uma AMI (ex.: Ubuntu Server).
   - Selecione o tipo de instância (ex.: `t2.micro` para testes gratuitos).
   - Configure storage, security groups e key pair.

   ![Launch Instance](images/ec2-launch-instance.png)

2. **Conectar à instância**
   - Via SSH:
     ```bash
     ssh -i "minha-chave.pem" ubuntu@ec2-xx-xx-xx-xx.compute.amazonaws.com
     ```
   - Ou via AWS Systems Manager (sem necessidade de chave).

   ![Conexão SSH](images/ec2-ssh-connect.png)

3. **Monitorar**
   - Use o **CloudWatch** para métricas (CPU, rede, disco).
   - Configure alarmes para eventos críticos.

   ![CloudWatch Monitoramento](images/cloudwatch-monitoring.png)

4. **Gerenciar ciclo de vida**
   - **Start**: iniciar a instância.
   - **Stop**: desligar sem perder dados do disco.
   - **Terminate**: excluir a instância e seus dados.

   ![Ciclo de vida EC2](images/ec2-lifecycle.png)

---

## 💡 Insights Importantes
- **Custos**: instâncias em execução geram cobrança por hora/segundo. Sempre desligue quando não estiver usando.
- **Elastic IP**: use IPs fixos para manter acessibilidade mesmo após reiniciar.
- **Auto Scaling**: configure para aumentar ou reduzir instâncias automaticamente conforme demanda.
- **Snapshots**: faça backups do volume EBS para restaurar facilmente.
- **Tags**: use tags para organizar e identificar instâncias em ambientes grandes.

![Auto Scaling](images/ec2-auto-scaling.png)

---

## 📚 Recursos para Estudo
- [Documentação oficial da AWS EC2](https://docs.aws.amazon.com/ec2/)
- [AWS Free Tier](https://aws.amazon.com/free/) – ideal para praticar sem custos elevados.
- [CloudWatch](https://aws.amazon.com/cloudwatch/) – monitoramento integrado.

---

## ✅ Conclusão
Gerenciar instâncias EC2 é o primeiro passo para dominar a AWS.  
Com práticas simples como **monitoramento, automação e uso consciente de recursos**, você garante eficiência e economia na nuvem.

![AWS Cloud](images/aws-cloud.png)
