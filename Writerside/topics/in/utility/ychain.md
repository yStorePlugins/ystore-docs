# yChain
<secondary-label ref="utility"/>

### Descrição
Múltiplas arenas cada uma com seu kit e várias funções!

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
<video src="//www.youtube.com/watch?v=YdhLezVIvaI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/chain - Abre o menu principal
/chain entrar  - Entra em uma arena
/chain sair - Sai da arena
/chain arenas - Vê todas as arenas do servidor
/chain ajuda - Vê todos os comandos
/chain kits - Vê os kits configurados (ADMIN)
/chain arenasadmin - Gerenciar as arenas (ADMIN)
/chain criararena - Cria uma nova arena (ADMIN)
/chain delarena - Deleta uma arena (ADMIN)
/chain criarkit - Cria um novo kit (ADMIN)
/chain delkit - Deleta um kit (ADMIN)
/chain setnpc - Seta o NPC do chain (ADMIN)
/chain delnpc - Deleta o NPC do chain (ADMIN)
/chain reload - Recarrega as configurações (ADMIN)</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ychain.usar - Permissão para o /chain
ychain.entrar - Permissão para o /chain entrar
ychain.sair - Permissão para o /chain sair
ychain.arenas - Permissão para o /chain arenas
ychain.kits - Permissão para o /chain kits
ychain.arenasadmin - Permissão para o /chain arenasadmin
ychain.criararena - Permissão para o /chain criararena
ychain.delarena - Permissão para o /chain delarena
ychain.criarkit - Permissão para o /chain criarkit
ychain.delkit - Permissão para o /chain delkit
ychain.setnpc - Permissão para o /chain setnpc
ychain.delnpc - Permissão para o /chain delnpc
ychain.reload - Permissão para o /chain reload
ychain.admin - Permissão para ser reconhecido como admin
ychain.bypass - Permissão para o bypass de comandos no chain</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ychain_killstreak_maximo% - Retorna o killstreak máximo do jogador
%ychain_killstreak% - Retorna o killstreak atual do jogador
%ychain_kills% - Retorna a quantia de kills do jogador
%ychain_deaths% - Retorna a quantia de mortes do jogador
%ychain_kdr% - Retorna o kdr do jogador
%ychain_time% - Retorna o tempo que o jogador passa nas arenas
%ychain_tag% - Retorna a tag caso seja o TOP 1 Kills
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{ychain} - Retorna a tag para o TOP 1 Kills
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yChain/
    ├── menus/
    │    ├── arenas.yml
    │    ├── principal.yml
    │    ├── recompensas.yml
    │    └── top.yml
    ├── config.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="arenas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Arenas do servidor'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16, 21, 22, 23, 24, 25]
BackSlot: 18
AnteriorSlot: 27
ProximoSlot: 35
Itens: {}
#  Enfeite:
#    Slot: 10
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: false
#    Name: '&aEnfeite'
#    Lore: []
  # Você pode adicionar enfeites, apenas adicionando itens iguais o Enfeite e mudando os dados.
##################
# Este item será mostrado para cada arena que não estiver configurada na seção Arenas.
Padrao:
  Name: '&e{nome}'
  Lore:
    - '&fJogadores na arena: &b{jogadores}&f.'
    - ''
    - '&7Clique para entrar nesta arena.'
# Configure as minas que irão aparecer
Arenas:
  Arena1:
    # Id da arena criada (nome do arquivo sem o .yml na pasta arenas)
    Arena: 'Chain'
    Name: '&e{nome}'
    Lore:
      - '&7Essa arena é a mais capaz de'
      - '&7suportar todos os tipos de pvp insanos!'
      - ''
      - '&fJogadores na arena: &b{jogadores}&f.'
      - ''
      - '&9&lyStore'

]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Chain'
Tamanho: 27
Itens:
  Informacoes:
    Slot: 10
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSuas informações'
    Lore:
      - ''
      - ' &fTempo total na arena: &7{tempo}&f.'
      - ' &fKillstreak máximo e atual: &7A: {killstreak} &8- &7M: {killstreak_maximo}&f.'
      - ''
      - ' &fKills: &a{kills}&f.'
      - ' &fMortes: &c{mortes}&f.'
      - ' &fKDR: &b{kdr}&f.'
      - ''
  Recompensas:
    Slot: 12
    CustomSkull: false
    URL: ''
    ID: 130
    Data: 0
    Glow: true
    Name: '&aRecompensas!'
    Lore:
      - '&7Recolha as recompensas'
      - '&7que você ganhou na arena!'
      - ''
      - '&aClique para acessar.'
  Top:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTop jogadores'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacaram na arena.'
      - ''
      - '&aClique para visualizar.'
  Entrar:
    Slot: 16
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/8e9b27fccd80921bd263c91dc511d09e9a746555e6c9cad52e8562ed0182a2f'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aEntrar'
    Lore:
      - '&7Entrar para o combate em'
      - '&7alguma das nossas arenas.'
      - ''
      - '&aClique para entrar.'
  Sair:
    Slot: 16
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 0
    Data: 0
    Glow: true
    Name: '&cSair'
    Lore:
      - '&7Você está batalhando!'
      - ''
      - '&aClique para sair.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Magnata:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Chain - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26
# Item para recolher todas as recompensas
Recolher todos:
  Slot: 49
  CustomSkull: false
  URL: ''
  ID: 408
  Data: 0
  Glow: true
  Name: '&6Recolher todos'
  Lore:
    - '&7Clique para recolher'
    - '&7todas as recompensas.'
# Item que irá mostrar quanto estiver vazio
Vazio:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: 408
  Data: 0
  Glow: true
  Name: '&cVazio!'
  Lore:
    - '&7Você não possui nenhuma'
    - '&7recompensa armazenada.'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Chain'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 30
AnteriorSlot: 9
ProximoSlot: 17
# Item do top Kills
Item kills:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fKills: &7{xp}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top KDR
Item kdr:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fK/D: &7{kdr}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top KillStreak
Item killstreak:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fKillStreak máximo: &7{killstreak}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top Tempo
Item tempo:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fTempo na arena: &7{tempo}'
    - '&fPosição: &e{pos}º'
    - ''
# Seletor dos tops
Seletor:
  Slot: 31
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: 0
  Data: 0
  Name: '&aSeletor do TOP'
# Tipos do seletor
Tipos:
  Kills:
    Ativar: true
    Nome: 'Kills'
  KDR:
    Ativar: true
    Nome: 'KDR'
  Killstreak:
    Ativar: true
    Nome: 'KillStreak'
  Tempo:
    Ativar: true
    Nome: 'Tempo'
# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome}'
  Selecionar: ' &f• &7{nome}'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE, MYSQL_FAST
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true

# Comandos e aliases do plugin
Comando:
  Chain:
    Comando: 'chain'
    Aliases: [ arenachain ]

# Opcoes de configuração do NPC
NPC:
  ID: 923284
  Skin: 'TheThunderGod063'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Chain'
      - '&7Clique para entrar na arena chain.'

# Opções gerais do plugin
Opcoes:
  # Tag do top kills
  Tag: '&c[MATADOR]'
  # o comando /chain arenas abrir um menu
  Arenas menu: true
  # o comando /chain kits abrir um menu
  Kits menu: true
  # Evitar reparar itens, regenerar, ganhar itens, ganhar recompensas, killstreak ao matar o jogador 2x ou mais seguidas.
  AntiFreeKill: true
  # Comandos que poderão ser usados na arena
  Command whitelist:
    - '/g'
  # Recompensas configuradas na recompensas.yml que poderão ser dadas ao matar um jogador
  # Deixe Recompensas: [] para não usar
  # chance,recompensa
  Recompensas:
    - '100.0,Reco1'
  # Regenerar a vida ao matar um jogador
  # a vida total do jogador é 20 (10 corações)
  # deixe 0 para não usar
  Regenerar: 5
  # Resetar inventário ao matar um jogador
  # Apenas se os itens forem setados
  ResetarMatar: false
  # Itens que poderão ser dado ao matar um jogador
  # será escolhido apenas um da lista por kill.
  Itens dar:
    - 'GOLDEN_APPLE:0'
  # Quando o jogador fizer x kills (minimo definido)
  # irá enviar mensagem para o broadcast e/ou para o jogador, informando
  # que ele está fazendo uma série de kills (matando muito)
  Killstreak:
    Ativar: true
    Minimo: 2
    # Deixe '' para não usar alguma das duas.
    Broadcast: '&aO jogador &f{player}&a está com um &nkillstreak&a de &6{kills} &a&nkills&a.'
    Player: '&aVocê está com um &nkillstreak&a de &6{kills} &a&nkills&a.'
    # Recompensas configuradas na recompensas.yml que poderão ser dadas ao atingir um killstreak
    # Deixe Recompensas: [] para não usar
    # KillStreak,chance,recompensa
    Recompensas:
      - '2,100.0,Reco1'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Setado npc: '&aNPC do chain setado com sucesso.'
  Removido npc: '&aNPC do chain removido com sucesso'
  Nao setado npc: '&cO NPC não está setado.'
  Setado: '&aLocal &7{local} &ada arena setado com sucesso.'
  Removido: '&aLocal &7{local} &ada arena removido com sucesso.'
  Nao setado: '&cO local &7{local} &cda arena chain não está setado.'
  Setado kit: '&aO kit da arena chain foi setado com sucesso. &7(Todos os itens do seu inventário foram reconhecidos)'
  Recebeu kit: '&aVocê recebeu o kit da arena chain.'
  Entrou: '&aVocê entrou na arena chain.'
  Saiu: '&aVocê saiu da arena chain.'
  Ja esta: '&cVocê já está na arena chain.'
  Nao esta: '&cVocê não está na arena chain.'
  Esvazie: '&cEsvazie seu inventário para entrar na arena chain.'
  Kit criado: '&aKit &7{kit} &8(#{id})&a criado com sucesso.'
  Arena criada: '&aArena &7{arena} &8(#{id})&a criada com sucesso.'
  Arena existe: '&cEsta arena já existe.'
  Kit existe: '&cEste kit já existe.'
  Arena nao existe: '&cEsta arena não existe.'
  Kit nao existe: '&cEste kit não existe.'
  Arena deletada: '&cArena deletada.'
  Kit deletado: '&cKit deletado.'
  Item nao: '&cO item não pode ser nulo.'
  Icone mudou: '&aÍcone alterado com sucesso.'
  Cancelou: '&cVocê cancelou a operação.'
  Mudou nome: '&aVocê alterou o nome da arena para &e{nome}&a.'
  Mudou kit: '&aVocê alterou o kit da arena para &e{kit}&a.'
  Inv cheio: '&cSeu inventário está cheio.'
  Digite nome:
    - ''
    - '&aDigite o nome para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Arenas:
    - '&aArenas disponíveis: &7{arenas}&a.'
  Kits:
    - '&aKits disponíveis: &7{kits}&a.'
  Recebeu:
    - '&aVocê recebeu uma recompensa, digite /chain para coletá-la.'
  Help admin:
    - ''
    - '&b--> &7Comandos disponíveis &b<--'
    - ''
    - '&b -> &f/chain &8- &7Abre o menu principal'
    - '&b -> &f/chain entrar &8- &7Entra na arena chain'
    - '&b -> &f/chain sair &8- &7Sai da arena chain'
    - '&b -> &f/chain arenas - Vê todas as arenas do servidor'
    - '&b -> &f/chain ajuda - Vê todos os comandos'
    - '&b -> &f/chain kits - Vê os kits configurados'
    - '&b -> &f/chain arenasadmin - Gerenciar as arenas'
    - '&b -> &f/chain criararena - Cria uma nova arena'
    - '&b -> &f/chain delarena - Deleta uma arena'
    - '&b -> &f/chain criarkit - Cria um novo kit'
    - '&b -> &f/chain delkit - Deleta um kit'
    - '&b -> &f/chain setnpc &8- &7Seta o NPC do chain'
    - '&b -> &f/chain delnpc &8- &7Deleta o NPC do chain'
    - ''
  Help:
    - ''
    - '&b--> &7Comandos disponíveis &b<--'
    - ''
    - '&b -> &f/chain &8- &7Abre o menu principal'
    - '&b -> &f/chain entrar &8- &7Entra na arena chain'
    - '&b -> &f/chain sair &8- &7Sai da arena chain'
    - '&b -> &f/chain arenas - Vê todas as arenas do servidor'
    - '&b -> &f/chain ajuda - Vê todos os comandos'
    - '&b -> &f/chain kits - Vê os kits configurados'
    - ''

# Setas dos menus
Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
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
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá no menu das recompensas.
    Preview:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEsta pedra vale muito dinheiro!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será dado o item se os comandos estiverem em false.
    # Item que será dado ao jogador.
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEu valho muito!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: false
      List:
        - 'give {player} stone 1'

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/75-yChain">Site do plugin yChain</a>
    </category>
</seealso>