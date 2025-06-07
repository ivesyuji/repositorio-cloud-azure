___
## Principais Componentes Arquitetônicos do Azure

Entender a arquitetura do Azure é fundamental para criar soluções robustas e escaláveis na nuvem. Ela é composta por uma hierarquia de elementos que garantem desde a disponibilidade física dos seus dados até a organização lógica dos seus recursos e faturamento.

- Descrever regiões, pares de regiões e regiões soberanas do Azure.
- Descrever as zonas de disponibilidade.
- Descrever os datacenters do Azure
- Descrever os recursos e os grupos de recursos do Azure.
- Descrever as assinaturas.
- Descrever os grupos de gerenciamento.
- Descrever a hierarquia de grupos de recursos, assinaturas e grupos de gerenciamento.

___
## Regiões

As **regiões** são a base geográfica da infraestrutura global do Azure.
![[Pasted image 20250320083855.png|700]]

- O Azure conta com **mais regiões globais (mais de 60)** do que qualquer outro provedor de nuvem, abrangendo mais de 140 países.
- Uma região é composta por **um ou mais datacenters** que estão localizados muito próximos uns dos outros.
- Elas oferecem **flexibilidade e escala**, permitindo que você implante seus serviços perto dos seus usuários para **reduzir a latência**.
- As regiões também são cruciais para a **residência dos dados** e para atender a **requisitos de conformidade** específicos de cada localidade ou país.

## Pares de Região

Os **Pares de Região** no Azure são um conceito fundamental para a estratégia de **recuperação de desastres** e **alta disponibilidade** da sua infraestrutura na nuvem. Eles consistem em duas regiões do Azure dentro da mesma geografia (por exemplo, "Leste dos EUA" e "Oeste dos EUA") que são pareadas e interconectadas.

![[Pasted image 20250320092050.png]]

- **Separação Geográfica Mínima:** As regiões em um par possuem, no mínimo, **300 milhas (aproximadamente 480 km) de separação** uma da outra.
- **Replicação Automática de Dados:** Para alguns serviços do Azure, como o Armazenamento de Leitura com Acesso Georredundante (RA-GRS), a **replicação de dados é automática** entre as regiões pareadas. Isso garante que seus dados estejam sempre sincronizados e disponíveis em um local secundário, mesmo que a região primária se torne indisponível.
- **Recuperação de Região Priorizada:** Em um cenário de interrupção regional significativa, o Azure prioriza a **recuperação de apenas uma região por par** de cada vez.
- **Atualizações Distribuídas Sequencialmente:** As atualizações e a manutenção planejada da plataforma Azure são distribuídas sequencialmente para as regiões em um par. Isso significa que apenas uma região do par é atualizada por vez, o que ajuda a **minimizar o tempo de inatividade** e os riscos para a sua aplicação.

Para mais informações e a lista completa de pares de região, você pode consultar a documentação oficial do Azure: [aka.ms/PairedRegions-ptb](https://aka.ms/PairedRegions-ptb)


## Regiões Soberanas do Azure

As **Regiões Soberanas do Azure** são instâncias fisicamente e logicamente separadas da nuvem pública global do Azure. Elas são projetadas especificamente para atender a rigorosos requisitos de **segurança, conformidade e residência de dados** de governos e entidades regulamentadas.

### **Azure Governamental (Azure Government)**

O **Azure Governamental** é um exemplo primário de região soberana, focada nas necessidades dos Estados Unidos.

- É uma **instância separada do Azure**, o que significa que opera independentemente da nuvem pública global do Azure.
- É **fisicamente isolada** de implantações que não são do governo dos EUA. Isso garante que os dados e a infraestrutura do governo dos EUA não se misturem com outros clientes.
- O acesso a essa instância é **somente permitido a pessoal verificado e autorizado** que atenda aos requisitos de triagem de fundo do governo dos EUA.
- **Atende às necessidades de segurança e conformidade mais rigorosas** das agências federais, governos estaduais e locais dos EUA, bem como seus provedores de soluções. Isso inclui certificações como FedRAMP High, DoD IL5, entre outras.

### **Azure China**

O **Azure China** é outra instância de região soberana, operada em parceria com uma entidade local para garantir a conformidade com as leis chinesas.

- É uma **instância fisicamente e logicamente separada** dos serviços de nuvem do Azure operados pela 21Vianet, um parceiro de data center chinês.
- Todos os dados de clientes que usam o Azure China **permanecem estritamente dentro da China**, garantindo a conformidade com as regulamentações locais de residência de dados e soberania.
- Assim como outras regiões soberanas, ele atende às necessidades específicas de segurança e regulamentação do mercado chinês.

___
## Zonas de disponibilidade

As **Zonas de Disponibilidade** são um conceito chave para garantir a **alta disponibilidade** dentro de uma região.

- Elas fornecem **proteção contra tempo de inatividade** causado por falhas em um único datacenter.
- Cada Zona de Disponibilidade é um conjunto de **um ou mais datacenters fisicamente separados e independentes** dentro da mesma região.
- Esses datacenters possuem infraestrutura isolada, incluindo **energia, resfriamento e rede independentes**, garantindo que a falha em uma zona não afete as outras.
- As Zonas de Disponibilidade dentro de uma região são conectadas por meio de **redes privadas de fibra óptica de alta velocidade e baixa latência**, permitindo a replicação e o roteamento eficiente do tráfego.

![[Pasted image 20250320085714.png|700]]

## **Datacenters do Azure**

Os **datacenters do Azure** são as instalações físicas que abrigam os servidores, o armazenamento e a infraestrutura de rede que executam os serviços do Azure.

- Eles são a espinha dorsal da infraestrutura global do Azure.
- São construídos com design de ponta em segurança física, redundância e sustentabilidade.
- Várias dessas instalações compõem uma Zona de Disponibilidade, e um ou mais conjuntos de Zonas de Disponibilidade formam uma Região.


## **Hierarquia: Grupos de Gerenciamento, Assinaturas e Grupos de Recursos**

A arquitetura de organização do Azure segue uma hierarquia lógica:

![[Pasted image 20250321090247.png]]

1. **Grupos de Gerenciamento (Management Groups):** No topo, servem como contêineres para organizar assinaturas. Permitem aplicar governança em larga escala.
2. **Assinaturas (Subscriptions):** Abaixo dos Grupos de Gerenciamento, atuam como um limite de faturamento e acesso, contendo os recursos.
3. **Grupos de Recursos (Resource Groups):** Dentro de cada assinatura, são contêineres lógicos para agrupar recursos relacionados, facilitando o gerenciamento e o ciclo de vida.
4. **Recursos (Resources):** As instâncias dos serviços do Azure, que residem dentro dos Grupos de Recursos.

Essa hierarquia permite uma organização flexível e robusta, desde a governança de alto nível de toda a empresa até o gerenciamento granular de recursos individuais.

### **Grupos de Gerenciamento (Management Groups)**

Os **Grupos de Gerenciamento** no Azure são uma camada de organização e governança que ficam acima das assinaturas. Eles foram criados para ajudar grandes empresas a gerenciar de forma eficiente múltiplas assinaturas, aplicando políticas e controles de acesso em larga escala.

- Os grupos de gerenciamento podem incluir **várias assinaturas do Azure**. Isso permite que você organize suas assinaturas em uma estrutura hierárquica que faça sentido para a sua organização (por exemplo, por departamento, por ambiente como produção/desenvolvimento, ou por região).
- As assinaturas dentro de um grupo de gerenciamento **herdam as condições aplicadas a esse grupo**. Isso significa que políticas de segurança, iniciativas de conformidade e permissões de controle de acesso baseado em função (RBAC) definidas em um grupo de gerenciamento são automaticamente aplicadas a todas as assinaturas e recursos contidos nele ou nos grupos aninhados. Isso simplifica a governança, garantindo consistência e conformidade em todo o seu patrimônio Azure sem precisar configurar cada assinatura individualmente.****
### **Assinaturas do Azure**

No Azure, a **assinatura** é um componente central para organizar e gerenciar seus recursos e custos. Pense nela como um acordo ou contrato que define o que você pode usar e como será cobrado.

![[Pasted image 20250321090018.png|700]]

Para cada uma das suas assinaturas, você receberá uma fatura separada. Isso permite que você tenha um controle financeiro granular, por exemplo, faturando diferentes projetos, departamentos ou ambientes (como desenvolvimento e produção) de forma independente.

- Uma **conta** (a identidade que você usa para entrar no Azure) pode ter **várias assinaturas**, mas uma **assinatura só pode pertencer a uma única conta**. Isso permite que uma única organização gerencie múltiplos centros de custo ou projetos sob um mesmo login principal.
- Uma assinatura do Azure também fornece a você **acesso autenticado e autorizado** aos serviços e recursos dentro do Azure. Quando você se autentica com sua conta, a assinatura é o que define quais recursos você tem permissão para acessar e provisionar.

#### **Limite de Cobrança**

A assinatura serve como o principal **limite de cobrança**. Isso significa que:

- Todos os recursos que você provisionar e utilizar sob uma determinada assinatura serão consolidados e aparecerão na fatura específica dessa assinatura.
- O Azure **gera relatórios de cobrança e faturas separados para cada assinatura**, facilitando a alocação de custos e o monitoramento de gastos.

#### **Limite de Controle de Acesso**

Além do faturamento, a assinatura também atua como um **limite de controle de acesso**. Isso permite que você:

- **Gerencie e controle o acesso** dos usuários aos recursos. Você pode definir quem tem permissão para provisionar, gerenciar ou visualizar recursos em assinaturas específicas.
- Ao conceder acesso no nível da assinatura, todos os recursos dentro dela herdam essas permissões por padrão, simplificando a governança.
- Essencialmente, a assinatura define o escopo dentro do qual os usuários podem operar e os serviços que podem utilizar.
### **Grupo de Recursos**

Um **Grupo de Recursos** no Azure é um contêiner lógico que te ajuda a gerenciar e organizar seus recursos de forma eficiente em uma única unidade. Ele serve como uma estrutura para agrupar serviços como **Máquinas Virtuais**, **Bancos de Dados**, **Redes Virtuais**, **Armazenamento** e outros recursos do Azure que compartilham o mesmo ciclo de vida, permissões e políticas.

Pense nele como uma pasta ou um projeto onde você coloca tudo o que pertence a uma aplicação ou solução específica. Isso simplifica o gerenciamento, o monitoramento e o controle de acesso dos seus recursos.

Algumas características importantes dos Grupos de Recursos são:

- Os recursos podem existir em apenas um grupo de recursos.
- Os recursos podem existir em diferentes regiões.
- Os recursos podem ser movidos para diferentes grupos de recursos.
- Os aplicativos podem utilizar vários grupos de recursos.

![[Pasted image 20250320092718.png]]
### **Recursos do Azure**

Os **Recursos do Azure** são os componentes essenciais para construir qualquer solução na plataforma. Eles representam todas as **instâncias de serviços** que você provisiona, configura e gerencia no Azure.

![[Pasted image 20250320092712.png]]

Em resumo, tudo o que você usa no Azure é um recurso, incluindo uma vasta gama de elementos como:

- **Armazenamento**: Contas para gerenciar blobs, arquivos, filas e tabelas.
- **Máquinas Virtuais (VMs)**: Servidores virtuais Linux ou Windows para hospedar aplicações e cargas de trabalho.
- **Redes**: Componentes como redes virtuais, sub-redes, balanceadores de carga, firewalls e gateways que garantem a conectividade segura dos seus serviços.
- **Bancos de Dados**: Opções gerenciadas como Azure SQL Database, Azure Cosmos DB e bancos de dados para MySQL/PostgreSQL.
- **Serviços de Aplicativos**: Plataformas para hospedar aplicações web, APIs e microsserviços, como Azure App Service e Azure Functions.
- **Serviços de IoT**: Soluções para conectar, monitorar e gerenciar dispositivos de Internet das Coisas.
- **Ferramentas de IA/Machine Learning**: Serviços para construir e implantar modelos de inteligência artificial.

Cada recurso possui suas próprias configurações e custos, e são gerenciados dentro de **Grupos de Recursos** e **Assinaturas**. Eles são a matéria-prima com a qual você constrói sua infraestrutura e aplicações na nuvem.