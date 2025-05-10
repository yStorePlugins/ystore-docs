# yClansRedisAddon
<secondary-label ref="addons"/>

### Descrição
Interligue os clans entre os seus servidores

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
<secondary-label ref="1.22"/>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yClansRedisAddon/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____ _                 ____          _ _        _       _     _
#  _   _ / ___| | __ _ _ __  ___|  _ \ ___  __| (_)___   / \   __| | __| | ___  _ __
# | | | | |   | |/ _` | '_ \/ __| |_) / _ \/ _` | / __| / _ \ / _` |/ _` |/ _ \| '_ \
# | |_| | |___| | (_| | | | \__ \  _ <  __/ (_| | \__ \/ ___ \ (_| | (_| | (_) | | | |
#  \__, |\____|_|\__,_|_| |_|___/_| \_\___|\__,_|_|___/_/   \_\__,_|\__,_|\___/|_| |_|
#  |___/
#
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

# Configurações do servidor redis
redis:
  # Ativar a conexão com o redis
  enabled: false
  # Endereço de conexão. [EX: 127.0.0.1]
  host: 'localhost'
  # Porta de conexão. [EX: 3306]
  port: 6379
  # Usuário de conexão. [EX: root]
  username: ''
  # Senha do usuário de conexão: [EX: 123]
  password: ''
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/164-yClansRedisAddon">Site do plugin yClansRedisAddon</a>
    </category>
</seealso>