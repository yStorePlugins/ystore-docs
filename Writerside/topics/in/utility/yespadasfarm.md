# yEspadasFarm
<secondary-label ref="utility"/>

### Descrição
Tenha espadas com looting infinito no teu servidor

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
<video src="//www.youtube.com/watch?v=uEwMPFPXmM4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/espadas - Abre o menu principal
/espadas ajuda - Envia a mensagem de ajuda
/espadas give - Dá uma espada à um jogador
/espadas givebook - Dá um item ativável com looting à um jogador
/espadas reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yespadasfarm.use - Permissão para o /espadas
yespadasfarm.help - Permissão para o /espadas ajuda
yespadasfarm.give - Permissão para o /espadas give
yespadasfarm.givebook - Permissão para o /espadas givebook
yespadasfarm.reload - Permissão para o /espadas reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEspadasFarm/
    ├── private_addon/
    │    ├── divine.yml
    │    ├── killstack.yml
    │    └── sharp.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── enchants.yml
    ├── menus.yml
    ├── messages.yml
    └── swords.yml
</code-block>
</chapter>

<chapter title="private_addon" collapsible="true">
<chapter title="divine.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Máximo de sharpness que uma espada pode ter
# essencial para o sistema de stack sharpness looting usando o item
# deixe 0 para não ter máximo
divine-maximum: 1500

chance-per-level: 10.0

# em segundos
duration: 30

multiplier: 1.5

# Slot no menu principal
slot: 17

title-activated: '&eDivine<nl>&eAtivado!'
actionbar-activated: '&eDivine ativado! Duração: &7{duration}&e.'
actionbar-duration: '&eDivine ativado! Duração: &7{duration}&e.'

give-book: '&bVocê deu &71x Livro de Divine {divine}&b para o jogador &f{player}.'
received-book: '&bVocê recebeu &71x Livro de Divine {divine}&b.'
maximum: '&cVocê não pode encantar esta espada, pois ela já está no máximo, com {divine} em Divine.'

# Item da sharpness ativável
usable-item:
  material: ENCHANTED_BOOK
  name: '&b+{divine} Divine'
  lore:
    - ''
    - '&fDivine: &b{divine}'
    - ''
    - '&7Clique em uma espada para ativar.'
]]>
</code-block>
</chapter>

<chapter title="killstack.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Máximo de kill-stack que uma espada pode ter
# deixe 0 para não ter máximo
kill-stack-maximum: 5

# Slot no menu principal
slot: 18

give-book: '&bVocê deu &71x Livro de Kill-Stack {killstack}&b para o jogador &f{player}.'
received-book: '&bVocê recebeu &71x Livro de Kill-Stack {killstack}&b.'
maximum: '&cVocê não pode encantar esta espada, pois ela já está no máximo, com {killstack} em Kill-Stack.'

# Item da sharpness ativável
usable-item:
  material: ENCHANTED_BOOK
  name: '&b+{killstack} Kill-Stack'
  lore:
    - ''
    - '&fKill-Stack: &b{killstack}'
    - ''
    - '&7Clique em uma espada para ativar.'
]]>
</code-block>
</chapter>

<chapter title="sharp.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Máximo de sharpness que uma espada pode ter
# essencial para o sistema de stack sharpness looting usando o item
# deixe 0 para não ter máximo
sharpness-maximum: 1500

# Slot no menu principal
slot: 16

give-book: '&bVocê deu &71x Livro de Sharpness {sharpness}&b para o jogador &f{player}.'
received-book: '&bVocê recebeu &71x Livro de Sharpness {sharpness}&b.'
maximum: '&cVocê não pode encantar esta espada, pois ela já está no máximo, com {sharpness} em Sharpness.'

# Item da sharpness ativável
usable-item:
  material: ENCHANTED_BOOK
  name: '&b+{sharpness} Sharpness'
  lore:
    - ''
    - '&fSharpness: &b{sharpness}'
    - ''
    - '&7Clique em uma espada para ativar.'
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
  sword: 'sword|swords|espada|espadas|espadafarm|espadasfarm'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         _____                     _           _____
#  _   _| ____|___ _ __   __ _  __| | __ _ ___|  ___|_ _ _ __ _ __ ___
# | | | |  _| / __| '_ \ / _` |/ _` |/ _` / __| |_ / _` | '__| '_ ` _ \
# | |_| | |___\__ \ |_) | (_| | (_| | (_| \__ \  _| (_| | |  | | | | | |
#  \__, |_____|___/ .__/ \__,_|\__,_|\__,_|___/_|  \__,_|_|  |_| |_| |_|
#  |___/          |_|
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

# Modo de depuração para correção de problemas no plugin.
debug-mode: false

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Sistemas gerais do plugin
general:
  # Máximo de looting que uma espada pode ter
  # essencial para o sistema de stack de looting usando o item
  # deixe 0 para não ter máximo
  looting-maximum: 1500
  # Permitir que a espada possa ser usada para atacar jogadores
  attack-players: false
  # Abrir menu de evolução ao interagir com a espada (Shift+Botão direito)
  interact-menu: true
  # Mundos que a matadora não irá funcionar
  world-blacklist: []
  # Item da looting ativável
  usable-item:
    material: ENCHANTED_BOOK
    name: '&b+{looting} Pilhagem'
    lore:
      - ''
      - '&fPilhagem: &b{looting}'
      - ''
      - '&7Clique em uma espada para ativar.'

# Sistema de bloquear matar mobs sem a espada-farm
kill-normal:
  # Ativar o sistema
  enable: false
  # Lista de metadatas que o sistema não vai funcionar
  blacklist-metadata: []

# Sistema de formatos de money e quantia
format:
  type: 'LETTER' # Tipos: LETTER - NUMBER
  max-decimals: 4
  formats:
    - ''
    - ''
    - 'K'
    - 'M'
    - 'B'
    - 'T'
    - 'Q'
    - 'QQ'
    - 'S'
    - 'SS'
    - 'O'
    - 'N'
    - 'D'
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
  Money:
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
    permission: 'yespadasfarm.provider.money'
]]>
</code-block>
</chapter>

<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Aumenta chance nas recompensas do ySpawners
lucky:
  display: 'Sortudo'
  default: 0
  maximum: -1
  bonus-per-level: 10.0 # em porcentagem
  prices-default:
    price1:
      provider: 'money'
      price: 10000.0
  prices-per-level:
    price1:
      provider: 'money'
      price: 10000.0
  displays: # Item que aparecerá no menu de evolução
    can: # quando puder evoluir
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aSortudo'
      lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    cant: # quando não puder evoluir
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aSortudo'
      lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem blocos ou nível suficientes.'
    maximum: # quando já estiver no máximo
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aSortudo'
      lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'

lucky_bossarena:
  display: 'Sortudo B.A'
  default: 0
  maximum: -1
  bonus-per-level: 10.0 # em porcentagem
  prices-default:
    price1:
      provider: 'money'
      price: 10000.0
  prices-per-level:
    price1:
      provider: 'money'
      price: 10000.0
  displays: # Item que aparecerá no menu de evolução
    can: # quando puder evoluir
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aSortudo B.A'
      lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    cant: # quando não puder evoluir
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aSortudo B.A'
      lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem blocos ou nível suficientes.'
    maximum: # quando já estiver no máximo
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aSortudo B.A'
      lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'

double_reward:
  display: 'Reco Duplo'
  default: 0
  maximum: -1
  bonus-per-level: 10.0 # em porcentagem
  prices-default:
    price1:
      provider: 'money'
      price: 10000.0
  prices-per-level:
    price1:
      provider: 'money'
      price: 10000.0
  displays: # Item que aparecerá no menu de evolução
    can: # quando puder evoluir
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aReco Duplo'
      lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe recompensas em dobro.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    cant: # quando não puder evoluir
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aReco Duplo'
      lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe recompensas em dobro.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem blocos ou nível suficientes.'
    maximum: # quando já estiver no máximo
      material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      name: '&aReco Duplo'
      lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe recompensas em dobro.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'
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
  name: '&8Espadas'
  size: 27
  items:
    sword-slot: 14
    sortudo-slot: 15
    sortudo-ba-slot: 16
    double-reward-slot: 17
    sword-no-has:
      material: 'BARRIER'
      name: '&eNão disponível'
      glow: true
      lore: ['', '&cVocê já possui a última espada', '&cdisponível para compra.', '']
  facing:
    info:
      slot: 12
      material: BOOK
      name: '&aInformações'
      lore:
        - '&7As espadas com pilhagem'
        - '&7no servidor são muito'
        - '&7importantes! Com elas,'
        - '&7você recebe mais drops'
        - '&7matando monstros.'
        - ''
        - ' &fPara ter níveis infinitos'
        - ' &fde pilhagem, você deve ter'
        - ' &fa espada mais avançada deste'
        - ' &fmenu. Compre-as ao lado!'
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
  permission: '&cVocê não tem permissão para fazer isto.'
  number: '&cO argumento não é um número.'
  list: |
    &cEspada não encontrada
    &7Disponíveis: {list}
  help: |
    <nl>
    &a/swords &8- &7Abre o menu principal.
    &a/sword give &8- &7Dar uma espada para um jogador.
    &a/sword givebook &8- &7Dar um item ativável com looting para um jogador.
    <nl>
  give: '&bVocê deu &71x {sword}&b para o jogador &f{player}.'
  received: '&bVocê recebeu &71x {sword}&b.'
  no-has-looting: '&cVocê não possui a &aEspada de Farm&7[{looting}] &cno inventário.'
  no-has-permission: '&cVocê não possui permissão para comprar esta espada.'
  no-has: '&cVocê não possui &f{value} {type}&c.'
  bought: '&bVocê comprou &71x {sword}&b.'
  give-book: '&bVocê deu &71x Livro de Pilhagem {looting}&b para o jogador &f{player}.'
  received-book: '&bVocê recebeu &71x Livro de Pilhagem {looting}&b.'
  maximum: '&cVocê não pode encantar esta espada, pois ela já está no máximo, com {looting} em pilhagem.'
  latest: '&cVocê não pode encantar esta espada, pois ela não é a última disponível para compra.'
  enchanted: '&aVocê encantou sua espada de farm.'
  attack: '&cVocê não pode bater em players com essa espada.'
  converted: '&bVocê compactou todos seus livros em 1.'
  need-sword: '&cVocê precisa de uma espada-farm para atacar este mob.'
  holding: '&cVocê precisa estar segurando sua espada-farm.'
]]>
</code-block>
</chapter>

<chapter title="swords.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   __                       _
#  / _\_      _____  _ __ __| |___
#  \ \\ \ /\ / / _ \| '__/ _` / __|
#  _\ \\ V  V / (_) | | | (_| \__ \
#  \__/ \_/\_/ \___/|_|  \__,_|___/
#
# Espadas de pilhagem disponíveis

swords:
  basic:
    priority: 1
    # Essa é a última looting disponível?
    latest: true
    # Pilhagem necessária para comprar essa
    looting-needed: 0
    # Pilhagem da espada
    looting: 1000
    # Permissão para poder comprar essa espada
    permission: ''
    # Display nas mensagens
    display: '&aEspada de Farm'
    # Tornar a espada inquebrável
    unbreakable: true
    # Preços para compra
    prices:
      cost1:
        type: 'PlayerPoints'
        price: 10.0
        display: 'cash'
    # Configuração da espada no menu
    menu:
      buy-item-cant:
        material: DIAMOND_SWORD
        name: '&aEspada de Farm &7[{looting}&7]'
        lore:
          - '&7Inquebrável ∞'
          - '&7Pilhagem {looting}'
          - '&7Sortudo {lucky}'
          - '&7Sortudo B.A {lucky_bossarena}'
          - '&7Reco Duplo {double_reward}'
          - ''
          - '&f Preço: &6{PlayerPoints} cash'
          - '&f Pilhagem necessária: &7Nenhuma!'
          - ''
          - '&cRequisitos insuficientes para compra.'
          - ''
      buy-item-can:
        material: DIAMOND_SWORD
        name: '&aEspada de Farm &7[{looting}&7]'
        lore:
          - '&7Inquebrável ∞'
          - '&7Pilhagem {looting}'
          - '&7Sortudo {lucky}'
          - '&7Sortudo B.A {lucky_bossarena}'
          - '&7Reco Duplo {double_reward}'
          - ''
          - '&f Preço: &6{PlayerPoints} cash'
          - '&f Pilhagem necessária: &7Nenhuma!'
          - ''
          - '&aClique para comprar.'
          - ''
    # Configuração da espada
    item:
      material: DIAMOND_SWORD
      name: '&aEspada de Farm &7[{looting}&7]'
      glow: true
      lore:
        - '&7Inquebrável ∞'
        - '&7Afiação {sharpness}'
        - '&7Pilhagem {looting}'
        - '&7Sortudo {lucky}'
        - '&7Sortudo B.A {lucky_bossarena}'
        - '&7Reco Duplo {double_reward}'
      enchants:
        - 'DAMAGE_ALL:35'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static EspadasFarmAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;EspadasFarmAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(EspadasFarmAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/95-yEspadasFarm">Site do plugin yEspadasFarm</a>
    </category>
</seealso>