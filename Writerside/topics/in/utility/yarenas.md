# yArenas
<secondary-label ref="utility"/>

### Descrição
Financie o PVP do seu servidor com arenas rankeadas

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
<video src="//www.youtube.com/watch?v=bI4diwaHqNo"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/arena&nbsp;- Abre o menu principal
/arena ir&nbsp;- Entra na arena
/arena sair&nbsp;- Sai da arena
/arena top&nbsp;- Abre o menu de TOP
/arena recompensas&nbsp;- Abre o menu de recompensas
/arena arenas&nbsp;- Abre o menu de arenas
/arena help&nbsp;- Envia a mensagem de ajuda
/arena add&nbsp;- Adiciona pontos para um clan
/arena&nbsp;remove&nbsp;-&nbsp;Remove pontos de um clan
/arena&nbsp;set&nbsp;-&nbsp;Seta pontos para um clan
/arena&nbsp;setsaida&nbsp;- Seta a saída da arena
/arena&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yarenas.use - Permissão para o /arena
yarenas.go - Permissão para o /arena go
yarenas.exit - Permissão para o /arena exit
yarenas.top - Permissão para o /arena top
yarenas.rewards - Permissão para o /arena recompensas
yarenas.arenas - Permissão para o /arena arenas
yarenas.points.add - Permissão para o /arena add
yarenas.points.remove - Permissão para o /arena remove
yarenas.points.set - Permissão para o /arena set
yarenas.admin.setexit - Permissão para o /arena setsaida
yarenas.admin.reload - Permissão para o /arena reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yarenas_points% - Retorna a quantia total de pontos do jogador
%yarenas_points_raw% - Retorna a quantia total de pontos do jogador sem formatar
%yarenas_kills% - Retorna a quantia total de abates do jogador
%yarenas_kills_raw% - Retorna a quantia total de abates do jogador sem formatar
%yarenas_deaths% - Retorna a quantia total de mortes do jogador
%yarenas_deaths_raw% - Retorna a quantia total de mortes do jogador sem formatar
%yarenas_rank% - Retorna o rank do jogador
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yArenas/
    ├── arenas/
    │    ├── chain.yml
    │    └── leather.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    ├── plugin.yml
    ├── ranks.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="arenas" collapsible="true">
<chapter title="chain.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome da arena
display-name: '&fArena chain'

# Permissão para entrar na arena
permission: ''

# Ordem da arena na lista
# os jogadores começam na arena de ordem ("order") 1
order: 2

# Lista de comandos que será possível executar na arena
command-whitelist: [ '/g', '/.' ]

# Sistema de desbloqueio de arena
unlock:
  # Pontos mínimos necessários para desbloquear essa arena
  need-points: 2.0
  # Habilitar a compra dessa arena
  buy: true
  # Preços para comprar o acesso a esta arena
  prices:
    price1:
      provider: 'money'
      amount: 10.0

private:
  # Mensagens e ações ao entrar
  entry:
    sound: 'ORB_PICKUP'
    title: '&bBem vindo à<nl>&fArena chain'
    actionbar: '&bVocê entrou na &fArena chain&b.'
    chat: '<nl>&bBem vindo à &fArena chain.<nl>&bLute bravamente.<nl>'
  # Mensagens e ações ao sair
  exit:
    sound: 'ORB_PICKUP'
    title: ''
    actionbar: '&bVocê saiu da &fArena chain&b.'
    chat: '<nl>&bVocê saiu da &fArena chain&b.<nl>'
  # Mensagens e ações ao morrer
  death:
    sound: 'ORB_PICKUP'
    title: ''
    actionbar: '&bVocê morreu na &cArena Couro&b.'
    chat: '<nl>&bVocê morreu na &cArena Couro&b.<nl>'

broadcast:
  # Mensagens e ações ao entrar
  entry:
    sound: ''
    title: ''
    actionbar: ''
    chat: ''
  # Mensagens e ações ao sair
  exit:
    sound: ''
    title: ''
    actionbar: ''
    chat: ''
  # Mensagens e ações ao sair
  death:
    sound: ''
    title: ''
    actionbar: ''
    chat: '&f{killer}&b matou &f{dead}&b.'
  # Mensagens e ações ao obter kill-streak
  kill-streak:
    sound: ''
    title: ''
    actionbar: '&aO jogador &f{player}&a está com um &nkillstreak&a de &6{killstreak} &a&nkills&a.'
    chat: ''

# Quando o jogador fizer x kills (minimo definido)
# irá enviar mensagem para o broadcast e/ou para o jogador, informando
# que ele está fazendo uma série de kills (matando muito)
kill-streak:
  enabled: true
  minimum: 2
  # Recompensas configuradas na recompensas.yml que poderão ser dadas ao atingir um killstreak
  # Deixe Recompensas: [] para não usar
  # KillStreak,chance,recompensa
  rewards:
    - '100.0,reward1'

scoreboard:
  enabled: true
  title: '&b&lyStore'
  lines:
    - '&7     Área de batalha'
    - ''
    - '&f &fArena Chain'
    - '&f Rank: &7{rank}'
    - ''
    - '&e Dados'
    - '&8  ❘&f Abates: &a{kills}'
    - '&8  ❘&f Mortes: &c{deaths}'
    - ''
    - '&f A. KillStreak&f: &e{killstreak}'
    - '&f M. KillStreak&f: &e{highest_killstreak}'
    - ''
    - '&b    ystoreplugins.com.br'

# Ícones no menu
icons:
  access:
    material: 'CHAINMAIL_CHESTPLATE'
    name: '&fArena chain'
    lore:
      - '&7Esta é a Arena Intermediária. Aqui você'
      - '&7poderá sentir o peso da espada'
      - '&7dos outros jogadores.'
      - ''
      - ' &8▶ &fAbates: &a{kills}'
      - ' &8▶ &fMortes: &c{deaths}'
      - ''
      - ' &8▶ &fKill-Streak: &c{killstreak}'
      - ' &8▶ &fMaior Kill-Streak: &c{highest_killstreak}'
      - ''
      - '&f> &aVocê pode acessar essa arena.'
      - ''
  unlock:
    material: 'CHAINMAIL_CHESTPLATE'
    name: '&fArena chain'
    lore:
      - '&7Esta é a Arena Intermediária. Aqui você'
      - '&7poderá sentir o peso da espada'
      - '&7dos outros jogadores.'
      - ''
      - ' &fPontos necessários: &a{points}'
      - ' &fRank necessário: &b[ÁguaI]'
      - ''
      - '&f> &aVocê já pode desbloquear essa arena.'
      - ''
  already:
    material: 'CHAINMAIL_CHESTPLATE'
    name: '&fArena chain'
    lore:
      - '&7Esta é a Arena Intermediária. Aqui você'
      - '&7poderá sentir o peso da espada'
      - '&7dos outros jogadores.'
      - ''
      - ' &8▶ &fAbates: &a{kills}'
      - ' &8▶ &fMortes: &c{deaths}'
      - ''
      - ' &8▶ &fKill-Streak: &c{killstreak}'
      - ' &8▶ &fMaior Kill-Streak: &c{highest_killstreak}'
      - ''
      - '&f> &cVocê já está dentro desta arena.'
      - ''
  permission:
    material: 'CHAINMAIL_CHESTPLATE'
    name: '&fArena chain'
    lore:
      - '&7Esta é a Arena Intermediária. Aqui você'
      - '&7poderá sentir o peso da espada'
      - '&7dos outros jogadores.'
      - ''
      - ' &fRank necessário: &b[ÁguaI]'
      - ''
      - '&f> &cVocê não tem permissão para'
      - '&c  entrar nesta arena.'
      - ''
  points:
    material: 'CHAINMAIL_CHESTPLATE'
    name: '&fArena chain'
    lore:
      - '&7Esta é a Arena Intermediária. Aqui você'
      - '&7poderá sentir o peso da espada'
      - '&7dos outros jogadores.'
      - ''
      - ' &fPontos necessários: &a{points}'
      - ''
      - '&f> &cVocê não tem pontos suficientes'
      - '&c  para entrar nesta arena.'
      - ''
      - '&f> &7Adquira o acesso pagando:'
      - '&2  $&a{money} coins&7.'
      - ''
  top:
    material: 'CHAINMAIL_CHESTPLATE'
    name: '&fArena chain'
    lore:
      - ''
      - ' &7Líderes:'
      - '  &f> 1º {player_1}: &a{amount_1}'
      - '  &f> 2º {player_2}: &a{amount_2}'
      - '  &f> 3º {player_3}: &a{amount_3}'
      - '  &f> 4º {player_4}: &a{amount_4}'
      - '  &f> 5º {player_5}: &a{amount_5}'
      - ''

# Itens que o jogador irá receber ao entrar na arena
kit:
  # Ativar o sistema itens setados
  enabled: true

player-kill:
  # Regenerar a vida ao matar um jogador
  # a vida total do jogador é 20 (10 corações)
  # deixe 0 para não usar
  heal: 5.0
  # Resetar o kit do inventário do jogador ao matar um jogador
  reset-kit: true
  # Pontos que serão dados por kill
  give-points: 1.0
  # Dar algum item ao matar um jogador
  give-items: {}
  # Dar algum comando ao matar um jogador
  give-commands: []
  # Efeitos que serão dados ao matar um jogador
  give-effects:
    - 'SPEED:1-15'
]]>
</code-block>
</chapter>

<chapter title="leather.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome da arena
display-name: '&cArena couro'

# Permissão para entrar na arena
permission: ''

# Ordem da arena na lista
# os jogadores começam na arena de ordem ("order") 1
order: 1

# Lista de comandos que será possível executar na arena
command-whitelist: [ '/g', '/.' ]

# Sistema de desbloqueio de arena
unlock:
  # Pontos mínimos necessários para desbloquear essa arena
  need-points: 0.0
  # Habilitar a compra dessa arena
  buy: false
  # Preços para comprar o acesso a esta arena
  prices:
    price1:
      provider: 'money'
      amount: 0.0

private:
  # Mensagens e ações ao entrar
  entry:
    sound: 'ORB_PICKUP'
    title: '&bBem vindo à<nl>&cArena Couro'
    actionbar: '&bVocê entrou na &cArena Couro&b.'
    chat: '<nl>&bBem vindo à &cArena Couro.<nl>&bLute bravamente.<nl>'
  # Mensagens e ações ao sair
  exit:
    sound: 'ORB_PICKUP'
    title: ''
    actionbar: '&bVocê saiu da &cArena Couro&b.'
    chat: '<nl>&bVocê saiu da &cArena Couro&b.<nl>'
  # Mensagens e ações ao morrer
  death:
    sound: 'ORB_PICKUP'
    title: ''
    actionbar: '&bVocê morreu na &cArena Couro&b.'
    chat: '<nl>&bVocê morreu na &cArena Couro&b.<nl>'

broadcast:
  # Mensagens e ações ao entrar
  entry:
    sound: ''
    title: ''
    actionbar: ''
    chat: ''
  # Mensagens e ações ao sair
  exit:
    sound: ''
    title: ''
    actionbar: ''
    chat: ''
  # Mensagens e ações ao sair
  death:
    sound: ''
    title: ''
    actionbar: ''
    chat: '&f{killer}&b matou &f{dead}&b.'
  # Mensagens e ações ao obter kill-streak
  kill-streak:
    sound: ''
    title: ''
    actionbar: '&aO jogador &f{player}&a está com um &nkillstreak&a de &6{killstreak} &a&nkills&a.'
    chat: ''

# Quando o jogador fizer x kills (minimo definido)
# irá enviar mensagem para o broadcast e/ou para o jogador, informando
# que ele está fazendo uma série de kills (matando muito)
kill-streak:
  enabled: true
  minimum: 2
  # Recompensas configuradas na recompensas.yml que poderão ser dadas ao atingir um killstreak
  # Deixe Recompensas: [] para não usar
  # KillStreak,chance,recompensa
  rewards:
    - '100.0,reward1'

scoreboard:
  enabled: true
  title: '&b&lyStore'
  lines:
    - '&7     Área de batalha'
    - ''
    - '&f &cArena Couro'
    - '&f Rank: &7{rank}'
    - ''
    - '&e Dados'
    - '&8  ❘&f Abates: &a{kills}'
    - '&8  ❘&f Mortes: &c{deaths}'
    - ''
    - '&f A. KillStreak&f: &e{killstreak}'
    - '&f M. KillStreak&f: &e{highest_killstreak}'
    - ''
    - '&b    ystoreplugins.com.br'

# Ícones no menu
icons:
  access:
    material: 'LEATHER_CHESTPLATE'
    name: '&cArena couro'
    lore:
      - '&7Esta é a Arena Inicial. Aqui você'
      - '&7poderá incrementar suas skills'
      - '&7e avançar para a demais arenas.'
      - ''
      - ' &8▶ &fAbates: &a{kills}'
      - ' &8▶ &fMortes: &c{deaths}'
      - ''
      - ' &8▶ &fKill-Streak: &c{killstreak}'
      - ' &8▶ &fMaior Kill-Streak: &c{highest_killstreak}'
      - ''
      - '&f> &aVocê pode acessar essa arena.'
      - ''
  unlock:
    material: 'LEATHER_CHESTPLATE'
    name: '&cArena couro'
    lore:
      - '&7Esta é a Arena Inicial. Aqui você'
      - '&7poderá incrementar suas skills'
      - '&7e avançar para a demais arenas.'
      - ''
      - ' &fPontos necessários: &a{points}'
      - ' &fRank necessário: &b[ÁguaI]'
      - ''
      - '&f> &aVocê já pode desbloquear essa arena.'
      - ''
  already:
    material: 'LEATHER_CHESTPLATE'
    name: '&cArena couro'
    lore:
      - '&7Esta é a Arena Inicial. Aqui você'
      - '&7poderá incrementar suas skills'
      - '&7e avançar para a demais arenas.'
      - ''
      - ' &8▶ &fAbates: &a{kills}'
      - ' &8▶ &fMortes: &c{deaths}'
      - ''
      - ' &8▶ &fKill-Streak: &c{killstreak}'
      - ' &8▶ &fMaior Kill-Streak: &c{highest_killstreak}'
      - ''
      - '&f> &cVocê já está dentro desta arena.'
      - ''
  permission:
    material: 'LEATHER_CHESTPLATE'
    name: '&cArena couro'
    lore:
      - '&7Esta é a Arena Inicial. Aqui você'
      - '&7poderá incrementar suas skills'
      - '&7e avançar para a demais arenas.'
      - ''
      - ' &fRank necessário: &b[ÁguaI]'
      - ''
      - '&f> &cVocê não tem permissão para'
      - '&c  entrar nesta arena.'
      - ''
  points:
    material: 'LEATHER_CHESTPLATE'
    name: '&cArena couro'
    lore:
      - '&7Esta é a Arena Inicial. Aqui você'
      - '&7poderá incrementar suas skills'
      - '&7e avançar para a demais arenas.'
      - ''
      - ' &fPontos necessários: &a{points}'
      - ''
      - '&f> &cVocê não tem pontos suficientes'
      - '&c  para entrar nesta arena.'
      - ''
      - '&f> &7Adquira o acesso pagando:'
      - '&2  $&a{money} coins&7.'
      - ''
  top:
    material: 'LEATHER_CHESTPLATE'
    name: '&cArena couro'
    lore:
      - ''
      - ' &7Líderes:'
      - '  &f> 1º {player_1}: &a{amount_1}'
      - '  &f> 2º {player_2}: &a{amount_2}'
      - '  &f> 3º {player_3}: &a{amount_3}'
      - '  &f> 4º {player_4}: &a{amount_4}'
      - '  &f> 5º {player_5}: &a{amount_5}'
      - ''

# Itens que o jogador irá receber ao entrar na arena
kit:
  # Ativar o sistema itens setados
  enabled: true

player-kill:
  # Regenerar a vida ao matar um jogador
  # a vida total do jogador é 20 (10 corações)
  # deixe 0 para não usar
  heal: 5.0
  # Resetar o kit do inventário do jogador ao matar um jogador
  reset-kit: true
  # Pontos que serão dados por kill
  give-points: 1.0
  # Dar algum item ao matar um jogador
  give-items: {}
  # Dar algum comando ao matar um jogador
  give-commands: []
  # Efeitos que serão dados ao matar um jogador
  give-effects:
    - 'SPEED:1-15'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="commands.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     ___                                          _
#    / __\___  _ __ ___  _ __ ___   __ _ _ __   __| |___
#   / /  / _ \| '_ ` _ \| '_ ` _ \ / _` | '_ \ / _` / __|
#  / /__| (_) | | | | | | | | | | | (_| | | | | (_| \__ \
#  \____/\___/|_| |_| |_|_| |_| |_|\__,_|_| |_|\__,_|___/
#
# Lista de comandos do plugin.

# Utilize "comando|comando" para criar aliases.
# Por exemplo: "gm|gamemode"
# Você pode criar quantas aliases quiser.
commands:
  arena: 'arena'
  arenas: 'arenas'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __            _        _
#  _   _|  \/  | __ _ _ __| | _____| |_
# | | | | |\/| |/ _` | '__| |/ / _ \ __|
# | |_| | |  | | (_| | |  |   <  __/ |_
#  \__, |_|  |_|\__,_|_|  |_|\_\___|\__|
#  |___/
#
# Modo de depuração para correção de problemas no plugin.
debug-mode: false

#      ___      _        _
#     /   \__ _| |_ __ _| |__   __ _ ___  ___
#    / /\ / _` | __/ _` | '_ \ / _` / __|/ _ \
#   / /_// (_| | || (_| | |_) | (_| \__ \  __/
#  /___,' \__,_|\__\__,_|_.__/ \__,_|___/\___|
#
# Configurações do banco de dados.

database:
  # Determina o tipo de banco de dados. Valores válidos: [SQLITE, MYSQL, HIKARI (recomendado)]
  storage-type: SQLITE

  # Dados para conexão ao banco de dados MYSQL.
  data:
    # Endereço de conexão do banco de dados. [EX: 127.0.0.1]
    host: localhost
    # Porta de conexão do banco de dados. [EX: 3306]
    port: 3306
    # Nome do banco de dados a ser conectado. [EX: minecraft]
    database: ''
    # Usuário de conexão. [EX: root]
    username: ''
    # Senha do usuário de conexão: [EX: 123]
    password: ''

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Sistemas gerais
general:
  # Sistema de anti-free-kill
  # Armazena por 3 minutos as últimas kills do jogador
  anti-free-kill: true
  # Deletar a recompensa ao clicar com botão direito
  right-delete-reward: true
  # Lista de comandos para sair da arena
  commands-exit:
    - '/sair'
    - '/spawn'
    - '/exit'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locations: {}
]]>
</code-block>
</chapter>

<chapter title="economies.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#  _____                                  _
# | ____| ___  ___  _ __   ___  _ __ ___ (_) ___  ___
# |  _|  / __|/ _ \| '_ \ / _ \| '_ ` _ \| |/ _ \/ __|
# | |___| (__| (_) | | | | (_) | | | | | | |  __/\__ \
# |_____|\___|\___/|_| |_|\___/|_| |_| |_|_|\___||___/

# Providers disponíveis:
#
#   AtlasEconomiaSecundaria, AtlasMinas, AtlasMinasV2,
#   JH_Shop, LegendaryEconomy, NextCash, PlayerPoints,
#   StormEconomiaSecundaria, StormMinas, TGCash,
#   yAlmas, yPoints, yRankup,
#   Vault
#

economies:
  money:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'Money'
    # Formato inteiro
    display: 'Dinheiro'
    # Formato abreviado
    abbreviated: 'coins'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yarenas.provider.money'
]]>
</code-block>
</chapter>

<chapter title="menus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___ _ __  _   _ ___
#   /    \ / _ \ '_ \| | | / __|
#  / /\/\ \  __/ | | | |_| \__ \
#  \/    \/\___|_| |_|\__,_|___/
#
# Sistema de menus.

# Ativar o sistema de atualizar o menu principal automaticamente enquanto estiver aberto
menu-updater: true
# Tempo para atualizar o menu automaticamente
# em ticks -> 20 ticks = 1s
menu-updater-time: 200

# Setas dos menus.
arrows:
  back:
    material: 'ARROW:0'
    name: '&cVoltar'
    lore: ['&7Clique para voltar ao menu anterior.']
  previous:
    material: 'ARROW:0'
    name: '&cAnterior'
    lore: ['&7Clique para ir à página anterior.']
  next:
    material: 'ARROW:0'
    name: '&aPróximo'
    lore: ['&7Clique para ir à próxima página.']

# Menu principal
main:
  name: '&8Arenas'
  size: 27
  items:
    profile-slot: 10
    rewards-slot: 11
    arenas-slot: 13
    top-slot: 14
    go-slot: 16
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7desempenho nas arenas.'
        - ''
        - ' &8▶ &fAbates: &a{kills}'
        - ' &8▶ &fMortes: &c{deaths}'
        - ''
        - ' &8▶ &fRank: &r{rank}'
        - ' &8▶ &fPontos: &b{points}'
        - ''
    rewards:
      material: 'CHEST'
      name: '&aRecompensas'
      lore:
        - ''
        - ' &fRecompensas no armazém: &a{amount}&f.'
        - ''
        - '&7Clique para gerenciar'
    arenas:
      material: 'd01afe973c5482fdc71e6aa10698833c79c437f21308ea9a1a095746ec274a0f'
      name: '&eArenas'
      lore:
        - '&7Confira aqui as arenas do nosso'
        - '&7servidor e comece já sua batalha!'
        - ''
        - '&6Clique para acessar!'
    top:
      material: '4ea96c49302132167c81c87b79e06dd343020ff20923fce87d388c462409261c'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em nossas arenas.'
        - ''
        - '&aClique para acessar!'
    go:
      material: DIAMOND_SWORD
      name: '&aIr batalhar'
      lore:
        - '&7Teleportar para sua arena e começar'
        - '&7a jornada de batalha.'
        - ''
        - ' &fSua arena: &b{arena}&f.'
        - ''
        - '&aClique para ir batalhar'
    exit:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&eSair da arena'
      lore:
        - '&7Terminar sua jornada de batalha'
        - '&7e sair da arena.'
        - ''
        - ' &fArena atual: &b{arena}&f.'
        - ''
        - '&aClique para sair da arena'

# Menu de recompensas
main-rewards:
  name: '&8Arenas'
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

# Menu de arenas
arenas:
  name: '&8Arenas'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  previous-slot: 32
  next-slot: 33
  back-slot: 29

# Menu de arenas
top:
  name: '&8Arenas'
  size: 45
  slots: [ 10, 12, 14, 16 ]
  previous-slot: 33
  next-slot: 34
  back-slot: 28

# Menu principal
manage:
  name: '&8Gerenciar Arena'
  size: 27
  items:
    locations-slot: 10
    kits-slot: 12
    locations:
      material: 'PAPER'
      name: '&aLocais'
      lore:
        - ''
        - ' &fLocais cadastrados: &a{amount}&f.'
        - ''
        - '&7Clique para gerenciar'
    kits:
      material: 'PAPER'
      name: '&aKits'
      lore:
        - ''
        - ' &fKits cadastrados: &a{amount}&f.'
        - ''
        - '&7Clique para gerenciar'

# Menu de configuração dos locais
locations:
  name: '&8Gerenciar Arena'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 47
  items:
    add-slot: 49
    location:
      material: 'PAPER'
      name: '&aLocal #{location}'
      lore:
        - ''
        - '&fLocalização: &fX:&b{x}&f - &fY:&b{y}&f - &fZ:&b{z} &7({world})'
        - ''
        - '&aBotão ESQUERDO para teleportar.'
        - '&aBotão Q para deletar.'
    add:
      material: '924757bc9a3171f9d0fdfbd209ac42e15f7744eb5f2db31920ff8af8d94567c6'
      name: '&aAdicionar Local'
      lore: [ '&7Clique para adicionar mais', '&7um local nesta arena.' ]

# Menu de configuração dos kits
kits:
  name: '&8Gerenciar Arena'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 47
  items:
    add-slot: 49
    kit:
      material: 'PAPER'
      name: '&aKit &e#{order}'
      lore:
        - ''
        - ' &fOrdem: &e{order}'
        - ' &fPermissão: &e{permission}'
        - ''
        - '&aBotão &fESQUERDO&a para gerenciar.'
        - '&aBotão &fDIREITO&a para pré-visualizar.'
        - '&aBotão &fQ&a para deletar.'
    add:
      material: '924757bc9a3171f9d0fdfbd209ac42e15f7744eb5f2db31920ff8af8d94567c6'
      name: '&aAdicionar Kit'
      lore: [ '&7Clique para adicionar mais', '&7um kit nesta arena.', '', '&f* &8(Necessário estar com os itens)', '' ]

# Menu de opções
options:
  name: '&8Gerenciar Arena'
  size: 27
  back-slot: 10
  items:
    order-slot: 12
    permission-slot: 14
    order:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aOrdem'
      lore:
        - '&7A ordem serve para classificar os kits'
        - '&7de acordo com sua permissão. Assim dando'
        - '&7o melhor kit que o jogador tem direito.'
        - ''
        - '&fOrdem: &7{order}&f.'
        - ''
        - '&aClique para alterar a ordem'
    permission:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aPermissão'
      lore:
        - '&7Permissão para obter esse kit ao'
        - '&7entrar na arena.'
        - ''
        - '&fPermissão: &7{permission}&f.'
        - ''
        - '&aBotão &fESQUERDO&a para alterar a permissão'
        - '&aBotão &fDIREITO&a para remover a permissão'
]]>
</code-block>
</chapter>

<chapter title="messages.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___  ___ ___  __ _  __ _  ___  ___
#   /    \ / _ \/ __/ __|/ _` |/ _` |/ _ \/ __|
#  / /\/\ \  __/\__ \__ \ (_| | (_| |  __/\__ \
#  \/    \/\___||___/___/\__,_|\__, |\___||___/
#                              |___/
#
# Mensagens a serem enviadas pelo plugin.

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/arena &8- &7Abre o menu principal.
    &a/arena ir &8- &7Entra na arena.
    &a/arena sair &8- &7Sai da arena.
    &a/arena top &8- &7Abre o menu de top.
    &a/arena recompensas &8- &7Abre o menu de recompensas.
    &a/arena arenas &8- &7Abre o menu de arenas.
    &a/arena setsaida &8- &7Define a saída das arenas.
    &a/arena add &8- &7Adiciona pontos para um jogador.
    &a/arena remove &8- &7Remove pontos de um jogador.
    &a/arena set &8- &7Seta pontos para um jogador.
    &a/arena reload &8- &7Recarregar as configurações.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  command: '&cVocê não pode executar este comando na arena.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  bought: '&aVocê comprou a ativação da arena &f{arena}&a.'
  arena-found: |
    &cEssa arena não existe.
    &cDisponiveis: {list}
  arena-location-added: '&aLocal adicionado.'
  arena-location-removed: '&aLocal removido.'
  arena-location-teleported: '&aTeleportado.'
  arena-player-found: '&cNenhuma arena disponível para você.'
  arena-not-in: '&cVocê não está está em uma arena.'
  arena-not-unlocked: '&cVocê não desbloqueou esta arena ainda.'
  arena-already-in: '&cVocê já está em uma arena.'
  arena-location-found: '&cNenhuma entrada encontrada.'
  arena-exit-found: '&cSaída da arena não encontrada.'
  arena-exit-set: '&aA saída das arenas foi setada com sucesso.'
  arena-kit-added: '&aKit adicionado.'
  arena-kit-removed: '&aKit removido.'
  arena-kit-empty: '&cO seu inventário está vazio.'
  arena-inventory-empty: '&cVocê deve esvaziar seu inventário.'
  digit-order: |

    &aDigite a ordem para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-permission: |

    &aDigite a permissão para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  change-order: '&aVocê alterou a ordem para {order}.'
  change-permission: '&aVocê alterou a permissão para {permission}.'
  points-changed: '&aPontos do jogador &f{player}&a alterado para &f{points}&a.'
]]>
</code-block>
</chapter>

<chapter title="plugin.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: yArenas
version: '${project.version}'
main: com.ystoreplugins.yarenas.Main
authors: [ yChusy ]
website: https://ystoreplugins.com.br
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
ranks:
   bronze:
      order: 1
      # Tag do rank
      tag: '&7[&6Bronze&7]'
      # Pontos necessários para ficar no rank
      points: 0.0
   iron:
      order: 2
      tag: '&7[&fFerro&7]'
      points: 2.0
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


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/158-yArenas">Site do plugin yArenas</a>
    </category>
</seealso>