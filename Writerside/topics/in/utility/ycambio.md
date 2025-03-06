# yCambio
<secondary-label ref="utility"/>

### Descrição
Realize a troca de economias dentro do servidor

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

### Demonstração
<video src="//www.youtube.com/watch?v=t4Hp1jXtXog"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/cambio - Abre o menu de câmbio
/cambio setnpc - Seta o NPC
/cambio delnpc - Deleta o NPC
/cambio reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycambio.use - Permissão para o /cambio
ycambio.setnpc - Permissão para o /cambio setnpc
ycambio.delnpc - Permissão para o /cambio delnpc
ycambio.admin.reload - Permissão para o /cambio reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCambio/
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── exchanges.yml
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
  exchange: 'exchange|cambio|cambios|cambiar'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____                _     _
#  _   _ / ___|__ _ _ __ ___ | |__ (_) ___
# | | | | |   / _` | '_ ` _ \| '_ \| |/ _ \
# | |_| | |__| (_| | | | | | | |_) | | (_) |
#  \__, |\____\__,_|_| |_| |_|_.__/|_|\___/
#  |___/
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

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

# Sistema de npc
npc:
  skin: 'Pitombaa'
  hologram:
    offset: 3.4
    hologram:
      - '&6&lCâmbio'
      - '&7Clique para trocar suas economias.'
      - '[item]EMERALD'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
version: '1.0.0'
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
    permission: 'ycambio.provider.money'
  ypoints:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yPoints'
    # Formato inteiro
    display: 'Cash'
    # Formato abreviado
    abbreviated: 'cash'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'ycambio.provider.ypoints'
]]>
</code-block>
</chapter>

<chapter title="exchanges.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
exchanges:
  coin-to-cash:
    # Economia que precisa
    from: 'money'
    # Economia que vai obter
    to: 'ypoints'
    # Taxa de câmbio
    taxes:
      tax1:
        order: 1
        permission: ''
        tax: 10.0
    # Mínimo para converter
    minimum: 1000.0
    # items
    items:
      display:
        material: '8381c529d52e03cd74c3bf38bb6ba3fde1337ae9bf50332faa889e0a28e8081f'
        name: '&aCoins &f-> &6Cash'
        lore:
          - '&7Realize o câmbio de coins para cash'
          - ''
          - '&7Taxa de conversão: &f{tax}%'
          - '&7Mínimo para converter: &f{minimum}'
          - ''
          - '&aClique para digitar o valor'
      confirm:
        material: '8381c529d52e03cd74c3bf38bb6ba3fde1337ae9bf50332faa889e0a28e8081f'
        name: '&aCoins &f-> &6Cash'
        lore:
          - '&7Informações sobre o câmbio pendente'
          - ''
          - '&7Valor que será pago: &c{from_value} {from_abbreviated}'
          - '&7Valor que irá receber: &c{to_value} {to_abbreviated}'
          - ''
          - '&7Taxa de conversão: &f{tax}% -> {tax_value} {from_abbreviated}'
          - ''
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
  name: '&8Câmbio'
  size: 45
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  previous-slot: 18
  next-slot: 26
  #
  profile-slot: 31
  #
  items:
    profile:
      material: '{player}'
      name: '&eSuas informações'
      lore: [ '', '&fCoins: &a%yeconomy_money%', '&fCash: &6%ypoints_points%', '' ]

# Menu de confirmação
confirm:
  name: '&8Câmbio'
  size: 27
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  items:
    item-slot: 13
    confirm-slot: 11
    cancel-slot: 15
    confirm:
      material: 'WOOL:5'
      name: '&aConfirmar'
      lore: [ '&7Clique para &aconfirmar&7 o câmbio.' ]
    cancel:
      material: 'WOOL:14'
      name: '&cCancelar'
      lore: [ '&7Clique para &ccancelar&7 o câmbio.' ]
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
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &aCâmbio comandos:

    &a> /cambio
    &a> /cambio reload

  digit-amount: |

    &aDigite no chat a quantia que quer cambiar.
    &7para cancelar digite &ncancelar&7.

  minimum: '&cO valor mínimo para cambiar de {from} para {to} é {minimum}.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  exchanged: |
    &eCâmbio
    &aVocê trocou de {from_display} para {to_display}

    &7Valor pago: &c{from_value} {from_abbreviated}
    &7Valor recebido: &a{to_value} {to_abbreviated}
    &7Taxa: &e{tax}% -> {tax_value}

  not-found: '&cEconomia {economy} não cadastrada no servidor.'
  npc-set: '&aNPC setado com sucesso.'
  npc-deleted: '&aNPC removido com sucesso.'
  npc-not-set: '&cNPC não está definido.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/111-yCambio">Site do plugin yCambio</a>
    </category>
</seealso>