# Serviços de Computação e Máquinas Virtuais Azure
## **Azure Virtual Desktop (AVD)**

O **Azure Virtual Desktop** é uma solução de virtualização de área de trabalho e aplicativo que roda inteiramente na nuvem. Ele oferece a você e seus usuários uma experiência completa de desktop virtualizado, acessível de qualquer lugar.

- **Ambiente Simplificado:** Com o AVD, você pode criar um ambiente completo de virtualização de área de trabalho **sem a necessidade de configurar e manter servidores de gateway** adicionais. Isso simplifica a arquitetura e o gerenciamento.
- **Eficiência de Recursos:** Ajuda a **reduzir o risco de ter recursos ociosos** ou "esquecidos", já que a infraestrutura é dimensionada e gerenciada pela nuvem.
- **Múltiplas Sessões Reais:** Uma das grandes vantagens do AVD é que ele permite **implantações de várias sessões reais** do Windows 10 e Windows 11 Enterprise. Isso significa que múltiplos usuários podem compartilhar a mesma máquina virtual otimizada, reduzindo custos e complexidade.
## **Serviços de Contêineres do Azure**

Os **Serviços de Contêineres do Azure** fornecem um ambiente leve e virtualizado para suas aplicações. Eles eliminam a necessidade de gerenciar o sistema operacional subjacente e permitem que suas aplicações respondam a mudanças de demanda de forma ágil.

O Azure oferece diversas opções para rodar contêineres:

- **Instâncias de Contêiner do Azure (ACI):**
    - É uma **oferta de PaaS (Platform as a Service)** que permite executar um contêiner ou um pod de contêineres (um grupo de contêineres que compartilha recursos) diretamente no Azure, sem a necessidade de provisionar máquinas virtuais.
    - Ideal para cenários de execução rápida, testes e cargas de trabalho que não exigem orquestração complexa.
- **Aplicativos de Contêiner do Azure (ACA):**
    - Também uma **oferta de PaaS**, o Aplicativos de Contêiner do Azure é construído sobre Kubernetes, mas abstrai a complexidade do gerenciamento da orquestração.
    - Ele é projetado para executar microsserviços e aplicações baseadas em contêineres que podem automaticamente **balancear a carga e escalar** com base no tráfego e na demanda.
    - Ótimo para quem precisa de recursos de orquestração sem o gerenciamento direto do Kubernetes.
- **Serviço de Kubernetes do Azure (AKS):**
    - É um serviço de **orquestração** completo para contêineres, baseado no popular Kubernetes de código aberto.
    - O AKS é ideal para gerenciar o ciclo de vida de **grandes volumes de contêineres** e arquiteturas distribuídas complexas. Ele simplifica a implantação, o dimensionamento e o gerenciamento de aplicações em contêineres.


