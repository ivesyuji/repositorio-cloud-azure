___
## **Microsoft Entra ID (Antigo Azure Active Directory)**

O **Microsoft Entra ID** é o serviço de **gerenciamento de identidades e acesso (Identity and Access Management - IAM) baseado em nuvem** da Microsoft. Ele funciona como o diretório central para usuários, grupos e dispositivos, permitindo que as organizações gerenciem o acesso a aplicativos e recursos tanto na nuvem (Azure, Microsoft 365) quanto no local.

Funcionalidades Chave do Microsoft Entra ID:

- **Autenticação:** Gerencia o processo de verificação da identidade de usuários e serviços que tentam acessar recursos, garantindo que apenas entidades legítimas possam entrar.
- **Login Único (SSO - Single Sign-On):** Permite que os usuários se autentiquem uma única vez e acessem múltiplos aplicativos e serviços (incluindo serviços da Microsoft como Office 365, e também aplicativos de terceiros como Google, YouTube, Facebook e milhares de outros) sem precisar inserir credenciais repetidamente.
- **Gerenciamento de Aplicativos:** Fornece um painel centralizado para registrar e gerenciar o acesso a aplicativos em nuvem e no local, controlando quem pode usá-los.
- **Negócios para Negócios (B2B):** Facilita a colaboração segura com parceiros externos, fornecedores e clientes, permitindo que eles acessem recursos específicos da sua organização usando suas próprias identidades.
- **Gerenciamento de Dispositivos:** Permite registrar e gerenciar a identidade de dispositivos (como laptops e smartphones) que acessam os recursos da sua organização, garantindo a conformidade e a segurança.

![[Pasted image 20250323112254.png]]
### **Benefícios Adicionais para Cenários Específicos:**

- **Simplificação de Domínios na Nuvem:** Permite obter os benefícios de serviços de domínio baseados em nuvem (como autenticação, gerenciamento de grupos e usuários) **sem a complexidade de gerenciar seus próprios controladores de domínio** (que são máquinas virtuais que precisam de manutenção e patches).
- **Suporte a Aplicativos Legados:** Capacita a execução de aplicativos herdados (que não podem utilizar padrões de autenticação modernos, como OAuth 2.0) na nuvem, estendendo sua vida útil e capacidade de integração.
- **Sincronização Híbrida:** Permite **sincronizar automaticamente identidades** de ambientes Active Directory (AD) locais para o Microsoft Entra ID, criando um ambiente de identidade híbrido e coeso.

___
## **Comparando Autenticação e Autorização**

Embora frequentemente usadas juntas, autenticação e autorização são processos distintos, mas complementares, no gerenciamento de acesso:
### **Autenticação**

- Identifica a pessoa ou serviço buscando acesso a um recurso.
- Solicita credenciais de acesso legítimo.
- Base para criar princípios de identidade e controle de acesso seguros

### **Autorização**

- Identifica a pessoa ou serviço buscando acesso a um recurso.
- Solicita credenciais de acesso legítimo.
- Base para criar princípios de identidade e controle de acesso seguros
### **Autenticação Multifator (MFA)**

A **Autenticação Multifator (MFA)** é uma camada de segurança essencial que aprimora a proteção das identidades.

- **Funcionalidade:** Fornece segurança adicional exigindo **dois ou mais elementos de autenticação** para uma autenticação completa bem-sucedida. Isso significa que, mesmo que uma senha seja comprometida, a identidade ainda estará protegida.
- **Tipos de Fatores:** Os fatores de autenticação são geralmente de três categorias:
    1. **Algo que você sabe** (ex: senha, PIN)
    2. **Algo que você tem** (ex: celular para código SMS, token de hardware, aplicativo autenticador)
    3. **Algo que você é** (ex: impressão digital, reconhecimento facial)

### **Autenticação B2B do Microsoft Entra External ID**

A **Autenticação B2B (Business-to-Business)** do Microsoft Entra External ID (anteriormente parte do Azure AD B2B) é um recurso que permite que sua organização colabore com usuários externos (parceiros, fornecedores, clientes) de forma segura e eficiente.

- **Como funciona:** Ele permite que usuários de fora da sua organização **acessem seus aplicativos e recursos usando suas próprias identidades**, sem a necessidade de criar contas de usuário em seu próprio diretório.
- **Benefícios:** Simplifica o gerenciamento de contas de convidados, melhora a segurança e a conformidade, e facilita a colaboração.

Fornece segurança adicional para as identidades, exigindo dois ou mais elementos para autenticação completa.

![[Pasted image 20250323112920.png]]
![[Pasted image 20250323113121.png]]

___
## Acesso Condicional

O **Acesso Condicional** no Microsoft Entra ID (antigo Azure Active Directory) é uma ferramenta poderosa de segurança que atua como um **mecanismo de política centralizada**. Ele é usado para **reunir sinais**, **tomar decisões inteligentes** e **impor políticas organizacionais** para controlar o acesso a aplicativos e recursos.

As políticas de Acesso Condicional podem ser configuradas com base em diversos sinais, incluindo:

- **Associação de Usuário ou Grupo:** Quem está tentando acessar (usuários específicos, membros de um grupo).
- **Local do IP:** De onde o usuário está tentando se conectar (rede corporativa, local confiável, ou um IP de um país bloqueado).
- **Dispositivo:** Qual dispositivo está sendo usado (dispositivo compatível, gerenciado, ou um dispositivo desconhecido).
- **Aplicativo:** Qual aplicativo ou serviço está sendo acessado (Office 365, um aplicativo corporativo, etc.).
- **Detecção de Risco:** Sinais de risco em tempo real do Microsoft Entra ID Protection (como login de localização atípica ou credenciais vazadas).

![[Pasted image 20250323113423.png]]

- Gerenciamento de acesso de granularidade fina.
- Divida as tarefas dentro da equipe e conceda somente a quantidade de acesso de que os usuários precisam para trabalhar.
- Habilite o acesso ao portal do Azure e o controle de acesso aos recursos.

![[Pasted image 20250323113711.png]]
___
## Modelo Confiança Zero

O **Modelo de Confiança Zero** é uma estratégia de segurança que parte do princípio de **"nunca confiar, sempre verificar"**. Em vez de confiar em usuários ou dispositivos dentro da rede corporativa, cada tentativa de acesso é tratada como se viesse de uma rede não confiável.

![[Pasted image 20250323113724.png]]

Seus princípios fundamentais são:

1. **Verificar Explicitamente:** Autenticar e autorizar todas as conexões de forma explícita, sem pressupor confiança.
2. **Usar Acesso com o Menor Privilégio:** Conceder aos usuários apenas o mínimo de acesso necessário para suas tarefas.
3. **Assumir Violação:** Projete sistemas e processos assumindo que uma violação já pode ter ocorrido, e esteja pronto para mitigar seus impactos.

___
## Modelo Proteção Completa

A **Proteção em Profundidade** (também conhecida como Defesa em Profundidade) é uma abordagem de segurança que emprega uma **estratégia de defesa em camadas** para proteger sistemas de computador.

- Ela fornece **vários níveis de proteção** (física, identidade, rede, computação, dados, aplicativo).
- A ideia é que, se um ataque conseguir penetrar uma camada de segurança, ele será **isolado das camadas subsequentes**, dificultando que o ataque atinja o alvo final. Isso cria múltiplos obstáculos para um atacante.

![[Pasted image 20250323113823.png]]

___
## Microsoft Defender para Nuvem

O **Microsoft Defender para Nuvem** é um serviço abrangente de **gerenciamento de postura de segurança em nuvem (CSPM)** e **proteção contra ameaças (CWPP)** que opera tanto em ambientes Azure quanto em data centers locais (híbridos) e outras nuvens.

- **Fornece recomendações de segurança** acionáveis para melhorar sua postura de segurança, baseadas em melhores práticas e padrões de conformidade.
- **Detecta e bloqueia malware** em tempo real em suas VMs e outros recursos.
- **Analisa e identifica ataques potenciais** contra seus recursos, fornecendo alertas de segurança e inteligência sobre ameaças.
- Oferece **controle de acesso just-in-time (JIT)** para portas de máquinas virtuais, que reduz drasticamente a superfície de ataque ao abrir portas de gerenciamento apenas quando necessário e por um tempo limitado.

![[Pasted image 20250323113931.png]]


