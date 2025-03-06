# yPesca
<secondary-label ref="rankup"/>

### Descrição
Sistema de pesca completo com torneios

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
<video src="//www.youtube.com/watch?v=Qk9F2Vl8ZPI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/pesca - Abre o menu principal
/pesca top - Abre o menu de top
/pesca ajuda - Envia a mensagem de ajuda
/pesca ir - Vai até a área de pesca
/pesca sair - Sai da área de pesca
/pesca peixes - Abre o menu de armazém de peixes
/corais - Vê a quantia de corais
/corais [player] - Vê a quantia de corais de um jogador
/corais enviar - Envia seus corais para um jogador
/corais add - Adiciona corais para um jogador
/corais give - Dá corais em forma de itens para um jogador
/corais set - Seta corais para um jogador
/corais remove - Remove corais de um jogador
/pesca setspawn - Seta o local de spawn da área de pesca
/pesca setsaida - Seta a saída da pesca
/pesca iniciartorneio - Inicia um torneio
/pesca parartorneio - Finaliza um torneio
/pesca givebooster - Dá um booster à um jogador
/pesca giveclasse - Dá uma classe à um jogador
/pesca givefish - Dá um peixe à um jogador
/pesca resetrod - Reseta a vara de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ypesca.use - Permissão para o /pesca
ypesca.top - Permissão para o /pesca top
ypesca.go - Permissão para o /pesca ir
ypesca.exit - Permissão para o /pesca sair
ypesca.sell - Permissão para o /pesca peixes
ypesca.sellall - Permissão para o sell - all
ypesca.coin.use - Permissão para o /corais
ypesca.coin.look - Permissão para o /corais [player]
ypesca.coin.send - Permissão para o /corais enviar
ypesca.coin.help - Permissão para o /corais ajuda
ypesca.coin.add - Permissão para o /corais add
ypesca.coin.remove - Permissão para o /corais remove
ypesca.coin.set - Permissão para o /corais set
ypesca.coin.give - Permissão para o /corais give
ypesca.setspawn - Permissão para o /pesca setspawn
ypesca.setexit - Permissão para o /pesca setexit
ypesca.tournament.start - Permissão para o /pesca iniciartorneio
ypesca.tournament.stop - Permissão para o /pesca parartorneio
ypesca.givebooster - Permissão para o /pesca givebooster
ypesca.giveclasse - Permissão para o /pesca giveclasse
ypesca.givefish - Permissão para o /pesca givefish
ypesca.resetrod - Permissão para o /pesca resetrod</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ypesca_time% - Retorna o tempo que o jogador ficou pescando
%ypesca_time_raw% - Retorna o tempo que o jogador ficou pescando sem formatar
%ypesca_best_weight% - Retorna o maior peso que o jogador já pescou
%ypesca_fished% - Retorna a quantia de peixes que o jogador pescou
%ypesca_fished_raw% - Retorna a quantia de peixes que o jogador pescou sem formatar
%ypesca_fished_round% - Retorna a quantia de peixes que o jogador pescou em uma rodada
%ypesca_fished_round_raw% - Retorna a quantia de peixes que o jogador pescou em uma rodada sem formatar
%ypesca_coin% - Retorna a quantia de corais do jogador
%ypesca_coin_raw% - Retorna a quantia de corais do jogador sem formatar
%ypesca_tag% - Retorna a tag para o ganhador do torneio
%ypesca_level% - Retorna a o level atual do jogador (formatado)
%ypesca_level_raw% - Retorna a o level atual do jogador (sem formatar)
%ypesca_classe% - Retorna a classe atual
%ypesca_classe_next% - Retorna a próxima classe
%ypesca_classe_progress% - Retorna a barra de progresso de evolução da classe
%ypesca_classe_percentage% - Retorna a porcentagem de progresso de evolução da classe
%ypesca_progress% - Retorna a barra de progresso de evolução da vara
%ypesca_percentage% - Retorna a porcentagem de progresso de evolução da vara
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{ypesca} - Tag do jogador que ganhou o torneio
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPesca/
    ├── bungeecord.yml
    ├── classes.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── enchantments.yml
    ├── fishs.yml
    ├── menus.yml
    ├── messages.yml
    ├── rewards.yml
    └── rods.yml
</code-block>
</chapter>

<chapter title="bungeecord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     ___                                               _
#    / __\_   _ _ __   __ _  ___  ___  ___ ___  _ __ __| |
#   /__\// | | | '_ \ / _` |/ _ \/ _ \/ __/ _ \| '__/ _` |
#  / \/  \ |_| | | | | (_| |  __/  __/ (_| (_) | | | (_| |
#  \_____/\__,_|_| |_|\__, |\___|\___|\___\___/|_|  \__,_|
#                     |___/
#
# Sistema de múltiplos servidores.

# Ativar o sistema de bungeecord
enabled: false

# Modo deste servidor
# LOBBY (ex: servidor de RankUP)
# SERVER (ex: servidor que contém a pesca)
mode: 'LOBBY'

# Nome do servidor na config do BungeeCord em que o jogador vai ao sair da pesca
exit: 'rankup'

# Nome do servidor na config do BungeeCord em que o jogador vai ao entrar na pesca
entry: 'pesca'

# Delay para enviar a vara ao trocar para o servidor da pesca
# em ticks
delay: 3
]]>
</code-block>
</chapter>

<chapter title="classes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
classes:
  class1:
    # O padrão é a ordem 0
    order: 0
    display: '&fQuartzo'
    # Cor da armadura
    # Formato: RED:GREEN:BLUE (255:255:255)
    # deixe RAINBOW para ser colorido
    color: '255:255:255'
    # Permissão para evoluir à esta classe
    # Deixe '' (vazio) para não usar
    permission: ''
    # Efeito:Nível
    effects: ['SPEED:1']
    # Bônus que serão dados
    bonus:
      fish-chance: 5.0
      coin: 10.0
    # Custos de evolução
    prices:
      price1:
        provider: 'money'
        price: 1000.0
      price2:
        provider: 'yminas'
        price: 1000.0
    # Item ativável
    item:
      material: LEATHER_HELMET
      name: '&fClasse Quartzo'
      lore:
        - ''
        - ' &7As classes irão te dar mais'
        - ' &7chance e coins ao pescar!'
        - ''
        - '&fBônus adquiridos:'
        - '&7- +{fish-chance}% de chance'
        - '&7- +{coin}% de coins'
        - ''
        - '&aClique para ativar'
    # Itens da armadura
    armor:
      helmet:
        material: LEATHER_HELMET
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
      chestplate:
        material: LEATHER_CHESTPLATE
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
      leggings:
        material: LEATHER_LEGGINGS
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
      boots:
        material: LEATHER_BOOTS
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
    # Itens do menu de classes
    menu:
      buy:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - '&7- &e{ypesca} moedas'
          - ''
          - '&aClique para evoluir'
      has:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
          - '&aClique para equipar.'
      equipped:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
          - '&aVocê está usando este.'
      need:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - '&7- &e{ypesca} moedas'
          - ''
          - '&cVocê não possui os custos para evoluir.'
      previous:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins ao pescar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{fish-chance}% de chance'
          - '&7- +{coin}% de coins'
          - ''
          - '&cVocê não possui a classe anterior.'
]]>
</code-block>
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
  fish: 'pesca|pescaria|fish|fishing'
  coin: 'corais|coral'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#           ___
#   _   _  / _ \___  ___  ___ __ _
#  | | | |/ /_)/ _ \/ __|/ __/ _` |
#  | |_| / ___/  __/\__ \ (_| (_| |
#   \__, \/    \___||___/\___\__,_|
#   |___/
#
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
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
# Sistemas principais.]

# Ativar a invisibilidade na área de pesca
invisibility: false

# O jogador deverá evoluir uma vara por vez
evolute-crescent: true

# Nome da skill de pesca no mcmmo
mcmmo-skill: 'FISHING'

# Somar um nível a mais na evolução
sum-evolute: true

# Ativar o menu de confirmação de compra
confirm-menu: true

# Sistema de bolsa de valores (yBolsa, StormEconomy ou HeroBolsa)
bolsa: true

# Quantidade do Y que vai teleportar ao spawn
# 1.19 usa-se -64
void-detect: 0

# Tag do ganhador do torneio
tournament-tag: '&e[*]'

# Ativar o sistema de classes
classes: true

# Para evoluir as classes ele deverá seguir a ordem delas?
classes-ordered: true

# Sistemas quando estiver pescando
fishing:
  # Raio de detecção de água perto ou quando clicar para pescar
  # em blocos
  water-radius: 10.0
  # Ativar a verificação de água por perto (quando se afastar, para de pescar)
  # Pode gerar lag
  verify-has-water: false
  # Cancelar quando o peixe vanila encostar na vara
  cancel-fish-interact: false
  # Horário para pescar
  time:
    enabled: false
    # Calibre o horário do plugin (Brasil: GMT-3)
    gmt-offset: -3
    # Horário de início
    from: '10:00'
    # Horário de término
    to: '18:00'
  # Sistema da sacola de peixe
  fishing-net:
    # Limite de peixes que poderá ser armazenado
    # Recomendado: 30
    # Deixe 0 para ser infinito
    limit: 40
  # Sistema de sell-all
  sell-all:
    # Ativar o sell-all em async
    async: true
    # Fechar o menu ao vender tudo
    close-menu: true
    # Limite de itens vendidos pelo sell-all
    # Recomendado: 40
    # Deixe 0 para ser infinito
    limit: 40

# Sistema de scoreboard
scoreboard:
  enabled: true
  title: '&b&lyStore'
  # Delay para atualizar a scoreboard (em segundos)
  delay: 1
  lines:
    - '&7         Área de pesca'
    - ''
    - '&f Status: &r{status}'
    - ''
    - '&f Peixes pescados: &7{fished}'
    - '&f Tempo pescando: &7{time}'
    - ''
    - '&e Vara'
    - '&8  ❘&f Nível: &7{level}'
    - '&8  ❘&f Corais: &7{coin_has}/{coin_next}'
    - '&8  ❘ {progressbar}'
    - ''
    - '&f Coins: &2$&a{money}'
    - ''
    - '&b    ystoreplugins.com.br'

# Itens padrões definidos para o jogador.
items:
  rod-slot: 1
  # Item utilizado para que o jogador veja os drops (peixes) armazenados/pescados
  fishing-net:
    material: '4cb3acdc11ca747bf710e59f4c8e9b3d949fdd364c6869831ca878f0763d1787'
    slot: 4
    name: '&bSacola de peixes'
    lore:
      - '&7Clique para gerenciar os'
      - '&7seus peixes pescados.'
  # Item utilizado para que o jogador saia da pesca.
  exit:
    material: 'BARRIER:0'
    slot: 7
    name: '&cSair da pesca'
    lore:
      - '&7Clique para sair da'
      - '&7área de pesca.'
  # Item utilizado para que o jogador saia da pesca.
  classes:
    material: 'LEATHER_CHESTPLATE:0'
    slot: 6
    name: '&bClasses'
    lore:
      - ' &7As classes irão te dar mais'
      - ' &7chance e coins ao pescar!'
      - ''
      - '&fSua classe: &7{classe}'
      - ''
      - '&aClique para upar sua classe'
  # Siga o exemplo abaixo para criar itens custom
  #custom:
  #  material: BARRIER:0
  #  slot: 0
  #  name: ''
  #  lore: []
  #  left-command: ''
  #  right-command: ''
  #  left-perm: 'ypesca.left-perm.custom'
  #  right-perm: 'ypesca.right-perm.custom'

# Sistema de comandos na pesca
commands:
  # Lista de comandos permitidos na pesca
  allowed: [ '/g', '/l', '/pesca' ]
  # Lista de comandos para sair da pesca
  exit: [ '/sair', '/spawn', '/exit' ]

# Sistema de barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-full: '&a'
  color-empty: '&7'

# Sistema de status
status:
  fishing: '&aPescando... {delay_now}s'
  not-fishing: '&cInativo'

# Sistema de boosters
# Você pode criar quantos boosters quiser
boosters:
  booster1:
    time: 60 # em segundos
    bonus: 10.0 # porcentagem a mais
    items:
      interact:
        material: 'EXP_BOTTLE:0'
        name: '&aBônus de pesca'
        lore:
          - '&7Este booster permite que você tenha'
          - '&7mais chances de pescar algo melhor.'
          - ''
          - '&aTempo: &e{time}'
          - '&aPorcentagem: &e{bonus}%'
          - ''
      menu:
        material: 'EXP_BOTTLE:0'
        name: '&aBônus de pesca'
        lore:
          - '&aVocê possui um booster ativo'
          - ''
          - '&7Este booster permite que você tenha'
          - '&7mais chances de pescar algo melhor.'
          - ''
          - '&aTempo: &e{time}'
          - '&aPorcentagem: &e{bonus}%'
          - ''

# Sistema de bônus
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender para a loja do servidor.
bonus:
  member:
    priority: 1
    # Permissão para ser reconhecido
    permission: 'ypesca.bonus.member'
    # Quantia do bônus em %
    bonus: 10.0

# Item de coin ativável
usable-item:
  material: '1ba16c3890af39c3f2d576586cff443de07dad32b2315e2ff6f0d5d6a3c663dd'
  name: '&b+{amount} Corais'
  lore:
    - ''
    - '&fQuantia: &b{amount}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus corais no inventário em 1 só.'
    - ''

# Sistema de formatos de money e quantia
format:
  type: 'LETTER' # Tipos: LETTER - NUMBER
  max-decimals: 4
  formats:
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

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locais: {}
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
  Money:
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
    permission: 'ypesca.provider.money'
  ypesca:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yPesca'
    # Formato inteiro
    display: 'Moedas'
    # Formato abreviado
    abbreviated: 'moedas'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'ypesca.provider.ypesca'
]]>
</code-block>
</chapter>

<chapter title="enchantments.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     __           _                 _                        _
#    /__\ __   ___| |__   __ _ _ __ | |_ _ __ ___   ___ _ __ | |_ ___
#   /_\| '_ \ / __| '_ \ / _` | '_ \| __| '_ ` _ \ / _ \ '_ \| __/ __|
#  //__| | | | (__| | | | (_| | | | | |_| | | | | |  __/ | | | |_\__ \
#  \__/|_| |_|\___|_| |_|\__,_|_| |_|\__|_| |_| |_|\___|_| |_|\__|___/
#
# Encantamentos das varas de pesca.

# Apague apenas os encantamentos que não for usar
enchantments:
  lucky: # Não mude este nome, ou o encantamento não será reconhecido
    display: 'Sortudo'
    default: 0.0
    maximum: 10.0 # Use -1 para ser infinito
    percentage: 0.01 # porcentagem adquirida por nível
    price:
      default: 100.0
      per-level: 200.0
    items: # Item que aparecerá no menu de evolução
      can: # quando puder evoluir
        material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        name: '&aSortudo'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte de receber peixes.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{coin} corais&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      can-not: # quando não puder evoluir
        material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        name: '&aSortudo'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte de receber peixes.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{coin} corais&f.'
          - ''
          - '&cVocê não tem corais suficientes.'
      maximum: # quando já estiver no máximo
        material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        name: '&aSortudo'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte de receber peixes.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'
  multiplier: # Não mude este nome, ou o encantamento não será reconhecido
    display: 'Multiplicador'
    default: 0.0
    maximum: 10.0 # Use -1 para ser infinito
    multiplier: 0.01 # multiplicador adquirido por nível
    price:
      default: 100.0
      per-level: 200.0
    items: # Item que aparecerá no menu de evolução
      can: # quando puder evoluir
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais corais ao pescar.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Multiplicador Atual: &b{multiplier}%&f.'
          - ''
          - '&f > Custo: &a{coin} corais&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      can-not: # quando não puder evoluir
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais corais ao pescar.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Porcentagem Atual: &b{multiplier}%&f.'
          - ''
          - '&f > Custo: &a{coin} corais&f.'
          - ''
          - '&cVocê não tem corais suficientes.'
      maximum: # quando já estiver no máximo
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais corais ao pescar.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Porcentagem Atual: &b{multiplier}%&f.'
          - ''
          - '&cVocê já está no máximo.'
custom-enchantments:
  keychain:
    display: 'Chaveiro'
    default: 0.0
    maximum: -1 # Use -1 para ser infinito
    percentage: 10 # porcentagem adquirida por nível
    price:
      default: 100.0
      per-level: 200.0
    # chance,comando
    commands:
      - '20,give {player} quartz 1'
    messages:
      title: '&aChave<nl>&eencontrado' # deixe '' para não usar
      actionbar: '' # deixe '' para não usar
      chat: [ ]
    items: # Item que aparecerá no menu de evolução
      can: # quando puder evoluir
        material: GOLD_INGOT
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao pescar.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Bônus atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{coin} corais&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      can-not: # quando não puder evoluir
        material: GOLD_INGOT
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao pescar.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Chance atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{coin} corais&f.'
          - ''
          - '&cVocê não tem corais suficientes.'
      maximum: # quando já estiver no máximo
        material: GOLD_INGOT
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao pescar.'
          - ''
          - '&f > Nível: &b{has}&f/&b{max}&f.'
          - '&f > Chance atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="fishs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     ___ _     _
#    / __(_)___| |__  ___
#   / _\ | / __| '_ \/ __|
#  / /   | \__ \ | | \__ \
#  \/    |_|___/_| |_|___/
#
# Peixes disponíveis para pesca.

fishs:
  normal:
    # Nível necessário da vara de pesca
    level: 1
    display-name: 'Normal L.1'
    # Raridades do peixe
    # Definida na rarities.yml
    # chance,raridade
    rarities:
      - '100.0,normal'
    # Preços base de venda do peixe
    base-prices:
      cost1:
        type: 'Money'
        price: 10.0
      cost2:
        type: 'PlayerPoints'
        price: 5.0
    # Preços por peso do peixe (será somado ao preço base)
    weight-prices:
      cost1:
        type: 'Money'
        price: 10.0
      cost2:
        type: 'PlayerPoints'
        price: 5.0
    # Peso mínimo e máximo do peixe
    weight:
      min: 1
      max: 10
    # Quantia mínima e máxima que pode ganhar de Moedas de evolução ao pescar um peixe
    coin:
      min: 1
      max: 2
    # Quantia mínima e máxima que pode ganhar de XP do MCMMO ao pescar um peixe
    mcmmo:
      min: 1
      max: 2
    # Item do peixe no menu de venda
    display-sell:
      material: 'RAW_FISH:0'
      name: '&aPeixe normal &7[&fL.1]'
      lore:
        - ''
        - ' &7Nível: &f{level}'
        - ' &7Raridade: &f{rarity} &8(+{rarity_price} coins) (+{rarity_price_PlayerPoints} pontos)'
        - ' &7Peso: &f{weight} &8(+{weight_price} coins) (+{weight_price_PlayerPoints} pontos)'
        - ' &7Quantia: &f{amount}'
        - ''
        - ' &7Preço unitário: &f10'
        - ' &fSeu bônus: &b{bonus}%'
        - ''
        - ' &7Preço total (somado bônus, peso e raridade):'
        - '  &f->&a {total_price} coins, {total_price_PlayerPoints} pontos'
        - ''
        - '&aClique para vender'
    # Item do peixe no menu de preview
    display:
      material: 'FISH:0'
      name: '&aPeixe normal &7[&fL.1]'
      lore:
        - ''
        - ' &7Pesos: &f1 à 10 gramas'
        - ' &7Raridades: &fNormal'
        - ' &7Preço unitário: &f10'
        - ''

rarities:
  normal:
    # Valores bônus que o peixe irá dar na venda
    bonus-prices:
      cost1:
        type: 'Money'
        price: 5.0
      cost2:
        type: 'PlayerPoints'
        price: 2.0
    # Pode utilizar cor
    display: 'Normal'
    # Mensagens que serão enviadas (ao jogador)
    messages:
      title: ''
      actionbar: '&aVocê pescou um peixe de raridade normal'
      chat: ''
    # Mensagens que serão enviadas (ao jogador)
    broadcast-messages:
      title: ''
      actionbar: '' #'&a{player} pescou um peixe de raridade normal'
      chat: ''
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
  name: '&8Pescaria'
  size: 36
  items:
    profile:
      slot: 10
      material: '{player}'
      name: '&aSuas informações'
      lore:
        - ''
        - '&7* Nível da vara: &f{level} -> &f{weight}g ({delay}s)'
        - '&7* Peixes pescados: &f{fished}'
        - '&7* Maior peso já pescado: &f{best_weight}g'
        - ''
        - '&e* Tempo pescando: &f{time}'
        - '&b* Quantia de corais: &f{coin_has}'
        - ''
    rod:
      slot: 12
      material: 'FISHING_ROD:0'
      name: '&aVara de Pesca'
      lore:
        - ''
        - '&b* Nível atual: &f{level}'
        - '&b* Peso suportado: &f{weight}g'
        - '&b* Delay para pescar: &f{delay}s'
        - ''
        - '&7Clique para gerenciar sua vara de pesca'
    fishing-net:
      slot: 13
      material: '4cb3acdc11ca747bf710e59f4c8e9b3d949fdd364c6869831ca878f0763d1787'
      name: '&aSacola de peixes'
      lore:
        - ''
        - '&b* Peixes armazenados: &f{fishs}'
        - ''
        - '&7Clique para gerenciar seus drops'
    top:
      slot: 14
      material: 'BOOK_AND_QUILL:0'
      name: '&aTOP'
      lore:
        - '&7Veja os jogadores que'
        - '&7se destacaram na pescaria.'
        - ''
        - '&aClique para visualizar'
    shop:
      slot: 15
      material: 'GOLD_INGOT'
      name: '&bLoja de Corais'
      lore:
        - '&7Aqui você pode adquirir itens utilizando'
        - '&7os seus &nCorais&7.'
        - ''
        - '&aClique para abrir a loja.'
    go:
      slot: 16
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aIr pescar'
      lore:
        - '&7Clique para entrar na'
        - '&7área de pesca'
    leave:
      slot: 16
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cSair da pesca'
      lore:
        - '&7Clique para sair da'
        - '&7área de pesca'
    booster:
      slot: 21
      material: 'GLASS_BOTTLE:0'
      name: '&aBooster'
      glow: true
      lore:
        - '&cVocê não possui nenhum booster ativo.'
    tournament-no-has:
      slot: 22
      material: 'BARRIER:0'
      name: '&aTorneio'
      glow: true
      lore:
        - '&cNo momento não está ocorrendo nenhum torneio.'
    tournament-weight:
      slot: 22
      material: 'GOLD_INGOT:0'
      name: '&aTorneio'
      glow: true
      lore:
        - '&aEsta ocorrendo um torneio na pesca!'
        - ''
        - '&7Irá ganhar o jogador que pescar o peixe'
        - '&7mais pesado.'
        - ''
        - '&fPrêmio: &a{prize} coins'
        - '&fTempo restante: &a{time}'
        - ''
        - '&f1º {player_pos1}: &b{weight_pos1}g'
        - '&f2º {player_pos2}: &b{weight_pos2}g'
        - '&f3º {player_pos3}: &b{weight_pos3}g'
        - ''
    tournament-fished:
      slot: 22
      material: 'GOLD_INGOT:0'
      name: '&aTorneio'
      glow: true
      lore:
        - '&aEsta ocorrendo um torneio na pesca!'
        - ''
        - '&7Irá ganhar o jogador que pescar a maior'
        - '&7quantia de peixes.'
        - ''
        - '&fPrêmio: &a{prize} coins'
        - '&fTempo restante: &a{time}'
        - ''
        - '&f1º {player_pos1}: &b{fished_pos1}g'
        - '&f2º {player_pos2}: &b{fished_pos2}g'
        - '&f3º {player_pos3}: &b{fished_pos3}g'
        - ''
    classes:
      slot: 23
      material: 'LEATHER_CHESTPLATE'
      name: '&bClasses'
      glow: true
      lore:
        - ' &7As classes irão te dar mais'
        - ' &7chance e coins ao pescar!'
        - ''
        - '&fSua classe: &7{classe}'
        - ''
        - '&aClique para gerenciar as classes'
# Menu top
top:
  name: '&8Top pescaria'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 30
  previous-slot: 9
  next-slot: 17
  # Seletor dos tops
  selector:
    slot: 31
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor do TOP'
    # Tipos do seletor
    types:
      fished:
        enabled: true
        name: 'Peixes pescados'
      coin:
        enabled: true
        name: 'Corais'
      weight:
        enabled: true
        name: 'Peixe mais pesado'
      time:
        enabled: true
        name: 'Tempo pescando'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{nome}'
      select: ' &f• &7{nome}'
  items:
    # Item do top peixes pescados
    fished:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fPeixes pescados: &7{fished}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top corais
    coin:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fCorais: &7{coin}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top peixe mais pesado
    weight:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fPeixe mais pesado: &7{weight}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top tempo pescando
    time:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fTempo pescando: &7{time}'
        - '&fPosição: &e{pos}º'
        - ''
# Menu de evolução
evolve:
  name: '&8Vara - Evoluir'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 28
  previous-slot: 18
  next-slot: 26
  items:
    profile-slot: 32
    rod-slot: 30
    buy-rod-slot: 34
    repair-slot: 31
    profile:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&fCorais: &b{coin_has}'
        - '&fPeixes pescados: &b{fished}'
        - ''
    buy-rod:
      material: 'DIAMOND'
      name: '&aEvoluir vara'
      lore:
        - '&7Compre varas melhores e tenha'
        - '&7mais vantagens para pescar.'
        - ''
        - '&b* Nível atual: &f{level}'
        - '&b* Peso suportado: &f{weight}g'
        - '&b* Delay para pescar: &f{delay}s'
        - ''
        - '&aClique para acessar'
    repair:
      material: 'ANVIL:0'
      name: '&aReparar vara'
      lore:
        - '&7Sua vara está quebrada.'
        - '&7Para continuar pescando você'
        - '&7irá precisar repará-la.'
        - ''
        - ' &f* Preço em corais: &b{coin}'
        - ' &f* Preço em money: &b{Money}'
        - ''
        - '&aClique para reparar'
# Menu de venda
fishing-net:
  name: '&8Sacola de peixes'
  size: 45
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  back-slot: 37
  previous-slot: 18
  next-slot: 26
  items:
    sell-all-slot: 40
    fish-format: '&f{fish_display} &8(Q.{amount}) &f- &7Peso: &f{weight}&7: (&2$&f{value}&7)'
    fish-format-none: '&cVocê não possui nenhum peixe'
    sell-all:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aVender tudo'
      lore:
        - '&7Venda todos os seus peixes armazenados'
        - ''
        - '&a* Todos os seus peixes valem: &f${total_price}'
        - ''
        - '{fishs}'
        - ''
        - '&aClique para vender'
    sell-all-no-perm:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aVender tudo'
      lore:
        - ''
        - '&cVocê não tem permissão.'
        - ''
# Menu de comprar varas
shop:
  name: '&8Evoluir vara'
  size: 27
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 22
  previous-slot: 9
  next-slot: 17

# Menu de shop
shop-fish:
  name: '&8PESCA SHOP'
  size: 27
  back-slot: 10
  profile:
    slot: 12
    material: '{player}'
    name: '&a{player}'
    lore: [ '&7Seus corais: &f{credit}' ]
  items:
    swords:
      price: 100.0
      preview:
        slot: 14
        material: 'DIAMOND'
        name: '&b&lVIP DIAMANTE'
        lore: ['&7Compre seu vip diamante', '&7muito especial para o servidor.']
      item:
        material: 'DIAMOND'
        name: 'EOQ'
        lore: []
      command: [ 'darvip {player} diamante 10000' ]

# Menu de confirmação
confirm:
  name: '&8Confirmação de compra'
  size: 27
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  items:
    item-slot: 13
    confirm-slot: 11
    cancel-slot: 15
    confirm:
      material: 'WOOL:5'
      name: '&aConfirmar'
      lore: [ '&7Clique para &aconfirmar&7 a compra.' ]
    cancel:
      material: 'WOOL:14'
      name: '&cCancelar'
      lore: [ '&7Clique para &ccancelar&7 a compra.' ]

# Menu de classes
classes:
  name: '&8Pesca - Classes'
  size: 54
  slots: [ 11, 12,13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33]
  back-slot: 48
  previous-slot: 18
  next-slot: 26
  items:
    classe-slot: 50
    classe:
      material: LEATHER_CHESTPLATE
      name: '&bClasses'
      lore:
        - ' &7As classes irão te dar mais'
        - ' &7chance e coins ao pescar!'
        - ''
        - '&fSua classe: &7{classe}'
        - ''
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

# Mensagens e ações ao entrar
enter:
  title: '&bBem vindo à área de pesca'
  actionbar: '&bVocê entrou na área de pesca.'
  sound: 'ORB_PICKUP'
  chat: |
    <nl>
    &bBem vindo à área de pesca.
    <nl>

# Mensagens e ações ao sair
leave:
  title: ''
  actionbar: '&bVocê saiu da área de pesca.'
  sound: 'ORB_PICKUP'
  chat: |
    <nl>
    &bVocê saiu da área de pesca.
    <nl>

# Mensagens e ações ao começar a pescar
start:
  title: '&aPesca<nl>&eVocê começou a pescar'
  actionbar: '&aPesca: &eVocê começou a pescar!'
  sound: 'ORB_PICKUP'
  chat: |
    <nl>
    &r  &aPesca:
    &r  &eVocê começou a pescar
    <nl>

# Mensagens e ações ao parar de pescar
stop:
  title: '&aPesca<nl>&cVocê parou de pescar'
  actionbar: '&aPesca: &cVocê parou de pescar!'
  sound: 'CAT_MEOW'
  chat: |
    <nl>
    &r  &aPesca:
    &r  &cVocê parou de pescar
    <nl>

actionbar:
  fishing: '&aPesca: &eVocê está pescando! Peixes pescados &a{fished}&e.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  spawn: '&cO spawn da área de pesca não foi setado.'
  exit: '&cA saída da área de pesca não foi setada.'
  empty: '&cVocê deve esvaziar seu inventário.'
  help: |
    <nl>
    &a/pesca &8- &7Abre o menu principal.
    &a/pesca ir &8- &7Vai até a pesca.
    &a/pesca sair &8- &7Sai da pesca.
    &a/pesca peixes &8- &7Abre o armazem de peixes.
    &a/pesca setspawn &8- &7Seta o local de spawn da pesca.
    &a/pesca setsaida &8- &7Seta o local de saída da pesca.
    &a/pesca iniciartorneio &8- &7Inicia um torneio.
    &a/pesca parartorneio &8- &7Finaliza um torneio.
    &a/pesca givebooster &8- &7Dá um booster à um jogador.
    &a/pesca givefish &8- &7Dá um peixe à um jogador.
    <nl>
  not-in: '&cVocê não está na área de pesca.'
  set-exit: '&aLocal de saída setado com sucesso.'
  set-spawn: '&aLocal de spawn setado com sucesso.'
  command: '&cVocê não pode usar este comando na área de pesca. Utilize /spawn para sair dela.'
  evolved: '&aO encantamento &f{enchantment}&a foi evoluido para o nível &f{level}&a.'
  coin-help: |
    <nl>
    &a/corais &8- &7Ver os seus corais.
    &a/corais <player> &8- &7Ver os corais de alguém.
    &a/corais enviar <player> <quantia> &8- &7Envia seus corais para alguém.
    &a/corais give <player/all> <quantia> &8- &7Dar corais a alguém.
    &a/corais add <player> <quantia> &8- &7Adiciona corais a alguém.
    &a/corais set <player> <quantia> &8- &7Remove corais de alguém.
    &a/corais remove <player> <quantia> &8- &7Seta corais a alguém.
    <nl>
  coin: '&bVocê possui &f{coin} corais&b.'
  coin-player: '&bO jogador &f{player}&b possui &f{coin} corais&b.'
  coin-added: '&bVocê adicionou &f{coin} corais&b ao jogador &f{player}&b.'
  coin-removed: '&bVocê removeu &f{coin} corais&b do jogador &f{player}&b.'
  coin-set: '&bVocê setou &f{coin} corais&b para o jogador &f{player}&b.'
  coin-sent: '&bVocê enviou &f{coin} corais&b para o jogador &f{player}&b.'
  coin-received: '&bVocê recebeu &f{coin} corais&b do jogador &f{player}&b.'
  coin-has: '&cVocê não possui a quantia de &f{coin}&c corais.'
  fished-heavy: '&cVocê pescou um peixe mais pesado do que sua vara suporta, portanto ele escapou.'
  fished-heavy-break: '&cVocê pescou um peixe mais pesado do que sua vara suporta, portanto sua vara quebrou.'
  broken: '&cSua vara está quebrada, você precisa repará-la antes de usar.'
  dont-has: '&cVocê não possui a quantia &7{amount} em &7{type}&c.'
  registered: '&cEste plugin &f{plugin}&c não está implementado no plugin de shop.'
  deactivated: '&cEste plugin &f{plugin}&c não está ligado.'
  repaired: '&aVocê reparou sua vara com sucesso.'
  bought: '&aVocê comprou a vara nível {level} com sucesso.'
  sell: '&aVocê vendeu &fx{amount} {fish} &apor &f{value} coins, {value_PlayerPoints} pontos&a.'
  sell-all: '&aVocê vendeu todos os seus peixes por &f{value} coins, {value_PlayerPoints} pontos&a.'
  fish-null: |
    &cEste peixe não existe.
    &cDisponíveis: &7{list}
  rarity-null: |
    &cEsta raridade não existe.
    &cDisponíveis: &7{list}
  booster-null: |
    &cEste booster não existe.
    &cDisponíveis: &7{list}
  fish-give: '&aVocê deu x{amount} {fish} &8({rarity}) &apara o jogador &f{player}&a.'
  fish-received: '&aVocê recebeu x{amount} {fish} &8({rarity})&a.'
  booster-give: '&aVocê deu x{amount} Booster(s) &8(+{bonus}%) &apara o jogador &f{player}&a.'
  booster-received: '&aVocê recebeu x{amount} Booster(s) &8(+{bonus}%)&a.'
  booster-finished: '&aPesca: &cSeu booster acabou.'
  booster-has: '&cVocê já está com um booster ativado.'
  booster-activated: '&aVocê ativou um booster de pesca. Multiplicador: &e{bonus}&a. Tempo: &e{time}&a.'
  tournament-type: '&cTipos disponíveis: &7WEIGHT, FISHED'
  tournament-already: '&cJá há um torneio ocorrendo.'
  tournament-no: '&cNão há um torneio ocorrendo.'
  tournament-weight-started: |
    <nl>
    &a&lTORNEIO
    &eFoi iniciado um novo torneio na pesca
    <nl>
    &aPrêmio: &b{prize} coins
    &aTempo de torneio: &b{time}
    <nl>
    &7Vencerá o jogador que pescar o peixe mais pesado!
    <nl>
  tournament-fished-started: |
    <nl>
    &a&lTORNEIO
    &eFoi iniciado um novo torneio na pesca
    <nl>
    &aPrêmio: &b{prize} coins
    &aTempo de torneio: &b{time}
    <nl>
    &7Vencerá o jogador que pescar a maior quantia de peixes!
    <nl>
  tournament-no-win: |
    <nl>
    &a&lTORNEIO
    &eO torneio foi encerrado sem vencedor
    <nl>
    &aPrêmio: &b{prize} coins
    <nl>
    &cNão houve vencedores.
    <nl>
  tournament-win: |
    <nl>
    &a&lTORNEIO
    &eO torneio foi encerrado com vencedor
    <nl>
    &aPrêmio: &b{prize} coins
    <nl>
    &aO jogador vencedor foi &f{player}&a!
    <nl>

  tournament-canceled: |
    <nl>
    &a&lTORNEIO
    &eO torneio foi cancelado por um administrador
    <nl>
    &cNão houve vencedores.
    <nl>
  time: '&cVocê só pode pescar das {from} às {to}.'
  time-removed: '&cVocê foi removido da área de pesca pois só pode pescar das {from} às {to}.'
  fishing-net-full: '&cSua sacola de peixes está cheia, venda os peixes antes de pescar novamente.'
  previous-rod: '&cVocê deve ter a vara anterior para conseguir evoluir à esta.'
  give: '&bVocê deu &f{coin} &bcorais para o jogador &f{player}&b.'
  give-all: |
    <nl>
    &bO usuário &f{player}&b deu &f{coin} &bcorais para todos os jogadores online&b.
    <nl>
  converted: '&bVocê compactou todos seus corais em 1.'
  activated: '&bVocê ativou &f{coin} corais&b.'
  reseted: '&aVocê resetou a vara do jogador &f{player}&a.'
  coin-added-all: '&bVocê adicionou &f{coin} corais&b para todos os jogadores&b.'
  shop-credit-has: '&cVocê não possui a quantia de {amount} corais.'
  shop-credit-spent: '&aVocê comprou na loja utilizando {amount} corais.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  classe-bought: '&aVocê evoluiu para a classe &7{classe}&a.'
  classe-permission: '&cVocê não tem permissão para evoluir para esta classe.'
  classe-previous: '&cVocê deve possuir a classe anterior primeiro.'
  classe-reset: '&aVocê resetou a classe do jogador &f{player}&a.'
  classe-set: '&aVocê definiu a classe {classe} ao jogador &f{player}&a.'
  classe-found: '&aEsta classe não existe. Disponíveis: {classes}'
  classe-give: '&aVocê deu x{amount} {classe} &apara o jogador &f{player}&a.'
  classe-received: '&aVocê recebeu x{amount} {classe}&a.'
  classe-activated: '&aVocê ativou a classe &7{classe}&a.'
  classe-already: '&cVocê já possui esta classe.'
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     __                            _
#    /__\ _____      ____ _ _ __ __| |___
#   / \/// _ \ \ /\ / / _` | '__/ _` / __|
#  / _  \  __/\ V  V / (_| | | | (_| \__ \
#  \/ \_/\___| \_/\_/ \__,_|_|  \__,_|___/
#
# Sistema de recompensa.

rewards:
  Reco1:
    item:
      material: STONE
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: [ '' ]
    command:
      use: false
      list: [ 'give {player} stone 1' ]

]]>
</code-block>
</chapter>

<chapter title="rods.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     __           _
#    /__\ ___   __| |___
#   / \/// _ \ / _` / __|
#  / _  \ (_) | (_| \__ \
#  \/ \_/\___/ \__,_|___/
#
# Configurações das varas de pesca.

# Item para quando o jogador não possui uma vara
default:
  material: 'BARRIER:0'
  name: '&cVocê não possui uma vara'
  lore:
    - '&7Clique para abrir o menu de compra'

rods:
  basic:
    # Nível da vara
    # Padrão: 1
    level: 1
    # Peso suportado pela vara
    supported-weight: 2
    # Delay para pescar
    # em segundos
    delay: 10
    # Quebrar a vara caso pesque um peixe mais pesado que o suportado
    break-heavy: true
    # Preço em coin (moeda do plugin) para reparar a vara
    repair-coin-cost: 0
    # Preço para reparar a vara
    repair-cost:
      cost1:
        type: 'Money'
        cost: 100.0
        display: 'Money'
    # Preço para upar para este nível
    upgrade-cost: {}
    # Preço em coin (moeda do plugin) para upar para este nível
    coin-cost: 0
    # Recompensas que podem ser dadas ao conseguir pescar um peixe
    # Definida na rewards.yml
    # chance,recompensa
    rewards:
      - '20.0,Reco1'
    # Nome e lore da vara
    rod:
      name: '&bVara de pesca &f[L.{level}]'
      lore:
        - '&7Inquebrável ∞'
        - '{enchants}'
        - ''
        - '&a* Vara de pesca &fLVL {level}'
        - '&a* Peso suportado: &f{weight} gramas'
        - ''
        - '&a* &fCorais: &7{coin_has}/{coin_next} &f({progressbar}&f)'
    shop:
      priority: 1
      items:
        upgrade:
          material: FISHING_ROD
          name: '&bVara de pesca &f[L.{level}]'
          lore:
            - ''
            - '&a* Vara de pesca &fLVL {level}'
            - '&a* Peso suportado: &f{weight} gramas'
            - ''
            - '&fPreço: &7Grátis'
            - ''
            - '&aClique para dar upgrade'
        has:
          material: FISHING_ROD
          name: '&bVara de pesca &f[L.{level}]'
          lore:
            - ''
            - '&a* Vara de pesca &fLVL {level}'
            - '&a* Peso suportado: &f{weight} gramas'
            - ''
            - '&cVocê já possui uma vara igual ou melhor que esta.'
  medium:
    level: 2
    supported-weight: 15
    delay: 5
    break-heavy: true
    # Preço em coin (moeda do plugin) para reparar a vara
    repair-coin-cost: 10
    repair-cost:
      cost1:
        type: 'Money'
        cost: 100.0
        display: 'Money'
    upgrade-cost:
      cost1:
        type: 'Money'
        cost: 200.0
        display: 'Money'
    coin-cost: 10
    rewards:
      - '20.0,Reco1'
    rod:
      name: '&bVara de pesca &f[L.{level}]'
      lore:
        - '&7Inquebrável ∞'
        - '{enchants}'
        - ''
        - '&a* Vara de pesca &fLVL {level}'
        - '&a* Peso suportado: &f{weight} gramas'
        - ''
        - '&a* &fCorais: &7{coin_has}/{coin_next} &f({progressbar}&f)'
    shop:
      priority: 1
      items:
        upgrade:
          material: FISHING_ROD
          name: '&bVara de pesca &f[L.{level}]'
          lore:
            - ''
            - '&a* Vara de pesca &fLVL {level}'
            - '&a* Peso suportado: &f{weight} gramas'
            - ''
            - '&fPreço em corais: &b{coin} corais'
            - '&fPreço: &a{Money} coins'
            - ''
            - '&aClique para dar upgrade'
        has:
          material: FISHING_ROD
          name: '&bVara de pesca &f[L.{level}]'
          lore:
            - ''
            - '&a* Vara de pesca &fLVL {level}'
            - '&a* Peso suportado: &f{weight} gramas'
            - ''
            - '&cVocê já possui uma vara igual ou melhor que esta.'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static PescaAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;PescaAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(PescaAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/92-yPesca">Site do plugin yPesca</a>
    </category>
</seealso>