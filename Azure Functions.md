
**Azure Functions** é uma oferta de **PaaS (Platform as a Service)** que habilita a **computação sem servidor**. Isso significa que você pode executar seu código sem se preocupar com a infraestrutura de servidor subjacente.

Seu código é **baseado em eventos** e só é executado quando chamado (por exemplo, por um HTTP request, uma mensagem em fila, ou um timer). Durante períodos de inatividade, nenhuma infraestrutura de servidor é necessária, resultando em **custos otimizados** e **escala automática** conforme a demanda.
## Comparando as Opções de Computação do Azure

O Azure oferece diversas opções de computação, cada uma com seus próprios casos de uso e níveis de gerenciamento.

### **Máquinas Virtuais (VMs)**

- **Servidores baseados em nuvem** que suportam ambientes **Windows ou Linux**.
- Ideal para **migrações de lift-and-shift** de cargas de trabalho existentes para a nuvem.
- Proporcionam um **pacote completo do sistema operacional**, incluindo controle total sobre o SO hospedeiro e o ambiente.

### **Azure Virtual Desktop (AVD)**

- Fornece uma **experiência de área de trabalho Windows baseada em nuvem**, acessível de qualquer lugar.
- Usuários podem se conectar e usar aplicativos através de clientes dedicados ou de qualquer navegador moderno.
- Permite **logins de múltiplos clientes**, o que significa que vários usuários podem acessar e compartilhar a mesma máquina virtual otimizada simultaneamente, gerando economia.

### **Contêineres**

- Oferecem um **ambiente leve e virtualizado**, perfeito para a execução de **microsserviços**.
- Projetados para **escalabilidade e resiliência** através da **orquestração** (como o Azure Kubernetes Service - AKS).
- Aplicativos e seus serviços são empacotados em um contêiner que roda sobre o sistema operacional do host, permitindo que **vários contêineres** compartilhem o mesmo SO hospedeiro de forma isolada.

___
## Serviços de Rede

Os serviços de rede são a espinha dorsal de qualquer solução na nuvem, garantindo que seus aplicativos e dados se comuniquem de forma segura e eficiente, seja dentro do Azure, com a internet ou com suas redes locais.
### **Azure App Service**

O **Azure App Service** é uma plataforma **totalmente gerenciada (PaaS)** para criar, implantar e escalar aplicativos web e APIs rapidamente. Ele abstrai a complexidade da infraestrutura, permitindo que você se concentre no código.

- Suporta uma ampla gama de linguagens, incluindo **.NET, .NET Core, Node.js, Java, Python** e **PHP**.
- Oferece desempenho, segurança e conformidade de nível corporativo, ideal para atender às demandas de aplicações empresariais.

### **Rede Virtual do Azure (VNet)**

A **Rede Virtual do Azure (VNet)** é o bloco fundamental para sua rede privada na nuvem. Ela permite que os recursos do Azure se comuniquem de forma segura entre si, com a internet e com suas redes locais.

- **Pontos de Extremidade Públicos:** Tornam seus recursos acessíveis de qualquer lugar na internet.
- **Pontos de Extremidade Privados:** Garantem que os recursos sejam acessíveis apenas de dentro da sua rede virtual, aumentando a segurança.
- **Sub-redes Virtuais:** Permitem segmentar sua VNet em redes menores, atendendo às suas necessidades de isolamento e organização.
- **Emparelhamento de Rede (VNet Peering):** Conecta suas redes virtuais privadas diretamente e com segurança, como se estivessem na mesma rede.
### **Gateway de VPN (VPN Gateway)**

O **Gateway de VPN** é usado para estabelecer uma conexão segura e **criptografada** entre uma rede virtual do Azure e uma rede local (on-premises) através da internet pública. É a escolha ideal para cenários de conectividade híbrida mais simples e com custo otimizado.

![[Pasted image 20250323080852.png]]
![[Pasted image 20250323080914.png]]

### **ExpressRoute**

O **ExpressRoute** estende suas redes locais para o Azure por meio de uma **conexão privada e dedicada**, não utilizando a internet pública. Essa conexão é facilitada por um provedor de conectividade, oferecendo **maior largura de banda, menor latência e mais segurança** em comparação com as VPNs sobre a internet. É a escolha preferencial para cargas de trabalho de missão crítica e com altos requisitos de desempenho.
## **DNS do Azure**

O **DNS do Azure** é um serviço gerenciado para hospedagem de domínios que garante que seus serviços sejam encontrados de forma rápida e segura. Ele integra a gestão de nomes de domínio à infraestrutura do Azure, oferecendo confiabilidade e performance.

Aqui estão os principais benefícios e características do DNS do Azure:

- **Confiabilidade e Desempenho Global:** Utiliza uma rede global de servidores DNS com tecnologia **Anycast**, direcionando consultas ao servidor mais próximo para baixa latência e alta disponibilidade.
- **Segurança Robusta:** Integrado ao **Azure Resource Manager**, permite o **Controle de Acesso Baseado em Função (RBAC)** e oferece **monitoramento e registro em log** detalhados para segurança aprimorada.
- **Gestão Unificada e Simplicidade:** Facilita o gerenciamento de domínios públicos e de recursos do Azure em um **único serviço**, simplificando a administração.
- **Domínios Privados:** Possibilita o uso de **nomes de domínio privados e personalizados** dentro das suas redes virtuais, essencial para a resolução de nomes internos.
- **Registros de Alias:** Permite que registros DNS apontem diretamente para **recursos do Azure** (como IPs públicos ou App Services), atualizando-se automaticamente com mudanças no recurso subjacente.






