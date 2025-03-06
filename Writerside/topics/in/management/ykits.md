# yKits
<secondary-label ref="management"/>

### Descrição
Crie kits e categorias e edite-as in-game

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
<video src="//www.youtube.com/watch?v=mItYRvYtm0M"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/kit - Abre o menu de kits
/kit [player] [kit] - Dá kit à um jogador
/tempokit [kit] [player] - Vê o delay do kit para o jogador
/kit reload - Recarrega as configurações
/editarkit - Edita um kit
/criarkit - Cria um kit
/delkit - Deleta um kit
/verkit - Vê os itens de um kit
/kitcategoria - Mostra todos os comandos de gerenciamento de categorias
/kitcategoria criar - Cria uma categoria
/kitcategoria editar - Edita uma categoria
/kitcategoria deletar - Deleta uma categoria
/kitcategoria lista- Vê todas as categorias
/resetkitdelay - Reseta o delay de um kit para um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ykits.admin - Permissão para ser reconhecido como admin
ykits.tempokit - Permissão para o /tempokit
ykits.createkit - Permissão para o /criarkit
ykits.delkit - Permissão para o /delkit
ykits.editkit - Permissão para o /editkit
ykits.verkit - Permissão para o /verkit
ykits.kitcategoria - Permissão para o /kitcategoria
ykits.kitcategoria.criar - Permissão para o /kitcategoria criar
ykits.kitcategoria.editar - Permissão para o /kitcategoria editar
ykits.kitcategoria.deletar - Permissão para o /kitcategoria deletar
ykits.resetkitdelay - Permissão para o /resetkitdelay
ykits.kit.bypass - Permissão para não ter delay para pegar kits
ykits.kits.* - Permissão para pegar todos os kits</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ykits_kitcooldown_[kit]% - Retorna o cooldown do kit do jogador
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yKits/
    ├── menus/
    │    ├── preview.yml
    │    ├── principal.yml
    │    └── verkit.yml
    ├── commands.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '{kit}'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
AnteriorSlot: 18
ProximoSlot: 26
BackSlot: 45
ArmorSlots: [ 47, 48, 49, 50 ]
Itens:
  Coletar:
    Slot: 53
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    ID: AIR
    Data: 0
    Glow: false
    Name: '&aColetar'
    Lore:
      - '&7Clique para coletar os itens deste kit.'
  # Você pode adicionar enfeites, apenas adicionando itens iguais o Coletar e mudando os dados.
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Kits'
Tamanho: 27
Itens: {}
#  Enfeite:
#    Slot: 0
#    CustomSkull: false
#    URL: ''
#    ID: AIR
#    Data: 0
#    Glow: false
#    Name: '&aEnfeite'
#    Lore: []
]]>
</code-block>
</chapter>

<chapter title="verkit.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '{kit}'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
AnteriorSlot: 18
ProximoSlot: 26
ArmorSlots: [ 47, 48, 49, 50 ]
Itens:
  Coletar:
    Slot: 52
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    ID: AIR
    Data: 0
    Glow: false
    Name: '&aColetar'
    Lore:
      - '&7Clique para coletar os itens deste kit.'
  # Você pode adicionar enfeites, apenas adicionando itens iguais o Coletar e mudando os dados.
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
  kit: 'kit|kits'
  see-kit: 'verkit|seekit|kitver|kitsee'
  time-kit: 'tempokit|timekit'
  create-kit: 'createkit|criarkit|kitcriar|kitcreate'
  del-kit: 'delkit|deletarkit|kitdeletar|kitdel'
  edit-kit: 'editkit|editarkit|kiteditar|kitedit'
  kit-category: 'kitcategoria|categoriakit'
  reset-kit-delay: 'resetkitdelay|resetkitcooldown'
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
  Tabela: 'ykits.players'
  Debug: true

# Opções gerais do plugin
Opcoes:
  # Ativar o menu ao digitar /kit
  Menu: true
  # Verificar se o inventário está cheio antes de pegar o kit
  Kit cheio: true
  # Só pegar o kit se estiver vinculado (yDiscordHook)
  Vinculado: false
  # Lore para quando o jogador precisar aguardar para pegar o kit novamente
  Lore aguardar:
    # Substituir a lore do kit
    Sobrepor: true
    Lore:
      - ''
      - '&cVocê deve aguardar &f{tempo} &cpara pegar'
      - '&ceste kit novamente.'
      - ''
  # Sistema de lore do jogador no kit
  Item Lore:
    Ativar: false
    Lore: [ '', '&eKit de &a{player}' ]

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Jogador: '&cEste jogador {player} não foi encontrado.'
  Existe: '&cJá existe um kit com esse nome.'
  Nao existe: |
    &cNão foi possível localizar esse kit.
    &cDisponíveis: &7{kits}&c.
  Criado: '&aKit &f{kit}&a criado com sucesso.'
  Deletado: '&aKit &f{kit}&a deletado com sucesso.'
  Numero: '&cO argumento não é um número.'
  Mudou nome: '&aVocê alterou o nome do kit para &e{nome}&a.'
  Mudou delay: '&aVocê alterou o tempo de reset do kit &f{kit}&a para &f{delay}&a.'
  Mudou permissao: '&aVocê alterou a permissao do kit &f{kit}&a para {permissao}.'
  Cancelou: '&cOperação cancelada.'
  Item nao: '&cO item não pode ser nulo.'
  Icone mudou: '&aÍcone do kit &f{kit}&a alterado com sucesso.'
  Icone mudou categoria: '&aÍcone da categoria &f{categoria}&a alterado com sucesso.'
  Itens mudou: '&aNovos itens do kit &f{kit}&a itens salvos com sucesso.'
  Recebeu: '&aVocê recebeu o kit {kit}&a com sucesso.'
  Cheio: '&cSeu inventário está cheio, alguns itens foram dropados no chão.'
  Permissao dar: '&cVocê não tem permissão para dar o kit {kit}&a.'
  Permissao pegar: '&cVocê não tem permissão para pegar o kit {kit}&a.'
  Dado: '&aKit {kit}&a dado ao jogador {player}.'
  Aguardar: '&cVocê deve aguardar &e{tempo}&c para pegar o kit {kit}&a novamente.'
  Existe categoria: '&cJá existe uma categoria com esse nome.'
  Nao existe categoria: '&cNão foi possível localizar essa categoria.'
  Criado categoria: '&aCategoria &f{categoria}&a criada com sucesso.'
  Deletado categoria: '&aCategoria &f{categoria}&a deletada com sucesso.'
  Categorias: '&cCategorias disponíveis: &f{categorias}&c.'
  Mudou nome categoria: '&aVocê alterou o nome da categoria para &e{nome}&a.'
  Mudou comando: '&aVocê alterou o comando da categoria para &e{comando}&a.'
  Slot maior: '&aO slot não pode ser maior que 53.'
  Mudou slot: '&aVocê alterou o slot para &e{slot}&a.'
  Mudou backslot: '&aVocê alterou o backslot da categoria para &e{slot}&a.'
  Tamanho: '&cO tamanho deve ser maior ou igual a 9, ou múltiplo de 9.'
  Mudou tamanho: '&aVocê alterou o tamanho da categoria para &e{tamanho}&a.'
  Cheio cancelado: '&cSeu inventário está cheio, esvazie-o antes de pegar o kit.'
  Vinculado: '&cVocê precisa vincular seu discord primeiro. /discord para vincular.'
  Delay resetado: '&aDelay do kit &f{kit} &aresetado para {player}.'
  Time player: '&cO jogador &f{player}&c ainda precisa aguardar &f{tempo}&c.'
  CategoriaHelp: |
    &cComandos disponíveis:
    &c-> /kitcategoria criar <categoria>
    &c-> /kitcategoria deletar <categoria>
    &c-> /kitcategoria editar <categoria>
    &c-> /kitcategoria lista
  Digite nome:
    - ''
    - '&aDigite o nome para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite delay:
    - ''
    - '&aDigite o delay (em seg) para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite permissao:
    - ''
    - '&aDigite a permissão para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite comando:
    - ''
    - '&aDigite o comando para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite slot:
    - ''
    - '&aDigite o slot para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite tamanho:
    - ''
    - '&aDigite o tamanho para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''

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
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/83-yKits">Site do plugin yKits</a>
    </category>
</seealso>