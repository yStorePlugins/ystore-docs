# yMito
<secondary-label ref="rankup"/>

### Descrição
Dê ao jogador que mais mata a tag Mito e, quando o mesmo morrer, a tag será repassada.

### Versões
<secondary-label ref="1.8"/>
<secondary-label ref="1.9"/>
<secondary-label ref="1.12"/>
<secondary-label ref="1.16"/>

### Demonstração
<video src="//www.youtube.com/watch?v=LzckktjQIBw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mito - Ver o mito atual.
/mito setar  - Setar o mito.
/mito setnpc - Setar o NPC do mito.
/mito delnpc - Deletar o NPC do mito.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymito.ver - Permissão para o /mito.
ymito.admin - Permissão para o /mito setar, /mito setnpc, /mito delnpc</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ymito_mito% - Mostra o mito atual ( PlaceholderAPI )
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{mito} - Tag do mito ( Legendchat )
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMito/
    ├── commands.yml
    ├── config.yml
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
  mito: 'mito'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         __  __ _ _
#  _   _|  \/  (_) |_ ___
# | | | | |\/| | | __/ _ \
# | |_| | |  | | | || (_) |
#  \__, |_|  |_|_|\__\___/
#  |___/
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

# Sistemas gerais do plugin
general:
  # Tag do Mito
  tag: '&5[MITO]'
  # Ativar abrir o menu ao digitar /mito
  mito-menu: true
  # Ativar o sistema de perder mito por inatividade
  lose: true
  # Tempo inativo no servidor para perder o Mito
  # em segundos
  time-lose: 30
  # Perder o mito por tempo apenas se tiver outro jogador on
  lose-has-player: true
  # Tempo que o jogador pode morrer sem perder a tag após recebê-la
  # em segundos
  cooldown-lose-death: 30

effect:
  # Soltar efeito de raio no novo mito
  strike-lightning: true
  # Spawnar morcegos ao redor do novo mito
  spawn-bats: true
  # Tocar som no novo mito
  sound: 'ENDERDRAGON_GROWL'

# Recompensas por matar o mito
rewards:
  amount: 1
  list:
    - '100.0,give {player} diamond 1'

# Comandos executados no mito
commands:
  - 'give {new} diamond 1'
  - 'give {old} stone 1'

# Configurações do npc
npc:
  # Altura do holograma
  off-set: 3.1
  hologram:
    - '&c&lMITO'
    - '&7Mito Atual &c{player}&7.'
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
menu-updater-time: 20

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
  name: '&8Mito'
  size: 27
  items:
    player-slot: 12
    top-slot: 14
    player-none:
      material: 'BARRIER'
      name: '&cNenhum'
      lore:
        - '&7Atualmente não há nenhum'
        - '&7mito no servidor.'
    player:
      material: '{player}'
      name: '&a{player}'
      lore:
        - '&7Este é o mito atual :)'
        - ''
        - '&fTempo como mito atual: &a{current_time}'
        - '&fTempo como mito total: &a{total_time}'
        - '&fVezes que foi mito: &a{times}'
        - ''
    top:
      material: 'BOOK_AND_QUILL'
      name: '&b&lTOP'
      lore:
        - '&7Veja os jogadores que mais'
        - '&7destacaram no servidor.'
        - ''
        - '&aClique para abrir'

# Menu top
top:
  name: '&8TOP MITO'
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
      total-time:
        enabled: true
        name: 'Tempo Total'
      times:
        enabled: true
        name: 'Vezes'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{nome}'
      select: ' &f• &7{nome}'
  items:
    # Item do top total-time
    total-time:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fTempo Total: &7{amount}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top times
    times:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fVezes: &7{amount}'
        - '&fPosição: &e{pos}º'
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
  help: |

    &bComandos do plugin:

    &b-> &f/mito &8-&7 Abre o menu principal
    &b-> &f/mito top &8-&7 Abre o menu de top

  help-admin: |

    &bComandos do plugin:

    &b-> &f/mito &8-&7 Abre o menu principal
    &b-> &f/mito top &8-&7 Abre o menu de top
    &b-> &f/mito set [player] &8-&7 Define um usuário como mito
    &b-> &f/mito random &8-&7 Define um usuário aleatório como mito
    &b-> &f/mito setnpc &8-&7 Define o NPC
    &b-> &f/mito delnpc &8-&7 Deleta o NPC
    &b-> &f/mito reload &8-&7 Recarrega as configurações

  mito-defined: '&aVocê definiu o jogador {player} como o novo mito.'
  mito-npc-set: '&aVocê definiu o NPC do MITO.'
  mito-npc-delete: '&aVocê deletou o NPC do MITO.'
  mito-join: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 acabou de entrar no servidor.
    &7Vocês agoram podem ficar com medo da lenda viva!

  mito-left: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 acabou de sair do servidor.
    &7Vocês agoram podem ficar calmos!

  mito-death: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 acabou de morrer e perdeu a TAG para o jogador(a) &f{killer}&5.
    &7Esse cara era muito ruim, hein!

  mito-death-delay: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 acabou de morrer para o jogador(a) &f{killer}&5, mas ele não perdeu a tag por causa do delay :o.
    &7Mais cuidado da próxima, você não vai ter o delay ao seu favor!

  mito-delay: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 perdeu a TAG por ficar muito tempo OFFLINE. A TAG foi dada aleatóriamente para o(a) jogador(a) &f{receiver}&5.
    &7O cara arregou no servidor mesmo, hein!

  mito-delay-none: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 perdeu a TAG por ficar muito tempo OFFLINE. A TAG está sem dono no momento.
    &7O cara arregou no servidor mesmo, hein!

  mito-actual: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 é o mito atual.
    &7Morra de medo dele!

  mito-none: |

    &5&l[MITO] &cAtualmente não há nenhum mito.

  mito-define: |

    &5&l[MITO] &5O(a) jogador(a) &f{player}&5 é o novo MITO do servidor!
    &7Morra de medo dele!

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/63-yMito">Site do plugin yMito</a>
    </category>
</seealso>