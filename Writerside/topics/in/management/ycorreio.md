# yCorreio
<secondary-label ref="management"/>

### Descrição
Envie itens entre jogadores e dê recompensas dentro de eventos!

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
<video src="//www.youtube.com/watch?v=_wIU7Hv1U78"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/correio - Abre o menu principal
/correio ajuda - Envia a mensagem de ajuda
/correio enviar [player] - Envia itens à um jogador.
/correio enviartodos - Envia itens à todos os jogadores online.
/correio enviargrupo [grupo] - Envia itens à todos os jogadores online de um grupo.
/correio give [player] [categoria] [recompensa] [quantia] - Dá x recompensa(s) configurada à um jogador.
/correio giveall [categoria] [recompensa] [quantia] - Dá x recompensa(s) configurada à todos os jogadores online.
/correio givegrupo [grupo] [categoria] [recompensa] [quantia] - Dá x recompensa(s) configurada à todos os jogadores online de um grupo.
/correio recompensas - Vê a lista de recompensas configuradas.
/correio grupos - Vê a lista de grupos configurados.
/correio categorias - Vê a lista de categorias configuradas.
/correio setnpc - Seta o NPC do correio.
/correio delnpc - Deleta o NPC do correio.
/correio reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycorreio.usar - Permissão para o /correio
ycorreio.enviar - Permissão para o /correio enviar
ycorreio.admin - Permissão para ser reconhecido como admin
ycorreio.enviartodos - Permissão para o /correio enviartodos
ycorreio.enviargrupo - Permissão para o /correio enviargrupo
ycorreio.give - Permissão para o /correio give
ycorreio.giveall - Permissão para o /correio giveall
ycorreio.givegrupo - Permissão para o /correio givegrupo
ycorreio.recompensas - Permissão para o /correio recompensas
ycorreio.grupos - Permissão para o /correio grupos
ycorreio.categorias - Permissão para o /correio categorias
ycorreio.setnpc - Permissão para o /correio setnpc
ycorreio.delnpc - Permissão para o /correio delnpc
ycorreio.reload - Permissão para o /correio reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ycorreio_encomendas% - Retorna a quantia de encomendas que o jogador tem (formatado)
%ycorreio_recompensas% - Retorna a quantia de recompensas que o jogador tem (formatado)
%ycorreio_total% - Retorna a quantia de encomendas mais recompensas que o jogador tem (formatado)
%ycorreio_encomendas_raw% - Retorna a quantia de encomendas que o jogador tem (sem formatar)
%ycorreio_recompensas_raw% - Retorna a quantia de encomendas que o jogador tem (sem formatar)
%ycorreio_total_raw% - Retorna a quantia de encomendas que o jogador tem (sem formatar)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCorreio/
    ├── menus/
    │    ├── enviar.yml
    │    └── principal.yml
    ├── categorias.yml
    ├── config.yml
    ├── data.yml
    ├── grupos.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="enviar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Itens'
Tamanho: 45
# Item de confirmar
Confirmar:
  Slot: 40
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: AIR
  Data: 0
  Glow: true
  Name: '&aConfirmar'
  Lore:
    - '&7Clique para confirmar e enviar.'
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Seu correio'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34]
VoltarSlot: 18
ProximoSlot: 26

# Item do perfil
Perfil:
  Slot: 46
  CustomSkull: true
  URL: '{player}'
  ID: AIR
  Data: 0
  Glow: true
  Name: '&eSuas informações'
  Lore:
    - ''
    - '&f Seu grupo: &a{grupo}&f.'
    - ''
    - '&f Recompensas armazenadas: &a{recompensas}&f.'
    - '&f Encomendas armazenadas: &a{entregas}&f.'
    - ''

# Item para recolher todas as recompensas
Recolher todos:
  Slot: 48
  CustomSkull: false
  URL: ''
  ID: HOPPER_MINECART
  Data: 0
  Glow: true
  Name: '&6Recolher todos'
  Lore:
    - '&7Clique para recolher'
    - '&7todos os armazenados'
    - '&7nesta categoria.'

# Item para enviar encomenda à um jogador
Enviar:
  Slot: 52
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: AIR
  Data: 0
  Glow: true
  Name: '&aEnviar'
  Lore:
    - '&7Clique para enviar encomenda'
    - '&7para um jogador.'

# Seletor da categoria
Seletor:
  Slot: 50
  CustomSkull: false
  URL: ''
  ID: HOPPER
  Data: 0
  Name: '&aSeletor de Categorias'

# Seletor da categoria
Empty:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: BARRIER
  Data: 0
  Name: '&cVazio'
  Lore: []

# Tipos do seletor
Tipos:
  Encomenda:
    Nome: 'Encomendas'

# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome} [{quantia}]'
  Selecionar: ' &f• &7{nome} [{quantia}]'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="categorias.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Categorias:
  cat1:
    Ordem: 1
    Nome: 'Recompensas'
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
  Correio:
    Comando: 'correio'
    Aliases: [ correios, encomendas, courier ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Opcoes de configuração do NPC
NPC:
  ID: 923292
  Skin: 'ySpeed_'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Correio'
      - '&7Clique para gerenciar suas encomendas.'

# Opções gerais do plugin
Opcoes:
  NPC-Name-Hide: false
  # Mundos onde não pode coletar encomendas/recompensas
  World blacklist:
    - 'none'
  # Enviar aviso de recompensas/encomendas no correio ao logar
  Logar mensagem: true
  # Limite de encomendas no correio
  Limite encomenda: 40
  # Ativar o sistema de encomendas
  Encomendas ativar: true
  # Delay para carregar os dados depois do login
  # Necessário para usar em servidor de mina separado
  # Recomendado: 20 ticks
  Login delay: 20
  # Ativar o botão Q para deletar as recompensas
  UsarQ: true

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Setado npc: '&aNPC do correio setado com sucesso.'
  Removido npc: '&aNPC do correio removido com sucesso'
  Nao setado npc: '&cO NPC não está setado.'
  Cancelou: '&cVocê cancelou a operação'
  Nao encontrado: '&cEste jogador não foi encontrado.'
  Enviou: '&aVocê enviou &f{quantia}x &aitens para o jogador &f{player}&a.'
  Recebeu: '&aVocê recebeu &f{quantia}x &aitens do jogador &f{player}&a. Acesse &f/correio&a para recolher.'
  Enviou todos: '&aVocê enviou &f{quantia}x &aitens para todos os jogadores online.'
  Enviou grupo: '&aVocê enviou &f{quantia}x &aitens para todos os jogadores do grupo &f{grupo}&a.'
  Recebeu todos: '&aTodos os jogadores receberam &f{quantia}x &aitens no /correio.'
  Recebeu grupo: '&aTodos os jogadores do grupo &f{grupo}&a receberam &f{quantia}x &aitens no /correio.'
  Fechar: '&cNão é possível fechar este inventário sem recolher os itens.'
  Inserir: '&cVocê deve inserir itens no menu.'
  Si mesmo: '&cVocê não pode realizar esta operação em si mesmo.'
  Deletado: '&cItem deletado com sucesso.'
  Deletado recompensa: '&cRecompensa deletada com sucesso.'
  InvCheio: '&cSeu inventário está cheio.'
  Recolheu encomenda: '&aVocê recolheu &f{quantia}x &aencomendas com sucesso.'
  Recolheu recompensa: '&aVocê recolheu &f{quantia}x &arecompensas da categoria &f{categoria}&a com sucesso.'
  Mundo: '&cVocê não pode coletar neste mundo.'
  Recompensas: '&aLista de recompensas disponíveis: &f{lista}&a.'
  Grupos: '&aLista de grupos disponíveis: &f{lista}&a.'
  Categorias: '&aLista de categorias disponíveis: &f{lista}&a.'
  Nao encontrado grupo: '&cEste grupo não existe. Disponíveis: &7{grupos}&c.'
  Nao encontrado categoria: '&cEsta categoria não existe. Disponíveis: &7{categorias}&c.'
  Nao encontrado recompensa: '&cEsta grupo recompensa existe. Disponíveis: &7{recompensas}&c.'
  Give player: '&aVocê deu &f{quantia}x &f{recompensa}&a na categoria &f{categoria}&a para o jogador &f{player}&a.'
  Give todos: '&aVocê deu &f{quantia}x &f{recompensa}&a na categoria &f{categoria}&a para todos os jogadores online.'
  Give grupo: '&aVocê deu &f{quantia}x &f{recompensa}&a na categoria &f{categoria}&a para todos os jogadores do grupo &f{grupo}&a.'
  Recebeu player: '&aVocê recebeu &f{quantia}x &f{recompensa}&a na categoria &f{categoria}&a.'
  Recebeu player actionbar: '&a+ &f{quantia}x &f{recompensa}&a na categoria &f{categoria}&a.'
  Numero: '&cO argumento não é um número.'
  Limite encomenda: '&cEste jogador atingiu o limite de 40 encomendas.'
  Nenhuma: '&cNenhuma categoria foi configurada.'
  Encomenda desativado: '&cO sistema de encomendas foi desativado.'
  Digite:
    - ''
    - '&aDigite o nome do jogador que deseja enviar itens.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Possui encomenda:
    - ''
    - '&aVocê possui &f{encomendas}&a encomenda(s) no seu /correio.'
    - ''
  Possui recompensa:
    - ''
    - '&aVocê possui &f{recompensas}&a recompensa(s) no seu /correio.'
    - ''
  Possui recompensa encomenda:
    - ''
    - '&aVocê possui &f{encomendas} encomenda(s)&a e &f{recompensas} recompensa(s)&a no seu /correio.'
    - ''
  Help:
    - '&aComandos disponíveis:'
    - ''
    - '&f > &a/correio &8- &7Abre o menu principal'
    - '&f > &a/correio ajuda &8- &7Envia esta mensagem'
    - '&f > &a/correio enviar [player] &8- &7Envia itens à um jogador.'
    - ''
  Help admin:
    - '&aComandos disponíveis:'
    - ''
    - '&f > &a/correio &8- &7Abre o menu principal'
    - '&f > &a/correio ajuda &8- &7Envia esta mensagem'
    - '&f > &a/correio enviar [player] &8- &7Envia itens à um jogador.'
    - '&f > &a/correio enviartodos &8- &7Envia itens à todos os jogadores online.'
    - '&f > &a/correio enviargrupo [grupo] &8- &7Envia itens à todos os jogadores online de um grupo.'
    - '&f > &a/correio give [player] [categoria] [recompensa] [quantia] &8- &7Dá x recompensa(s) configurada à um jogador.'
    - '&f > &a/correio giveall [categoria] [recompensa] [quantia] &8- &7Dá x recompensa(s) configurada à todos os jogadores online.'
    - '&f > &a/correio givegrupo [grupo] [categoria] [recompensa] [quantia] &8- &7Dá x recompensa(s) configurada à todos os jogadores online de um grupo.'
    - '&f > &a/correio recompensas &8- &7Vê a lista de recompensas configuradas.'
    - '&f > &a/correio grupos &8- &7Vê a lista de grupos configurados.'
    - '&f > &a/correio categorias &8- &7Vê a lista de categorias configuradas.'
    - '&f > &a/correio setnpc &8- &7Seta o NPC do correio.'
    - '&f > &a/correio delnpc &8- &7Deleta o NPC do correio.'
    - ''

# Lores de sobreposição
Lores:
  Principal:
    Ativar: true
    Lore:
      - ''
      - '&aBotão esquerdo para coletar'
      - '&aBotão Q para deletar'
  Recompensa:
    Ativar: true
    Lore:
      - ''
      - '&fQuantia: &b{quantia}&f.'
      - ''
      - '&aBotão ESQUERDO para coletar'
      - '&aBotão Q para deletar'
      - '&aBotão SHIFT+ESQUERDO para coletar todos'

# Setas dos menus
Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
  Anterior:
    CustomSkull: false
    URL: ''
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'

# Formatos de quantia
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

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Npc local: 'none'

Data: {}
]]>
</code-block>
</chapter>

<chapter title="grupos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Grupos:
  gp1:
    Ordem: 1
    Permissao: 'ycorreio.membro'
    Display: '&7[Membro]'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Nome que aparecerá nas mensagens
    Nome: '&6Pedra mística'
    # Item que aparecerá no preview do menu.
    Preview:
      CustomSkull: false
      URL: ''
      ID: STONE
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
      ID: STONE
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
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: false
      # Ativando essa opção ele vai executar o comando apenas 1x
      # e vai dar a quantia usando a placeholder {quantia}
      UsarQuantia: true
      # Limitar a quantia de recolher para o disponível no inventário
      LimiteInv: false
      # quantia padrão da placeholder {quantia} no comando (valor base)
      placeholder-amount: 1
      List:
        - 'give {player} stone {quantia}'

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/81-yCorreio">Site do plugin yCorreio</a>
    </category>
</seealso>