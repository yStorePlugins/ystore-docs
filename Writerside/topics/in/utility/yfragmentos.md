# yFragmentos
<secondary-label ref="utility"/>

### Descrição
Crie múltiplos fragmentos, com diferentes meios de recebê-los, contando com uma loja para vender itens e comandos por meio deles.

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
<video src="//www.youtube.com/watch?v=GsjVFikKmB8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/fragmentos - Abrir o menu da loja.
/fragmentos give - Dar x fragmentos de x tipo para x jogador.
/fragmentos reload - Recarregar as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yfragmentos.usar - Permissão para o /fragmentos
yfragmentos.give - Permissão para o /fragmentos give
yfragmentos.reload - Permissão para o /fragmentos reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yFragmentos/
    ├── categorias/
    │    └── padrao.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="categorias" collapsible="true">
<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Tamanho: 27 #tamanho do inventário
Nome: '&7Fragmentos loja padrão' #nome do inventário
Backslot: 9
#
Comando: '' #deixe '' para não usar
Permissao: ''
#
Icone:
    Slot: 10
    CustomSkull: false
    URL: ''
    Name: '&cCategoria das pedras'
    ID: 1
    Data: 0
    Lore:
    - '&7Clique para abrir.'
#
Items:
   Item1:
       Slot: 10
       Preco:
        - 'Fragmento1:32'
        - 'Fragmento2:10'
       Money: 0
       Item:
          CustomSkull: false
          URL: ''
          Name: '&cPedra preciosa'
          ID: 1
          Data: 0
          Amount: 64
          Lore:
          - ''
          - '&fCusto: &e32x &aFragmento de Rocha'
          - '&fCusto: &e10x &aFragmento de Terra'
          - ''
          Lore normal:
          - ''
          - '&fEssa pedra é preciosa'
          - ''
          Enchants:
          - 'DIG_SPEED:1'
          Use command: false
          Commands:
          - ''
   Item2:
       Slot: 12
       Preco:
        - 'Fragmento1:64'
       Money: 0
       Item:
          CustomSkull: false
          URL: ''
          Name: '&cSay'
          ID: 1
          Data: 0
          Amount: 64
          Lore:
          - ''
          Lore normal:
          - ''
          - '&fEssa pedra é preciosa'
          - ''
          Enchants:
          - ''
          Use command: true
          Commands:
          - 'say {player} e bonito'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Comando:
  Comando: 'fragmentos'
  Aliases: []

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Ativar o sistema de loja
Loja ativar: true

# Abrir a loja ao clicar com botão direito no fragmento
Loja interagir: true

# Dropar os fragmentos no chão ao conseguí-los
Dropar: false

# Habilitar a compra com o botão esquerdo
CompraEsquerdo: true

# Habilitar a compra com o botão direito
CompraDireito: true

# Habilitar o drop de fragmentos em bosses
Bosses: false

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para fazer isto.'
  Nao encontrado: '&cJogador não encontrado'
  Nao e numero: '&cO argumento não é um número.'
  Deu: '&aVocê deu &ex{quantia} &afragmento&e {fragmento}&a para o jogador &e{player}'
  Inv cheio: '&cVocê está com o inventário cheio.'
  Suficiente: '&cVocê não possui fragmentos suficiente.'
  Comprou: '&aVocê adquiriu coisas na loja de fragmentos.'
  Recebeu: '&aVocê recebeu &7{quantia} &ade fragmentos.' #deixe '' para não usar
  Money: '&cVocê não possui &f{money} &ccoins.'

# Blacklist de mundos
World blacklist:
  - 'nenhum'

# Coloque as regiões que o plugin vai funcionar
Whitelist:
  Ativar: false
  Lista:
    - 'mina'

Voltar:
  CustomSkull: false #se colocar true, coloque o URL
  URL: ''
  ID: 262
  Data: 0
  Glow: false
  Name: '&cVoltar'
  Lore:
    - ''
    - '&eClique para voltar.'
    - ''

Loja:
  Tamanho: 27
  Nome: '&aCategorias da loja'

# Tipos: MATAR, QUEBRAR, MCMMO (upar nível)
Fragmentos:
  Fragmento1:
    Metodos:
      Metodo1:
        Tipo: 'MATAR'
        Ativar especifico: false
        Especifico:
          - 'none'
        Chance: 50.0
        Quantia: 1
      Metodo2:
        Tipo: 'QUEBRAR'
        Ativar especifico: true
        Especifico:
          - 'STONE'
        Chance: 50.0
        Quantia: 1
      Metodo3:
        Tipo: 'MATAR'
        Ativar especifico: true
        Especifico:
          - 'PLAYER'
        Chance: 20.0
        Quantia: 1
    Mensagens:
      Chat:
        Ativar: true
        Mensagem: '&aVocê encontrou &e{quantia} &afragmentos de rocha.'
      Actionbar:
        Ativar: true
        Mensagem: '&aVocê encontrou &e{quantia} &afragmentos de rocha.'
      Title:
        Ativar: true
        Title: '&aVocê encontrou &e{quantia} &afragmentos de rocha.'
    Item:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/36d1fabdf3e342671bd9f95f687fe263f439ddc2f1c9ea8ff15b13f1e7e48b9'
      ID: 0
      Data: 0
      Glow: false
      Name: '&aFragmento de Rocha'
      Lore:
        - ''
        - '&eUse este fragmento na loja: /fragmentos'
        - ''
  Fragmento2:
    Metodos:
      Metodo1:
        Tipo: 'MATAR'
        Ativar especifico: false
        Especifico:
          - 'none'
        Chance: 20.0
        Quantia: 1
      Metodo2:
        Tipo: 'QUEBRAR'
        Ativar especifico: true
        Especifico:
          - 'STONE'
        Chance: 20.0
        Quantia: 1
      Metodo3:
        Tipo: 'MATAR'
        Ativar especifico: true
        Especifico:
          - 'PLAYER'
        Chance: 50.0
        Quantia: 1
    Mensagens:
      Chat:
        Ativar: true
        Mensagem: '&aVocê encontrou &e{quantia} &afragmentos de terra.'
      Actionbar:
        Ativar: true
        Mensagem: '&aVocê encontrou &e{quantia} &afragmentos de terra.'
      Title:
        Ativar: true
        Title: '&aVocê encontrou &e{quantia} &afragmentos de terra.'
    Item:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/6036bf97926c02a6da524bf487db5b9742d5bc5884aa2faf94e576fc869'
      ID: 0
      Data: 0
      Glow: false
      Name: '&aFragmento de Terra'
      Lore:
        - ''
        - '&eUse este fragmento na loja: /fragmentos'
        - ''

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
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/25-yFragmentos">Site do plugin yFragmentos</a>
    </category>
</seealso>