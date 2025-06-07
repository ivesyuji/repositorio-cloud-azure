# repositorio-cloud-azure
 Repositório contendo resumos, anotações da Azure

# Beneficios da Nuvem
## **Alta disponibilidade**

- Concentra-se em garantir a disponibilidade máxima, independente de interrupções ou eventos que possam ocorrer.
- O Azure é um ambiente de nuvem altamente disponível com garantias de tempo de atividade, dependendo do serviço.
- Essas garantias fazem parte dos SLAs  (Contratos de Nível de Serviço).
___
### **SLA (Service Level Agreement)** 

É um **Acordo de Nível de Serviço** entre um provedor de cloud (como AWS, Azure ou Google Cloud) e o cliente. Ele define métricas de desempenho e disponibilidade dos serviços oferecidos.

| SLA     | Tempo de inatividade por semana | Tempo de inatividade por mês | Tempo de inatividade por ano |
| ------- | ------------------------------- | ---------------------------- | ---------------------------- |
| 99%     | 1,68 hora                       | 7,2 horas                    | 3,65 dias                    |
| 99,9%   | 10,1 minutos                    | 43,2 minutos                 | 8,76 horas                   |
| 99,95%  | 5 minutos                       | 21,6 minutos                 | 4,38 horas                   |
| 99,99%  | 1,01 minuto                     | 4,32 minutos                 | 52,56 minutos                |
| 99,999% | 6 segundos                      | 25,9 segundos                | 5,26 minutos                 |
___
### **Principais Elementos do SLA em Cloud**

1. **Disponibilidade (Uptime)** – Percentual garantido de tempo que o serviço estará operacional (exemplo: 99,9%, 99,99% ou 99,999%).
2. **Desempenho** – Tempo de resposta dos servidores, velocidade de processamento e latência.
3. **Suporte Técnico** – Tempo de resposta e canais de atendimento em caso de falhas.
4. **Penalidades** – Compensações caso o provedor não cumpra o SLA, como descontos ou créditos.
5. **Escopo dos Serviços** – Quais serviços estão cobertos pelo SLA e quais não estão.
___
### **Exemplo de SLA na Prática**

- Se um provedor garante **99,9% de uptime**, significa que ele pode ficar indisponível no máximo **8,76 horas por ano**.
- Se a disponibilidade cair abaixo disso, o cliente pode receber créditos ou descontos.



