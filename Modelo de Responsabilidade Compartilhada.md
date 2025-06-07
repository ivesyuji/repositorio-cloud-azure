___

O **Modelo de Responsabilidade Compartilhada** é um conceito fundamental na segurança em nuvem que descreve as obrigações de segurança, especificando claramente os direitos e responsabilidades tanto do provedor de serviços em nuvem quanto do cliente. 

Essa divisão de responsabilidades varia dependendo do modelo de serviço em nuvem que você escolher: IaaS, PaaS ou SaaS.
![[Pasted image 20250320080813.png|700]]
### **Responsabilidade no IaaS (Infrastructure as a Service)**

No IaaS, que é o **serviço de nuvem mais flexível**, você tem o maior controle, mas também a **maior responsabilidade** sobre o hardware para seu aplicativo.

- **Sua Responsabilidade (Cliente):**
    - **Configura e gerencia o hardware virtualizado para seu aplicativo** (máquinas virtuais, redes virtuais, armazenamento virtual).
    - **Gerencia:** Sistemas operacionais (SO), aplicações, dados, middleware, tempo de execução (runtime), configuração de rede (IPs, firewalls virtuais), segurança de rede (NSGs), patches do SO, e a segurança dos dados e aplicações.
- **Responsabilidade do Provedor de Nuvem:**
    - Gerencia a **infraestrutura física que suporta a nuvem: o prédio, a energia, o resfriamento, o hardware de rede físico, o hardware de servidor e a camada de virtualização. Ele garante que a nuvem esteja operacional.

**Exemplo Prático:** Ao usar uma Máquina Virtual do Azure, você é responsável por manter o sistema operacional atualizado, instalar softwares de segurança, proteger os dados dentro da VM e configurar as regras de firewall da VM. O Azure garante que a VM possa ser provisionada e que a infraestrutura subjacente funcione.
## Responsabilidade no PaaS (Platform as a Service)

No **PaaS**, o foco principal está no **desenvolvimento e implantação de aplicativos**. Aqui, o provedor de nuvem assume a maior parte do gerenciamento, cuidando da **plataforma completa**. Isso significa que você pode se concentrar em criar seu código e seus dados, sem se preocupar com a infraestrutura subjacente, como sistemas operacionais, hardware e servidores.

- **Sua Responsabilidade (Cliente):**
    - **Configura e gerencia o hardware virtualizado para seu aplicativo** (máquinas virtuais, redes virtuais, armazenamento virtual).
    - **Gerencia:** Sistemas operacionais (SO), aplicações, dados, middleware, tempo de execução (runtime), configuração de rede (IPs, firewalls virtuais), segurança de rede (NSGs), patches do SO, e a segurança dos dados e aplicações.
- **Responsabilidade do Provedor de Nuvem:**
    - Gerencia a **infraestrutura física** que suporta a nuvem: o prédio, a energia, o resfriamento, o hardware de rede físico, o hardware de servidor e a camada de virtualização. Ele garante que a nuvem esteja operacional.

**Exemplo Prático:** Ao usar uma Máquina Virtual do Azure, você é responsável por manter o sistema operacional atualizado, instalar softwares de segurança, proteger os dados dentro da 

### **Responsabilidade no SaaS (Software as a Service)**

O SaaS é o modelo de nuvem onde você tem a **menor responsabilidade de gerenciamento**. É um **modelo de preço de pagamento conforme o uso**, onde os usuários pagam pelo software que utilizam em um modelo de assinatura, acessando-o via internet.

- **Sua Responsabilidade (Cliente):**
    - **Gerencia:** Praticamente nada, além do uso dos seus dados dentro do aplicativo e, em alguns casos, as permissões de acesso dos seus usuários.
- **Responsabilidade do Provedor de Nuvem:**
    - O provedor é **responsável por tudo** — a aplicação em si, os dados, os servidores, o armazenamento, a rede e toda a infraestrutura subjacente. Ele cuida de atualizações, patches, segurança e disponibilidade do serviço.
    
**Exemplo Prático:** Ao usar o Microsoft 365 (SaaS), a Microsoft gerencia os servidores de e-mail, os softwares (Word, Excel, etc.), a segurança da plataforma e a infraestrutura. Sua responsabilidade se limita a garantir a segurança da sua senha e a forma como você compartilha seus documentos.