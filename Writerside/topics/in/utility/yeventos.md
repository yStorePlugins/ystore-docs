# yEventos
<secondary-label ref="utility"/>

### Descrição
Crie interações e competições entre os jogadores, vários eventos para divertir seus players.

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
<video src="//www.youtube.com/watch?v=GoJAAM4Hc8s"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/eventos - Abre o menu principal
/eventos top - Abre o menu do top
/eventos info - Abre o menu de eventos
/eventos entrar - Entra no evento presencial que está ocorrendo
/eventos camarote - Entra no camarote do evento presencial que está ocorrendo
/eventos sair - Sair do evento presencial que está ocorrendo
/eventos setexitall - Seta a saída de todos os eventos
/eventos reload - Recarrega as configurações
/[name] - Para participar do evento
/[name] [resposta] - Para responder um evento chat
/[name] camarote - Para ir ao camarote do evento
/[name] apostar - Para apostar em alguém no evento
/[name] sair - Para sair do evento
/[name] iniciar - Para iniciar o evento
/[name] parar - Para parar o evento
/[name] setloc - Para setar um local do evento
/[name] addloc - Para adicionar multiplas entradas ao evento
/[name] delloc - Para deletar um local do evento
/[name] wand - Para pegar a ferramenta de seleção do evento
/[name] define - Para definir a área do evento
/[name] addwall - Para adicionar uma parede ao evento
/[name] clearwalls - Para limpar as paredes do evento
/[name] addsafezone - Para adicionar uma safezone ao evento
/[name] clearsafezones - Para limpar as safezones do evento
/[name] forcestart - Para forçar a inicialização do evento
/[name] ajuda - Mostra todos os comandos daquele evento</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yeventos.use - Permissão para o /eventos
yeventos.top - Permissão para o /eventos top
yeventos.info - Permissão para o /eventos info
yeventos.enter - Permissão para o /eventos entrar
yeventos.exit - Permissão para o /eventos exit
yeventos.reload - Permissão para o /eventos reload
yeventos.setexitall - Permissão para o /eventos setexitall
yeventos.[name].participate - Permissão para o /[name] e /[name] [resposta]
yeventos.[name].camarote - Permissão para o /[name] camarote
yeventos.[name].bet - Permissão para o /[name] apostar
yeventos.[name].exit - Permissão para o /[name] sair
yeventos.[name].start - Permissão para o /[name] iniciar
yeventos.[name].stop - Permissão para o /[name] parar
yeventos.[name].forcestart - Permissão para o /[name] forcestart
yeventos.[name].setloc - Permissão para o /[name] setloc
yeventos.[name].addloc - Permissão para o /[name] addloc
yeventos.[name].delloc - Permissão para o /[name] delloc
yeventos.[name].wand - Permissão para o /[name] wand
yeventos.[name].define - Permissão para o /[name] define
yeventos.[name].addwalls - Permissão para o /[name] addwalls
yeventos.[name].clearwalls - Permissão para o /[name] clearwalls
yeventos.[name].addsafezone - Permissão para o /[name] addsafezone
yeventos.[name].clearsafezones - Permissão para o /[name] clearsafezones
yeventos.staff - Permissão para ser reconhecido como staff
yeventos.command.bypass - Permissão para executar comandos nos eventos
yeventos.vanish.bypass - Permissão para não ficar invisível no camarote
yeventos.blockplace.bypass - Permissão para colocar blocos nos eventos</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yeventos_wins% - Retorna a quantia de eventos que o player ganhou com formatação (1K, 1000,00...)
%yeventos_wins_raw% - Retorna a quantia de eventos que o player ganhou sem formatação.
%yeventos_wins_[name]% - Retorna a quantia de vezes que o player ganhou o evento, com formatação (1K, 1000,00...)
%yeventos_wins_[name]_raw% - Retorna a quantia de vezes que o player ganhou o evento, sem formatação.
%yeventos_[name]&nbsp;- Retorna se o evento está ativo% - yeventos_[name]_tag
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{[name]} - Retorna a tag (se possuir)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEventos/
    ├── events/
    ├── commands.yml
    ├── config.yml
    ├── discord.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="events" collapsible="true">
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
  yeventos: 'yeventos|yevents|eventos|events'
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

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Altura do void do seu servidor
void-detect: 0

# Mundos em que não irá receber anúncios dos eventos
announce-world-blacklist: []

# Ativar dar fly no camarote
camarote-fly: false

# Comandos liberados no camarote
camarote-allowed-commands:
  - '/g'
  - '/l'
  - '/.'

# Delay de desaparecimento de blocos da arena (TNTRUN ou similar)
# em ticks (20t = 1s)
disappear-delay: 8

# Sistema de anúncios na proxy
proxy:
  # Ativar o sistema
  enabled: true
  # Whitelist de servidores que irão receber os anúncios
  server-whitelist: [ 'mina' ]

# Autostart dos eventos
auto-start:
  schedule1:
    # nome do arquivo do evento sem o ".yml"
    type: 'fastclick'
    # todos, segunda, terca, quarta, quinta, sexta, sabado, domingo
    # dia-hora:minuto:segundo
    schedule: [ 'todos-00:00:01' ]

# Configuração do item da varinha
wand:
  material: 'GOLD_AXE'
  name: '&eSeleção de Área'
  lore: [ '&7Evento: &f{event}', '', '&aEsquerdo -> POS1', '&aDireito -> POS2' ]
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
options:
  url: ''
  username: 'yEventos'

embeds:
  jackpot:
    title: ':mailbox: Um novo Evento começou!'
    thumbnail: ''
    color: '#fff'
    content: ''
    image: ''
    footer:
      text: 'yStore © Todos os direitos reservados'
      image: ''
    fields:
      event:
        inline: false
        header: 'Evento'
        content: '```Bolão```'
      server:
        inline: false
        header: 'Servidor'
        content: '```RankUP```'
      date_activated:
        inline: false
        header: 'Começou em'
        content: '```{date} às {hour}```'
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
    permission: 'yeventos.provider.money'
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
  name: '&8Eventos'
  size: 27
  items:
    profile-slot: 11
    events-slot: 13
    top-slot: 15
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7desempenho nos eventos.'
        - ''
        - ' &8▶ &fVitórias: &7{wins}'
        - ''
    events:
      material: 'd01afe973c5482fdc71e6aa10698833c79c437f21308ea9a1a095746ec274a0f'
      name: '&eEventos'
      lore:
        - '&7Confira todas as informações'
        - '&7sobre cada um dos eventos.'
        - ''
        - '&6Clique para acessar!'
    top:
      material: '4ea96c49302132167c81c87b79e06dd343020ff20923fce87d388c462409261c'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em nossos eventos.'
        - ''
        - '&aClique para acessar!'

# Menu de eventos
events:
  name: '&8Eventos'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu de votação
voting:
  name: '&8Eventos'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu top
top:
  name: '&8TOP'
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
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'
  items:
    # Item do top que mais ganhou
    event:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fVitórias: &7{amount}'
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

    &a/evento &8- &7Abre o menu principal.
    &a/evento reload &8- &7Recarrega as configurações.

  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  no-time: '&cVocê não tem tempo online. Necessário: {time}.'
  empty: '&cEsvazie seu inventário (&7conteúdo e armadura)&c para entrar no evento.'
  command: '&cVocê não pode executar este comando no evento.'
  already: '&cVocê já está em um evento.'
  exit-found: '&cVocê precisar setar a saída do evento primeiro.'
  entry-found: '&cVocê precisar setar a entrada do evento primeiro.'
  wait-found: '&cVocê precisar setar a sala de espera do evento primeiro.'
  area-found: '&cVocê precisar setar a área do evento primeiro.'
  walls-found: '&cVocê precisar setar as paredes do evento primeiro.'
  camarote-found: '&cO camarote do evento não foi setado.'
  camarote-exit-found: '&cA saída do camarote do evento não foi setado.'
  location-set: '&aLocalização &f{location} &asetada com sucesso.'
  location-found: '&cLocalização &f{location} &cnão encontrada. Disponíveis: {list}'
  location-del: '&aLocalização &f{location} &adeletada com sucesso.'
  pos-set: '&aPosição &f{pos} &asetada com sucesso.'
  pos-found: '&cPosição &f{pos} &cnão encontrada.'
  area-none: '&cNenhum bloco permitido localizado na área.'
  area-set: '&aÁrea setada com sucesso.'
  wall-added: '&aParede adicionada com sucesso.'
  wall-cleared: '&aParedes limpas.'
  safezone-added: '&aÁrea segura adicionada com sucesso.'
  safezone-cleared: '&aÁreas seguras limpas.'
  duel-pos-1-found: '&cPosição 1 do duelo não encontrada.'
  duel-pos-2-found: '&cPosição 2 do duelo não encontrada.'
  camarote-enter: '&aTeleportado ao camarote.'
  camarote-exit: '&cVocê saiu do camarote.'
  target-event-found: '&cO jogador {player} não está participando do evento.'
  economy-found: '&cEconomia não encontrada. Disponíveis: {list}.'
  bet-already: '&cVocê já está apostando neste evento.'
  bet: '&cVocê apostou &f{amount} coins&a no jogador &f{player}&a.'
  bought: '&aVocê comprou a ativação do evento &f{event}&a.'
  bought-delay: '&cAguarde {time} para comprar este evento novamente.'
  not-setup: '&cEste evento não está 100% configurado.'
  already-initialized: '&cEste evento já começou.'
  already-voted: '&cVocê já votou em um evento.'
  event-found: '&cVocê não pode adentrar em nenhum evento ou nenhum evento está ocorrendo.'
  exit-all: '&cSaídas de todos os eventos setadas.'
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static EventAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;EventAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(EventAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/29-yEventos">Site do plugin yEventos</a>
    </category>
</seealso>