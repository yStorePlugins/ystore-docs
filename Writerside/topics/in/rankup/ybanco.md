# yBanco
<secondary-label ref="rankup"/>

### Descrição
Jogadores agora podem guardar seu dinheiro em um banco, rendendo de acordo com a selic e, com limite de saque e criação de cheques diário.

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
<video src="//www.youtube.com/watch?v=OGYqM5AHUWc"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/banco - Abrir o menu do banco
/banco [player] - Vê o saldo de outro jogador
/banco ajuda - Ver todos os comandos
/banco add - Adiciona dinheiro ao banco de um jogador
/banco set - Seta dinheiro ao banco de um jogador
/banco remove - Remove dinheiro do banco de um jogador
/banco setnpc - Setar o npc do banco
/banco delnpc - Deletar o npc do banco
/banco reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ybanco.usar - Permissão para o /banco
ybanco.look - Permissão para o /banco [player]
ybanco.add - Permissão para o /banco add
ybanco.set - Permissão para o /banco set
ybanco.remove - Permissão para o /banco remove
ybanco.help - Permissão para o /banco ajuda
ybanco.admin - Permissão para o /banco setnpc e /banco delnpc</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ybanco_raw% - Retorna o money do banco do jogador sem formatação ( 100000 ).
%ybanco_formatted% - Retorna o money do banco do jogador com formatação ( 100K ).
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{ybanco} - Retorna a tag rico para o Top 1 do banco.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yBanco/
    ├── menus/
    │    ├── historico.yml
    │    ├── operacoes.yml
    │    ├── principal.yml
    │    └── top.yml
    ├── config.yml
    ├── morrer.yml
    └── taxa.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="historico.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Histórico de operações'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
VoltarSlot: 27
ProximoSlot: 35

Adicionar:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
   - ''
   - '&7Data: &f{data} &8- &f{hora}&7.'
   - '&7Quantia adicionada: &a{money}&.'
   - ''
   
Render:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
   - ''
   - '&7Data: &f{data} &8- &f{hora}&7.'
   - '&7Rendeu: &a{money}&.'
   - ''
   
Sacar:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
   - ''
   - '&7Data: &f{data} &8- &f{hora}&7.'
   - '&7Quantia sacada: &a{money}&.'
   - '&7Taxa: &c{taxa}%&7.'
   - ''
   
Cheque:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
   - ''
   - '&7Data: &f{data} &8- &f{hora}&7.'
   - '&7Cheque criado: &a{money}&.'
   - '&7Taxa: &c{taxa}%&7.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="operacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Banco operações'
Tamanho: 27
Backslot: 18
Itens:
   Saque:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aSacar'
      Lore:
      - '&7Clique para realizar um saque.'
      - '&7Limite diário usado: &c{sacou}&7/&a{pode}&7.'
   Deposito:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/2c9e601ed9198dbb34c51ddf323929f01a5f958ab11133e3e0407b698393b3f'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aDepositar'
      Lore:
      - '&7Clique para realizar um depósito.'
   Cheque:
      Slot: 15
      CustomSkull: false
      URL: ''
      ID: 339
      Data: 0
      Glow: true
      Name: '&aCheques'
      Lore:
      - '&7Clique para criar um cheque.'
      - '&7Limite diário usado: &c{criou}&7/&a{pode}&7.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Cheque:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Banco principal'
Tamanho: 27
Itens:
   Perfil:
      Slot: 11
      CustomSkull: true
      URL: '{player}'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aSuas informações'
      Lore:
      - ''
      - '&7Dinheiro no banco: &a{banco}&7.'
      - '&7Dinheiro em mãos: &a{money_player}&7.'
      - ''
      - '&7Selic atual: &b{selic}%&7.'
      - ''
   Historico:
      Slot: 12
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/97a530f5c5742bf19e175a4d78ad435ac0f4396d3b5464bd6182ab382aca417d'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aHistórico'
      Lore:
      - '&7Clique para ver seu histórico de transações.'
   Operacoes:
      Slot: 14
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aOperações'
      Lore:
      - '&7Clique para realizar um depósito,'
      - '&7saque ou criar um cheque.'
   Top:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/15a7ee9a86de203674a93b570bc8992e500363dd32f2b9813daaeeabccf92151'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aTop'
      Lore:
      - '&7Clique para ver os jogadores mais ricos do banco.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Top:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Banco'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fDinheiro no banco: &6{money}'
   - '&fPosição: &6{pos}'
   - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true

# Configure o comando e as aliases de cada opção
# Comando principal
Comando:
  Comando: 'banco'
  Aliases: [ bank ]

#Coloque Legendchat, OpeNChat (ou nChat), UltimateChat, NoxusChat ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'

# Tag do top banco
Tag: '&6[RICO]'

# Npc e holograma do banco
NPC:
  Skin: 'deliveryman'
  Altura: 3.1
  Holograma:
    - '&6&lBanco'
    - '&7Clique para abrir o banco.'
  Mensagens:
    Setado: '&a&lSUCESSO! &aNPC do banco setado com sucesso.'
    Removido: '&a&lSUCESSO! &aNPC do banco removido com sucesso.'
    Nao removido: '&c&lERRO! &aNPC do banco não está setado.'

# Mundos em que poderá morrer sem perder % do money.
# Tipo: BLACKLIST
Morrer blacklist:
  - 'Plot'

# Limites para saque e criação de cheques
Limites:
  Saque: 10
  Cheque: 10
  Resetar com: 60 # Em segundos

# Minimos para depositar, sacar e criar um cheque
Minimos:
  Saque: 2000.0
  Cheque: 2000.0
  Deposito: 1000.0

# Ativar o sistema de perder x % do money em mãos ao morrer.
# Porcentagens configuráveis na morrer.yml.
Perder ao morrer: true

# Quando o jogador realizar uma operação: depósito, saque ou criação de cheque, já salvar na database
Auto salvar: false

# Máximo de dinheiro que poderá render no banco
# deixe 0 para infinito
Render max: 0

# O dinheiro do banco dos jogadores irá render de acordo esta taxa
Selic:
  Ativar: true
  Valor: 1.8
  # segunda, terca, quarta, quinta, sexta, sabado, domingo, todos
  # dia-hora:minuto:segundo
  Horarios:
    - 'todos-9:00:00'
    - 'todos-9:11:00'

# O dinheiro do banco irá render de acordo a bolsa do yBolsa
Bolsa:
  Ativar: true
  Tempo: 30 # em segundos

# Item do cheque
Cheque:
  CustomSkull: false
  URL: ''
  ID: 339
  Data: 0
  Glow: true
  Name: '&aCheque de dinheiro'
  Lore:
    - ''
    - '&7Criado por: &a{player}&7.'
    - '&7Criado em: &f{data} &8- &f{hora}&7.'
    - ''
    - '&bValor do cheque: &a{money}&b.'
    - ''
    - '&7Clique com botão direito para ativar'

# Mensagens do plugin
Mensagens:
  Permissao: '&c&lERRO! &cVocê não tem permissão para fazer isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Nao e numero: '&cO argumento não é um número.'
  Nao possui player: '&cVocê não possui a quantia &7{quantia}&c em mãos.'
  Nao possui banco: '&cVocê não possui a quantia &7{quantia}&c no banco.'
  Menor minimo: '&cEsta operação requer um mínimo de &7{quantia}&c.'
  Depositou: '&aVocê depositou &7{quantia}&a com sucesso.'
  Sacou taxa: '&aVocê sacou &7{quantia}&a com sucesso. &7Taxa: &8{taxa}%&7.'
  Sacou: '&aVocê sacou &7{quantia}&a com sucesso.'
  Criou taxa: '&aVocê criou um cheque de &7{quantia}&a com sucesso. &7Taxa: &8{taxa}%&7.'
  Criou: '&aVocê criou um cheque de &7{quantia}&a com sucesso.'
  Aguarde: '&cVocê atingiu seu limite diário desta operação, aguarde &7{tempo}&c para realizar essa operação novamente.'
  Inv cheio: '&cSeu inventário está cheio.'
  Ativou: '&aVocê ativou um cheque de &7{quantia}&a.'
  Jogador: '&cJogador {player} não encontrado.'
  Alterado: '&aDinheiro do banco do jogador &f{player} &aalterado para &f{money}&a.'
  Saldo player: '&aDinheiro que o jogador &f{player}&a possui no banco: &2R$ &f{money}&a.'
  Rendeu:
    - ''
    - '&aSeu dinheiro no banco rendeu!'
    - '&7Montante antigo: &c{antigo}&7.'
    - '&7Montate atual: &a{atual}&7.'
    - ''
    - '&bValor da selic: &7{selic}%&b.'
    - ''
  Depositar:
    - ''
    - '&aDigite no chat a quantia que quer depositar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Sacar:
    - ''
    - '&aDigite no chat a quantia que quer sacar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Sacar taxa:
    - ''
    - '&aDigite no chat a quantia que quer sacar.'
    - '&cVocê está pagando uma taxa de &7{taxa}%&c.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Cheque:
    - ''
    - '&aDigite no chat a quantia que quer criar um cheque.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Cheque taxa:
    - ''
    - '&aDigite no chat a quantia que quer criar um cheque.'
    - '&cVocê está pagando uma taxa de &7{taxa}%&c.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Rendeu bolsa:
    - ''
    - '&aSeu dinheiro no banco rendeu!'
    - '&7Montante antigo: &c{antigo}&7.'
    - '&7Montate atual: &a{atual}&7.'
    - ''
    - '&bValor da bolsa: &7{bolsa}%&b.'
    - ''

# As setas dos menus
Setas:
  # Voltar ao menu anterior
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
  # Voltar a página anterior
  Anterior:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar à página anterior.'
  # Ir para a próxima página
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'
]]>
</code-block>
</chapter>

<chapter title="morrer.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Quando o jogador morrer, ele irá perder essa porcentagem de money
# O money do banco não é afetado
Grupos:
 membro:
  Permissao: 'ybanco.membro'
  Porcentagem: 10.0
  Mensagem:
  - ''
  - '&cVocê morreu e perdeu 10% de todo seu money em mãos.'
  - '&fMontante antigo: &7{antigo}&f.'
  - '&fMontante atual: &7{atual}&f.'
  - ''
  
]]>
</code-block>
</chapter>

<chapter title="taxa.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Taxa que acrescenta o valor para sacar e criar cheques
Grupos:
  membro:
    Ordem: 1
    Permissao: 'ybanco.membro'
    Porcentagem: 10.0
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/16-yBanco">Site do plugin yBanco</a>
    </category>
</seealso>