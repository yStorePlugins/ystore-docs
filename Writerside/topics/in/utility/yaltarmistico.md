# yAltarMistico
<secondary-label ref="utility"/>

### Descrição
Aumente o fluxo de players que entram em PVP, coloque altares que dropam itens em cada arena do servidor.

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
<video src="//www.youtube.com/watch?v=OS5xD5dbYu8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/altaradmin criar [altar] - Cria um novo altar
/altaradmin deletar [altar] - Deleta um altar
/altaradmin editar [altar] - Edita um altar
/altaradmin dar [altar] - Pega um altar
/altaradmin reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yaltarmistico.use - Permissão para o /altaradmin
yaltarmistico.admin.create - Permissão para o /altaradmin criar
yaltarmistico.admin.delete - Permissão para o /altaradmin deletar
yaltarmistico.admin.edit - Permissão para o /altaradmin editar
yaltarmistico.admin.reload - Permissão para o /altaradmin reload
yaltarmistico.admin - Permissão para ser reconhecido como admin</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yAltarMistico/
    ├── altars/
    │    └── teste.yml
    ├── commands.yml
    ├── config.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="altars" collapsible="true">
<chapter title="teste.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
key: teste
icon: rO0ABXNyABpvcmcuYnVra2l0LnV0aWwuaW8uV3JhcHBlcvJQR+zxEm8FAgABTAADbWFwdAAPTGphdmEvdXRpbC9NYXA7eHBzcgA1Y29tLmdvb2dsZS5jb21tb24uY29sbGVjdC5JbW11dGFibGVNYXAkU2VyaWFsaXplZEZvcm0AAAAAAAAAAAIAAlsABGtleXN0ABNbTGphdmEvbGFuZy9PYmplY3Q7WwAGdmFsdWVzcQB+AAR4cHVyABNbTGphdmEubGFuZy5PYmplY3Q7kM5YnxBzKWwCAAB4cAAAAAN0AAI9PXQABHR5cGV0AARtZXRhdXEAfgAGAAAAA3QAHm9yZy5idWtraXQuaW52ZW50b3J5Lkl0ZW1TdGFja3QAEkVOREVSX1BPUlRBTF9GUkFNRXNxAH4AAHNxAH4AA3VxAH4ABgAAAAZxAH4ACHQACW1ldGEtdHlwZXQADGRpc3BsYXktbmFtZXQABGxvcmV0AAhlbmNoYW50c3QACUl0ZW1GbGFnc3VxAH4ABgAAAAZ0AAhJdGVtTWV0YXQAClVOU1BFQ0lGSUN0AB7Cp2JBbHRhciBNw61zdGljbyDCpzcoZGVmYXVsdClzcgA2Y29tLmdvb2dsZS5jb21tb24uY29sbGVjdC5JbW11dGFibGVMaXN0JFNlcmlhbGl6ZWRGb3JtAAAAAAAAAAACAAFbAAhlbGVtZW50c3EAfgAEeHB1cQB+AAYAAAACdAAAdAAewqc3Q29sb3F1ZSBubyBjaMOjbyBwYXJhIHNldGFyc3IAN2NvbS5nb29nbGUuY29tbW9uLmNvbGxlY3QuSW1tdXRhYmxlQmlNYXAkU2VyaWFsaXplZEZvcm0AAAAAAAAAAAIAAHhxAH4AA3VxAH4ABgAAAAF0AApEVVJBQklMSVRZdXEAfgAGAAAAAXNyABFqYXZhLmxhbmcuSW50ZWdlchLioKT3gYc4AgABSQAFdmFsdWV4cgAQamF2YS5sYW5nLk51bWJlcoaslR0LlOCLAgAAeHAAAAABc3IAEWphdmEudXRpbC5IYXNoU2V0ukSFlZa4tzQDAAB4cHcMAAAAED9AAAAAAAABdAANSElERV9FTkNIQU5UU3g=
barsSymbol: █
blockMaterial: ENDER_PORTAL_FRAME
entityType: ENDER_CRYSTAL
bossArenaBoss: creeper
replacesWaiting: §cAguardando Jogadores
messageDrop: ''
messageSpawned: ''
time: 60
dropAmount: 1
minimumPlayer: 1
radiusX: 30
radiusY: 5
radiusZ: 30
barsAmount: 16
blockData: 0
entityOffset: 1.0
hologramOffset: 4.0
throwUp: true
entity: true
entityBossArena: false
strikeLightning: true
forceItemDrop: true
hologram:
- §bAltar Místico §7(default)
- §7Gerador de itens básicos.
- '§fPróximo drop em:'
- §e{time}
- '{progressbar} §7({percentage})'
announces:
  an10:
    time: 10
    message: §b§l[Altar] §bO altar irá dropar em &710s&b.

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
  altaradmin: 'altaradmin'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#            _    _ _             __  __ _     _   _
#  _   _   / \  | | |_ __ _ _ __|  \/  (_)___| |_(_) ___ ___
# | | | | / _ \ | | __/ _` | '__| |\/| | / __| __| |/ __/ _ \
# | |_| |/ ___ \| | || (_| | |  | |  | | \__ \ |_| | (_| (_) |
#  \__, /_/   \_\_|\__\__,_|_|  |_|  |_|_|___/\__|_|\___\___/
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

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false
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

# Menu principal
main:
  name: '&8Altar'
  size: 45
  items:
    icon-slot: 10
    hologram-slot: 11
    bars-slot: 13
    block-slot: 15
    entity-slot: 16
    bossArena-slot: 21
    time-slot: 23
    dropAmount-slot: 28
    minimumPlayer-slot: 29
    radius-slot: 31
    throwUp-slot: 33
    strikeLightning-slot: 34
    icon:
      material: 'ITEM_FRAME'
      name: '&aÍcone do Altar'
      lore:
        - '&7Clique em um item do seu inventário para alterar'
    hologram:
      material: 'ARMOR_STAND'
      name: '&aHolograma'
      lore:
        - '&fOff-set: &a{offset}&f.'
        - ''
        - '&7Clique para alterar'
    bars:
      material: 'LEGACY_NAME_TAG'
      name: '&aBarra de Progresso'
      lore:
        - '&fSímbolo: &a{symbol}&f.'
        - '&fQuantia: &a{amount}&f.'
        - ''
        - '&7Clique ESQUERDO para alterar o símbolo'
        - '&7Clique DIREITO para alterar a quantia'
    block:
      material: 'STONE'
      name: '&aBloco'
      lore:
        - '&fAtual: &a{block}&f.'
        - ''
        - '&7Clique para alterar'
    entity:
      material: 'MONSTER_EGG'
      name: '&aEntidade'
      lore:
        - '&fAtivado: &a{status}&f.'
        - '&fEntidade: &a{entity}&f.'
        - '&fOff-set: &a{offset}&f.'
        - ''
        - '&7Clique ESQUERDO para alternar'
        - '&7Clique DIREITO para alterar a entidade'
        - '&7Clique Q para alterar o offset'
    bossArena:
      material: 'DIAMOND_SWORD'
      name: '&aBoss Arena'
      lore:
        - '&fAtivado: &a{status}&f.'
        - '&fEntidade: &a{entity}&f.'
        - ''
        - '&7Clique ESQUERDO para alternar'
        - '&7Clique DIREITO para alterar a entidade'
    time:
      material: 'WATCH'
      name: '&aTempo'
      lore:
        - '&fAtual: &a{time}&f.'
        - ''
        - '&7Clique para alterar'
    dropAmount:
      material: 'EMERALD'
      name: '&aQuantia de drops'
      lore:
        - '&fAtual: &a{amount}&f.'
        - '&7(mesmo com boss ativo)'
        - '&fForçar drop: &a{status}&f.'
        - ''
        - '&7Clique DIREITO para alternar'
        - '&7Clique ESQUERDO para alterar a quantia'
    minimumPlayer:
      material: 'DIAMOND'
      name: '&aPlayers mínimos'
      lore:
        - '&fAtual: &a{amount}&f.'
        - ''
        - '&7Clique para alterar'
    radius:
      material: 'BARRIER'
      name: '&aRaio de checagem'
      lore:
        - '&fX: &a{x} blocos&f.'
        - '&fY: &a{y} blocos&f.'
        - '&fZ: &a{z} blocos&f.'
        - ''
        - '&7Clique ESQUERDO para alterar X'
        - '&7Clique DIREITO para alterar Y'
        - '&7Clique Q para alterar Z'
    throwUp:
      material: 'SLIME_BLOCK'
      name: '&aJogar para cima'
      lore:
        - '&fEstado: &a{status}&f.'
        - ''
        - '&7Clique para alterar'
    strikeLightning:
      material: 'BLAZE_ROD'
      name: '&aRaio'
      lore:
        - '&fEstado: &a{status}&f.'
        - ''
        - '&7Clique para alterar'
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

actionbar:
  not-cancelled: '&cA operação ainda não foi cancelada.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  help: '&cVocê não tem permissão para fazer isto.'
  help-admin: |

    &bComandos do plugin:

    &b-> &f/altaradmin criar [altar] &8-&7 Cria um novo altar
    &b-> &f/altaradmin deletar [altar] &8-&7 Deleta um altar
    &b-> &f/altaradmin editar [altar] &8-&7 Edita um altar
    &b-> &f/altaradmin dar [altar] &8-&7 Pega um altar
    &b-> &f/altaradmin reload &8-&7 Recarrega as configurações

  altar-found: '&cEste altar não existe. Disponíveis: {list}'
  altar-exists: '&cEste altar {altar} já existe.'
  altar-created: '&aEste altar {altar} foi criado.'
  altar-deleted: '&aEste altar {altar} foi deletado.'
  altar-gived: '&aVocê pegou o item para por o altar {altar} no chão.'
  altar-placed: '&aVocê colocou o altar {altar} no chão.'
  altar-breaked: '&aVocê removeu o altar {altar} do chão.'
  digit-symbol: |

    &aDigite o SÍMBOLO que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-time: |

    &aDigite o TEMPO que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-amount: |

    &aDigite a QUANTIA que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-block: |

    &aDigite o BLOCO que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-entity: |

    &aDigite a ENTIDADE que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-boss: |

    &aDigite o BOSS que você quer.
    &7Para cancelar, digite &ncancelar&7.

  material-found: '&cMaterial não encontrado.'
  entity-found: '&cEntidade não encontrada.'
  boss-found: '&cBoss não encontrado. Disponíveis: {bosses}'
  change-symbol: '&aSímbolo alterado para &f{symbol}&a.'
  change-barAmount: '&aQuantia de barras alterada para &f{amount}&a.'
  change-block: '&aBloco alterado para &f{block}&a.'
  change-entity: '&aEntidade alterada para &f{entity}&a.'
  change-boss: '&aBoss alterado para &f{boss}&a.'
  change-time: '&aTempo alterado para &f{time}&a.'
  change-dropAmount: '&aQuantia de drops alterada para &f{amount}&a.'
  change-playerMinimum: '&aQuantia de players mínimos alterada para &f{amount}&a.'
  change-radiusX: '&aRaio X alterado para &f{amount}&a.'
  change-radiusY: '&aRaio Y alterado para &f{amount}&a.'
  change-radiusZ: '&aRaio Z alterado para &f{amount}&a.'
  change-entityOffset: '&aOff-set da entidade alterado para &f{amount}&a.'
  change-hologramOffset: '&aOff-set do holograma alterado para &f{amount}&a.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/21-yAltarMistico">Site do plugin yAltarMistico</a>
    </category>
</seealso>