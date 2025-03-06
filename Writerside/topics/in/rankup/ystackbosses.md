# yStackBosses
<secondary-label ref="rankup"/>

### Descrição
Agrupe bosses no melhor sistema da atualidade

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
<video src="//www.youtube.com/watch?v=dSRzcTK8J-M"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/boss - Abre o menu principal
/boss shop - Abre o menu do shop
/boss armazem - Abre o menu do armazem
/boss top - Abre o menu do top
/boss amuletos - Abre o menu dos amuletos
/boss bosses - Abre o menu dos bosses do servidor
/boss giveboss - Dar bosses para um jogador
/boss givematadora - Dar matadoras para um jogador
/boss giveamuleto - Dar amuletos para um jogador
/boss givebookdamage - Dar livro de dano ao jogador
/boss givestackdamage - Dar livro de stack ao jogador
/boss reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ystackbosses.use - Permissão para o /boss, /boss armazem, /boss top, /boss amuletos, /boss bosses
ystackbosses.shop - Permissão para o /boss shop
ystackbosses.giveboss - Permissão para o /boss giveboss
ystackbosses.giveamulet - Permissão para o /boss giveamuleto
ystackbosses.givesword - Permissão para o /boss givematadora
ystackbosses.givedamagebook - Permissão para o /boss givebookdamage
ystackbosses.givestackbook - Permissão para o /boss givestackdamage</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ystackbosses_killed% - Retorna a quantia de bosses mortos do jogador formatado (1K, 1M, 1T...)
%ystackbosses_killed_raw% - Retorna&nbsp;a quantia de bosses mortos&nbsp;do&nbsp;jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yStackBosses/
    ├── bosses/
    │    └── creeper.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="bosses" collapsible="true">
<chapter title="creeper.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# item do ovo
egg:
  material: '383:50'
  name: '&a&lBOSS CREEPER'
  lore: [ '&fHP: &4❤&c1000&f.' ]

# Entidade que será spawnada
# Lista de entidades: https://helpch.at/docs/1.8.8/org/bukkit/entity/EntityType.html
entity: 'CREEPER'

# Vida do boss
health: 1000

# Nome do boss
name: '&a&lBOSS CREEPER &7x{stack}'

# Bater no boss apenas com uma matadora
sword-hit: true

message:
  kill:
    actionbar: '&c-1 &a&lBOSS CREEPER.'
    title: '&c-1 &a&lBOSS CREEPER.'
    chat: |

      &a&lBOSS CREEPER: &7Parabéns guerreiro, você conseguiu me matar. Recolha suas recompensas no &f&n/boss&7.

  hit:
    actionbar: '&a&lBOSS CREEPER &7 ({stack}) > &c❤ {health} &4[-{damage}] {progressbar}'
    title: ''
    chat: ''
  interact:
    actionbar: '&a&lBOSS CREEPER &7 ({stack}) > &c❤ {health} {progressbar}'
    title: ''
    chat: ''

# Efeitos que serão aplicados quando um jogador bater no boss
# Tipos: FOGO, EXPLOSAO, DANO, VENENO, EMPURRAR, NAUSEA, CEGUEIRA
effects:
  e1:
    chance: 10.0
    # Use: EFEITO:AMPLIFIER
    list: [ 'FOGO:10', 'EXPLOSAO:1', 'EMPURRAR:3' ]

# Recompensas do boss
# As recompensas são cadastradas na recompensas.yml
# Use: chance,recompense
# Quantia de recompensas que serão dadas
reward-amount: 1
rewards: [ '100,Reco1' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        ____                   _
#  _   _| __ )  ___  ___ ___   / \   _ __ ___ _ __   __ _
# | | | |  _ \ / _ \/ __/ __| / _ \ | '__/ _ \ '_ \ / _` |
# | |_| | |_) | (_) \__ \__ \/ ___ \| | |  __/ | | | (_| |
#  \__, |____/ \___/|___/___/_/   \_\_|  \___|_| |_|\__,_|
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
# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

effects:
  explosion:
    # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/Sound.html
    # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/Sound.html
    # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/Sound.html
    sound: 'EXPLODE'
    # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/Effect.html
    # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/Effect.html
    # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/Effect.html
    particle1: 'LAVA'
    particle2: 'VILLAGER_ANGRY'
    particle3: 'CLOUD'
  # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/potion/PotionEffectType.html
  # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/potion/PotionEffectType.html
  # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/potion/PotionEffectType.html
  poison: 'POISON'
  confusion: 'CONFUSION'
  blindness: 'BLINDNESS'

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static StackBossAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;StackBossAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(StackBossAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/106-yStackBosses">Site do plugin yStackBosses</a>
    </category>
</seealso>