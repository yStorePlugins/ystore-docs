# yTops
<secondary-label ref="management"/>

### Descrição
Mostre para todos quem são os melhores do servidor

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
<video src="//www.youtube.com/watch?v=OG_8NdVB8-0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/topentity&nbsp;- Gerencia os tops de entidades (NPC, ARMORSTAND)
/tophologram&nbsp;- Gerencia os tops de hologramas
/ytops force&nbsp;- Força o envio da mensagem de top
/ytops reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytops.topentity - Permissão para o /topentity
ytops.tophologram - Permissão para o /tophologram
ytops.admin - Permissão para o /ytops</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTops/
    ├── armorstands.yml
    ├── commands.yml
    ├── config.yml
    ├── holograms.yml
    ├── menus.yml
    ├── messages.yml
    └── npcs.yml
</code-block>
</chapter>

<chapter title="armorstands.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     _                              ____  _                  _
#    / \   _ __ _ __ ___   ___  _ __/ ___|| |_ __ _ _ __   __| |___
#   / _ \ | '__| '_ ` _ \ / _ \| '__\___ \| __/ _` | '_ \ / _` / __|
#  / ___ \| |  | | | | | | (_) | |   ___) | || (_| | | | | (_| \__ \
# /_/   \_\_|  |_| |_| |_|\___/|_|  |____/ \__\__,_|_| |_|\__,_|___/
#

# TOP-TYPE DISPONÍVEIS:
# VAULT, YPLANTACOES_MOEDAS, YMAQUINAS_VALOR, YTEMPOONLINE_TEMPO, YLOJAS_VISITAS, YEVENTOS_GANHADOS, YMINAS_QUEBRADOS, YMINAS_BLOCOS, YBOSSES_MATADOS, YNEWBOSSES_MATADOS, YMISSOES_ORDEM, YALMAS_ALMAS, YKILLRANK_KILLS,
# YKILLSYSTEM_XP, YKILLSYSTEM_MONEY, YKILLSYSTEM_KILLS, YKILLSYSTEM_KDR, YRANKUP_PRESTIGIO, YRANKUP_FRAGMENTOS, YSPAWNERS_COMPRADOS, YSPAWNERSSHOP_COMPRADOS, YSPAWNERSSHOP_LIMITE, YSPAWNERSSHOP_GASTO, YCLANS_MONEY, YCLANS_KDR, YCLANS_MAQUINAS,
# YCLANS_SPAWNERS, MCMMO_TODOS, MCMMO_ALQUIMIA, MCMMO_ESPADAS, MCMMO_ARQUERIA, MCMMO_MINERACAO, MCMMO_EXCAVACAO, MCMMO_MACHADOS, MCMMO_REPARACAO, MCMMO_ACROBACIA, YPOINTS_PONTOS, YPESCA_COINS, YPESCA_PESCADOS, YGUERRA_GANHADAS,
# YGUERRA_CLAN_GANHADAS, YCHAIN_KILL, YCHAIN_KILLSTREAK, YCHAIN_KDR, YCHAIN_TEMPO, YCRATESVIRTUAIS_ABERTAS, YRECOMENDAR_RECOMENDADOS, YCLANS_KILLS, YCLANS_DEATHS, YVIPS_ATIVADOS, YVIPS_CREDITOS, YMITO_TIMES, YMITO_TOTAL_TIME,
# YCAMPO_COINS, YCAMPO_BROKEN, YCAMPO_TIME, YPAYMENTS_SPENT, YMINASPACKETS_QUEBRADOS, YMINASPACKETS_BLOCOS, YBANCO_RICOS, YPESCASIMPLES_PESCADOS, YSTACKBOSSES_KILLED, YSTACKBOSSES_DAMAGE

# PLACEHOLDERS DISPONÍVEIS
# {index}, {player_<index>}, {value_<index>}, {value_formatted_<index>}, {value_time_<index>}, {value_kdr_<index>}

armorstand:
  money:
    top-type: 'VAULT'
    hologram:
      offset: 3.1
      lines: [ '&a&lTOP {index}', '&fJogador: &7{player}', '&fDinheiro: &a{value_formatted}' ]
    customs:
      custom_index_1:
        index: 1
        baby: true
        items:
          chestplate: 'DIAMOND_CHESTPLATE'
          leggings: 'DIAMOND_LEGGINGS'
          boots: 'DIAMOND_BOOTS'
          hand: 'null'
        euler-positions:
          head: '0;0;0'
          body: '0;0;0'
          left-arm: '0;0;0'
          right-arm: '0;0;0'
          left-leg: '0;0;0'
          right-leg: '0;0;0'
      custom_index_2:
        index: 2
        baby: true
        items:
          chestplate: 'GOLD_CHESTPLATE'
          leggings: 'GOLD_LEGGINGS'
          boots: 'GOLD_BOOTS'
          hand: 'null'
        euler-positions:
          head: '0;0;0'
          body: '0;0;0'
          left-arm: '0;0;0'
          right-arm: '0;0;0'
          left-leg: '0;0;0'
          right-leg: '0;0;0'
      custom_index_3:
        index: 3
        baby: true
        items:
          chestplate: 'IRON_CHESTPLATE'
          leggings: 'IRON_LEGGINGS'
          boots: 'IRON_BOOTS'
          hand: 'null'
        euler-positions:
          head: '0;0;0'
          body: '0;0;0'
          left-arm: '0;0;0'
          right-arm: '0;0;0'
          left-leg: '0;0;0'
          right-leg: '0;0;0'
      custom_index_4:
        index: 4
        baby: true
        items:
          chestplate: 'CHAINMAIL_CHESTPLATE'
          leggings: 'CHAINMAIL_LEGGINGS'
          boots: 'CHAINMAIL_BOOTS'
          hand: 'null'
        euler-positions:
          head: '0;0;0'
          body: '0;0;0'
          left-arm: '0;0;0'
          right-arm: '0;0;0'
          left-leg: '0;0;0'
          right-leg: '0;0;0'
      custom_index_5:
        index: 5
        baby: true
        items:
          chestplate: 'LEATHER_CHESTPLATE'
          leggings: 'LEATHER_LEGGINGS'
          boots: 'LEATHER_BOOTS'
          hand: 'null'
        euler-positions:
          head: '0;0;0'
          body: '0;0;0'
          left-arm: '0;0;0'
          right-arm: '0;0;0'
          left-leg: '0;0;0'
          right-leg: '0;0;0'
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
  top-entity: 'topentity|topentidade|topnpc'
  top-hologram: 'topholo|topholograma|tophologram'
  ytops: 'ytops'
  tops: 'tops|top'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#       _____
#  _   |_   _|__  _ __  ___
# | | | || |/ _ \| '_ \/ __|
# | |_| || | (_) | |_) \__ \
#  \__, ||_|\___/| .__/|___/
#  |___/         |_|
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

# Tempo para atualizar a lista de tops
# em segundos
top-list-tick: 1800

# Tempo para atualizar as entidades
# em segundos
top-entity-tick: 1810

# Ativar o NPC ficar olhando pro player
look-close: true

# Configuração do menu de TOP
top-menu:
  # em segundos
  time: 600
  player-format: '%ytopspapiaddon_luckperms_prefix% {player}'

# Mensagem de anúncio de jogadores do top
top-message:
  enable: true
  # em segundos
  time: 600
  #
  # PLACEHOLDERS DISPONÍVEIS:
  # {value_<TYPE>_formatted}, {value_<TYPE>_time}, {value_<TYPE>_kdr}
  #
  # TYPES:
  # VAULT, YPLANTACOES_MOEDAS, YMAQUINAS_VALOR, YTEMPOONLINE_TEMPO, YLOJAS_VISITAS, YEVENTOS_GANHADOS, YMINAS_QUEBRADOS, YMINAS_BLOCOS, YBOSSES_MATADOS, YNEWBOSSES_MATADOS, YMISSOES_ORDEM, YALMAS_ALMAS, YKILLRANK_KILLS,
  # YKILLSYSTEM_XP, YKILLSYSTEM_MONEY, YKILLSYSTEM_KILLS, YKILLSYSTEM_KDR, YRANKUP_PRESTIGIO, YRANKUP_FRAGMENTOS, YSPAWNERS_COMPRADOS, YSPAWNERSSHOP_COMPRADOS, YSPAWNERSSHOP_LIMITE, YCLANS_MONEY, YCLANS_KDR, YCLANS_MAQUINAS,
  # YCLANS_SPAWNERS, MCMMO_TODOS, MCMMO_ALQUIMIA, MCMMO_ESPADAS, MCMMO_ARQUERIA, MCMMO_MINERACAO, MCMMO_EXCAVACAO, MCMMO_MACHADOS, MCMMO_REPARACAO, MCMMO_ACROBACIA, YPOINTS_PONTOS, YPESCA_COINS, YPESCA_PESCADOS, YGUERRA_GANHADAS,
  # YGUERRA_CLAN_GANHADAS, YCHAIN_KILL, YCHAIN_KILLSTREAK, YCHAIN_KDR, YCHAIN_TEMPO, YCRATESVIRTUAIS_ABERTAS, YRECOMENDAR_RECOMENDADOS, YCLANS_KILLS, YCLANS_DEATHS, YVIPS_ATIVADOS, YVIPS_CREDITOS, YMITO_TIMES, YMITO_TOTAL_TIME,
  # YMINASPACKETS_QUEBRADOS, YMINASPACKETS_BLOCOS
  #
  player-format: '%ytopspapiaddon_luckperms_prefix% {player}'
  message: |

    &aVeja os jogadores que se destacam no servidor!
    &7(Clique na mensagem para acessar o TOP escolhido)

    <click:run_command:/money top><hover:show_text:"<green>Clique para acessar o TOP</green>"><dark_gray>-></dark_gray> <green>{player_VAULT}</green> <dark_gray>-</dark_gray> <dark_green>$</dark_green><white>{value_VAULT_formatted}</white></hover></click>
]]>
</code-block>
</chapter>

<chapter title="holograms.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   _   _       _
# | | | | ___ | | ___   __ _ _ __ __ _ _ __ ___  ___
# | |_| |/ _ \| |/ _ \ / _` | '__/ _` | '_ ` _ \/ __|
# |  _  | (_) | | (_) | (_| | | | (_| | | | | | \__ \
# |_| |_|\___/|_|\___/ \__, |_|  \__,_|_| |_| |_|___/
#                      |___/

# TOP-TYPE DISPONÍVEIS:
# VAULT, YPLANTACOES_MOEDAS, YMAQUINAS_VALOR, YTEMPOONLINE_TEMPO, YLOJAS_VISITAS, YEVENTOS_GANHADOS, YMINAS_QUEBRADOS, YMINAS_BLOCOS, YBOSSES_MATADOS, YNEWBOSSES_MATADOS, YMISSOES_ORDEM, YALMAS_ALMAS, YKILLRANK_KILLS,
# YKILLSYSTEM_XP, YKILLSYSTEM_MONEY, YKILLSYSTEM_KILLS, YKILLSYSTEM_KDR, YRANKUP_PRESTIGIO, YRANKUP_FRAGMENTOS, YSPAWNERS_COMPRADOS, YSPAWNERSSHOP_COMPRADOS, YSPAWNERSSHOP_LIMITE, YSPAWNERSSHOP_GASTO, YCLANS_MONEY, YCLANS_KDR, YCLANS_MAQUINAS,
# YCLANS_SPAWNERS, MCMMO_TODOS, MCMMO_ALQUIMIA, MCMMO_ESPADAS, MCMMO_ARQUERIA, MCMMO_MINERACAO, MCMMO_EXCAVACAO, MCMMO_MACHADOS, MCMMO_REPARACAO, MCMMO_ACROBACIA, YPOINTS_PONTOS, YPESCA_COINS, YPESCA_PESCADOS, YGUERRA_GANHADAS,
# YGUERRA_CLAN_GANHADAS, YCHAIN_KILL, YCHAIN_KILLSTREAK, YCHAIN_KDR, YCHAIN_TEMPO, YCRATESVIRTUAIS_ABERTAS, YRECOMENDAR_RECOMENDADOS, YCLANS_KILLS, YCLANS_DEATHS, YVIPS_ATIVADOS, YVIPS_CREDITOS, YMITO_TIMES, YMITO_TOTAL_TIME,
# YCAMPO_COINS, YCAMPO_BROKEN, YCAMPO_TIME, YPAYMENTS_SPENT, YMINASPACKETS_QUEBRADOS, YMINASPACKETS_BLOCOS, YBANCO_RICOS, YPESCASIMPLES_PESCADOS, YSTACKBOSSES_KILLED, YSTACKBOSSES_DAMAGE

# PLACEHOLDERS DISPONÍVEIS
# {index}, {player_<index>}, {value_<index>}, {value_formatted_<index>}, {value_time_<index>}, {value_kdr_<index>}

hologram:
  money:
    top-type: 'VAULT'
    hologram:
      lines: [ '&a&lTOP MONEY', '', '&f1º: &7{player_1} &f-> &2$&a{value_1_formatted}', '&f2º: &7{player_2} &f-> &2$&a{value_2_formatted}', '&f3º: &7{player_3} &f-> &2$&a{value_3_formatted}', '&f4º: &7{player_4} &f-> &2$&a{value_4_formatted}', '&f5º: &7{player_5} &f-> &2$&a{value_5_formatted}' ]
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

# Menu top
main:
  name: '&8Tops'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 30
  previous-slot: 9
  next-slot: 17
  # Itens dos tops
  items:
    money:
      top-type: 'VAULT'
      material: 'EMERALD'
      name: '&2$ &aTOP Money'
      lore:
        - ''
        - '&81º &f{player_1}&7: &2$ &a{value_formatted_1}'
        - '&82º &f{player_2}&7: &2$ &a{value_formatted_2}'
        - '&83º &f{player_3}&7: &2$ &a{value_formatted_3}'
        - '&84º &f{player_4}&7: &2$ &a{value_formatted_4}'
        - '&85º &f{player_5}&7: &2$ &a{value_formatted_5}'
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
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  top-type: |
    &cEste tipo não foi encontrado.
    &7Disponíveis: {types}&c.
  top-entity: |
    &cEsta entidade não foi encontrada.
    &7Disponíveis: ARMORSTAND, NPC&c.
  top-index: '&cO TOP deve estar entre 1 e 10.'
  top-already: '&cEste TOP do tipo, entidade e index, já está setado. Delete-o utilizando: /topentity delete'
  top-not-set: '&cEste TOP do tipo, entidade e index, não está setado. Defina-o utilizando: /topentity set'
  top-set: '&aTOP definido com sucesso.'
  top-deleted: '&aTOP deletado com sucesso.'
]]>
</code-block>
</chapter>

<chapter title="npcs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   _   _
# | \ | |_ __   ___ ___
# |  \| | '_ \ / __/ __|
# | |\  | |_) | (__\__ \
# |_| \_| .__/ \___|___/
#       |_|

# TOP-TYPE DISPONÍVEIS:
# VAULT, YPLANTACOES_MOEDAS, YMAQUINAS_VALOR, YTEMPOONLINE_TEMPO, YLOJAS_VISITAS, YEVENTOS_GANHADOS, YMINAS_QUEBRADOS, YMINAS_BLOCOS, YBOSSES_MATADOS, YNEWBOSSES_MATADOS, YMISSOES_ORDEM, YALMAS_ALMAS, YKILLRANK_KILLS,
# YKILLSYSTEM_XP, YKILLSYSTEM_MONEY, YKILLSYSTEM_KILLS, YKILLSYSTEM_KDR, YRANKUP_PRESTIGIO, YRANKUP_FRAGMENTOS, YSPAWNERS_COMPRADOS, YSPAWNERSSHOP_COMPRADOS, YSPAWNERSSHOP_LIMITE, YSPAWNERSSHOP_GASTO, YCLANS_MONEY, YCLANS_KDR, YCLANS_MAQUINAS,
# YCLANS_SPAWNERS, MCMMO_TODOS, MCMMO_ALQUIMIA, MCMMO_ESPADAS, MCMMO_ARQUERIA, MCMMO_MINERACAO, MCMMO_EXCAVACAO, MCMMO_MACHADOS, MCMMO_REPARACAO, MCMMO_ACROBACIA, YPOINTS_PONTOS, YPESCA_COINS, YPESCA_PESCADOS, YGUERRA_GANHADAS,
# YGUERRA_CLAN_GANHADAS, YCHAIN_KILL, YCHAIN_KILLSTREAK, YCHAIN_KDR, YCHAIN_TEMPO, YCRATESVIRTUAIS_ABERTAS, YRECOMENDAR_RECOMENDADOS, YCLANS_KILLS, YCLANS_DEATHS, YVIPS_ATIVADOS, YVIPS_CREDITOS, YMITO_TIMES, YMITO_TOTAL_TIME,
# YCAMPO_COINS, YCAMPO_BROKEN, YCAMPO_TIME, YPAYMENTS_SPENT, YMINASPACKETS_QUEBRADOS, YMINASPACKETS_BLOCOS, YBANCO_RICOS, YPESCASIMPLES_PESCADOS, YSTACKBOSSES_KILLED, YSTACKBOSSES_DAMAGE

# PLACEHOLDERS DISPONÍVEIS
# {index}, {player_<index>}, {value_<index>}, {value_formatted_<index>}, {value_time_<index>}, {value_kdr_<index>}

npc:
  money:
    top-type: 'VAULT'
    hologram:
      offset: 3.1
      lines: [ '&a&lTOP {index}', '&fJogador: &7{player}', '&fDinheiro: &a{value_formatted}' ]
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static TopAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;TopAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(TopAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/96-yTops">Site do plugin yTops</a>
    </category>
</seealso>