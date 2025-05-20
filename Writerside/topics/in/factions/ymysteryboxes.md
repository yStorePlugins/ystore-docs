# yMysteryBoxes
<secondary-label ref="factions"/>

### Descrição
Caixas misteriosas em formato de itens

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
<video src="//www.youtube.com/watch?v=Ne72BLtk2Zc"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mbox - Mostra a mensagem de ajuda
/mbox ver - Vê o preview de uma caixa
/mbox give - Dá uma caixa à um jogador
/mbox giveall - Dá uma caixa à todos os jogadores</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymysteryboxes.admin - Permissão para o /mbox give e /mbox giveall</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMysteryBoxes/
    ├── menus/
    │    ├── confirmar.yml
    │    └── preview.yml
    ├── caixas.yml
    ├── commands.yml
    ├── config.yml
    ├── messages.yml
    ├── raridades.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caixas - Confirmação'
Tamanho: 36
CaixaSlot: 13
Itens:
  Confirmar:
    Slot: 20
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 5
    Glow: false
    Name: '&aConfirmar (Leia abaixo)'
    Lore:
      - '&7Você ganhará 1 item ao abrir esta caixa.'
      - ''
      - '&7Clique para confirmar a abertura da caixa.'
  Cancelar:
    Slot: 24
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 14
    Glow: false
    Name: '&cCancelar'
    Lore:
      - '&7Clique para cancelar a abertura da caixa.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Top:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caixa - Preview'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
VoltarSlot: 9
ProximoSlot: 17
Lore:
  - ''
  - '&fChance: &b{chance}%'
  - '&fRaridade: &7{raridade}&f.'
  - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="caixas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Caixas:
  basica:
    # Nome que aparecerá nas mensagens
    Display: '&5Básica'
    # Item que será interagido
    Item:
      CustomSkull: false
      URL: ''
      ID: CHEST
      Data: 0
      Name: '&5Caixa Misteriosa'
      Lore:
        - '&7Tipo: &fBásica&7.'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # chance,recompensa-raridade
    # a raridade, caso não tenha, deixe: Nenhuma
    Recompensas:
      - '50.00,Reco1-raro'
    # Dê uma chance a mais para os vips
    # permissão,recompensa-chance
    Chance-adicional:
      - 'ymysteryboxes.vip,Reco1-15.00'
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
  mysterybox: 'mysterybox|caixamisteriosa|mbox'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
   Comando: 'caixamisteriosa'
   Aliases: [ mysterybox, mbox ]

# Opções gerais do plugin
Opcoes:
   # Ativar o sistema de animação
   Animacao: true

# Setas dos menus
Setas:
   Voltar:
      material: ARROW
      name: '&cVoltar'
      lore: [ '&7Clique para voltar ao menu anterior.' ]
   Anterior:
      material: ARROW
      name: '&cVoltar'
      lore: [ '&7Clique para voltar à página anterior.' ]
   Proximo:
      material: ARROW
      name: '&aPróxima'
      lore: [ '&7Clique para ir à próxima página.' ]
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
  inv-full: '&cSeu inventário está cheio.'
  help: |

    &aCaixas comandos:

    &a> /caixamisteriosa give
    &a> /caixamisteriosa giveall
    &a> /caixamisteriosa ver

  box-give: '&aVocê deu &7{amount}x &acaixa(s) {box} &apara o jogador &7{player}&a.'
  box-give-all: '&aVocê deu &7{amount}x &acaixa(s) &7{box}&a para &7({players}) &ajogadores online.'
  box-received: '&aVocê recebeu &7{amount}x &acaixa(s) {box}&a.'
  box-received-all: |

    &aTodos os jogadores receberam &7{amount}x &acaixa(s) &7{box}&a.

  box-command: '&cVocê não pode executar comandos enquanto estiver abrindo uma caixa.'
]]>
</code-block>
</chapter>

<chapter title="raridades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Raridades:
  raro:
    Display: '&6Raro'
    Raio: false # pode causar lag
    Morcegos: false # pode causar lag
    Actionbar: '&b[CAIXA MISTERIOSA] &fO jogador &b{player}&f encontrou uma recompensa rara na caixa &b{caixa}&f.'
    Title: ''
    Chat: |

      &b[CAIXA MISTERIOSA] &fO jogador &b{player}&f encontrou uma recompensa rara na caixa &b{caixa}&f.
      &b> &7{item}

]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá no preview do boss.
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
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMysteryBoxes/
    ├── menus/
    │    ├── confirmar.yml
    │    └── preview.yml
    ├── caixas.yml
    ├── commands.yml
    ├── config.yml
    ├── messages.yml
    ├── raridades.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caixas - Confirmação'
Tamanho: 36
CaixaSlot: 13
Itens:
  Confirmar:
    Slot: 20
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 5
    Glow: false
    Name: '&aConfirmar (Leia abaixo)'
    Lore:
      - '&7Você ganhará 1 item ao abrir esta caixa.'
      - ''
      - '&7Clique para confirmar a abertura da caixa.'
  Cancelar:
    Slot: 24
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 14
    Glow: false
    Name: '&cCancelar'
    Lore:
      - '&7Clique para cancelar a abertura da caixa.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Top:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caixa - Preview'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
VoltarSlot: 9
ProximoSlot: 17
Lore:
  - ''
  - '&fChance: &b{chance}%'
  - '&fRaridade: &7{raridade}&f.'
  - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="caixas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Caixas:
  basica:
    # Nome que aparecerá nas mensagens
    Display: '&5Básica'
    # Item que será interagido
    Item:
      CustomSkull: false
      URL: ''
      ID: CHEST
      Data: 0
      Name: '&5Caixa Misteriosa'
      Lore:
        - '&7Tipo: &fBásica&7.'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # chance,recompensa-raridade
    # a raridade, caso não tenha, deixe: Nenhuma
    Recompensas:
      - '50.00,Reco1-raro'
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
  mysterybox: 'mysterybox|caixamisteriosa|mbox'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
   Comando: 'caixamisteriosa'
   Aliases: [ mysterybox, mbox ]

# Opções gerais do plugin
Opcoes:
   # Ativar o sistema de animação
   Animacao: true

# Setas dos menus
Setas:
   Voltar:
      material: ARROW
      name: '&cVoltar'
      lore: [ '&7Clique para voltar ao menu anterior.' ]
   Anterior:
      material: ARROW
      name: '&cVoltar'
      lore: [ '&7Clique para voltar à página anterior.' ]
   Proximo:
      material: ARROW
      name: '&aPróxima'
      lore: [ '&7Clique para ir à próxima página.' ]
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
  inv-full: '&cSeu inventário está cheio.'
  help: |

    &aCaixas comandos:

    &a> /caixamisteriosa give
    &a> /caixamisteriosa giveall
    &a> /caixamisteriosa ver

  box-give: '&aVocê deu &7{amount}x &acaixa(s) {box} &apara o jogador &7{player}&a.'
  box-give-all: '&aVocê deu &7{amount}x &acaixa(s) &7{box}&a para &7({players}) &ajogadores online.'
  box-received: '&aVocê recebeu &7{amount}x &acaixa(s) {box}&a.'
  box-received-all: |

    &aTodos os jogadores receberam &7{amount}x &acaixa(s) &7{box}&a.

  box-command: '&cVocê não pode executar comandos enquanto estiver abrindo uma caixa.'
]]>
</code-block>
</chapter>

<chapter title="raridades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Raridades:
  raro:
    Display: '&6Raro'
    Raio: false # pode causar lag
    Morcegos: false # pode causar lag
    Actionbar: '&b[CAIXA MISTERIOSA] &fO jogador &b{player}&f encontrou uma recompensa rara na caixa &b{caixa}&f.'
    Title: ''
    Chat: |

      &b[CAIXA MISTERIOSA] &fO jogador &b{player}&f encontrou uma recompensa rara na caixa &b{caixa}&f.
      &b> &7{item}

]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá no preview do boss.
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/82-yMysteryBoxes">Site do plugin yMysteryBoxes</a>
    </category>
</seealso>