# yMobSetSpawn
<secondary-label ref="management"/>

### Descrição
Defina o local de spawn dos mobs da tua facção ou plot

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
<video src="//www.youtube.com/watch?v=9fL_4C2dBEA"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/f setspawn - Abrir o menu de mobs para setar
/deletar o spawn. (comando configurável)
/f setspawn reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymobsetspawn.use - Permissão para o /f setspawn
ymobsetspawn.reload - Permissão para o /f setspawn reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMobSetSpawn/
    ├── schema/
    ├── config.yml
    ├── menus.yml
    ├── messages.yml
    └── mobs.yml
</code-block>
</chapter>

<chapter title="schema" collapsible="true">
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#                      _     __      _   __
#   _   _  /\/\   ___ | |__ / _\ ___| |_/ _\_ __   __ ___      ___ __
#  | | | |/    \ / _ \| '_ \\ \ / _ \ __\ \| '_ \ / _` \ \ /\ / / '_ \
#  | |_| / /\/\ \ (_) | |_) |\ \  __/ |__\ \ |_) | (_| |\ V  V /| | | |
#   \__, \/    \/\___/|_.__/\__/\___|\__\__/ .__/ \__,_| \_/\_/ |_| |_|
#   |___/                                  |_|
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
  # Determina o tipo de banco de dados. Valores válidos: [SQLITE, MYSQL, MARIADB (Recomendado)]
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
  # Aqui você poderá configurar algumas coisas do HikariCP.
  # Por padrão, já são dadas algumas configurações com base na documentação do hikari:
  # https://github.com/brettwooldridge/HikariCP/wiki/MySQL-Configuration
  properties:
    cachePrepStmts: true
    prepStmtCacheSize: 250
    prepStmtCacheSqlLimit: 2048
    useServerPrepStmts: true
    useLocalSessionState: true
    rewriteBatchedStatements: true
    cacheResultSetMetadata: true
    cacheServerConfiguration: true
    elideSetAutoCommits: true
    maintainTimeStats: true

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Configurações gerais
general:
  # Blacklist de mundos onde o plugin não funciona
  blacklisted-worlds: ['none']
  # Comandos que serão detectados pelo plugin
  # Escreva em letras minúsculas
  commands:
    - '/mobsetspawn'
    - '/f setspawn'
    - '/p setspawn'
  # Coloque aqui os cargos permitidos do factions
  # Se teu plugin de factions for MassiveCore editado, é possível que
  # estes nomes estejam diferentes, portanto consulte o desenvolvedor
  # que editou o plugin.
  faction-roles:
    - 'LEADER'
    - 'OFFICER'

# Sistema de inteligência artificial dos mobs
artificial-intelligence:
  enabled: false
  # Whitelist de mundos em que o sistema de AI irá funcionar
  whitelisted-worlds: ['none']
  # Blacklist de entidades que o sistema de AI não vai funcionar
  blacklisted-entities: ['none']
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

# Menu de gerenciamento dos mobs
set-spawn:
  name: '&8Mobs - SetSpawn'
  size: 27
  #facing:
  #  soon:
  #    material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
  #    slot: 11
  #    name: '&cEm Breve'
  #    lore: []
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
  permission: '&cVocê não tem permissão para fazer isto.'
  retrieving: '&aCarregando dados...'
  blacklisted-world: '&cVocê não pode realizar esta ação neste mundo.'
  plot-null: '&cVocê não está em um terreno.'
  plot-owner: '&cEste terreno não tem dono.'
  plot-permission: '&cVocê não tem permissão neste terreno.'
  faction-null: '&cVocê não possui facção.'
  faction-role: '&cVocê não é o líder ou capitão da facção.'
  faction-location: '&cVocê não está no território da sua facção.'
  mob-permission: '&cVocê não tem a permissão deste mob.'
  mob-removed: '&aLocalização do mob &f{mob}&a removida com sucesso.'
  mob-set: '&aLocalização do mob &f{mob}&a  setada com sucesso.'
]]>
</code-block>
</chapter>

<chapter title="mobs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#                _
#    /\/\   ___ | |__  ___
#   /    \ / _ \| '_ \/ __|
#  / /\/\ \ (_) | |_) \__ \
#  \/    \/\___/|_.__/|___/
#
# Cadastre aqui os mobs permitidos.

mobs:
   cow:
      slot: 10
      permission: 'ymobsetspawn.cow'
      display: 'Vaca'
      entity: 'COW'
      items:
         set:
            material: 'c5a9cd58d4c67bccc8fb1f5f756a2d381c9ffac2924b7f4cb71aa9fa13fb5c'
            name: '&eVaca'
            lore:
               - ''
               - '&aX: &f{x}&8 - &aY: &f{y} &8- &aZ: &f{z} &7({world})'
               - ''
               - '&7Botão &FESQUERDO&7 para mudar a localização.'
               - '&7Botão &fDIREITO&7 para deletar a localização.'
               - ''
         not-set:
            material: 'c5a9cd58d4c67bccc8fb1f5f756a2d381c9ffac2924b7f4cb71aa9fa13fb5c'
            name: '&eVaca'
            lore:
               - ''
               - '&cEste mob ainda não possui uma localização setada.'
               - ''
               - '&7Botão &FESQUERDO&7 para setar a localização.'
               - ''
   pig:
      slot: 11
      permission: 'ymobsetspawn.pig'
      display: 'Porco'
      entity: 'PIG'
      items:
         set:
            material: '621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4'
            name: '&ePorco'
            lore:
               - ''
               - '&aX: &f{x}&8 - &aY: &f{y} &8- &aZ: &f{z} &7({world})'
               - ''
               - '&7Botão &FESQUERDO&7 para mudar a localização.'
               - '&7Botão &fDIREITO&7 para deletar a localização.'
               - ''
         not-set:
            material: '621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4'
            name: '&ePorco'
            lore:
               - ''
               - '&cEste mob ainda não possui uma localização setada.'
               - ''
               - '&7Botão &FESQUERDO&7 para setar a localização.'
               - ''
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/10-yMobSetSpawn">Site do plugin yMobSetSpawn</a>
    </category>
</seealso>