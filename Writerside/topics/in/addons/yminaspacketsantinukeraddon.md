# yMinasPacketsAntiNukerAddon
<secondary-label ref="addons"/>

### Descrição
Proteja sua mineração dos jogadores mal intencionados

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
<video src="//www.youtube.com/watch?v=qZ6mK73EffA"/>


## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMinasPacketsAntiNukerAddon/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __ _                 ____            _        _          _          _   _ _   _       _
#  _   _|  \/  (_)_ __   __ _ ___|  _ \ __ _  ___| | _____| |_ ___   / \   _ __ | |_(_) \ | |_   _| | _____ _ __
# | | | | |\/| | | '_ \ / _` / __| |_) / _` |/ __| |/ / _ \ __/ __| / _ \ | '_ \| __| |  \| | | | | |/ / _ \ '__|
# | |_| | |  | | | | | | (_| \__ \  __/ (_| | (__|   <  __/ |_\__ \/ ___ \| | | | |_| | |\  | |_| |   <  __/ |
#  \__, |_|  |_|_|_| |_|\__,_|___/_|   \__,_|\___|_|\_\___|\__|___/_/   \_\_| |_|\__|_|_| \_|\__,_|_|\_\___|_|
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

# Limite aceitável de blocos quebrados por checagem
limit: 25

# Limite de warns até executar o kick
warn-limit: 5

# Sistemas gerais do plugin
general:
  # Sistema de notificar o ganho de pontos
  discordhook:
    enabled: true
    channel: ''
    # Placeholders disponíveis:
    # {player}
    # {limit}
    embed: ''

actions:
  # Expulsar o jogador do servidor quando ultrapassar o limite
  kick: false
  # Avisar os staffs que tem um jogador com possível nuker (permissão: "yminaspacketsantinuker.staff")
  warn: true

messages:
  kick: |

    &c&lANTI NUKER

    <s><s><s><s><s><s><s><s>&cVocê&f foi expulso do servidor por possível uso de nuker

    &eVocê ainda pode entrar no servidor, porém todos os staffs foram avisados.

  warn-logout: '&c&l[ANTI NUKER] &cO jogador &f{player} &cfoi expulso por estar quebrando &f{limit} blocos por segundo &cna área de mineração.'
  warn: '&c&l[ANTI NUKER] &cO jogador &f{player} &cestá quebrando &f{limit} blocos por segundo &cna área de mineração.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/148-yMinasPacketsAntiNukerAddon">Site do plugin yMinasPacketsAntiNukerAddon</a>
    </category>
</seealso>