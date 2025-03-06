# yRecompensas
<secondary-label ref="utility"/>

### Descrição
Faça com que blocos e mobs não dropem itens normais, mas sim recompensas!

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
<video src="//www.youtube.com/watch?v=-sLlCAWla2o"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/recogivesortudo - Dar o livro de encantamento à um jogador. 
/recogivesortudo reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yrecompensas.givelivro - Permissão para o /recogivesortudo
yrecompensas.admin - Permissão para o /recogivesortudo admin</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yRecompensas/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Comando: 'recogivesortudo'
  Aliases: [ ]

# Mundos que poderão vir recompensas
Mundos:
  - 'world'
  - 'mundo'

Usar blocos: true
Usar mobs: true
Msg ganhou: true

# Recompensas droparem mesmo com inventário cheio
Inv cheio: false

# Coloque as regiões do worldguard para não bugar fragmentos
Regioes blacklist:
  - 'spawn'

# Encantamento que poderá ser aplicado no item
# para somar % de chances para ganhar recompensas
Encantamento:
  # Ativar o encantamento
  Ativar: true
  # Nome do encantamento
  Nome: 'Sortudo'
  # Chance que irá somar para ganhar recompensas
  Chance: 5.0
  # Livro do encantamento
  Item:
    CustomSkull: false
    URL: ''
    ID: 403
    Data: 0
    Glow: false
    Name: '&eLivro de encantamento'
    Lore:
      - '&7Sortudo I'
      - ''
      - '&eClique em cima de uma espada ou picareta para encantá-la.'
  # Itens que poderá ser aplicado
  Itens:
    - 'DIAMOND_SWORD'
    - 'GOLD_SWORD'
    - 'IRON_SWORD'
    - 'STONE_SWORD'
    - 'WOOD_SWORD'
    - 'DIAMOND_PICKAXE'
    - 'IRON_PICKAXE'
    - 'GOLD_PICKAXE'
    - 'STONE_PICKAXE'
    - 'WOOD_PICKAXE'

Mensagens:
  Nao encontrado: '&cEste jogador não foi encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Nao pode: '&cEste encantamento não serve para este item.'
  Ja possui: '&cSeu item já possui este encantamento.'
  Encantado: '&aSeu item foi encantado com sucesso.'
  Deu: '&aVocê deu &7{quantia}&a de livros ceifador para o jogador &7{player}&a.'
  Recebeu: '&aVocê recebeu &7{quantia} &a de livros ceifador.'

Blocos:
  Reco1:
    ID: STONE #id do bloco quebrado
    Data: 0 #data do bloco quebrado
    Chance: 50.0
    Mensagem: '&aVocê ganhou 1 recompensa por quebrar este bloco.'
    Actionbar: '&eVocê encontrou uma recompensa!'
    Title: '&eRecompensa encontrada'
    Gives:
      - '[daritem] item1'
      - 'say {player} ganhou 1 item na recompensa'

Mobs:
  Reco1:
    Entidade: 'PIG'
    Chance: 50.0
    Mensagem: '&aVocê ganhou 1 recompensa por matar este mob.'
    Actionbar: '&eVocê encontrou uma recompensa!'
    Title: '&eRecompensa encontrada'
    Gives:
      - '[daritem] item1'
      - 'say {player} ganhou 1 item na recompensa'

Items:
  item1:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/c641682f43606c5c9ad26bc7ea8a30ee47547c9dfd3c6cda49e1c1a2816cf0ba'
    ID: 0
    Data: 0
    Glow: true
    Name: '&eRecompensa 1'
    Lore:
      - ''
      - '&7Isto é uma recompensa.'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/14-yRecompensas">Site do plugin yRecompensas</a>
    </category>
</seealso>