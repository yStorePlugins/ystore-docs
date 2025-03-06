# yEconomias
<secondary-label ref="management"/>

### Descrição
Crie múltiplas novas economias no seu servidor

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
<video src="//www.youtube.com/watch?v=ifDtUaXUERw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/currencies reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">/
yeconomias.use - Permissão para o /currencies reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yeconomias_[identificador_da_config]_amount% - Retorna a quantia do jogador na economia
%yeconomias_[identificador_da_config]_amount_raw% - Retorna a quantia do jogador na economia sem formatar
%yeconomias_[identificador_da_config]_rich% - Retorna a tag de top se o jogador for o mais rico na economia
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{identificador_da_config} - Tag do jogador mais rico&nbsp;
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEconomias/
    ├── economies/
    │    └── token.yml
    ├── commands.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="economies" collapsible="true">
<chapter title="token.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Identificação necessária para a API de Economias do yPlugins
# Identificação necessária para a API de Tops do yTops
# Identificação necessária para a API do PAPI
# Identificação necessária para a API de Chat
yplugins-id: 'yeconomias-token'
top-user: 'none'
# yPlugins -> puxar a formatação do yPlugins
# LETTER -> formatar em letras: 1K, 1M...
# NUMBER -> formatar em números decimais: 1.000, 10.000.000...
format: 'yPlugins'

# Ativar o sistema de receber a mensagem de pagamento na proxy (Velocity e BungeeCord)
proxy-chat: true

command:
  command: 'token'
  aliases: ['tokens']

sub-command:
  add: [ 'add', 'adicionar', 'somar', 'sum', 'depositar', 'deposit' ]
  remove: [ 'remove', 'remover', 'subtrair', 'subtract', 'withdraw', 'sacar', 'retirar' ]
  set: [ 'set', 'setar', 'define', 'definir' ]
  pay: [ 'pay', 'pagar', 'enviar', 'send' ]
  top: [ 'top' ]
  help: [ 'help', 'ajuda' ]
  force-update: [ 'forceupdate' ]
  check: [ 'check', 'cheque' ]

usage:
  add: '&cUse: /{command} {arg} <player> <quantia>'
  remove: '&cUse: /{command} {arg} <player> <quantia>'
  set: '&cUse: /{command} {arg} <player> <quantia>'
  pay: '&cUse: /{command} {arg} <player> <quantia>'
  check: '&cUse: /{command} {arg} <player> <porcentagem> <multiplier>'

permission:
  main: 'yeconomias.token.use'
  look: 'yeconomias.token.look'
  add: 'yeconomias.token.add'
  remove: 'yeconomias.token.remove'
  set: 'yeconomias.token.set'
  pay: 'yeconomias.token.pay'
  top: 'yeconomias.token.top'
  help: 'yeconomias.token.help'
  force-update: 'yeconomias.token.forceupdate'
  admin: 'yeconomias.token.admin'
  check: 'yeconomias.token.check'

general:
  # Quantia que recebe ao registrar
  default: 0
  # Abrir menu ao digitar /token
  main-menu: true
  # Abrir menu ao digitar /token top
  top-menu: true
  # Proibir o "pay/enviar" caso o jogador esteja offline
  block-offline-pay: false
  # Formato da economia na quantia singular
  singular: 'token'
  # Formato da economia no plural
  plural: 'tokens'
  # Tag do mais rico na economia
  tag: '&5[$]'

# Configuração do money top em chat
top-chat:
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  rich-format: '{currency} '
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  prefix-format: '%luckperms_prefix% '
  tags: '{rich}{prefix}'
  format: '  &f{pos}º {tags}&7{player}&6: &7(c {currency})'
  message:
    - '&5Top 10 Mais Ricos &7(Atualizado de 10 em 10 minutos)'
    - ''
    - '{format}'
    - ''

# Mensagens gerais do plugin
messages:
  permission: '&cVocê não possui permissão para isto.'
  target: '&cEste jogador não foi encontrado.'
  number: '&cO argumento não é um número.'
  has: '&cVocê não possui esta quantia de tokens.'
  yourself: '&cVocê não pode pagar à si mesmo.'
  force-update: '&aVocê forçou a atualização do TOP.'
  balance: |
    &aVocê possui: &f{currency}&a {unit}.
  balance-target: |
    &aO jogador &7{player}&a possui: &f{currency}&a {unit}.
  set: |
    &aVocê setou os tokens do jogador &7{player} &apara: &f{currency}&a {unit}.
  remove: |
    &aVocê removeu &f{currency}&a {unit} do jogador &7{player}&a.
  add: |
    &aVocê adicionou &f{currency}&a {unit} para o jogador &7{player}&a.
  send: |
    &aVocê enviou &f{currency}&a {unit} para o jogador &7{player}&a.
  received: |
    &aVocê recebeu &f{currency}&a {unit} do jogador &7{player}&a.
  help: |
    &a<--> Comandos de tokens <-->
    <nl>
    - '&f > &a/tokens &8- &7Ver suas informações.
    - '&f > &a/tokens &f<jogador> &8- &7Ver as informações de outro jogador.
    - '&f > &a/tokens enviar &f<jogador> <quantia> &8- &7Enviar tokens para um jogador.
    - '&f > &a/tokens top &8- &7Ver o TOP mais ricos em tokens.
    <nl>
  help-admin: |
    &a<--> Comandos de tokens &7(STAFF)&a <-->
    <nl>
    &f > &a/tokens &8- &7Ver suas informações.
    &f > &a/tokens &f<jogador> &8- &7Ver as informações de outro jogador.
    &f > &a/tokens enviar &f<jogador> <quantia> &8- &7Enviar tokens para um jogador.
    &f > &a/tokens adicionar &f<jogador> <quantia> &8- &7Adicionar tokens para um jogador.
    &f > &a/tokens remover &f<jogador> <quantia> &8- &7Remover tokens de um jogador.
    &f > &a/tokens setar &f<jogador> <quantia> &8- &7Setar tokens para um jogador.
    &f > &a/tokens top &8- &7Ver o TOP mais ricos em tokens.
    &f > &a/tokens forceupdate &8- &7Forçar a atualização do TOP.
    <nl>
  rich: |
    <nl>
    &5&l[c]&d O jogador &f{player} &dé o novo &d&nRICO&d do servidor.
    &7O novo rico possui &f{currency} &7{unit}.
    <nl>
  check-give: |
    &aVocê enviou &f{currency}&a {unit} para o jogador &7{player}&a em forma de cheque.
  check-converted: |
    &aVocê juntou seus cheques com sucesso.
  check-activated: |
    &aVocê ativou um cheque de &e{amount}&a {unit}.

# Item do cheque da média
check:
  material: 'INK_SACK:14'
  name: '&aCheque de Tokens'
  lore:
    - ''
    - ' &a&l| &fValor: &a{amount}'
    - ''

menu:
  top:
    name: '&8TOP Ricos'
    size: 36
    slots: [ 10, 11, 12, 13, 14, 15, 16 ]
    back-slot: 31
    previous-slot: 9
    next-slot: 17
    # Item do top
    item:
      material: '{player}'
      name: '&f#{pos} &7> &a{player}'
      lore: [ '', '&fTokens: &a{currency}&f.', '' ]
    # Seta de voltar
    back-item:
      material: 'ARROW'
      name: '&cVoltar'
      lore: [ '&7Clique para voltar ao menu anterior.' ]
    previous-item:
      material: 'ARROW'
      name: '&cAnterior'
      lore: [ '&7Clique para ir à página anterior.' ]
    next-item:
      material: 'ARROW'
      name: '&aPróximo'
      lore: [ '&7Clique para ir à próxima página.' ]
  main:
    name: '&8Tokens'
    size: 27
    # Item de informações
    item:
      slot: 11
      material: '{player}'
      name: '&aSuas informações'
      lore:
        - '&7Veja suas informações'
        - '&7referente ao token.'
        - ''
        - ' &fSaldo atual: &a{currency}&f.'
        - ''
    # Item do top
    top:
      slot: 15
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTop jogadores'
      lore:
        - '&7Veja os jogadores que'
        - '&7se destacam sendo os'
        - '&7mais ricos do servidor.'
        - ''
        - '&aClique para visualizar.'
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
  currencies: 'currencies|economies|economias'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _____                                _
#  _   _| ____|___ ___  _ __   ___  _ __ ___ (_) __ _ ___
# | | | |  _| / __/ _ \| '_ \ / _ \| '_ ` _ \| |/ _` / __|
# | |_| | |__| (_| (_) | | | | (_) | | | | | | | (_| \__ \
#  \__, |_____\___\___/|_| |_|\___/|_| |_| |_|_|\__,_|___/
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

  # Nome da tabela dos usuários
  table: 'yeconomias.players'

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
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static EconomiasAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;EconomiasAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(EconomiasAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/102-yEconomias">Site do plugin yEconomias</a>
    </category>
</seealso>