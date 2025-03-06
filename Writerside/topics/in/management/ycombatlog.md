# yCombatLog
<secondary-label ref="management"/>

### Descrição
O plugin mais versátil de combatlog

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
<video src="//www.youtube.com/watch?v=tGgfJXG4SIU"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/combatlog toggle [player] - Alterna o estado do PVP
/combatlog reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycombatlog.use - Permissão para o /combatlog
ycombatlog.admin - Permissão para o /combatlog reload
ycombatlog.toggle - Permissão para o /combatlog toggle
ycombatlog.toggle.others - Permissão para o /combatlog toggle [player]
ycombatlog.staff - Permissão para ser reconhecido como staff</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCombatLog/
    ├── commands.yml
    └── config.yml
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
  combatlog: 'cl|combat|combatlog'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
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
# Sistemas principais.

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Formatos da placeholder %ycombatlog_pvp%
papi-toggle-off: '&cPVP OFF'
papi-toggle-on: '&aPVP ON'

# Formatos da placeholder %ycombatlog_status%
papi-status-off: '&cEM COMBATE'
papi-status-on: '&aLIVRE'

# Comandos que serão executados caso o jogador
# deslogue em combate
# Placeholder para o nick do player: {player}
Comandos deslogar: []

# Comandos permitidos em combate
Comandos permitidos:
  - '/l'
  - '/g'

# Mundos permitidos para teleportar
Mundos permitidos:
  - 'guerra'

# Mundos em que não entra em combatlog
Mundos blacklist:
  - 'nenhum'

# Blacklist de regiões que o sistema de desativar PVP NÃO irá funcionar
region-disable-blacklist: []

# Blacklist de mundos que o sistema de desativar PVP NÃO irá funcionar
world-disable-blacklist: []

# Blacklist de causas que o sistema de desativar PVP irá bloquear
# Lista: https://helpch.at/docs/1.8/org/bukkit/event/entity/EntityDamageEvent.DamageCause.html
causes-blacklist: [ 'LIGHTNING' ]

# Ações para o plugin bloquear
Bloquear:
  Comando: true # Bloqueia de usar comandos em combate
  Teleportar: true # Bloqueia de teleportar em combate
  Enderpearl: true # Bloqueia de jogar ender-pearl em combate
  Pickup: true # Bloqueia de pegar itens com o pvp OFF

# Quando o jogador sair do servidor em combate, matar ele
Matar ao sair: true

# Porcentagem de money que será removida ao deslogar em combate
Sair porcentagem: 0.0

# Valor máximo que será removido ao deslogar em combate
# -1 para ser infinito
Valor maximo: -1

# Tirar o fly quando entrar em combate
Remover fly: true

# Staff poder entrar em combate (permissão: ycombatlog.staff)
Staff combate: false

# Tempo que o jogador fica em combate
Tempo combate: 15 # Em segundos

# Bloquear de entrar em regiões sem pvp em combate (WorldGuard, WorldEdit (ou FAWE)
Bloquear regioes: true

# Bloquear entrar em combate no x1 (yX1)
Bloquear x1: true

# Permissão para receber a mensagem de quitou
Permissao quitou: ''

# Ao registrar no servidor, desativar o PVP automaticamente (PVP TOGGLE)
toggle-register: false

# Mensagens do plugin
Mensagens:
  Quitou:
    - '&c[Combate] O jogador &7{player} &cdeslogou em combate.'
  Saiu:
    - '&aVocê não está mais em combate. Pode deslogar sem perigo.'
  Teleportar:
    - '&cVocê não pode teleportar em combate.'
  Comando:
    - '&cVocê não pode usar comandos em combate.'
  Area:
    - '&cVocê não pode entrar nesta área enquanto estiver em combate.'
  Enderpearl:
    - '&cVocê não pode jogar ender pearl enquanto estiver em combate.'
  Actionbar: '&cVocê está em combate por {tempo} segundos &8[{progressbar}&8]&a.'
  target-pvp: '&cO jogador {player} desativou o PVP.'
  damager-pvp: '&cVocê desativou o PVP.'
  toggle-on: '&aVocê ativou seu PVP.'
  toggle-off: '&cVocê desativou seu PVP.'
  toggle-target-on: '&aVocê ativou o PVP do jogador {player}.'
  toggle-target-off: '&cVocê desativou o PVP do jogador {player}.'
  target: '&cJogador {player} não encontrado.'
  help:
    - '&cComandos disponíveis:'
    - '-> /cl toggle [player]'
    - '-> /cl reload'

# Configuração da barra de progresso
Progress bar:
  Quantia: 10
  Simbolo: ':'
  Cor sim: '&a'
  Cor nao: '&7'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static CombatAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;CombatAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(CombatAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/43-yCombatLog">Site do plugin yCombatLog</a>
    </category>
</seealso>