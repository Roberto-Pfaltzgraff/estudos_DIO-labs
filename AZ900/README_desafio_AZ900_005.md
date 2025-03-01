# Desafio: 05-Microsoft Azure - Configurando Recursos e Dimensionamentos em VMs na Azure  
Módulo: 01-Conceito de Nuvem  
---
  
## O que fazer?  
1. Fazer um resumo sobre o que foi aprendido até o momento neste treinamento de certificação da Microsoft AZ-900.  
   OBS: Apenas as últimas atividades desde o desafio anterior a este.  

---
## Parte 1 - Resumo:  
Configurando Recursos e Dimensionamentos em VMs na Azure  
- Criando Máquina Virtual (VM)
    - 1ª informação já estará selecionada, devido a nossa conta não ser corporativa e possuirmos apenas 1 assinatura.
    - O dado seguinte é o Grupo de Recursos. Estamos registrando o `AZ-900-Lab-DIO` criado anteriormente.
    - Nome da Máquina Virtual a ser criada. Coloquei: `vm-001-lab-DIO-AZ900`.
    - Região.
    - Opção de disponibilidade. Neste caso, escolheremos a de Nenhuma Redundância de Infraestrutura Necessária.
    Caso escolhêssemos outra opção, teríamos que escolher as informações seguintes de zonas.
        - ❗Neste vídeo, ela explicou sobre “***Dimensionamento de Máquinas Virtuais***”.
            - Nesta opção podemos configurar o *Dimensionamento Escalar **Automático***, estabelecendo **limites** inferiores e superiores.
            - Onde definimos os Gatilhos de *Escala* ou *Redução* **horizontal**. E sua respectiva quantidade de Crescimento ou Redução.
            Exemplo:
            Posso definir que se a CPU atingir ou passar a 80% de uso, aumente em 2 instância.
            E se a CPU a cair para 40% ou menos de uso, reduzir em 2 instâncias.
            OBS:
            Tudo isso considerando os limites Inferior e Superior definidos anteriormente.
            Exemplo: Limite inferior = 2 e superior = 20 de instâncias de VMs.
            - Um último valor nessa configuração é a `Duração de Consulta`. Que é o tempo entre uma verificação e a seguinte da situação ser verificada se atingiu o mínimo ou máximo do Gatilho.
            - A opção de dimensionamento automático estava desabilitado para mim. Mas aparecia no vídeo da instrutora.
            Será uma tarefa para posteriormente descobrir.
    - Explicou sobre a opção `Executar com desconto de Spot do Azure` de marcar ou desmarcar. Está opção permite que utilize a VM por um preço bem abaixo. Entretanto, se alguém que paga o preço cheio, sem opção, surgir, sua VM será derrubada até a disponibilidade ficar vaga novamente.
    Veja o que está escrito no Hint deste campo:
        
        > *O Azure Spot oferece a capacidade não usada do Azure a uma taxa com desconto, ao contrário dos preços pagos conforme o uso. As cargas de trabalho devem ser tolerantes à perda de infraestrutura, pois o Azure pode recuperar a capacidade para as cargas de trabalho pagas conforme o uso.*
        > 
        
        > [Saiba mais](http://go.microsoft.com/fwlink/?LinkId=2104270)
        > 
    - Tamanho de máquina onde iremos especificar uma com a capacidade computacional que desejamos ou precisamos.
    - Informar Conta de Usuário. Login e Senha.
    - E Regras de Portas de Entradas deixamos com as opções default.
    Embora não seja recomendado pelo próprio alerta do Azure por questão de segurança.
    OBS: A instrutura deixará assim, para retomar esse ponto mais a frente.
    - Clicar no botão `Avançar para Discos`.
    - Tipo de Disco de SO selecionado foi o Premmium, pois é o mais recomendado para carga de trabalho.
    - ❗Campo `Excluir com a VM` de marcar e desmarcar. Alerta: É recomendado que deixe marcado.
    Pois ao excluir a VM o Disco pode ficar ativo.
    
    Ela citou caso do cliente que reclamou estar pagando caro. E sua 1ª ação foi executar operação de descobrir discos órfãos.
    - Clicar no botão `Avançar para Rede`.
    - Campo Rede Virtual. Por default o Azure traz um nome para criação de um novo Vnet. Esse nome é o mesmo nome da VM acrescido do sufixo `-vnet`.
    OBS: A VNet que criamos anteriormente não aparece porque a criamos na região do Sul do Brasil e esta VM estamos criando na região US East 2.
    - Os demais dados de rede tal como sub-rede são preenchidos automaticamente.
    - ❗Campo `Excluir o IP público e a NIC quando a VM for excluída` de marcar e desmarcar. Alerta: É recomendado que deixe marcado.
    Pois ao excluir a VM a Placa de Rede e o IP Público podem ficar ativos.
    - Clicar no botão `Avançar para Gerenciamento`.
    - Aqui existem opções de desligamento automático, aviso desse desligamento, opção de Backup e etc.
    - Clicar no botão `Avançar para Monitoramento`.
    - Campo **Habilitar regras de alerta recomendadas** de marcar e desmarcar.
    Quando habilitado, abre uma tela para especificar o email a ser notificado e as métricas para notificação.
    OBS: Inclusive, tem um grupo de ações a ser especificado.
    - Clicar no botão `Avançar para Avançado`.
    - Permite instalar **extensões** tal como de segurança e outras agendamento/schedule.
    Exemplos: Agent For Windows Server, Norton, Fortify, Control-M Agent e etc.
    - Não selecionamos nada para este teste.
    - Clicar no botão `Avançar para Marcas`.
    - Clicar no botão `Avançar para Revisar&Criar`.
    - Aqui é exibido a ideia do preço/custo.
- Área de Trabalho Virtual do Azure
    - Clicar na `Barra de Pesquisa`, localizada no Centro Superior da tela.
    - Digite e pesquise por área de trabalho.
    - Clique no respectivo ícone.
    - É possível criar uma imagem da área de trabalho que se quer disponibilizar para o usuário ou múltiplos usuários.
    - Clicar no botão `Criar um pool de hosts`.
    - 1ª informação já estará selecionada, devido a nossa conta não ser corporativa e possuirmos apenas 1 assinatura.
    - O dado seguinte é o Grupo de Recursos. Estamos registrando o `AZ-900-Lab-DIO` criado anteriormente.
    - Nome do Pool de Hosts a ser criado. Coloquei: `dsktop-001-lab-DIO-AZ900`.
    - Localização é o seguinte.
    - O campo `Tipo de grupo de aplicativos preferencial` possui os valores `Área de Trabalho` e `RemoteApp` como alternativas de seleção.
    Normalmente selecionamos a Área de Trabalho.
    - No grupo **Detalhes do pool de hosts** e campo `Tipo de pool de hosts` definimos se será `Em Pool` ou `Pessoal`.
    Escolhemos o **Em Pool**.
    - Depois basta seguir com o preenchimento dos demais campos e baseado na documentação.
- **Aplicativo de Funções** do Azure
    - Clicar na `Barra de Pesquisa`, localizada no Centro Superior da tela.
    - Digite e pesquise por **Aplicativo de Funções**.
    - Clique no ícone.
    - Clicar no botão `Criar Aplicativo de Funções`.
    - Aparecerá uma quadro explicativo e de seleção para escolher a **opção de hospedagem**.
    Essa opção não apareceu no vídeo da aula. Selecionei o Flexível.
    - 1ª informação já estará selecionada, devido a nossa conta não ser corporativa e possuirmos apenas 1 assinatura.
    - O dado seguinte é o Grupo de Recursos. Estamos registrando o `AZ-900-Lab-DIO` criado anteriormente.
    - Nome do Pool de Hosts a ser criado. Coloquei: `fcs-001-lab-DIO-AZ900`.
    - Região.
    - O campo `Pilha de Runtime` é de seleção, apresentando os valores .NET, Node.js, Python, Java e PowerShell Core.
    No vídeo, ao mudar essas opções, o campo Sistema Operacional também mudava seu valor entre Windows e Linux, conforme a seleção.
    Atualmente, fazendo isso no Azure, o campo do Sistema Operacional nem apareceu.  
  
--- 
  
