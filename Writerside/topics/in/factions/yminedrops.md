# yMineDrops
<secondary-label ref="factions"/>

### Descrição
Drope minérios ao quebrar pedras, porcentagem editável, permita que dropem também recompensas.

### Versões
<secondary-label ref="1.8"/>
<secondary-label ref="1.9"/>
<secondary-label ref="1.12"/>
<secondary-label ref="1.16"/>

### Demonstração
<video src="//www.youtube.com/watch?v=tAjvIYekJoY"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/minerar - Para ir até o mundo de mineração</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMineDrops/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comandos:
  Minerar:
    Comando: 'minerar'
    Aliases: [ mine, mina ]
#
Mensagens:
  Ja esta: '&cVocê já está na mina.'
  Delay: '&cAguarde &e{time} &cpara usar o comando novamente.'
  Comando bloqueado: '&cEste comando está bloqueado neste mundo.'

Mundo:
  Gerar: true
  # Mundo desenhado pelo plugin
  Custom: true
  Nomes:
    - 'world_mining'
  # Mundos onde ao minerar ORES não droparão nada
  Ore block:
    - 'world'

Opcoes:
  # XP (vanila) que será dado ao quebrar o bloco
  XP: 3
  # XP (mcmmo) que será dado ao quebrar o bloco
  XP mcmmo: 3
  # Ativar o PVP no mundo
  Pvp: false
  # Deixar o jogador invencivel
  Invencibilidade: false
  # Se ativo, só irá vir esmeraldas na Extreme Hills
  Esmeralda extremehills: true
  # Se ativo, irá proibir o spawn de mobs
  Desabilitar mobs: true
  # Enviar os itens direto para o inventário do jogador
  Autopickup: true
  # Bloco que ao quebrar irá dar minérios
  Bloco: 'STONE'
  Remover drops:
    - 'COBBLESTONE'
    - 'STONE'
  Bloquear comandos:
    - '/g oi'
  # Ao ativar, quando um jogador quebrar um bloco, enviará para ele no chat o bioma que está.
  Bioma debug: false
  # Biomas que serão considerados extreme hills
  Biomas:
    - 'EXTREME_HILLS'
    - 'EXTREME_HILLS_PLUS'
    - 'EXTREME_HILLS_MOUNTAINS'
    - 'EXTREME_HILLS_PLUS_MOUNTAINS'
    - 'EXTREME_HILLS_WITH_TREES'
    - 'MUTATED_EXTREME_HILLS'
    - 'MUTATED_EXTREME_HILLS_WITH_TREES'
    - 'SMALLER_EXTREME_HILLS'
    - 'BIRCH_FOREST_HILLS'
    - 'BIRCH_FOREST_HILLS_MOUNTAINS'
    - 'COLD_TAIGA_HILLS'
    - 'DESERT_HILLS'
    - 'FOREST_HILLS'
    - 'JUNGLE_HILLS'
    - 'MEGA_SPRUCE_TAIGA_HILLS'
    - 'MEGA_TAIGA_HILLS'
    - 'TAIGA_HILLS'
  # Efeitos que serão aplicados nos jogadores
  # EFEITO:AMPLIFIER
  Efeitos:
    - 'FAST_DIGGING:1'
    - 'INVISIBILITY:1'

Comando:
  Cooldown: 120 #em segundos
  Entrar:
    - ''
    - '&aVoce entrou na mina'
    - ''
  Raio:
    X: 2000
    Z: 2000

Recompensas:
  Recompensa1:
    Permissao: ''
    Actionbar: '&aVocê encontrou uma recompensa minerando'
    Title: '&aRecompensa <nl>&aencontrada!'
    Chance: 10.0
    Comandos:
      - 'give {player} stone 1'

Fortune:
  Porcentagem: 3

Minerios:
  COAL:
    Data: 0
    Camada: 63
    Chance: 40.0
    Fortune: true
    Actionbar: '' # deixe '' para não usar
  IRON_INGOT:
    Data: 0
    Camada: 63
    Chance: 20.0
    Fortune: false
    Actionbar: '' # deixe '' para não usar
  GOLD_INGOT:
    Data: 0
    Camada: 31
    Chance: 15.0
    Fortune: false
    Actionbar: '' # deixe '' para não usar
  INK_SACK:
    Data: 4
    Camada: 30
    Chance: 10.0
    Fortune: true
    Actionbar: '' # deixe '' para não usar
  REDSTONE:
    Data: 0
    Camada: 15
    Chance: 10.0
    Fortune: true
    Actionbar: '' # deixe '' para não usar
  DIAMOND:
    Data: 0
    Camada: 15
    Chance: 5.0
    Fortune: true
    Actionbar: '' # deixe '' para não usar
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/22-yMineDrops">Site do plugin yMineDrops</a>
    </category>
</seealso>