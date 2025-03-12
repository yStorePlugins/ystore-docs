# yTrades
<secondary-label ref="management"/>

### Descrição
Realize trocas de itens e economias com seus parceiros

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
<video src="//www.youtube.com/watch?v=HYx5MSyteoM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/trocar - Envia a mensagem de ajuda
/trocar [player] - Envia a solicitação de troca
/trocar aceitar [player] - Aceita a solicitação de troca
/trocar negar [player] - Nega a solicitação de troca
/trocar reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytrades.use - Permissão para o /trocar [player], /trocar aceitar [player] e /trocar negar [player]
ytrades.admin.reload - Permissão para o /trocar reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTrades/
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
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
  trade: 'trade|troca|trocar'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#       _____              _
#  _   |_   _| __ __ _  __| | ___  ___
# | | | || || '__/ _` |/ _` |/ _ \/ __|
# | |_| || || | | (_| | (_| |  __/\__ \
#  \__, ||_||_|  \__,_|\__,_|\___||___/
#  |___/
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

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
    permission: 'ytrades.provider.money'
    # Formato do símbolo
    symbol: '$'
    # ‘Item’ que aparecerá
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ' &7Valor atual: &f{value}&7.'
        - ''
        - '&aClique para alterar'
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
  name: '&8Troca'
  size: 54
  player-1-slots: [ 18, 19, 20, 27, 28, 29, 36, 37, 38, 45, 46, 47 ]
  player-2-slots: [ 24, 25, 26, 33, 34, 35, 42, 43, 44, 51, 52, 53 ]
  items:
    profile-player-1-slot: 0
    profile-player-2-slot: 8
    economies-player-1-slot: 2
    economies-player-2-slot: 6
    confirm-slot: 13
    cancel-slot: 40
    profile-player-1:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - ' &fPronto: &r{status}'
        - ''
    profile-player-2:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - ' &fPronto: &r{status}'
        - ''
    economies-player-1:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomias'
      lore:
        - ''
        - ' &fMoney: &2$ &a{money}'
        - ''
    economies-player-2:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomias'
      lore:
        - ''
        - ' &fMoney: &2$ &a{money}'
        - ''
    confirm:
      material: '1e38fa3131e2da04a8f8d50872a8232d7d9dea340d06c9097ffa3cc48208df1d'
      name: '&aConfirmar'
      lore:
        - '&7Clique aqui para confirmar'
        - '&7sua intenção de realizar a'
        - '&7troca com o outro jogador.'
    cancel:
      material: '68d40935279771adc63936ed9c8463abdf5c5ba78d2e86cb1ec10b4d1d225fb'
      name: '&cCancelar'
      lore:
        - '&7Clique aqui para cancelar'
        - '&7a requisição de troca.'
  facing:
    e0:
      slot: 3
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e1:
      slot: 4
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e2:
      slot: 5
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e3:
      slot: 9
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e4:
      slot: 10
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e5:
      slot: 11
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e6:
      slot: 12
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e7:
      slot: 14
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e8:
      slot: 15
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e9:
      slot: 16
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e10:
      slot: 17
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e11:
      slot: 21
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e12:
      slot: 22
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e13:
      slot: 23
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e14:
      slot: 30
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e15:
      slot: 31
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e16:
      slot: 32
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e17:
      slot: 39
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e18:
      slot: 41
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e19:
      slot: 48
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e20:
      slot: 49
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
    e21:
      slot: 50
      material: 'STAINED_GLASS_PANE:0'
      name: ' '
      lore: []
  facing-1-ready:
    e0:
      slot: 3
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e1:
      slot: 9
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e2:
      slot: 10
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e3:
      slot: 11
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e4:
      slot: 12
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e5:
      slot: 21
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e6:
      slot: 30
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e7:
      slot: 39
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e8:
      slot: 48
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
  facing-2-ready:
    e0:
      slot: 5
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e1:
      slot: 14
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e2:
      slot: 15
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e3:
      slot: 16
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e4:
      slot: 17
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e5:
      slot: 23
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e6:
      slot: 32
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e7:
      slot: 41
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []
    e8:
      slot: 50
      material: 'STAINED_GLASS_PANE:5'
      name: ' '
      lore: []

# Menu de economias
providers:
  name: '&8Troca'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
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
# Plugin messages

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  cancelled-other: '&cA outra parte cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &aTroca comandos:

    &a> /troca [player]
    &a> /troca aceitar [player]

  yourself: '&cVocê não pode trocar com você mesmo.'
  none: '&cNinguém colocou nada na troca.'
  full: '&cVocê já selecionou itens demais.'
  ready: '&cVocê não pode mais modificar, pois já está confirmado. Clique em confirmar novamente para conseguir alterar a troca.'

  digit-price: |

    &aDigite o preço para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  change-price: '&aVocê alterou o preço para {price}.'
  changed-items: '&cOs itens foram alterados pois uma das partes ({player}) não os possuiam mais.'
  changed-economies: '&cAs economias foram alteradas pois uma das partes ({player}) não as possuiam suficientemente.'
  finished: '&aTroca realizada com sucesso.'
  expired: '&cSua solicitação de troca para {player} expirou.'
  already-sent: '&cVocê já possui uma solicitação de troca pendente.'
  target-sent: '&cEste jogador não enviou nenhuma solicitação de troca.'
  target-sent-you: '&cEste jogador não enviou nenhuma solicitação de troca para você.'
  sent: '&aSolicitação de troca enviada para &f{player}&a.'
  received: '&aSolicitação de troca recebida de &f{player}&a. Clique &f&l<click:run_command:/troca aceitar {player}>AQUI</click>&a para aceitar.'
  accepted: '&aVocê aceitou a solicitação de troca de &f{player}&a.'
  accepted-player: '&aO jogador &f{player}&a aceitou a sua solicitação de troca.'
  denied: '&aVocê negou a solicitação de troca de &f{player}&c.'
  denied-player: '&cO negou &f{player}&c aceitou a sua solicitação de troca.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/155-yTrades">Site do plugin yTrades</a>
    </category>
</seealso>