# yEconomy
<secondary-label ref="management"/>

### Descrição
Gerencie a economia do seu servidor de uma forma simples e eficaz.

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
<video src="//www.youtube.com/watch?v=Pb0N5YV7HOw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/money - Abre o menu principal ou envia a quantia de money do jogador no chat.
/money [player] - Ver a quantia de money de outro jogador.
/money transacoes - Ver as transações recentes.
/money transacoes [player] - Ver as transações recentes de outro jogador.
/money enviar - Enviar coins para um jogador.
/money cheque - Criar um cheque.
/money criarcheque - Gerar um cheque para outro jogador
/money adicionar - Adicionar coins para um jogador.
/money remover - Remover coins de um jogador.
/money setar - Setar coins para um jogador.
/money formatar - Formatar ou deformatar uma quantia.
/money toggle - Ativar
/Desativar o recebimento de coins.
/money top - Abre o menu do top.
/money setnpc  - Setar o NPC do TOP.
/money delnpc  - Deletar o NPC do TOP.
/magnata - Mostra o magnata atual.
/cheque - Cria um cheque
/cheque [quantia] [player] - Gerar um cheque para outro jogador
/pay - Enviar coins para um jogador.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yeconomy.usar - Permissão para o /money
yeconomy.outros - Permissão para o /money
yeconomy.enviar - Permissão para o /money enviar e /pay
yeconomy.cheque - Permissão para o /money cheque e /cheque
yeconomy.criarcheque - Permissão para o /money criarcheque e /cheque [quantia] [player]
yeconomy.adicionar - Permissão para o /money adicionar
yeconomy.remover - Permissão para o /money remover
yeconomy.setar - Permissão para o /money setar
yeconomy.formatar - Permissão para o /money formatar
yeconomy.toggle - Permissão para o /money toggle
yeconomy.top - Permissão para o /money top
yeconomy.setnpc - Permissão para o /money setnpc
yeconomy.delnpc - Permissão para o /money delnpc
yeconomy.magnata - Permissão para o /magnata
yeconomy.transactions.others - Permissão para o /money transacoes [player]
yeconomy.death.bypass - Permissão para não perder money ao morrer</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yeconomy_money% - Retorna a quantia de money do jogador formatado.
%yeconomy_money_raw% - Retorna a quantia de money do jogador sem formatar.&nbsp;
%yeconomy_magnata% - Retorna a tag caso o jogador for o magnata.
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{magnata} - Tag do jogador mais rico (magnata)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEconomy/
    ├── menus/
    │    ├── principal.yml
    │    ├── top.yml
    │    ├── transacoes.yml
    │    └── transacoes_player.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Balanço'
Tamanho: 27
Itens:
  Informacoes:
    Slot: 10
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSuas informações'
    Lore:
      - '&7Veja suas informações'
      - '&7referente ao money.'
      - ''
      - ' &fSaldo atual: &a{saldo}&f.'
      - ' &fTransações realizadas: &b{transacoes}&f.'
      - ' &fRecebimento de coins: &r{toggle}&f.'
      - ''
      - '&7Clique para ativar/desativar o'
      - '&7recebimento de coins.'
      - ''
  Transacoes:
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4883d656e49c38c6b5378572f31c63c4c7a5dd4375b6ecbca43f5971c2cc4ff'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTransações'
    Lore:
      - '&7Veja as movimentações que'
      - '&7você realizou.'
      - ''
      - '&aClique para visualizar.'
  Top:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTop jogadores'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacam sendo os'
      - '&7mais ricos do servidor.'
      - ''
      - '&aClique para visualizar.'
  Magnata:
    Slot: 16
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/f809d2e69610f1e6b75fe0d4598e441e560325d2d52d97cf66859c44fa3d8a79'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aMagnata'
    Lore:
      - ''
      - ' &fMagnata atual: &6{player}&f.'
      - ' &fSaldo do magnata: &a{saldo} {unidade}&f.'
      - ''

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Magnata:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Ricos'
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
    - '&fCoins: &a{money}&f.'
    - ''
]]>
</code-block>
</chapter>

<chapter title="transacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Histórico de transações'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
VoltarSlot: 27
ProximoSlot: 35

Adicionou:
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

Recebeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Recebeu de &f{player}&7: &a{money}&.'
      - ''

Removeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Quantia removida: &a{money}&.'
      - ''

Pagou:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Pagou para &f{player}&7: &a{money}&.'
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
      - '&7Cheque criado no valor: &a{money}&.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="transacoes_player.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Transações de {player}'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
VoltarSlot: 27
ProximoSlot: 35

Adicionou:
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

Recebeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Recebeu de &f{player}&7: &a{money}&.'
      - ''

Removeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Quantia removida: &a{money}&.'
      - ''

Pagou:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Pagou para &f{player}&7: &a{money}&.'
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
      - '&7Cheque criado no valor: &a{money}&.'
      - ''
]]>
</code-block>
</chapter>

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
  Avancado:
    CacheMemoryEntries: 150 # Numeros de jogadores que irão fizer armazenados na ram.
    CacheDiskSpace: 1024 # Espaço disponivel (em MB) no disco para armazenar o resto. Sempre coloque um numero muito superior ao necessário para não ter problemas
#Coloque Legendchat, OpeNChat (ou nChat), UltimateChat, NoxusChat ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'
# Comandos e aliases do plugin
Comando:
  Money:
    Comando: 'money'
    Aliases: [ coin, coins, balanço, balanco, balance ]
  Magnata:
    Comando: 'magnata'
    Aliases: [ rico ]
  Pagar:
    Comando: 'pay'
    Aliases: [ pagar, enviar ]
  Cheque:
    Comando: 'cheque'
    Aliases: [ cheques ]
# Opções gerais do plugin
Opcoes:
  # Ativar para funcionar transações com players offline
  Offline: true
  # Formato do money na quantia singular
  Singular: 'coin'
  # Formato do money no plural
  Plural: 'coins'
  # Ao digitar /money abrir o menu.
  # False = Vai enviar a quantia de money que ele tem no chat
  # True = Vai abrir o menu
  Menu money: true
  # Ao ativar irá abrir o menu do top ao digitar /money top
  Top menu: true
  # Quantia de money que o jogador vai começar
  Money inicial: 30.0
  # Tempo que irá atualizar o top
  # Em segundos
  Top atualizar: 600
  # Tag do magnata no chat
  Tag: '&2[$]'
  # Title que será enviado quando houver um
  # novo magnata.
  # Deixe '' para não usar
  Magnata title: '&6{player}<nl>&aé o novo magnata.'
  # Quantidade de casas decimais que irá mostrar nas placeholders (FORMATAÇÃO NUMERO)
  MaxDecimals: 4
# Configurações do Holograma do NPC
Holograma:
  # Altura do holograma em cima do NPC
  Altura: 3.1
  # Holograma do NPC
  Holograma:
    - '&a&lTOP &7&l#{pos}'
    - ''
    - '&e{nome}'
    - '&7Money: &f{money}'
    - ''
# Configuração do money top em chat
Top chat:
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  Magnata formato: '{magnata} '
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  Prefixo formato: '%luckperms_prefix% '
  Tags: '{magnata}{prefixo}'
  Formato: '  &f{pos}º {tags}&7{player}&2: &7($ {money})'
  Mensagem:
    - '&2Top 10 Mais Ricos &7(Atualizado de 10 em 10 minutos)'
    - ''
    - '{formato}'
    - ''
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Nao encontrado: '&cEste jogador não está online.'
  Nao e numero: '&cO argumento não é um número.'
  Nao possui: '&cVocê não possui esta quantia de coins.'
  Si mesmo: '&cVocê não pode pagar à si mesmo.'
  Sem magnata: '&cNão há nenhum magnata no servidor.'
  Nenhum top: '&cNão há nenhum top nesta posição ainda.'
  Setado: '&aNPC setado.'
  Removido: '&aNPC removido.'
  Desativou: '&cEste jogador desativou o recebimento de coins.'
  Ilegal: '&cO argumento contém caracteres ilegais. Use apenas letras e números.'
  Balanco:
    - '&aVocê possui: &f{money}&a {unidade}.'
  Balanco target:
    - '&aO jogador &7{player}&a possui: &f{money}&a {unidade}.'
  Setou:
    - '&aVocê setou o money do jogador &7{player} &apara: &f{money}&a {unidade}.'
  Removeu:
    - '&aVocê removeu &f{money}&a {unidade} do jogador &7{player}&a.'
  Adicionou:
    - '&aVocê adicionou &f{money}&a {unidade} para o jogador &7{player}&a.'
  Enviou:
    - '&aVocê enviou &f{money}&a {unidade} para o jogador &7{player}&a.'
  Ativou:
    - '&aVocê ativou um cheque no valor de &f{money}&a {unidade}&a.'
  Criou:
    - '&aVocê criou um cheque no valor de &f{money}&a {unidade}&a.'
  DeuCheque:
    - '&aVocê criou um cheque no valor de &f{money}&a {unidade}&a para o jogador &f{player}&a.'
  Recebeu:
    - '&aVocê recebeu &f{money}&a {unidade} do jogador &7{player}&a.'
  Toggle ativou:
    - '&aVocê ativou o recebimento de coins.'
  Toggle desativou:
    - '&cVocê desativou o recebimento de coins.'
  Formatado:
    - '&f > &a&n{entrada} &e-> &a&n{saida}&a.'
  Novo magnata:
    - ''
    - '&2&l[$]&a O jogador &f{player} &aé o novo &a&nMAGNATA&a do servidor.'
    - '&7O novo magnata possui &f{money} &7{unidade}.'
    - ''
  Magnata atual:
    - ''
    - '&2&l[$]&a O jogador &f{player} &aé o &a&nMAGNATA&a do servidor.'
    - '&7O magnata possui &f{money} &7{unidade}.'
    - ''
  Help:
    - '&a<--> Comandos da economia <-->'
    - ''
    - '&f > &a/money &8- &7Ver suas informações.'
    - '&f > &a/money &f<jogador> &8- &7Ver as informações de outro jogador.'
    - '&f > &a/money enviar &f<jogador> <quantia> &8- &7Enviar coins para um jogador.'
    - '&f > &a/money formatar &f<quantia> &8- &7Formata a quantia em (numeros -> letras) ou (letras -> números).'
    - '&f > &a/money toggle &8- &7Ativar/Desativar o recebimento de coins.'
    - '&f > &a/money top &8- &7Ver o TOP mais ricos.'
    - '&f > &a/magnata &8- &7Ver o jogador mais rico do servidor.'
    - ''
  Help staff:
    - '&a<--> Comandos da economia &7(STAFF)&a <-->'
    - ''
    - '&f > &a/money &8- &7Ver suas informações.'
    - '&f > &a/money &f<jogador> &8- &7Ver as informações de outro jogador.'
    - '&f > &a/money enviar &f<jogador> <quantia> &8- &7Enviar coins para um jogador.'
    - '&f > &a/money adicionar &f<jogador> <quantia> &8- &7Adicionar coins para um jogador.'
    - '&f > &a/money remover &f<jogador> <quantia> &8- &7Remover coins de um jogador.'
    - '&f > &a/money setar &f<jogador> <quantia> &8- &7Setar coins para um jogador.'
    - '&f > &a/money formatar &f<quantia> &8- &7Formata a quantia em (numeros -> letras) ou (letras -> números).'
    - '&f > &a/money toggle &8- &7Ativar/Desativar o recebimento de coins.'
    - '&f > &a/money top &8- &7Ver o TOP mais ricos.'
    - '&f > &a/money setnpc &f<1/2/3> &8- &7Setar o TOP NPC.'
    - '&f > &a/money delnpc &f<1/2/3> &8- &7Deletar o TOP NPC.'
    - '&f > &a/magnata &8- &7Ver o jogador mais rico do servidor.'
    - ''

Cheque:
  ID: 339
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

Cheque morte:
  enabled: true
  # máximo de money para o morto perder ( x % do seu money )
  maximum: 20000.0
  # quando o jogador morrer, perder esta % de money
  percentage: 10.0
  item:
    ID: 339
    Glow: true
    Name: '&aCheque de dinheiro'
    Lore:
      - ''
      - '&7Dropado por: &a{player}&7.'
      - '&7Aniquiliado em: &f{data} &8- &f{hora}&7.'
      - ''
      - '&bValor do cheque: &a{money}&b.'
      - ''
      - '&7Clique com botão direito para ativar'

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
# Sistema de formatos de money e quantia
format:
  type: 'LETRA' # Tipos: LETRA - NUMERO
  max-decimals: 4
  decimal-separator: ','
  grouping-separator: '.'
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

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/51-yEconomy">Site do plugin yEconomy</a>
    </category>
</seealso>