# Desafio: 04-Microsoft Azure - Construindo Arquiteturas no Azure  
Módulo: 01-Conceito de Nuvem  
---
  
## O que fazer?  
1. Fazer um resumo sobre o que foi aprendido até o momento neste treinamento de certificação da Microsoft AZ-900.
   OBS: Apenas as últimas atividades desde o último desafio.  
2. Montar passo a passo para criação de Grupo de Recursos e Rede Virtual no Azure.

---
## Parte 1 - Resumo:  
Componentes de Arquitetura do Azure  
- Regiões
    - Mapa e Globo dos Datacenters da Microsoft: [https://datacenters.microsoft.com/globe/explore/](https://datacenters.microsoft.com/globe/explore/)
    - Atualmente o Azure oferece mais de 60 regiões globalmente, cobrindo mais de 140 países. Isso é mais do que qualquer provedor de nuvem oferece.
    - Os preços variam de região, elas não segue uma tabela, pois cada região possui suas particularidades, tal como impostos e restrições.
    - As regiões são compostas por um ou mais datacenters, normalmente são 3, caracterizando assim uma zona de disponibilidade.
    
    OBS: Esses Datacenters se comunicam por um Backbone da Microsoft.
    - Desta forma, a Região é composta por um grupo de Datacenters.
    - A Microsoft garante as questões de conformidade dos dados. Está de acordo com LGPD local.
    - Zona de Disponibilidade ⇒ Vamos entender cada uma como sendo um datacenter.
    - Região do Azure e suas Zonas de Disponibilidades
        
        ![AZ900_Desafio04_img_001.png](https://iili.io/3dcbra2.png)
        <!-- [https://freeimage.host/i/3dcbra2](https://iili.io/3dcbra2.png) -->
        
    - As Zonas de Disponibilidade juntas fornecem proteção contra tempo de inatividade devido a falha de Zona/Datacenter.
    - Separe fisicamente os datacenters dentro da mesma região.
    - Cada Datacenter é equipado com *alimentação*, *resfriamento* e *rede* de forma independente.
    - Esses Datacenters de uma determinada Região são conectados por redes privadas de fibra ótica.
- Pares de Regiões
    - Cada Região possuirá uma Região Secundária, para no caso de indisponibilidade da original, a secundária conseguir atender as demandas da Principal.
    - A distância de separação entre as regiões pares é de no mínimo 300 milhas (≈480 km).
    - A replicação é automática, apenas para alguns serviços.
    - Recuperação de região priorizada em caso de interrupção. Quem não tiver contigência de recuperação, terá que aguardar a recuperação da região contratada.
    - As atualizações são distribuídas sequencialmente para minimizar o tempo de inatividade.
    - Link da Web:
        - [https://aka.ms/PairedRegions-ptb](https://aka.ms/PairedRegions-ptb)
- Regiões Soberanas do Azure
    - Visa atender Nações Soberanas, diferentes de cliente pessoas física e jurídica.
    - Serviços Governamentais dos EUA
        - Atende às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções.
    - Azure China
        - A Microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com as regulamentações governamentais.
        - Recursos do Azure China:
            - Todos os dados permanecem na China para garantir a conformidade.
            - Instância fisicamente separada dos serviços de nuvem do Azure operados pela 21Vianet.
- Recursos do Azure
    - Os recursos do Azure são componentes como *armazenamento*, *máquinas virtuais* e *redes* que estão disponíveis para criar soluções de nuvem.
    - Logo se as Regiões refere-se a parte física e como estão estruturadas fisicamente.
    Os Recursos são o que podemos utilizar, o que é oferecido pelo Azure para utilizarmos como clientes/usuários.
        
        ![AZ900_Desafio04_img_002.png](https://iili.io/3dlJeZ7.png)
        
- Grupos de Recursos
    - Nenhum Recurso é criado sem que haja um Grupo de Recursos.
    Pois o Recurso fará parte de um determinado Grupo de Recursos.
    - É possível migrar um determinado Recurso de um Grupo de Recursos para outro.
    Permitindo assim a organização e reorganização.
    - Um Grupo de Recursos é um contêiner que você usa para gerenciar e agregar recursos em uma única unidade.
- Assinaturas do Azure
    
    ![AZ900_Desafio04_img_003.png](https://iili.io/3dl2lqX.png)
    
    - A Assinatura é muito útil no mundo corporativo, onde teremos pessoas e grupo de pessoa com responsabilidades diferentes na criação e utilização de recursos do Azure.
    - Uma **Conta Azure** pode possuir diversas **Assinaturas**.
    - Porém, uma **Assinatura** pode estar associada a somente uma **Conta Azure**.
    - Cada Assinatura possuirá uma fatura correspondente ao que consumiu.
    As Faturas de cada Assinatura será paga pela Conta Azure ao qual essas Assinaturas estão vinculadas.
        
        > Analogia:
        É similar ao pai que leva sua família a um Resort. O pai faz o registro no hotel e cria uma conta. O hotel/Resort distribui aquelas pulseiras que dão acesso aos quartos alocados e ao consumo de bebidas e comidas. Essas pulseiras são similares as assinaturas, onde cada membro da família estará consumindo por meio da pulseira e gerando uma fatura. O Resort é o Azure oferecendo tudo a ser consumido. E a conta que o pai registrou no Resort é a Conta Azure, onde no final da estádia irá reunir todas as faturas dos membros e deverá pagar a conta.
        > 
    - Uma assinatura do Azure fornece a você acesso autenticado e autorizado aos recursos do Azure.
    - Limite de cobrança:
    Gere relatórios de cobrança e faturas separados para cada assinatura.
    - Limite do controle de acesso:
    Gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas.
- Grupos de Gerenciamento
    
    ![AZ900_Desafio04_img_004.png](https://iili.io/3dlBM7e.png)
    
    - Grupos de Gerenciamentos ajudam na organização, padronização realizando o agrupamento de assinaturas que terão mesmas características e segurança.
    - Os grupos de gerenciamento podem incluir várias assinaturas do Azure.
    - As assinaturas herdam as condições aplicadas ao grupo de gerenciamento.
- Link de referência:
    - eLearn Microsoft deste assunto: [https://learn.microsoft.com/pt-br/training/modules/describe-core-architectural-components-of-azure/1-introduction](https://learn.microsoft.com/pt-br/training/modules/describe-core-architectural-components-of-azure/1-introduction)
    - Infraestrutura global da Microsoft: [http://azure.microsoft.com/en-us/explore/global-infrastructure](http://azure.microsoft.com/en-us/explore/global-infrastructure)
    - Globo com mapeamento da estrutura mundial da Microsoft: [https://datacenters.microsoft.com/globe/explore/](https://datacenters.microsoft.com/globe/explore/)
    - Instruções do Desafio de Projeto e minhas ações:
        - Criar um Grupo de Recursos no Azure!
        - Criei com esse nome ⇒ `AZ-900_Lab_DIO`
        - Criar Rede Virtual!
        - Criei a `v-net-001`

## Parte 2 - Passo a passo na criação de recursos do Azure:  
### 🔹 Guia 1: Como Criar um **Grupo de Recursos** no Microsoft Azure via Portal do Azure  
Um **Grupo de Recursos** no Azure é um contêiner lógico que permite gerenciar e organizar recursos como máquinas virtuais, bancos de dados e redes.  
  
1️⃣ Acesse o Portal do Azure  
- Vá para https://portal.azure.com e faça login com sua conta.
  
2️⃣ Navegue até "Grupos de Recursos"  
- No menu esquerdo, clique em "Grupos de Recursos".  
- Se não encontrar, use a barra de pesquisa no topo e digite "Grupos de Recursos".
  
3️⃣ Criar um Novo Grupo de Recursos  
- Clique no botão “Criar”.
  
4️⃣ Preencha os Detalhes  
- Assinatura: Selecione a assinatura do Azure onde deseja criar o grupo.  
- Nome do Grupo de Recursos: Escolha um nome único e descritivo (exemplo: MeuGrupoRecursos).  
- Região: Escolha a localização geográfica onde os recursos serão armazenados.  
🔹 Exemplo: East US, Brazil South, West Europe.
Dica: Escolha uma região próxima de seus usuários para reduzir latência.
5️⃣ Revisar e Criar
- Clique em "Revisar + Criar".  
- Após a validação, clique em “Criar” para finalizar.  
- ✅ Pronto! Seu grupo de recursos foi criado com sucesso.  
  
### 🔹 Guia 2: Como Criar uma **Rede Virtual (VNet)** no Microsoft Azure via Portal do Azure  
Uma **Rede Virtual (VNet)** no Azure permite conectar recursos como máquinas virtuais, bancos de dados e aplicativos dentro de uma rede privada segura.  
  

1️⃣ Acesse o Portal do Azure  
- Vá para https://portal.azure.com e faça login com sua conta.
  
2️⃣ Navegue até "Rede Virtual"  
- No menu esquerdo, clique em "Rede Virtual".  
- Se não encontrar, use a barra de pesquisa no topo e digite "Rede Virtual".
  
3️⃣ Criar uma Nova Rede Virtual  
- Clique no botão “Criar”.
  
4️⃣ Preencha os Detalhes  
- Assinatura: Escolha a assinatura do Azure.
- Grupo de Recursos: Selecione um existente ou crie um novo.
- Nome da Rede Virtual: Escolha um nome (exemplo: MinhaRedeVirtual).
- Região: Escolha a localização (exemplo: Brazil South).  
  
5️⃣ Configurar o Espaço de Endereçamento  
- Defina um intervalo de endereços IP para a VNet (exemplo: 10.0.0.0/16).  
  
6️⃣ Configurar Sub-redes  
- Adicione uma sub-rede para segmentar a rede.  
- Exemplo:
  Nome da Sub-rede: MinhaSubRede
  Intervalo de Endereços: 10.0.1.0/24
  
7️⃣ Revisar e Criar
- Clique em "Revisar + Criar".  
- Após a validação, clique em “Criar” para finalizar.  
- ✅ Pronto! Rede Virtual criada com sucesso.  
  
--- 
  
