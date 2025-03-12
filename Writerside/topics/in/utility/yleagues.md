# yLeagues
<secondary-label ref="utility"/>

### Descrição
Crie competições entre os clans/facções do seu servidor

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
<video src="//www.youtube.com/watch?v=QZIZB6sKD1c"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/liga - Abre o menu principal
/liga help - Envia a mensagem de ajuda
/liga add - Adiciona pontos para um clan
/liga remove - Remove pontos de um clan
/liga set - Seta pontos para um clan
/liga finalizar - Recarrega as configurações
/liga reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yleagues.use - Permissão para o /liga
yleagues.finish - Permissão para o /liga finalizar
yleagues.points.add - Permissão para o /liga add
yleagues.points.remove - Permissão para o /liga remove
yleagues.points.set - Permissão para o /liga set
yleagues.admin.reload - Permissão para o /liga reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yleagues_points% - Retorna a quantia total de pontos do clan
%yleagues_points_raw% - Retorna a quantia total de pontos do clan sem formatar
%yleagues_rank% - Retorna o rank (patente) do clan
%yleagues_medal_enemy-of-life% - Retorna a tag da medalha de inimigo da vida (maior número de mortes na última liga)
%yleagues_medal_hard-to-kill% - Retorna a tag da medalha de duro de matar (maior número de kills na última liga)
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{yleagues_rank} - Retorna o rank (patente) do clan&nbsp;
{yleagues_medal_enemy-of-life} - Retorna a tag da medalha de inimigo da vida (maior número de mortes na última liga)
{yleagues_medal_hard-to-kill} - Retorna a tag da medalha de duro de matar (maior número de kills na última liga)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLeagues/
    ├── leagues/
    │    └── iron.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    ├── ranks.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="leagues" collapsible="true">
<chapter title="iron.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Identificação necessária para a API de TOP do yPlugins
yplugins-id: 'yleagues-iron'

order: 1

# Data de ínicio da liga
start-date: '01/01/2020-10:00'

# Data de término da liga
end-date: '01/01/2028-10:00'

# Nome da liga
display: '&fLiga de Ferro'

# Ícones nos menus
icons:
  finished:
    material: 'IRON_INGOT'
    name: '&fLiga de Ferro'
    lore:
      - ''
      - ' &7Líderes:'
      - '  &f> 1º {clan_1}: &a{amount_1}'
      - '  &f> 2º {clan_2}: &a{amount_2}'
      - '  &f> 3º {clan_3}: &a{amount_3}'
      - ''
      - '&cEsta liga já finalizou.'
  current:
    material: 'IRON_INGOT'
    name: '&fLiga de Ferro'
    lore:
      - ''
      - ' &7Líderes:'
      - '  &f> 1º {clan_1}: &a{amount_1}'
      - '  &f> 2º {clan_2}: &a{amount_2}'
      - '  &f> 3º {clan_3}: &a{amount_3}'
      - ''
      - '&f Finaliza em: &b{end_time} &7({end_date}-{end_hour})'
      - ''
      - '&aEsta liga está ocorrendo.'
  coming:
    material: 'IRON_INGOT'
    name: '&fLiga de Ferro'
    lore:
      - '&7Esta liga ainda será iniciada,'
      - '&7não perca tempo e fique preparado'
      - '&7para garantir sua participação.'
      - ''
      - '&f Inicia em: &b{start_time} &7({start_date}-{start_hour})'
      - ''
  participate:
    material: 'IRON_INGOT'
    name: '&fLiga de Ferro'
    lore:
      - '&7Participe da liga dos clans e'
      - '&7garanta prêmios exclusivos.'
      - ''
      - ' &fPontos iniciais necessários: &b{points}'
      - ' &fMoney necessário: &2$ &a{money}'
      - ''
      - ' &7Líderes Atuais:'
      - '  &f> 1º {clan_1}: &a{amount_1}'
      - '  &f> 2º {clan_2}: &a{amount_2}'
      - '  &f> 3º {clan_3}: &a{amount_3}'
      - ''
      - '&aClique para participar.'
  participating:
    material: 'IRON_INGOT'
    name: '&fLiga de Ferro'
    lore:
      - '&7Seu clan está participando desta liga'
      - '&7e pode garantir prêmios exclusivos.'
      - ''
      - ' &7Líderes Atuais:'
      - '  &f> 1º {clan_1}: &a{amount_1}'
      - '  &f> 2º {clan_2}: &a{amount_2}'
      - '  &f> 3º {clan_3}: &a{amount_3}'
      - ''
      - '&f Finaliza em: &b{end_time} &7({end_date}-{end_hour})'
      - ''
  no-clan:
    material: 'IRON_INGOT'
    name: '&fLiga de Ferro'
    lore:
      - '&7Você precisa entrar ou criar'
      - '&7um clan para participar das ligas.'
      - ''
      - '&c Você não possui um clan.'
      - ''

participate:
  # Limite de clans participando da liga
  clan-limit: 10
  # Quantidade mínima de pontos para ingressar na liga
  min-initial-points: 10.0
  # Liga anterior participada necessária para entrar nesta
  # Deixe 0 caso não queira
  previous-league: 0
  # Mensagem de compra
  message:
    private: '&aVocê pagou &f{money}&a para ingressar seu clan na liga de clans.'
    broadcast: ''
  # Preços para participar
  prices:
    price1:
      provider: 'money'
      amount: 1000.0

win:
  # Ganhar a liga quando atingir X pontos acumulados
  # Caso não queira, deixe 0 (irá ganhar apenas na data de término)
  amount: 100.0
  # Resetar os pontos dos clans participantes ao finalizar a liga
  reset: true
  # Recompensas (serão dadas ao líder do clan)
  # chance, recompensa
  rewards:
    - '100.0,reward1'

# Mensagens do torneio
messages:
  start: |

    &f&lLIGA DE FERRO: &aA liga COMEÇOU!

  stop: |

    &f&lLIGA DE FERRO: &aA liga acabou!
    &bGanhador: &a{clan} com {amount} pontos!

  stop-none: |

    &f&lLIGA DE FERRO: &aA liga acabou!
    &cNINGUÉM GANHOU!

  rewards-give: |
    &f&lLIGA DE FERRO: &aAs recompensas foram depositadas no correio de recompensas do líder &f{player}&a.

# Sistema de mercado da liga
market:
  # Itens do mercado
  items:
    item1:
      # Slot do item do menu
      slot: 11
      # Preço em pontos
      price: 10.0
      # Ícone no menu
      display:
        material: 'STONE'
        name: '&cPedra Misteriosa'
        lore:
          - '&7Esta pedra irá lhe causar'
          - '&7efeitos diferenciados.'
          - ''
          - ' &fPDL necessário: &b10'
          - ''
          - '&7Clique para comprar a pedra'
      # Item que será dado
      # Caso não queira, apague
      item:
        material: 'STONE'
        amount: 64
        name: '&cPedra Misteriosa'
      # Comandos que serão dados
      commands: []

finished: false
started: false
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
  league: 'league|leagues|liga|ligas|ligaclan|ligasclan|ligasclans'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _____                     _
#  _   |_   _|__  _ __ _ __   ___(_) ___  ___
# | | | || |/ _ \| '__| '_ \ / _ \ |/ _ \/ __|
# | |_| || | (_) | |  | | | |  __/ | (_) \__ \
#  \__, ||_|\___/|_|  |_| |_|\___|_|\___/|___/
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

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Sistemas gerais do plugin
general:
  # Apenas o líder conseguir clicar para participar da liga
  just-leader: true
  # Sistema de notificar o ganho de pontos
  discordhook:
    enabled: true
    channel: ''
    # Placeholders disponíveis:
    # {action}
    # {player}
    # {clan_tag}
    # {clan_name}
    # {points}
    embed: ''

# Configuração do ganho de pontos
points:
  # Ao morrer
  player-death: -1.0
  # Ao matar um player
  player-kill: 1.0
  # Ao upar de rank
  yrankup: 1.0
  # Ao ganhar um evento
  yeventos: 1.0
  # Ao perder um evento
  yeventos-lose: 1.0
  # Ao kickar um jogador do clan (yClans)
  yclans-kick: -1.0
  # Ao ganhar um evento
  yguerra: 1.0
  # Ao matar um mob
  yspawners: 0.3
  # Ao matar um boss
  ystackbosses: 0.5
  # Ao matar um boss
  ybosses: 0.5
  # Ao quebrar um bloco
  yminas: 0.1
  # Ao quebrar um bloco
  yminaspackets: 0.1
  # Ao quebrar uma plantação
  yplantacoes: 0.1
  # Ao quebrar uma plantação
  ycampo: 0.1
  # Ao quebrar um bloco
  yfloresta: 0.1
  # Ao pescar um peixe
  ypesca: 0.3
  # Ao levar mute (yPunish)
  punish-mute: -5.0
  # Ao levar ban (yPunish e StormPunish)
  punish-ban: -10.0

# Sistema de medalhas
medals:
  # Maior número de mortes ao final da temporada
  enemy-of-life: '&c[X]'
  # Maior número de kills ao final da temporada
  hard-to-kill: '&a[V]'
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
    permission: 'yleagues.provider.money'
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
  name: '&8Liga'
  size: 36
  items:
    profile-slot: 10
    clan-slot: 19
    rewards-slot: 20
    participate-slot: 13
    leagues-slot: 24
    market-slot: 16
    profile:
      material: '{player}'
      name: '&eSuas informações'
      lore:
        - '&7Veja as suas informações'
        - '&7referente a todas as ligas do'
        - '&7servidor.'
        - ''
        - ' &fLigas participadas: &a{leagues}'
        - ' &fPontos ganhos &8(total)&f: &a{total_points}'
        - ''
        - ' &fLigas ganhas: &b{wins}'
        - ''
        - ' &fMortes na liga atual: &c{deaths}'
        - ' &fKills na liga atual: &c{kills}'
        - ''
        - ' &fMedalhas ganhas: {medals} &8({medal_amount}/2)'
        - ''
    clan:
      material: 'c09741fca109c4cb0b5efaa0634616503051a199e1d44e4e1149ede0bdc49c8a'
      name: '&eInformações do Clan'
      lore:
        - '&7Veja as informações do seu clan'
        - '&7referente a todas as ligas do'
        - '&7servidor.'
        - ''
        - ' &fPontos atuais: &a{points}'
        - ' &fRank atual: &c{rank}'
        - ' &fLiga atual: &c{league}'
        - ''
        - ' &fLigas participadas: &b{participated}'
        - ' &fLigas ganhas: &b{wins}'
        - ''
        - ' &fMaior col.: &b{highest_clan}º'
        - ' &fMaior col. &8(liga atual)&f: &b{highest_clan_league}º'
        - ''
    clan-no-has:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&eInformações do Clan'
      lore:
        - '&cVocê não possui um clan'
    leagues:
      material: 'BOOK'
      name: '&eLigas de Clans'
      lore:
        - '&7Confira todas as ligas'
        - '&7existentes no servidor.'
        - ''
        - '&aClique para acessar'
    rewards:
      material: 'cf128540839bd1b70930353112a3b8d295713c0eece615fd4a0340a00d8d55e2'
      name: '&6Recompensas'
      lore:
        - '&7Gerencie as recompensas'
        - '&7que você ganhou.'
        - ''
        - ' &8▶ &fRecompensas: &7{rewards}'
        - ''
        - '&6Clique para gerenciar!'
    participate-none:
      material: 'BARRIER'
      name: '&cNenhuma'
      lore:
        - ''
        - '&7Nenhuma liga encontrada.'
        - ''
    market:
      material: '533fc9a45be13ca57a78b21762c6e1262dae411f13048b963d972a29e07096ab'
      name: '&eMercado da Liga'
      lore:
        - '&7Troque os pontos da liga (PDL)'
        - '&7em itens exclusivos na nossa loja!'
        - ''
        - '&aClique para acessar.'
  facing:
    information:
      slot: 25
      material: '7ff8cf8ee2f233b172e162182cefac84b1b8e13d948c15dc892731bb2aba729d'
      name: '&eInformações'
      lore:
        - '&7Veja quantos pontos você'
        - '&7pode ganhar ao realizar'
        - '&7certas ações no nosso servidor!'
        - ''
        - ' &f> Matar um jogador: &b1 ponto'
        - ' &f> Upar de rank: &b1 ponto'
        - ' &f> Ganhar eventos: &b1 ponto'
        - ' &f> Matar mobs: &b0.3 ponto'
        - ' &f> Matar bosses: &b0.5 ponto'
        - ' &f> Quebrar blocos &7(mina)&f: &b0.1 ponto'
        - ' &f> Quebrar plantações: &b0.1 ponto'
        - ' &f> Pescar um peixe: &b0.3 ponto'
        - ''
        - ' &c> Morrer: -1 ponto'
        - ' &c> Perder eventos: -1 ponto'
        - ' &c> Expulsar jogador &8(durante a liga)&c: -1 ponto'
        - ''

# Menu de ligas
main-leagues:
  name: '&7Ligas'
  size: 45
  slots: [ 11, 12, 13, 14, 15 ]
  previous-slot: 32
  next-slot: 33
  back-slot: 29

# Menu de recompensas
main-rewards:
  name: '&7Ligas'
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

# Menu do mercado
main-market:
  name: '&8Liga'
  size: 45
  back-slot: 30
  items:
    permission-slot: 32
    permission:
      material: '7ff8cf8ee2f233b172e162182cefac84b1b8e13d948c15dc892731bb2aba729d'
      name: '&ePermissões de acesso'
      lore:
        - '&7Gerencie os jogadores do seu clan'
        - '&7que podem acessar o mercado da liga.'
        - ''
        - '&aClique para gerenciar.'

# Menu de permissões do mercado
market-permissions:
  name: '&7Ligas'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  items:
    player-on:
      material: '{player}'
      name: '&a{player}'
      lore: [ '&7Este jogador consegue SIM acessar', '&7o mercado da liga.', '', '&cClique para não permitir.' ]
    player-off:
      material: '{player}'
      name: '&a{player}'
      lore: [ '&7Este jogador NÃO consegue acessar', '&7o mercado da liga.', '', '&aClique para permitir.' ]

# Menu de clans participantes da liga
league-clans:
  name: '&7Ligas'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  items:
    clan:
      material: '{banner}'
      name: '&a{league}'
      lore:
        - ''
        - ' &7Clan: &f{clan_tag} &8- &f{clan_name}'
        - ''
        - ' &fPontuação total: &a{points} &8- &b{pos}º'
        - ' &fJogador com maior pontuação &8(na liga)&f: &b{highest_actual_player} &8- &a{highest_actual_player_points}'
        - ' &fJogador com maior pontuação &8(total)&f: &b{highest_player} &8- &a{highest_player_points}'
        - ''
        - '&aClique para ver mais detalhes.'

# Menu de players do clan
league-clan-players:
  name: '&7Ligas'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  items:
    player:
      material: '{player}'
      name: '&b{player}'
      lore:
        - ''
        - ' &7Clan: &f{clan_tag} &8- &f{clan_name}'
        - ''
        - ' &eAuditoria de pontos:'
        - ' &f> Abates: &a{kills} pontos'
        - ' &f> Ranks evoluídos: &a{yrankup} pontos'
        - ' &f> Eventos ganhos: &a{yeventos} pontos'
        - ' &f> Mobs mortos: &a{mobs} pontos'
        - ' &f> Bosses mortos: &a{bosses} pontos'
        - ' &f> Blocos quebrados: &a{blocks_broken} pontos'
        - ' &f> Plantações quebradas: &a{farm_broken} pontos'
        - ' &f> Peixes pescados: &a{fished} pontos'
        - ' &f> Vips ativados: &a{yvips} pontos'
        - ''
        - ' &f> Mortes: &c-{deaths} pontos'
        - ' &f> Eventos perdidos: &c-{yeventos_lose} pontos'
        - ' &f> Banimentos: &c-{punish_ban} pontos'
        - ' &f> Mutes: &c-{punish_mute} pontos'
        - ''
        - '&eTotal de pontos: &a{points}'
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

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/league &8- &7Abre o menu principal.
    &a/league add &8- &7Adiciona pontos para um clan.
    &a/league remove &8- &7Remove pontos de um clan.
    &a/league set &8- &7Seta pontos para um clan.

  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  just-leader: '&cApenas o líder do clan ({player}) pode ingressar a liga.'
  no-points: '&cSeu clan precisa de {need_points} pontos para participar da liga. Atual: {points}'
  no-previous: '&cSeu clan precisaria ter participado da liga {league} para participar desta.'
  no-limit: '&cA liga chegou ao limite de clans participantes ({amount}).'
  target-clan: '&cNenhum clan ou jogador encontrado com o nome {name}.'
  target-has: '&cO jogador {player} não possui um clan.'
  points-changed: '&aPontos do clan &f{clan}&a alterado para &f{points}&a.'
  league-none: '&cNenhuma liga acontecendo.'
  league-already: '&cA liga já foi encerrada.'
  league-finished: '&cA liga foi encerrada.'
  market-clan: '&cVocê precisa de um clan para acessar o mercado da liga.'
  market-just-leader: '&cApenas o líder do clan ({player}) pode alterar as permissões de acesso.'
  market-permission: '&cVocê não tem permissão para acessar o mercado da liga.'
  market-need: '&cO seu clan precisa de {need_points} pontos para comprar. Atual: {points}.'
  market-buy: '&aVocê comprou itens no mercado da liga por {points} pontos.'
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
ranks:
  silver1:
    # Ordem do rank
    order: 0
    # Tag do rank
    display: '&7[>]'
    # Pontos necessários
    points: 0
  silver2:
    order: 1
    display: '&7[>>]'
    points: 10
  silver3:
    order: 2
    display: '&7[>>>]'
    points: 20
  silver4:
    order: 3
    display: '&7[>>>>]'
    points: 40
  silver5:
    order: 4
    display: '&7[(>>>>]'
    points: 80
  silver6:
    order: 5
    display: '&7[(*>>>>]'
    points: 160
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
      lore: [ '&aEsta pedra vale muito dinheiro!', '', '&6Chance: {chance}%' ]
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
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', '&6Chance: {chance}%' ]
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
      lore: [ '&aEsmeraldas valem muito?', '', '&6Chance: {chance}%' ]
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/151-yLeagues">Site do plugin yLeagues</a>
    </category>
</seealso>