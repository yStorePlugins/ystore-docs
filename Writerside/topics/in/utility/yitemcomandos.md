# yItemComandos
<secondary-label ref="utility"/>

### Descrição
Crie items que ao ser ativados se transformam em comandos.

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
<video src="//www.youtube.com/watch?v=K4Lu1R5RrG0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/giveitemcomando - Dar um item para um jogador.
/giveitemcomando reload - Recarregar as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yitemcomandos.give - Permissão para o /giveitemcomando</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yItemComandos/
    ├── config.yml
    └── items.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  GiveItem:
    Comando: 'giveitemcomando'
    Aliases: [ gic, giveitemcomandos, givecustomitem, giveitemcustom ]

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Nao e numero: '&cO argumento não é um número.'
  Nao encontrado: '&cJogador não encontrado.'
  Inv cheio: '&cO seu inventário está cheio.'
  Deu: '&aVocê deu &7{quantia}x&a {item}&a para o jogador &7{player}&a.' # deixe '' para não usar
  Recebeu: '&aVocê recebeu &7{quantia}x&a {item}&a do jogador &7{player}&a.' # deixe '' para não usar
]]>
</code-block>
</chapter>

<chapter title="items.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Items:
  item1:
    # Display para aparecer nas mensagens
    Display: '&5Pedra Misteriosa'
    # Som que será enviado ao ativar
    Som: 'ORB_PICKUP'
    # Consumir usos do item
    Consumir: true
    Necessario:
      # Permissão para poder usar o item
      # Deixe Permissao: '' para não usar
      Permissao: ''
      # Bloco que será necessário clicar com o item
      # Deixe Bloco: '' para não usar
      Bloco: 'STONE:0'
      # Tempo necessário para usar o item
      # em segundos (yTempoOnline)
      Tempo: 10
      # Money necessário para usar o item
      Money:
        Quantia: 10
        Consumir: true
    Item:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
      ID: AIR
      Data: 0
      Glow: false
      Name: '&5Pedra misteriosa'
      Lore:
        - '&7Usos: &a{usos}&7.'
        - ''
        - '&fClique para ativar e descobrir o tesouro.'
    Mensagem:
      # Será enviada caso ele não tenha permissao
      Permissao: '&cVocê não pode ativar este item.'
      # Será enviada caso precise clicar no bloco
      Bloco: '&cVocê deve clicar numa pedra.'
      # Será enviada caso não tenha money
      Money: '&cVocê precisa ter 10 coins.'
      # Será enviada caso não tenha tempo sucifiente
      Tempo: '&cVocê precisa ter jogador por 10 segundos.'
      # Deixe Chat: '' para não usar
      Chat: |
        '&bVocê ativou uma &5Pedra misteriosa&b, descubra seu segredo!'
      # Deixe Actionbar: '' para não usar
      Actionbar: '&bObrigado por ativar-me.'
      # Deixe Title: '' para não usar
      Title: '&5Pedra Misteriosa<nl>&bAtivada!'
    # Quantia máxima de comandos que o item pode dar
    # Deixe 0 para rodar toda a lista
    max-commands: 0
    # Quantia mínima de comandos que o item pode dar
    # Deixe 0 para não ter mínimo
    min-commands: 0
    # Comandos a serem executados ao ativar o item
    # Chance, comando
    Comandos:
      - '10,alerta O jogador {player} ganhou uma pedra'
      - '100,give {player} stone 64'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/13-yItemComandos">Site do plugin yItemComandos</a>
    </category>
</seealso>