# yBosses
<secondary-label ref="rankup"/>

### Descrição
Entidades editadas que dão recompensas!

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
<video src="//www.youtube.com/watch?v=U6XEYS7mMdQ"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/boss - Abre o menu principal
/boss verconteudo - Vê o preview de recompensas de um boss
/boss giveboss - Dar boss à um jogador
/boss givematadora - Dar matadora à um jogador
/boss wand - Dar a vara de seleção de área
/boss reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ynewbosses.usar - Permissão para o /bossynewbosses.verconteudo - Permissão para o /boss verconteudoynewbosses.giveboss - Permissão para o /boss givebossynewbosses.givematadora - Permissão para o /boss givematadoraynewbosses.wand - Permissão para o /boss wandynewbosses.reload - Permissão para o /boss reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yBosses/
    ├── menus/
    │    ├── loja.yml
    │    ├── lojabosses.yml
    │    ├── lojamatadoras.yml
    │    ├── preview.yml
    │    ├── principal.yml
    │    ├── recompensas.yml
    │    └── top.yml
    ├── bosses.yml
    ├── config.yml
    ├── matadoras.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="loja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Loja'
Tamanho: 27
BackSlot: 18
Itens:
  Bosses:
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/3857d6b17901fd3f0109bd9bdcc28021b65947fce0a958327247d26d92915b85'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aBosses'
    Lore:
      - '&7Clique para comprar bosses.'
  Matadoras:
    Slot: 14
    CustomSkull: false
    URL: ''
    ID: 276
    Data: 0
    Glow: true
    Name: '&aMatadoras'
    Lore:
      - '&7Clique para comprar matadoras.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Matadoras:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="lojabosses.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja de Bosses'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 18
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="lojamatadoras.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja de Matadoras'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 18
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Preview'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Menu'
Tamanho: 27
Itens:
  Recompensas:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: 130
    Data: 0
    Glow: true
    Name: '&aRecompensas!'
    Lore:
      - '&7Recolha as recompensas'
      - '&7de todos os bosses mortos!'
      - ''
      - '&aClique para acessar.'
  Informacoes:
    Slot: 12
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSuas informações'
    Lore:
      - '&7Veja suas informações'
      - '&7referente aos bosses.'
      - ''
      - ' &fBosses mortos: &a{mortos}&f.'
      - ' &fDano causado: &a{dano}&f.'
      - ''
  Loja:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aLoja'
    Lore:
      - '&7Compre aqui bosses e'
      - '&7matadoras.'
      - ''
      - '&aClique para visualizar.'
  Top:
    Slot: 15
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTop jogadores'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacaram matando'
      - '&7diversos bosses.'
      - ''
      - '&aClique para visualizar.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Top:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26
# Item para recolher todas as recompensas
Recolher todos:
  Slot: 49
  CustomSkull: false
  URL: ''
  ID: 408
  Data: 0
  Glow: true
  Name: '&6Recolher todos'
  Lore:
    - '&7Clique para recolher'
    - '&7todas as recompensas.'
# Item que irá mostrar quanto estiver vazio
Vazio:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: 408
  Data: 0
  Glow: true
  Name: '&cVazio!'
  Lore:
    - '&7Você não possui nenhuma'
    - '&7recompensa armazenada.'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&6&lTOP JOGADORES'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17
# Item do top
Item:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f#{pos} &7> &a{player}'
  Lore:
    - ''
    - '&fBosses mortos: &a{mortos}&f.'
    - '&fDano causado: &a{dano}&f.'
    - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bosses.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bosses:
  BossCreeper:
    # Item que o jogador receberá
    Ovo:
      CustomSkull: false
      URL: ''
      ID: 383
      Data: 50
      Glow: true
      Name: '&a&lBOSS CREEPER'
      Lore:
        - '&fHP: &4❤&c1000&f.'
    # Entidade que será spawnada
    # Lista de entidades: https://helpch.at/docs/1.8.8/org/bukkit/entity/EntityType.html
    Entidade: 'CREEPER'
    # Vida do boss
    Vida: 1000
    # Nome do boss
    Nome: '&a&lBOSS CREEPER'
    # Bater no boss apenas com uma matadora
    Bater matadora: true
    # Mensagem que será enviada quando um jogador matar o boss
    # Deixe "Matou: []" caso não queira usar.
    Matou:
      - ''
      - '&a&lBOSS CREEPER: &7Parabéns guerreiro, você conseguiu me matar. Recolha suas recompensas no &f&n/boss&7.'
      - ''
    # Mensagens que serão enviadas no actionbar
    # Deixe '' para não usar alguma.
    Actionbar:
      # Actionbar ao bater
      Bater: '&a&lBOSS CREEPER &7> &c❤ {vida} &4[-{dano}] {progressbar}'
      # Actionbar ao clicar com botão direito
      Direito: '&a&lBOSS CREEPER &7> &c❤ {vida} {progressbar}'
    # Efeitos que serão aplicados quando um jogador bater no boss
    # Tipos: FOGO, EXPLOSAO, DANO, VENENO, EMPURRAR, NAUSEA, CEGUEIRA
    Efeitos:
      e1:
        Chance: 10.0
        # Use: EFEITO:AMPLIFIER
        Lista:
          - 'FOGO:10'
          - 'EXPLOSAO:1'
          - 'EMPURRAR:3'
    # Opões de compra da matadora
    # Apague esta seção caso não queira usar.
    Comprar:
      Compravel: true
      Preco: 100.0
      # Ordem que irá ser representada na Loja de Bosses
      # Do menor ao maior.
      Ordem: 1
      Item:
        CustomSkull: false
        URL: ''
        ID: 276
        Data: 0
        Glow: true
        Name: '&a&lBOSS CREEPER'
        Lore:
        - '&fHP: &4❤&c1000&f.'
        - '&fPreço: &b100 coins&f.'
        - ''
        - '&aClique com esquerdo para comprar.'
        - '&aClique com direito para ver as recompensas.'
    # Recompensas do boss
    # As recompensas são cadastradas na recompensas.yml
    # Use: chance,recompense
    # Sempre dar alguma recompensa? (ativando essa opção, evita que o jogador fique sem receber nada)
    SempreDar: true
    Recompensas:
      - '100,Reco1'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE, MYSQL_FAST
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true
# Comandos e aliases do plugin
Comando:
  Comando: 'boss'
  Aliases: [ bosses ]
# Permitir colocar bosses e matar bosses apenas nos plots
Somente plot: false
# Verifica se há mobs por perto antes de spawnar
# Raio em blocos.
Raio checagem: 5
# Deixar a matadora inquebrável
Matadora inquebravel: true
# Dar as recompensas diretamente ao jogador (sem armazenar)
RecompensasDiretas: false
# Mundos bloqueados para colocar bosses
MundosBloqueados:
  - 'none'
# Configurações dos efeitos
Efeitos:
  Explosao:
    # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/Sound.html
    # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/Sound.html
    # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/Sound.html
    Som: 'EXPLODE'
    # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/Effect.html
    # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/Effect.html
    # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/Effect.html
    Particula1: 'LAVA'
    Particula2: 'VILLAGER_ANGRY'
    Particula3: 'CLOUD'
  # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/potion/PotionEffectType.html
  # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/potion/PotionEffectType.html
  # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/potion/PotionEffectType.html
  Veneno: 'POISON'
  Nausea: 'CONFUSION'
  Cegueira: 'BLINDNESS'
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Inv cheio: '&cSeu inventário está cheio.'
  Usar matadora: '&cVocê deve usar uma matadora para bater neste boss.'
  Permissao plot: '&cVocê não tem permissão neste terreno.'
  Mobs spawners: '&cHá mobs ou spawners num raio de 5 blocos.'
  Nao tem money: '&cVocê não possui a quantia necessária de money: &7{money}&c.'
  Comprou matadora: '&aVocê adquiriu uma matadora {matadora}&a com sucesso.'
  Comprou boss: '&aVocê adquiriu um boss {boss}&a com sucesso.'
  Deu boss: '&aVocê deu &7{quantia}x {boss}&a para o jogador &7{player}&a.'
  Recebeu boss: '&aVocê recebeu &7{quantia}x {boss}&a.'
  Deu matadora: '&aVocê deu &71 {matadora}&a para o jogador &7{player}&a.'
  Recebeu matadora: '&aVocê recebeu &71 {matadora}&a.'
# Configuração da barra de progresso
Progress bar:
  Quantia: 10
  Simbolo: ':'
  Cor sim: '&a'
  Cor nao: '&7'
# Setas dos menus.
Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
  Anterior:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para ir à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróximo'
    Lore:
      - '&7Clique para ir à próxima página.'
# Formatos de quantia e money
Formats:
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

<chapter title="matadoras.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Matadoras:
  Default:
    # Dano da matadora
    # Deixe 0 para ser uma HitKill
    Dano: 20
    # Nome da matadora
    Nome: '&7Padrão'
    # Opões de compra da matadora
    # Apague esta seção caso não queira usar.
    Comprar:
      Compravel: true
      Preco: 100.0
      Item:
        CustomSkull: false
        URL: ''
        ID: 276
        Data: 0
        Glow: true
        Name: '&aMatadora de Bosses'
        Lore:
          - '&7Essa espada fornece mais'
          - '&7dano aos bosses!'
          - ''
          - ' &fDano: &c20❤'
          - ' &fPreço: &b100 coins&f.'
          - ''
          - '&aClique para comprar.'
    # Item da matadora
    Item:
      CustomSkull: false
      URL: ''
      ID: 276
      Data: 0
      Glow: true
      Name: '&aMatadora de Bosses'
      Lore:
        - '&7Essa espada fornece mais'
        - '&7dano aos bosses!'
        - ''
        - ' &fDano: &c20❤'
  Avancada:
    Dano: 0 #deixe 0 para hitkill
    Nome: '&7Avançada'
    Item:
      CustomSkull: false
      URL: ''
      ID: 276
      Data: 0
      Glow: true
      Name: '&aMatadora de Bosses'
      Lore:
        - '&7Essa espada fornece mais'
        - '&7dano aos bosses!'
        - ''
        - ' &fDano: &cHitKill&f.'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá no preview do boss.
    Preview:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEsta pedra vale muito dinheiro!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será dado o item se os comandos estiverem em false.
    # Item que será dado ao jogador.
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEu valho muito!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Money que será dado ao jogador
    Money: 0.0
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: false
      List:
        - 'give {player} stone 1'

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/48-yBosses">Site do plugin yBosses</a>
    </category>
</seealso>