Desafio: 02-Microsoft Azure - Benefícios da Computação em Nuvem  
Módulo: 01-Conceito de Nuvem

O que é? Fazer um resumo sobre o que foi aprendido até o momento neste treinamento de certificação da Microsoft AZ-900.

Resumo:
- Benefícios da Nuvem
    
    ```mermaid
    flowchart LR
    A[Benefícios] --> B[1 - Alta disponibilidade]
    A --> C[2 - Escalabilidade]
    A --> D[3 - Confiabilidade]
    A --> E[4 - Previsibilidade]
    A --> F[5 - Segurança]
    A --> G[6 - Governança]
    A --> H[7 - Capacidade de gerenciamento]
    ```
    
1. Alta Disponibilidade
    - Disponibilidade tem a ver com estar sempre disponível.
    - Está relacionado a **SLA** (Service Level Agreement).
    - A Microsoft oferece um serviço que possui certo grau de disponibilidade, como qualquer recurso físico que a empresa fizesse em sua estrutura. Entretanto, na nuvem o fornecedor consegue oferecer uma espécie de seguro para aumentar essa disponibilidade com sub-serviços suplantados ao original contratado.
    - SLA Azure
        
        
        | 99% | ou | 99,9% | ou | 99,95% | ou | 99,99% |
        | --- | --- | --- | --- | --- | --- | --- |
    - Essas garantias de disponibilidade e SLA são garantidos em contrato, onde o cliente recebe um crédito, caso a indisponibilidade ocorra sem a devida cobertura e além do previsto. Este é o exemplo do cliente ressarcido com créditos na próxima fatura, caso não consiga garantir o serviço com a disponibilidade dentro do previsto (Tempo, Qtd de indisponibilidade, etc).
        - Exemplo:
        `EntraID` (Atual **Serviço de Autenticação** / O antigo era `Active Directory`) para de funcionar.
            - OBS: O `EntraID` é **Cloud Native** (Nativo de Nuvem).
        - ❓Quando o EntraId, por exemplo, fica indisponível, como podemos verificar se realmente está indisponível ou se é outro problema?
        R.: A Microsoft possui um site que mostra todas as localidades a nível global, mostrando os serviços e suas respectivas situações de disponibilidade.
    - **Degradado** ⇒ Termo utilizado quando o serviço está com algum problema, podendo inclusive ser indisponibilidade.
    - A **alta disponibilidade** se concentra em garantir a disponibilidade máxima, independentemente de interrupções ou eventos que possam ocorrer.
    - Os créditos de ressarcimento são realizados na conta do usuário na Microsoft, como uma espécie de Voucher/Crédito para a próxima fatura.
2. Escalabilidade (elasticidade é um tipo especifico de escalabilidade)
    - A **Escalabilidade** refere-se à capacidade de ajustar recursos para atender à demanda.
    - A capacidade de escalar significa que você poderá adicionar mais recursos para lidar melhor com o aumento da demanda.
        - Exemplo p/ entender:
        Imagine o ambiente on-premises, onde o File-Server chega em 100% da sua capacidade máxima de armazenamento.
        Então, será necessário a adição de um recurso, de colocar mais um disco no servidor.
        Isso é exemplo de escalar, onde se redimensiona a capacidade de recursos da infra ou serviço.
    - Não paga além do necessário pelos serviços. Pois o ***Modelo Baseado em Consumo*** permite pagar apenas pelo que usar.
    - **Se a demanda diminuir**, poderá reduzir seus recursos e consequentemente reduzir os custos.
    - **Escala Vertical** permite adicionar recursos computacionais.
    Exemplo:
    Precisa adicionar mais CPU ou RAM à uma VM (Máquina Virtual) para desenvolvimento de um aplicativo que precise de mais capacidade de processamento.
    - A **elasticidade** é uma *extensão* da **escalabilidade**, adicionando a capacidade de ajuste **automático** e **autônomo** dos recursos conforme necessário.
        - Um bom exemplo de uso da **Elasticidade** é a **Black Friday**.
        - Com a Elasticidade, se você experimentasse um salto repentino acentuado na demanda, seus recursos implantados poderiam ser expandidos automaticamente ou manualmente.
        - Pois podemos redimensionar os ambientes com base em requisições.
        Exemplo:
        Poder adicionar VMs ou Contêineres por meio da expansão.
        - Da mesma forma, se houver uma queda significativa da demanda, os recursos implantados poderão ser reduzidos horizontalmente.
    - Diferenças (≠) Sutis dos Conceitos:
        - **Escalabilidade** (Scalability) ⇒ Poder de redimensionar.
            - **Vertical** ⇒ Aumento ou redução de capacidade de um recurso individual.
            - **Horizontal** ⇒ Adicionar ou retirar uma instância completa/inteira.
        - **Elasticidade** (Elasticity) ⇒ É uma Extensão da Escalabilidade. Redimensionamento em tempo real de forma dinâmica e automática.
3. Confiabilidade
    - Devido à estrutura descentralizada, a nuvem naturalmente dá suporte a uma infraestrutura **confiável** e **resiliente**.
        
        > ***Resiliente** = Mesmo sofrendo impacto, consegue retornar a sua forma original*.
        > 
        
        > Reflexão:
        Pois se uma determinada localidade sofre algum impacto, o uso do serviço pode continuar automaticamente por outra localidade, tornando os serviços de nuvem oferecidos de certa forma mais confiáveis.
        > 
4. Previsibilidade
    - A **previsibilidade** na nuvem permite que você avance com confiança, seja no **desempenho** ou no **custo**.
    - Ambas são influenciadas pelo ***Microsoft Azure Well-Architected Framework***.
5. Segurança
    - A nuvem oferece ferramentas de segurança que atende às necessidades dos clientes.
    - Mas é importante lembrar que a implementação de muitas delas devem ser realizadas pelo cliente.
6. Governança
    - Governança está relacionado a como vamos gerir nossos recursos.
    - A auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora de conformidade com seus padrões corporativos e fornece estratégias de mitigação.
    - Uma empresa possui padrões, normas e regulamentos estabelecidos pelas autoridades do seu setor de atuação, no qual precisam ser seguidos. Além disso, é necessário seguir determinados padrões ou protocolos de segurança e confidencialidade.
    - Exemplo, podemos restringir o uso de determinado recurso em uma região, porque naquela localidade ele pode não ser permitido.
7. Gerenciabilidade
    - Um dos principais benefícios da computação em nuvem são as opções de capacidade de gerenciamento.
    - O gerenciamento da nuvem diz respeito a gerenciar seus recursos de nuvem.

- Tabela de SLA do Azure:
    
    ![image.png](attachment:1e51741e-b848-4f0b-8118-6ed9395f960d:image.png)

.
