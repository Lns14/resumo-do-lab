# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

# Benefícios da Nuvem  

## Alta Disponibilidade  
A nuvem garante um alto nível de disponibilidade por meio de Acordos de Nível de Serviço (SLA), minimizando o tempo de inatividade.  

- **Exemplo:**  
  - SLA 99,99% → Máximo de 52 minutos de indisponibilidade por ano.  
  - SLA 99,9% → Máximo de 3 dias de indisponibilidade por ano.  

## Escalabilidade  
Capacidade de aumentar ou reduzir recursos conforme a demanda.  

- **Benefícios:**  
  - Balanceamento de carga para otimizar a distribuição do tráfego.  
  - Adaptação automática ao volume de acessos e consumo de recursos.  

## Elasticidade  
Ajuste dinâmico dos recursos com base no uso em tempo real.  

- **Exemplo:**  
  - Durante um evento como a **Black Friday**, a infraestrutura pode ser programada para escalar automaticamente.  
  - Se o consumo médio dos hosts atingir um certo percentual, novos recursos são adicionados.  
  - Um limite máximo pode ser estabelecido para evitar custos excessivos.  

## Confiabilidade  
A nuvem permite a distribuição de recursos em diversas regiões, garantindo:  

- **Redundância:** Falhas em um servidor não afetam toda a aplicação.  
- **Alta disponibilidade:** Serviços continuam funcionando mesmo em caso de falhas.  
- **Recuperação rápida:** Planos de Disaster Recovery para minimizar impactos.  

## Previsibilidade  
Garante que os processos e serviços funcionarão conforme esperado.  

## Segurança  
A nuvem oferece ferramentas para garantir a proteção dos dados e aplicações.  

- **A implementação é responsabilidade do cliente.**  
- Regras de segurança podem ser configuradas para atender às necessidades específicas de cada empresa.  

## Governança  
Permite auditoria e conformidade com políticas corporativas.  

- **Benefícios:**  
  - Monitoramento e controle dos recursos em nuvem.  
  - Definição de padrões para garantir conformidade e mitigação de riscos.  

## Gerenciabilidade  
Facilidade no gerenciamento dos recursos em nuvem, seja via interface gráfica ou comandos.  

- **Exemplo:**  
  - Gerenciamento via **portal web (UI)**.  
  - Administração via **linha de comando (CLI)** ou **API**.  


# Tipos de Serviços

## IaaS (Infrastructure as a Service)
- **Exemplo:** Infraestrutura como serviço
- **Descrição:** Recursos com maior personalização. São versões de infraestrutura sob demanda, incluindo serviços de armazenamento e redes.

## PaaS (Platform as a Service)
- **Exemplo:** Elastic Beanstalk
- **Descrição:** Plataforma como serviço. O usuário não precisa se preocupar com a infraestrutura. Oferece um ambiente completo para desenvolvimento, execução e gerenciamento de aplicações, sem a necessidade de gerenciar a infraestrutura.

## SaaS (Software as a Service)
- **Exemplo:** Microsoft 365
- **Descrição:** Software como serviço. Aplicações fornecidas como um serviço acessado pela internet, sem a necessidade de instalação.

---

## Modelo de Responsabilidade Compartilhada
- **Infraestrutura:** O provedor é responsável pela infraestrutura física, como servidores, redes e data centers.
- **Cliente:** O cliente é responsável pela gestão de aplicações, controle de virtualização, identidade e diretórios.

### Exemplo:
- **Provedor:** Infraestrutura, servidores físicos, rede e data centers.
- **Cliente:** Aplicações, controle de identidade e diretórios, contas e identidades.

  ## Regiões

Ao criar um recurso, você escolhe onde alocar. Deve verificar se sempre deve haver uma resposta, por exemplo, ou custo. 
As regiões são compostas por um ou mais datacenters muito próximos.

### Zona de Disponibilidade
Os datacenters de uma região formam uma zona de disponibilidade. 
Exemplo: se um datacenter falhar, outro assume. 
Se houver três datacenters, os serviços essenciais devem estar ativos em pelo menos um deles.

### Região
Fornece flexibilidade e escalabilidade para reduzir a latência do cliente. 
Tudo é replicado entre os datacenters para que, independentemente de uma falha, a resposta seja garantida. 
No Brasil, isso é feito para assegurar disponibilidade. Essa replicação é automática para alguns serviços.

### Regiões Soberanas
São áreas exclusivas, como a China, operadas pela 21Vianet.

## Recursos do Azure

- Máquinas virtuais
- Contas de armazenamento
- Redes virtuais
- Serviços de aplicativo

### Exemplos
- Por categoria, por projetos.
- Podem estar em regiões diferentes.
- Só podem existir dentro de um grupo.

## Assinaturas do Azure

Uma conta pode ter diversas assinaturas, porém, cada assinatura deve estar vinculada a apenas uma conta.

### Tipos de Assinaturas
- Assinatura por projeto
- Assinatura de desenvolvimento
- Assinatura de produção (uso dos usuários)
- Assinatura de teste

Cada assinatura tem uma cobrança específica.
Uma assinatura do Azure fornece acesso autenticado e autorizado às contas do Azure.

### Limite de Acesso
Permite gerenciar e controlar o acesso aos recursos que os usuários podem provisionar.

### Gerenciamento
Aplica-se a grupos de gerenciamento.

# Passo a Passo do Azure Search

1. Criar um novo recurso. Azure AI Search  
2. Criar um novo recurso. Azure AI Services
3. Criar uma Storage Account
4. Criar novo contêiner
5. Fazer o upload dos arquivos no contêiner
6. Importar os dados no AI Search
7. Realizar busca, ex: search = locations: 'Chicago' (o resultado vem em JSON)
