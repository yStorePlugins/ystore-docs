# yArmazem
<secondary-label ref="rankup"/>

### Descrição
Armazene plantações por plots!

### Versões
<secondary-label ref="1.8"/>
<secondary-label ref="1.9"/>
<secondary-label ref="1.10"/>
<secondary-label ref="1.11"/>
<secondary-label ref="1.12"/>
<secondary-label ref="1.13"/>
<secondary-label ref="1.14"/>
<secondary-label ref="1.15"/>
<secondary-label ref="1.16"/>
<secondary-label ref="1.17"/>
<secondary-label ref="1.18"/>
<secondary-label ref="1.19"/>
<secondary-label ref="1.20"/>
<secondary-label ref="1.21"/>

### Demonstração
<video src="//www.youtube.com/watch?v=K6kI8VV4F-g"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/armazem - Abrir o menu do armazem
/armazem givelimitevenda - Dá limite de venda a um jogador.
/armazem givelimitearmazem - Dá limite de armazenamento a um jogador.
/armazem add - Adiciona limite de venda a um jogador.
/armazem remove - Remove limite de venda a um jogador.
/armazem set - Seta limite de venda a um jogador.
/armazem ajuda - Envia a mensagem de ajuda
/armazem reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yarmazem.usar - Permissão para o /armazem
yarmazem.vender - Permissão para vender itens.
yarmazem.coletar - Permissão para coletar itens.
yarmazem.vendertudo - Permissão para o vender tudo.
yarmazem.givelimite - Permissão para o /armazem givelimitevenda e /armazem givelimitearmazem
yarmazem.add - Permissão para o /armazem add
yarmazem.remove - Permissão para o /armazem remove
yarmazem.set - Permissão para o /armazem set
yarmazem.help - Permissão para o /armazem ajuda
yarmazem.reload - Permissão para o /armazem reload
yarmazem.autosell - Permissão para o auto - sell</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yarmazem_limite% - Retorna a quantia de limite do jogador com formatação (1K, 1M...)
%yarmazem_limite_raw% - Retorna a quantia de limite do jogador sem formatação.
%yarmazem_limite_armazem% - Retorna a quantia de limite do armazém atual com formatação (1K, 1M...)
%yarmazem_limite_armazem_raw% - Retorna a quantia de limite do armazém atual&nbsp;sem formatação.
%yarmazem_armazenado% - Retorna a quantia de plantações armazenadas no plot com formatação
%yarmazem_armazenado_raw% - Retorna a quantia de plantações armazenadas no plot sem formatação
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yArmazem/
    ├── limites/
    │    ├── limite_armazem.yml
    │    └── limite_venda.yml
    ├── menus/
    │    ├── principal.yml
    │    └── recompensas.yml
    ├── bonus.yml
    ├── config.yml
    ├── plantacoes.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="limites" collapsible="true">
<chapter title="limite_armazem.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de armazenamento
Ativar: true

# Quantia que dá ao registrar.
Default: 10

# O limite vai ser total ou por plantação?
LimiteTotal: false

# Quantia máxima que cada plot terá de limite
# deixe 0 para ser infinito
Maximo: 0

# Compra de limite por menu
AdicionarPorLevel: 25
Prices-PerLevel:
  price1:
    provider: 'Money'
    display: 'Money'
    price: 10000.0

Item:
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  ID: 0
  Data: 0
  Glow: true
  Name: '&bLimite do armazém'
  Lore:
    - '&fQuantia: &a{quantia}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
]]>
</code-block>
</chapter>

<chapter title="limite_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de venda
Ativar: true
# Deixar o valor fixo do "Fixos" abaixo
Fixo: true
# Configurações do limite ativável ( apenas se o "Fixo" estiver false )
Ativavel:
  # Quantia que dá ao registrar.
  Default: 10
  Item:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    ID: 0
    Data: 0
    Glow: true
    Name: '&bLimite de venda do armazém'
    Lore:
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em true, assim desabilitando o uso do item ativável e os máximos.
Fixos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.fixo.membro'
    # Quantia de limite que terá
    Limite: 100

# O Maximos serve para definir quanto de limite o jogador poderá ativar.
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em false, assim habilitando o limite ativável e os máximos.
Maximos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.max.membro'
    # Quantia máxima de limite que poderá ter.
    Maximo: 100
]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Armazém de plantações'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
AnteriorSlot: 18
ProximoSlot: 26
Plantacao:
  Nome: '&b{display}'
  Lore:
    - '&fQuantia: &a{quantia}&f.'
    - '&fPreço unitário: &a{unitario}&f.'
    - '&fPreço total: &a{total}&f.'
    - ''
    - '&7Clique com esquerdo para vender.'
    - '&7Clique com direito para coletar.'
Itens:
  Informacoes:
    Slot: 30
    CustomSkull: false
    URL: ''
    ID: 339
    Data: 0
    Glow: true
    Name: '&aInformações'
    Lore:
      - '&fItens armazenados: &b{itens}&f.'
      - '&fQuantia de tipos: &b{tipos}&f.'
      - ''
      - '&fSeu limite: &a{limite_venda}&f.'
      - '&fLimite do armazem: &a{limite_armazem}&f.'
      - '&fPlantações armazenadas: &a{armazenado}&f.'
      - '&fSeu bonus: &b{bonus}%&f.'
      - '&fValor da bolsa: &a{bolsa}%&f.'
  Vender:
    Slot: 32
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/d883f946202bbdf25f8a1062e8c3317194333128207c89a474bde300c533dc3c'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aVender tudo'
    Lore:
      - '&f* Uso exclusivo &6VIP&f.'
    Lore perm:
      - '&7Clique para vender todos os itens.'
  Recompensas:
    Slot: 33
    material: 'CHEST'
    name: '&aRecompensas'
    lore:
      - ''
      - ' &fRecompensas no armazém: &a{rewards}&f.'
      - ''
      - '&7Clique para gerenciar'
  AutoSell:
    Slot: 34
    material: 'GOLD_INGOT'
    name: '&aAuto-Sell'
    lore:
      - '&7Venda automaticamente enquanto'
      - '&7você estiver dentro do plot.'
      - ''
      - ' &fAtivado: &a{status}&f.'
      - ''
      - '&aClique para alternar'
  AutoSell permissao:
    material: 'GOLD_INGOT'
    name: '&aAuto-Sell'
    lore:
      - '&7Venda automaticamente enquanto'
      - '&7você estiver dentro do plot.'
      - ''
      - '&cVocê não tem permissão.'
  LimiteUpgrade:
    Slot: 28
    material: FIREBALL
    name: '&aUpgrade de Capacidade'
    lore:
      - ''
      - ' &fAtual: &7{limite_armazem_atual}/{limite_armazem_maximo}&f.'
      - ' &fCusto para +{limite_armazem_addperlevel}: &7{Money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  LimiteUpgradeMaximo:
    material: FIREBALL
    name: '&aUpgrade de Capacidade'
    lore:
      - ''
      - ' &fAtual: &7{limite_armazem_atual}/{limite_armazem_maximo}&f.'
      - ''
      - '&cEste armazém já está no máximo.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Vender:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&8Armazém recompensas'
size: 54
slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
previous-slot: 18
next-slot: 26
back-slot: 48
#
empty-slot: 22
collect-slot: 50
#
items:
  empty:
    material: 'WEB'
    name: '&eVazio...'
    lore: [ '&7Nenhuma recompensa para', '&7coletar.' ]
  collect:
    material: 'a6cc486c2be1cb9dfcb2e53dd9a3e9a883bfadb27cb956f1896d602b4067'
    name: '&eRecolher tudo'
    lore: [ '&7Clique para recolher', '&7todas as recompensas.' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender as platanções.
Bonus:
  membros:
    Ordem: 1
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true

# Comandos e aliases do plugin
Comando:
  Comando: 'armazem'
  Aliases: [ ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Mundos que irá funcionar o armazem
# Deixe ALL para todos
Mundos plot:
  - 'MundoPlot'

# Mundos que não irá funcionar o armazem
# Útil se você usa o ALL no "Mundos plot"
Mundos plot blacklist: []

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Opções gerais
Opcoes:
  # Ativar o sistema de bolsa
  Bolsa: false
  # Ativar a coleta de plantações
  Coletar: true
  # Ativar a venda de plantações
  Vender: true
  # Ativar a venda de tudo
  Vender tudo: true
  # A opção vender tudo ignorar o limite
  # false = ignorar o limite
  Tudo limite: true
  # Armazenar mesmo com o jogador offline
  Armazenar off: false
  # Armazenar mesmo com os jogadores afk
  Armazenar afk: false
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Acesso para quem está com add na plot
  Plot add: true
  # Acesso para quem está com trust na plot
  Plot trust: true
  # Ativar o sistema de atualizar o menu do armazém automaticamente enquanto estiver aberto
  MenuUpdater: true
  # Coletar o disponível no inventário (sem ter que digitar no chat)
  ColetarDisponivel: false
  # Armazenar itens com meta? (nome e/ou lore, nbt)
  Armazenar meta: false
  # Ativar a coleta usando o botão Q para coletar o disponível no inventário
  Botao Q: true
  # Aparecer a plantação no armazém mesmo sem ter uma unidade
  Aparecer sem: true
  # Ativar o sistema de recompensas
  # Pode GERAR LAG
  Recompensas: false
  # Tempo para depositar as recompensas pendentes
  Recompensas tempo: 180
  # Fechar menu ao vender uma plantação
  Fechar vender: false
  # Fechar menu ao vender todas as plantações
  Fechar vender todos: false
  # Fechar menu ao coletar uma plantação
  Fechar coletar: false
  # Delay do auto-sell
  # em segundos
  AutoSell-delay: 5
  # Delay entre vendas do sell-all para o player
  # em segundos
  Player-SellAll-delay: 5

# Sistema de auto-break quando crescer um bloco
AutoBreak:
  Ativar: true
  Blocos:
    bloco1:
      Tipo: 'CACTUS'
      Drop: 'CACTUS'
    bloco2:
      Tipo: 'SUGAR_CANE_BLOCK'
      Drop: 'SUGAR_CANE'

# Mensagens em title do plugin
Title:
  Vendeu: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA!<nl>&fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens em actionbar do plugin
Actionbar:
  Vendeu: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA! &fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Terreno permissao: '&cVocê não tem permissão neste terreno.'
  Sem dono: '&cEste terreno não tem dono.'
  Terreno nulo: '&cVocê não está em um terreno.'
  Mundo: '&cEste mundo não está cadastrado.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Deu: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Max limite: '&cVocê já chegou no máximo.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Vendeu: '&aVocê vendeu &7x{quantia} {display}&a e ganhou &6{money}&a coins! {bonus}'
  Vendeu tudo: '&aVocê vendeu &7x{quantia} em plantações &a e ganhou &6{money}&a coins! {bonus}'
  Coletou: '&aVocê coletou &7x{quantia} {display}&a.'
  Inv cheio: '&cVocê está com o inventário cheio!'
  Slot: '&cÉ necessário 1 slot vazio para fazer isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Suficiente: '&cEsta plantação não possui quantia suficiente.'
  Alterou: '&aVocê alterou o limite de venda do jogador &f{player}&a para &f{quantia}&a.'
  SellAll-Delay: '&c&lERRO! &cAguarde &e{time} &cpara vender plantações novamente.'
  Coletar:
    - ''
    - '&aDigite a quantia que você quer coletar.'
    - ''
    - '&8| &fPossui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara coletar tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  upgraded: '&aVocê adquiriu uma expansão da capacidade do armazém.'
  Ajuda:
    - '&aComandos do armazem:'
    - ''
    - '&e/armazem'
    - '&e/armazem ajuda'
    - '&e/armazem reload'
    - '&e/armazem add'
    - '&e/armazem set'
    - '&e/armazem remove'
    - '&e/armazem givelimitevenda'
    - '&e/armazem givelimitearmazem'

# Formatador de mensagens
Formatador:
  Bonus tem: '&7Bônus: &f{bonus}%&7 ({display}&7).'
  Bonus nao tem: ''

# Setas do menu
Setas:
  Anterior:
    material: ARROW
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    material: ARROW
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'

# Formatos de money e quantia
Formats:
  - ''
  - ''
  - 'K'
  - 'M'
  - 'B'
  - 'T'
  - 'Q'
  - 'QQ'
  - 'S'
  - 'SS'
  - 'O'
  - 'N'
  - 'D'

]]>
</code-block>
</chapter>

<chapter title="plantacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode configurar quantas plantas quiser.
Plantacoes:
  cacto:
    # Ordenação no menu
    Ordem: 1
    # Id do item da planta
    ID: CACTUS
    # Data do item da planta
    Data: 0
    # Nome que irá aparecer no menu e nas mensagens
    Display: '&aCacto'
    # Preço por cada unidade (para a sessão de comando)
    Preco: 10.0
    # Preços por cada unidade
    Precos:
      preco1:
        Provider: 'Money'
        Amount: 10.0
    # Permissão para vender a plantação
    PermissionVender: ''
    # Permissão para recolher a plantação
    PermissionRecolher: ''
    # Item que aparecerá no menu
    ItemDisplay:
      CustomSkull: false
      URL: ''
      ID: CACTUS
      Data: 0
      Glow: true
      Name: '&aCacto'
      Lore:
        - '&fQuantia: &a{quantia}&f.'
        - '&fPreço unitário: &a{unitario}&f.'
        - '&fPreço total: &a{total}&f.'
        - ''
        - '&7Clique com esquerdo para vender.'
        - '&7Clique com direito para coletar.'
    # Recompensas que poderão vir ao armazenar esta plantação
    Recompensas:
      - '0.0,reward1'
    # Botão que será realizada a venda (LEFT | RIGHT)
    Vender botao: 'LEFT'
    # Botão que será realizado recolher (LEFT | RIGHT)
    Recolher botao: 'RIGHT'
    # O Drop vai executar um comando ao ser recolhido?
    Comando:
      Ativar: false
      UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
      MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
      InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
      Comandos:
        - 'give {player} cactus {quantia}'
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yArmazem/
    ├── limites/
    │    ├── limite_armazem.yml
    │    └── limite_venda.yml
    ├── menus/
    │    ├── principal.yml
    │    └── recompensas.yml
    ├── bonus.yml
    ├── config.yml
    ├── plantacoes.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="limites" collapsible="true">
<chapter title="limite_armazem.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de armazenamento
Ativar: true

# Quantia que dá ao registrar.
Default: 10

# O limite vai ser total ou por plantação?
LimiteTotal: false

# Quantia máxima que cada plot terá de limite
# deixe 0 para ser infinito
Maximo: 0

# Compra de limite por menu
AdicionarPorLevel: 25
Prices-PerLevel:
  price1:
    provider: 'Money'
    display: 'Money'
    price: 10000.0

Item:
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  ID: 0
  Data: 0
  Glow: true
  Name: '&bLimite do armazém'
  Lore:
    - '&fQuantia: &a{quantia}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
]]>
</code-block>
</chapter>

<chapter title="limite_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de venda
Ativar: true
# Deixar o valor fixo do "Fixos" abaixo
Fixo: true
# Configurações do limite ativável ( apenas se o "Fixo" estiver false )
Ativavel:
  # Quantia que dá ao registrar.
  Default: 10
  Item:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    ID: 0
    Data: 0
    Glow: true
    Name: '&bLimite de venda do armazém'
    Lore:
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em true, assim desabilitando o uso do item ativável e os máximos.
Fixos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.fixo.membro'
    # Quantia de limite que terá
    Limite: 100

# O Maximos serve para definir quanto de limite o jogador poderá ativar.
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em false, assim habilitando o limite ativável e os máximos.
Maximos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.max.membro'
    # Quantia máxima de limite que poderá ter.
    Maximo: 100
]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Armazém de plantações'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
AnteriorSlot: 18
ProximoSlot: 26
Plantacao:
  Nome: '&b{display}'
  Lore:
    - '&fQuantia: &a{quantia}&f.'
    - '&fPreço unitário: &a{unitario}&f.'
    - '&fPreço total: &a{total}&f.'
    - ''
    - '&7Clique com esquerdo para vender.'
    - '&7Clique com direito para coletar.'
Itens:
  Informacoes:
    Slot: 30
    CustomSkull: false
    URL: ''
    ID: 339
    Data: 0
    Glow: true
    Name: '&aInformações'
    Lore:
      - '&fItens armazenados: &b{itens}&f.'
      - '&fQuantia de tipos: &b{tipos}&f.'
      - ''
      - '&fSeu limite: &a{limite_venda}&f.'
      - '&fLimite do armazem: &a{limite_armazem}&f.'
      - '&fPlantações armazenadas: &a{armazenado}&f.'
      - '&fSeu bonus: &b{bonus}%&f.'
      - '&fValor da bolsa: &a{bolsa}%&f.'
  Vender:
    Slot: 32
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/d883f946202bbdf25f8a1062e8c3317194333128207c89a474bde300c533dc3c'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aVender tudo'
    Lore:
      - '&f* Uso exclusivo &6VIP&f.'
    Lore perm:
      - '&7Clique para vender todos os itens.'
  Recompensas:
    Slot: 33
    material: 'CHEST'
    name: '&aRecompensas'
    lore:
      - ''
      - ' &fRecompensas no armazém: &a{rewards}&f.'
      - ''
      - '&7Clique para gerenciar'
  AutoSell:
    Slot: 34
    material: 'GOLD_INGOT'
    name: '&aAuto-Sell'
    lore:
      - '&7Venda automaticamente enquanto'
      - '&7você estiver dentro do plot.'
      - ''
      - ' &fAtivado: &a{status}&f.'
      - ''
      - '&aClique para alternar'
  AutoSell permissao:
    material: 'GOLD_INGOT'
    name: '&aAuto-Sell'
    lore:
      - '&7Venda automaticamente enquanto'
      - '&7você estiver dentro do plot.'
      - ''
      - '&cVocê não tem permissão.'
  LimiteUpgrade:
    Slot: 28
    material: FIREBALL
    name: '&aUpgrade de Capacidade'
    lore:
      - ''
      - ' &fAtual: &7{limite_armazem_atual}/{limite_armazem_maximo}&f.'
      - ' &fCusto para +{limite_armazem_addperlevel}: &7{Money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  LimiteUpgradeMaximo:
    material: FIREBALL
    name: '&aUpgrade de Capacidade'
    lore:
      - ''
      - ' &fAtual: &7{limite_armazem_atual}/{limite_armazem_maximo}&f.'
      - ''
      - '&cEste armazém já está no máximo.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Vender:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&8Armazém recompensas'
size: 54
slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
previous-slot: 18
next-slot: 26
back-slot: 48
#
empty-slot: 22
collect-slot: 50
#
items:
  empty:
    material: 'WEB'
    name: '&eVazio...'
    lore: [ '&7Nenhuma recompensa para', '&7coletar.' ]
  collect:
    material: 'a6cc486c2be1cb9dfcb2e53dd9a3e9a883bfadb27cb956f1896d602b4067'
    name: '&eRecolher tudo'
    lore: [ '&7Clique para recolher', '&7todas as recompensas.' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender as platanções.
Bonus:
  membros:
    Ordem: 1
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true

# Comandos e aliases do plugin
Comando:
  Comando: 'armazem'
  Aliases: [ ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Mundos que irá funcionar o armazem
# Deixe ALL para todos
Mundos plot:
  - 'MundoPlot'

# Mundos que não irá funcionar o armazem
# Útil se você usa o ALL no "Mundos plot"
Mundos plot blacklist: []

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Opções gerais
Opcoes:
  # Ativar o sistema de bolsa
  Bolsa: false
  # Ativar a coleta de plantações
  Coletar: true
  # Ativar a venda de plantações
  Vender: true
  # Ativar a venda de tudo
  Vender tudo: true
  # A opção vender tudo ignorar o limite
  # false = ignorar o limite
  Tudo limite: true
  # Armazenar mesmo com o jogador offline
  Armazenar off: false
  # Armazenar mesmo com os jogadores afk
  Armazenar afk: false
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Acesso para quem está com add na plot
  Plot add: true
  # Acesso para quem está com trust na plot
  Plot trust: true
  # Ativar o sistema de atualizar o menu do armazém automaticamente enquanto estiver aberto
  MenuUpdater: true
  # Coletar o disponível no inventário (sem ter que digitar no chat)
  ColetarDisponivel: false
  # Armazenar itens com meta? (nome e/ou lore, nbt)
  Armazenar meta: false
  # Ativar a coleta usando o botão Q para coletar o disponível no inventário
  Botao Q: true
  # Aparecer a plantação no armazém mesmo sem ter uma unidade
  Aparecer sem: true
  # Ativar o sistema de recompensas
  # Pode GERAR LAG
  Recompensas: false
  # Tempo para depositar as recompensas pendentes
  Recompensas tempo: 180
  # Fechar menu ao vender uma plantação
  Fechar vender: false
  # Fechar menu ao vender todas as plantações
  Fechar vender todos: false
  # Fechar menu ao coletar uma plantação
  Fechar coletar: false
  # Delay do auto-sell
  # em segundos
  AutoSell-delay: 5
  # Delay entre vendas do sell-all para o player
  # em segundos
  Player-SellAll-delay: 5

# Sistema de auto-break quando crescer um bloco
AutoBreak:
  Ativar: true
  Blocos:
    bloco1:
      Tipo: 'CACTUS'
      Drop: 'CACTUS'
    bloco2:
      Tipo: 'SUGAR_CANE_BLOCK'
      Drop: 'SUGAR_CANE'

# Mensagens em title do plugin
Title:
  Vendeu: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA!<nl>&fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens em actionbar do plugin
Actionbar:
  Vendeu: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA! &fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Terreno permissao: '&cVocê não tem permissão neste terreno.'
  Sem dono: '&cEste terreno não tem dono.'
  Terreno nulo: '&cVocê não está em um terreno.'
  Mundo: '&cEste mundo não está cadastrado.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Deu: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Max limite: '&cVocê já chegou no máximo.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Vendeu: '&aVocê vendeu &7x{quantia} {display}&a e ganhou &6{money}&a coins! {bonus}'
  Vendeu tudo: '&aVocê vendeu &7x{quantia} em plantações &a e ganhou &6{money}&a coins! {bonus}'
  Coletou: '&aVocê coletou &7x{quantia} {display}&a.'
  Inv cheio: '&cVocê está com o inventário cheio!'
  Slot: '&cÉ necessário 1 slot vazio para fazer isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Suficiente: '&cEsta plantação não possui quantia suficiente.'
  Alterou: '&aVocê alterou o limite de venda do jogador &f{player}&a para &f{quantia}&a.'
  SellAll-Delay: '&c&lERRO! &cAguarde &e{time} &cpara vender plantações novamente.'
  Coletar:
    - ''
    - '&aDigite a quantia que você quer coletar.'
    - ''
    - '&8| &fPossui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara coletar tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  upgraded: '&aVocê adquiriu uma expansão da capacidade do armazém.'
  Ajuda:
    - '&aComandos do armazem:'
    - ''
    - '&e/armazem'
    - '&e/armazem ajuda'
    - '&e/armazem reload'
    - '&e/armazem add'
    - '&e/armazem set'
    - '&e/armazem remove'
    - '&e/armazem givelimitevenda'
    - '&e/armazem givelimitearmazem'

# Formatador de mensagens
Formatador:
  Bonus tem: '&7Bônus: &f{bonus}%&7 ({display}&7).'
  Bonus nao tem: ''

# Setas do menu
Setas:
  Anterior:
    material: ARROW
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    material: ARROW
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'

# Formatos de money e quantia
Formats:
  - ''
  - ''
  - 'K'
  - 'M'
  - 'B'
  - 'T'
  - 'Q'
  - 'QQ'
  - 'S'
  - 'SS'
  - 'O'
  - 'N'
  - 'D'

]]>
</code-block>
</chapter>

<chapter title="plantacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode configurar quantas plantas quiser.
Plantacoes:
  cacto:
    # Ordenação no menu
    Ordem: 1
    # Id do item da planta
    ID: CACTUS
    # Data do item da planta
    Data: 0
    # Nome que irá aparecer no menu e nas mensagens
    Display: '&aCacto'
    # Preço por cada unidade (para a sessão de comando)
    Preco: 10.0
    # Preços por cada unidade
    Precos:
      preco1:
        Provider: 'Money'
        Amount: 10.0
    # Permissão para vender a plantação
    PermissionVender: ''
    # Permissão para recolher a plantação
    PermissionRecolher: ''
    # Item que aparecerá no menu
    ItemDisplay:
      CustomSkull: false
      URL: ''
      ID: CACTUS
      Data: 0
      Glow: true
      Name: '&aCacto'
      Lore:
        - '&fQuantia: &a{quantia}&f.'
        - '&fPreço unitário: &a{unitario}&f.'
        - '&fPreço total: &a{total}&f.'
        - ''
        - '&7Clique com esquerdo para vender.'
        - '&7Clique com direito para coletar.'
    # Recompensas que poderão vir ao armazenar esta plantação
    Recompensas:
      - '0.0,reward1'
    # Botão que será realizada a venda (LEFT | RIGHT)
    Vender botao: 'LEFT'
    # Botão que será realizado recolher (LEFT | RIGHT)
    Recolher botao: 'RIGHT'
    # O Drop vai executar um comando ao ser recolhido?
    Comando:
      Ativar: false
      UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
      MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
      InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
      Comandos:
        - 'give {player} cactus {quantia}'
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yArmazem/
    ├── limites/
    │    ├── limite_armazem.yml
    │    └── limite_venda.yml
    ├── menus/
    │    ├── principal.yml
    │    └── recompensas.yml
    ├── bonus.yml
    ├── config.yml
    ├── plantacoes.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="limites" collapsible="true">
<chapter title="limite_armazem.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de armazenamento
Ativar: true

# Quantia que dá ao registrar.
Default: 10

# O limite vai ser total ou por plantação?
LimiteTotal: false

# Quantia máxima que cada plot terá de limite
# deixe 0 para ser infinito
Maximo: 0

# Compra de limite por menu
AdicionarPorLevel: 25
Prices-PerLevel:
  price1:
    provider: 'Money'
    display: 'Money'
    price: 10000.0

Item:
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  ID: 0
  Data: 0
  Glow: true
  Name: '&bLimite do armazém'
  Lore:
    - '&fQuantia: &a{quantia}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
]]>
</code-block>
</chapter>

<chapter title="limite_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de venda
Ativar: true
# Deixar o valor fixo do "Fixos" abaixo
Fixo: true
# Configurações do limite ativável ( apenas se o "Fixo" estiver false )
Ativavel:
  # Quantia que dá ao registrar.
  Default: 10
  Item:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    ID: 0
    Data: 0
    Glow: true
    Name: '&bLimite de venda do armazém'
    Lore:
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em true, assim desabilitando o uso do item ativável e os máximos.
Fixos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.fixo.membro'
    # Quantia de limite que terá
    Limite: 100

# O Maximos serve para definir quanto de limite o jogador poderá ativar.
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em false, assim habilitando o limite ativável e os máximos.
Maximos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.max.membro'
    # Quantia máxima de limite que poderá ter.
    Maximo: 100
]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Armazém de plantações'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
AnteriorSlot: 18
ProximoSlot: 26
Plantacao:
  Nome: '&b{display}'
  Lore:
    - '&fQuantia: &a{quantia}&f.'
    - '&fPreço unitário: &a{unitario}&f.'
    - '&fPreço total: &a{total}&f.'
    - ''
    - '&7Clique com esquerdo para vender.'
    - '&7Clique com direito para coletar.'
Itens:
  Informacoes:
    Slot: 30
    CustomSkull: false
    URL: ''
    ID: 339
    Data: 0
    Glow: true
    Name: '&aInformações'
    Lore:
      - '&fItens armazenados: &b{itens}&f.'
      - '&fQuantia de tipos: &b{tipos}&f.'
      - ''
      - '&fSeu limite: &a{limite_venda}&f.'
      - '&fLimite do armazem: &a{limite_armazem}&f.'
      - '&fPlantações armazenadas: &a{armazenado}&f.'
      - '&fSeu bonus: &b{bonus}%&f.'
      - '&fValor da bolsa: &a{bolsa}%&f.'
  Vender:
    Slot: 32
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/d883f946202bbdf25f8a1062e8c3317194333128207c89a474bde300c533dc3c'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aVender tudo'
    Lore:
      - '&f* Uso exclusivo &6VIP&f.'
    Lore perm:
      - '&7Clique para vender todos os itens.'
  Recompensas:
    Slot: 33
    material: 'CHEST'
    name: '&aRecompensas'
    lore:
      - ''
      - ' &fRecompensas no armazém: &a{rewards}&f.'
      - ''
      - '&7Clique para gerenciar'
  AutoSell:
    Slot: 34
    material: 'GOLD_INGOT'
    name: '&aAuto-Sell'
    lore:
      - '&7Venda automaticamente enquanto'
      - '&7você estiver dentro do plot.'
      - ''
      - ' &fAtivado: &a{status}&f.'
      - ''
      - '&aClique para alternar'
  AutoSell permissao:
    material: 'GOLD_INGOT'
    name: '&aAuto-Sell'
    lore:
      - '&7Venda automaticamente enquanto'
      - '&7você estiver dentro do plot.'
      - ''
      - '&cVocê não tem permissão.'
  LimiteUpgrade:
    Slot: 28
    material: FIREBALL
    name: '&aUpgrade de Capacidade'
    lore:
      - ''
      - ' &fAtual: &7{limite_armazem_atual}/{limite_armazem_maximo}&f.'
      - ' &fCusto para +{limite_armazem_addperlevel}: &7{Money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  LimiteUpgradeMaximo:
    material: FIREBALL
    name: '&aUpgrade de Capacidade'
    lore:
      - ''
      - ' &fAtual: &7{limite_armazem_atual}/{limite_armazem_maximo}&f.'
      - ''
      - '&cEste armazém já está no máximo.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Vender:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&8Armazém recompensas'
size: 54
slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
previous-slot: 18
next-slot: 26
back-slot: 48
#
empty-slot: 22
collect-slot: 50
#
items:
  empty:
    material: 'WEB'
    name: '&eVazio...'
    lore: [ '&7Nenhuma recompensa para', '&7coletar.' ]
  collect:
    material: 'a6cc486c2be1cb9dfcb2e53dd9a3e9a883bfadb27cb956f1896d602b4067'
    name: '&eRecolher tudo'
    lore: [ '&7Clique para recolher', '&7todas as recompensas.' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender as platanções.
Bonus:
  membros:
    Ordem: 1
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true

# Comandos e aliases do plugin
Comando:
  Comando: 'armazem'
  Aliases: [ ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Mundos que irá funcionar o armazem
# Deixe ALL para todos
Mundos plot:
  - 'MundoPlot'

# Mundos que não irá funcionar o armazem
# Útil se você usa o ALL no "Mundos plot"
Mundos plot blacklist: []

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Opções gerais
Opcoes:
  # Ativar o sistema de bolsa
  Bolsa: false
  # Ativar a coleta de plantações
  Coletar: true
  # Ativar a venda de plantações
  Vender: true
  # Ativar a venda de tudo
  Vender tudo: true
  # A opção vender tudo ignorar o limite
  # false = ignorar o limite
  Tudo limite: true
  # Armazenar mesmo com o jogador offline
  Armazenar off: false
  # Armazenar mesmo com os jogadores afk
  Armazenar afk: false
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Acesso para quem está com add na plot
  Plot add: true
  # Acesso para quem está com trust na plot
  Plot trust: true
  # Ativar o sistema de atualizar o menu do armazém automaticamente enquanto estiver aberto
  MenuUpdater: true
  # Coletar o disponível no inventário (sem ter que digitar no chat)
  ColetarDisponivel: false
  # Armazenar itens com meta? (nome e/ou lore, nbt)
  Armazenar meta: false
  # Ativar a coleta usando o botão Q para coletar o disponível no inventário
  Botao Q: true
  # Aparecer a plantação no armazém mesmo sem ter uma unidade
  Aparecer sem: true
  # Ativar o sistema de recompensas
  # Pode GERAR LAG
  Recompensas: false
  # Tempo para depositar as recompensas pendentes
  Recompensas tempo: 180
  # Fechar menu ao vender uma plantação
  Fechar vender: false
  # Fechar menu ao vender todas as plantações
  Fechar vender todos: false
  # Fechar menu ao coletar uma plantação
  Fechar coletar: false
  # Delay do auto-sell
  # em segundos
  AutoSell-delay: 5
  # Delay entre vendas do auto-sell para o player
  # em segundos
  Player-AutoSell-delay: 5

# Sistema de auto-break quando crescer um bloco
AutoBreak:
  Ativar: true
  Blocos:
    bloco1:
      Tipo: 'CACTUS'
      Drop: 'CACTUS'
    bloco2:
      Tipo: 'SUGAR_CANE_BLOCK'
      Drop: 'SUGAR_CANE'

# Mensagens em title do plugin
Title:
  Vendeu: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA!<nl>&fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens em actionbar do plugin
Actionbar:
  Vendeu: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA! &fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Terreno permissao: '&cVocê não tem permissão neste terreno.'
  Sem dono: '&cEste terreno não tem dono.'
  Terreno nulo: '&cVocê não está em um terreno.'
  Mundo: '&cEste mundo não está cadastrado.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Deu: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Max limite: '&cVocê já chegou no máximo.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Vendeu: '&aVocê vendeu &7x{quantia} {display}&a e ganhou &6{money}&a coins! {bonus}'
  Vendeu tudo: '&aVocê vendeu &7x{quantia} em plantações &a e ganhou &6{money}&a coins! {bonus}'
  Coletou: '&aVocê coletou &7x{quantia} {display}&a.'
  Inv cheio: '&cVocê está com o inventário cheio!'
  Slot: '&cÉ necessário 1 slot vazio para fazer isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Suficiente: '&cEsta plantação não possui quantia suficiente.'
  Alterou: '&aVocê alterou o limite de venda do jogador &f{player}&a para &f{quantia}&a.'
  AutoSell-Delay: '&c&lERRO! &cAguarde &e{time} &cpara vender plantações novamente.'
  Coletar:
    - ''
    - '&aDigite a quantia que você quer coletar.'
    - ''
    - '&8| &fPossui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara coletar tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  upgraded: '&aVocê adquiriu uma expansão da capacidade do armazém.'
  Ajuda:
    - '&aComandos do armazem:'
    - ''
    - '&e/armazem'
    - '&e/armazem ajuda'
    - '&e/armazem reload'
    - '&e/armazem add'
    - '&e/armazem set'
    - '&e/armazem remove'
    - '&e/armazem givelimitevenda'
    - '&e/armazem givelimitearmazem'

# Formatador de mensagens
Formatador:
  Bonus tem: '&7Bônus: &f{bonus}%&7 ({display}&7).'
  Bonus nao tem: ''

# Setas do menu
Setas:
  Anterior:
    material: ARROW
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    material: ARROW
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'

# Formatos de money e quantia
Formats:
  - ''
  - ''
  - 'K'
  - 'M'
  - 'B'
  - 'T'
  - 'Q'
  - 'QQ'
  - 'S'
  - 'SS'
  - 'O'
  - 'N'
  - 'D'
]]>
</code-block>
</chapter>

<chapter title="plantacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode configurar quantas plantas quiser.
Plantacoes:
  cacto:
    # Ordenação no menu
    Ordem: 1
    # Id do item da planta
    ID: CACTUS
    # Data do item da planta
    Data: 0
    # Nome que irá aparecer no menu e nas mensagens
    Display: '&aCacto'
    # Preço por cada unidade (para a sessão de comando)
    Preco: 10.0
    # Preços por cada unidade
    Precos:
      preco1:
        Provider: 'Money'
        Amount: 10.0
    # Permissão para vender a plantação
    PermissionVender: ''
    # Permissão para recolher a plantação
    PermissionRecolher: ''
    # Item que aparecerá no menu
    ItemDisplay:
      CustomSkull: false
      URL: ''
      ID: CACTUS
      Data: 0
      Glow: true
      Name: '&aCacto'
      Lore:
        - '&fQuantia: &a{quantia}&f.'
        - '&fPreço unitário: &a{unitario}&f.'
        - '&fPreço total: &a{total}&f.'
        - ''
        - '&7Clique com esquerdo para vender.'
        - '&7Clique com direito para coletar.'
    # Recompensas que poderão vir ao armazenar esta plantação
    Recompensas:
      - '0.0,reward1'
    # Botão que será realizada a venda (LEFT | RIGHT)
    Vender botao: 'LEFT'
    # Botão que será realizado recolher (LEFT | RIGHT)
    Recolher botao: 'RIGHT'
    # O Drop vai executar um comando ao ser recolhido?
    Comando:
      Ativar: false
      UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
      MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
      InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
      Comandos:
        - 'give {player} cactus {quantia}'
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yArmazem/
    ├── limites/
    │    ├── limite_armazem.yml
    │    └── limite_venda.yml
    ├── menus/
    │    └── principal.yml
    ├── bonus.yml
    ├── config.yml
    └── plantacoes.yml
</code-block>
</chapter>

<chapter title="limites" collapsible="true">
<chapter title="limite_armazem.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de armazenamento
Ativar: true
# Quantia que dá ao registrar.
Default: 10
# O limite vai ser total ou por plantação?
LimiteTotal: false
# Quantia máxima que cada plot terá de limite
# deixe 0 para ser infinito
Maximo: 0
Item:
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  ID: 0
  Data: 0
  Glow: true
  Name: '&bLimite do armazém'
  Lore:
    - '&fQuantia: &a{quantia}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
]]>
</code-block>
</chapter>

<chapter title="limite_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de limite de venda
Ativar: true
# Deixar o valor fixo do "Fixos" abaixo
Fixo: true
# Configurações do limite ativável ( apenas se o "Fixo" estiver false )
Ativavel:
  # Quantia que dá ao registrar.
  Default: 10
  Item:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    ID: 0
    Data: 0
    Glow: true
    Name: '&bLimite de venda do armazém'
    Lore:
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em true, assim desabilitando o uso do item ativável e os máximos.
Fixos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.fixo.membro'
    # Quantia de limite que terá
    Limite: 100

# O Maximos serve para definir quanto de limite o jogador poderá ativar.
# Lembrando que só estará disponível, caso a opção "Limite fixo" da config.yml
# estiver em false, assim habilitando o limite ativável e os máximos.
Maximos:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.limitevenda.max.membro'
    # Quantia máxima de limite que poderá ter.
    Maximo: 100
]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Armazém de plantações'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
AnteriorSlot: 18
ProximoSlot: 26
Plantacao:
  Nome: '&b{display}'
  Lore:
    - '&fQuantia: &a{quantia}&f.'
    - '&fPreço unitário: &a{unitario}&f.'
    - '&fPreço total: &a{total}&f.'
    - ''
    - '&7Clique com esquerdo para vender.'
    - '&7Clique com direito para coletar.'
Itens:
  Informacoes:
    Slot: 30
    CustomSkull: false
    URL: ''
    ID: 339
    Data: 0
    Glow: true
    Name: '&aInformações'
    Lore:
      - '&fItens armazenados: &b{itens}&f.'
      - '&fQuantia de tipos: &b{tipos}&f.'
      - ''
      - '&fSeu limite: &a{limite_venda}&f.'
      - '&fLimite do armazem: &a{limite_armazem}&f.'
      - '&fPlantações armazenadas: &a{armazenado}&f.'
      - '&fSeu bonus: &b{bonus}%&f.'
      - '&fValor da bolsa: &a{bolsa}%&f.'
  Vender:
    Slot: 32
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/d883f946202bbdf25f8a1062e8c3317194333128207c89a474bde300c533dc3c'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aVender tudo'
    Lore:
      - '&f* Uso exclusivo &6VIP&f.'
    Lore perm:
      - '&7Clique para vender todos os itens.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Vender:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender as platanções.
Bonus:
  membros:
    Ordem: 1
    # Permissão para ser reconhecido
    Permissao: 'yarmazem.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true
# Comandos e aliases do plugin
Comando:
  Comando: 'armazem'
  Aliases: [ ]
# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'
# Mundos que irá funcionar o armazem
Mundos plot:
  - 'MundoPlot'
# Opções gerais
Opcoes:
  # Ativar o sistema de bolsa
  Bolsa: false
  # Ativar a coleta de plantações
  Coletar: true
  # Ativar a venda de plantações
  Vender: true
  # Ativar a venda de tudo
  Vender tudo: true
  # A opção vender tudo ignorar o limite
  # false = ignorar o limite
  Tudo limite: true
  # Armazenar mesmo com o jogador offline
  Armazenar off: false
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Acesso para quem está com add na plot
  Plot add: true
  # Acesso para quem está com trust na plot
  Plot trust: true
  # Ativar o sistema de atualizar o menu do armazém automaticamente enquanto estiver aberto
  MenuUpdater: true
  # Coletar o disponível no inventário (sem ter que digitar no chat)
  ColetarDisponivel: false
  # Armazenar itens com meta? (nome e/ou lore, nbt)
  Armazenar meta: false
  # Ativar a coleta usando o botão Q para coletar o disponível no inventário
  Botao Q: true
  # Aparecer a plantação no armazém mesmo sem ter uma unidade
  Aparecer sem: true

# Mensagens em title do plugin
Title:
  Vendeu: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA!<nl>&fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA!<nl>&fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens em actionbar do plugin
Actionbar:
  Vendeu: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Vendeu tudo: '&a&lVENDA! &fVocê recebeu &2$&a{money}&f de coins.'
  Coletou: '&a&lCOLETA! &fVocê coletou &2$&a{quantia}&f plantas.'

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Terreno permissao: '&cVocê não tem permissão neste terreno.'
  Sem dono: '&cEste terreno não tem dono.'
  Terreno nulo: '&cVocê não está em um terreno.'
  Mundo: '&cEste mundo não está cadastrado.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Deu: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Max limite: '&cVocê já chegou no máximo.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Vendeu: '&aVocê vendeu &7x{quantia} {display}&a e ganhou &6{money}&a coins! {bonus}'
  Vendeu tudo: '&aVocê vendeu &7x{quantia} em plantações &a e ganhou &6{money}&a coins! {bonus}'
  Coletou: '&aVocê coletou &7x{quantia} {display}&a.'
  Inv cheio: '&cVocê está com o inventário cheio!'
  Slot: '&cÉ necessário 1 slot vazio para fazer isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Suficiente: '&cEsta plantação não possui quantia suficiente.'
  Coletar:
    - ''
    - '&aDigite a quantia que você quer coletar.'
    - ''
    - '&8| &fPossui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara coletar tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''
# Formatador de mensagens
Formatador:
  Bonus tem: '&7Bônus: &f{bonus}%&7 ({display}&7).'
  Bonus nao tem: ''
# Setas do menu
Setas:
  Anterior:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'
# Formatos de money e quantia
Formats:
  - ''
  - ''
  - 'K'
  - 'M'
  - 'B'
  - 'T'
  - 'Q'
  - 'QQ'
  - 'S'
  - 'SS'
  - 'O'
  - 'N'
  - 'D'
]]>
</code-block>
</chapter>

<chapter title="plantacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode configurar quantas plantas quiser.
Plantacoes:
  cacto:
    # Id do item da planta
    ID: 81
    # Data do item da planta
    Data: 0
    # Nome que irá aparecer no menu e nas mensagens
    Display: '&aCacto'
    # Preço por cada unidade
    Preco: 10.0
    # Item que aparecerá no menu
    ItemDisplay:
      CustomSkull: false
      URL: ''
      ID: 81
      Data: 0
      Glow: true
      Name: '&aCacto'
    # Botão que será realizada a venda (LEFT | RIGHT)
    Vender botao: 'LEFT'
    # Botão que será realizado recolher (LEFT | RIGHT)
    Recolher botao: 'RIGHT'
    # O Drop vai executar um comando ao ser recolhido?
    Comando:
      Ativar: false
      UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
      MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
      InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
      Comandos:
        - 'give {player} cactus {quantia}'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static ArmazemAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;ArmazemAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(ArmazemAPIHolder.class);
        return rsp == null ? null : rsp.getProvider();
    } catch (Throwable var1) {
        return null;
    }
}
</code-block>

## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/8-yArmazem">Site do plugin yArmazem</a>
    </category>
</seealso>