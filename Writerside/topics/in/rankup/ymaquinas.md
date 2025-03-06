# yMaquinas
<secondary-label ref="rankup"/>

### Descrição
Blocos que geram drops ao consumir combustível

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
<video src="//www.youtube.com/watch?v=vTKsVokRwi4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/maquinas - Abre a loja de máquinas
/maquinas top - Abre o menu de top
/maquinas help - Envia a mensagem de ajuda
/maquinas booster - Vê o tempo restante do booster
/maquinas lista - Mostra a lista de máquinas disponíveis
/maquinas give - Dá máquinas para um jogador
/maquinas givebooster - Dá boosters para um jogador
/maquinas reload - Recarrega as configurações
/combustiveis - Abre a loja de combustíveis
/combustiveis help - Envia a mensagem de ajuda
/combustiveis lista - Mostra a lista de combustíveis disponíveis
/combustiveis give - Dá combustíveis para um jogador
/limite - Mostra o seu limite
/limite [player] - Mostra o limite de outro jogador
/limite help - Envia a mensagem de ajuda
/limite top - Abre o menu do top limite
/limite enviar - Envia limite para outro jogador
/limite give - Dá limite em item para um jogador
/limite remove - Remove limite de um jogador
/limite add - Adiciona limite para um jogador
/limite set - Seta o limite de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymaquinas.admin - Permissão para ser reconhecido como admin
ymaquinas.maquina.usar - Permissão para o /maquina e /maquina top
ymaquinas.maquina.booster - Permissão para o /maquina booster
ymaquinas.multiplicador.[quantia] - Permissão para ter uma x quantia de multiplicador
ymaquinas.maquina.give - Permissão para o /maquina give
ymaquinas.maquina.givebooster - Permissão para o /maquina givebooster
ymaquinas.maquina.lista - Permissão para o /maquina lista
ymaquinas.maquina.reload - Permissão para o /maquina reload
ymaquinas.combustivel.usar - Permissão para o /combustivel
ymaquinas.combustivel.give - Permissão para o /combustivel give
ymaquinas.combustivel.lista - Permissão para o /combustivel lista
ymaquinas.limite.usar - Permissão para o /limite
ymaquinas.limite.outros - Permissão para o /limite [player]
ymaquinas.limite.enviar - Permissão para o /limite enviar
ymaquinas.limite.set - Permissão para o /limite set
ymaquinas.limite.add - Permissão para o /limite add
ymaquinas.limite.remove - Permissão para o /limite remove
ymaquinas.limite.give - Permissão para o /limite give
ymaquinas.limite.remove - Permissão para o /limite remove
ymaquinas.place.bypass - Permissão para colocar todas as máquinas</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ymaquinas_limite% - Retorna o limite do jogador formatado (1K, 1M, 1T...)
%ymaquinas_limite_raw% - Retorna o limite do jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMaquinas/
    ├── menus/
    │    ├── all_drops.yml
    │    ├── amigos.yml
    │    ├── drops.yml
    │    ├── principal.yml
    │    ├── top.yml
    │    └── upgrades.yml
    ├── shop/
    │    ├── combustiveis.yml
    │    └── maquinas.yml
    ├── bonus.yml
    ├── boosters.yml
    ├── combustiveis.yml
    ├── config.yml
    ├── descontos.yml
    ├── economies.yml
    └── maquinas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="all_drops.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Máquinas Drops'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
VoltarSlot: 9
ProximoSlot: 17
# Item de vender tudo
SellAll:
  Slot: 31
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: 0
  Data: 0
  Name: '&aVender Tudo'
  Lore: ['&7Clique para vender todos', '&7os drops de todas as', '&7suas máquinas.']
#Itens
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU CRIE DENTRO DE ITENS :)
]]>
</code-block>
</chapter>

<chapter title="amigos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8{maquina}'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
Backslot: 18
VoltarSlot: 9
ProximoSlot: 17
# Item do amigo
Amigo:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Glow: true
  Name: '&a{player}'
  Lore:
    - ''
    - '&aBotão &fDIREITO&a para deletar.'
    - ''
# Itens que aparecerão no menu
Itens:
  Adicionar:
    Slot: 27
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/8e9b27fccd80921bd263c91dc511d09e9a746555e6c9cad52e8562ed0182a2f'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aAdicionar amigo'
    Lore:
      - '&7Clique aqui para adicionar'
      - '&7amigos para poder usar'
      - '&7esta máquina.'

  ## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Adicionar:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="drops.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '{maquina}'
Tamanho: 27
Backslot: 18
Drop slot: 13
Itens: {}
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU CRIE DENTRO DE ITENS :)
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '{maquina}'
Tamanho: 36
Itens:
  Informacoes:
    Slot: 11
    CustomSkull: true
    # caso queira o item da maquina, deixe {maquina}
    URL: '{maquina}'
    ID: AIR
    Data: 0
    Glow: false
    Name: '&aInformações Gerais'
    Lore:
      - ''
      - ' &fDono: &7{dono}&f.'
      - ' &fStack: &7{stack}&f.'
      - ' &fStatus: &r{status}&f.'
      - ' &fDrops armazenados: &a{drops_armazenados}&f.'
      - ' &fCombustível: &7{combustivel_tem}/{capacidade}&f.'
      - ''
      - ' &f> Drops gerados por rodada: &b{drops_rodada}&f.'
      - ' &f> Velocidade de geração: &b{velocidade_upgrade}s&f.'
      - ''
  Combustivel:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: COAL
    Data: 0
    Glow: false
    Name: '&aCombústivel'
    Lore:
      - '&7A sua máquina necessita de'
      - '&7combustível para funcionar!'
      - ''
      - ' &fCombustível: &7{combustivel_tem}/{capacidade} &8{progressbar} &8{porcentagem}%'
      - ' &fInfinito: &r{infinito}&f.'
      - ''
  Drops:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/12ef39437d7d43a034c5a40b974e8d2c6734a218c76485d04910f507bdc2e809'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aDrops'
    Lore:
      - '&7Gerencie os drops que estão'
      - '&7armazenados nesta máquina.'
      - ''
      - ' &fDrops armazenados: &a{drops_armazenados}&f.'
      - ''
      - '&aClique para gerenciar.'
  Upgrades:
    Slot: 15
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/365fc0426230a2e88df29d2d8ec4512e6dbdbc0777b4b83cdda2ede81864d6'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aUpgrades'
    Lore:
      - '&7Sua máquina necessita de'
      - '&7melhorias para ficar mais'
      - '&7eficiente.'
      - ''
      - '&aClique para acessar.'
  Opcoes:
    Slot: 22
    CustomSkull: false
    URL: ''
    ID: SULPHUR
    Data: 0
    Glow: false
    Name: '&aOpções'
    Lore:
      - '&7Gerencie as opções gerais da'
      - '&7sua máquina.'
      - ''
      - ' &fStatus: &r{status}&f.'
      - ' &fHolograma: &r{holograma_status}&f.'
      - ''
      - '&aBotão &fESQUERDO&a para alternar o status.'
      - '&aBotão &fDIREITO&a para alternar o holograma.'
  Amigos:
    Slot: 23
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/1cba7277fc895bf3b673694159864b83351a4d14717e476ebda1c3bf38fcf37'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aAmigos'
    Lore:
      - '&7Acesse as preferências de'
      - '&7amizade deste gerador.'
      - ''
      - '&aClique para acessar.'
  Funcional:
    Slot: 24
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/333dcfb4da10177264968b449e724adebee3bc33b72bae85842b4aab9bd9c4db'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aFuncional'
    Lore:
      - '&7Sua máquina está funcionando normalmente.'
      - '&7Nenhum problema detectado.'
  Quebrada:
    Slot: 24
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/1fdeaa7e3ce7e7434f8c983a3bad0ac2d020f81533bffc238bfb73cf824c92e'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&cQuebrada'
    Lore:
      - '&7Sua máquina está quebrada!'
      - ''
      - ' &fConserto: &a{conserto} coins&f.'
      - ''
      - '&aClique para consertar.'
  Remover:
    Slot: 20
    CustomSkull: false
    URL: ''
    ID: BARRIER
    Data: 0
    Glow: false
    Name: '&cRemover'
    Lore:
      - '&7Remova máquinas deste stack de'
      - '&7geradores.'
      - ''
      - '&aBotão &fESQUERDO&a para remover TODAS.'
      - '&aBotão &fDIREITO&a para escolher a quantia.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Upgrades:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Máquinas'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17
# Item do top Limite
Item:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fLimite: &7{limite}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top máquinas compradas
Item compradas:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fMáquinas comprados: &7{maquinas}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top máquinas colocadas
Item colocadas:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fMáquinas colocadas: &7{maquinas}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top valor em coins das máquinas
Item valor:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fValor em coins: &2$ &a{money}'
    - '&fPosição: &e{pos}º'
    - ''
# Seletor dos tops
Seletor:
  Slot: 32
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: 0
  Data: 0
  Name: '&aSeletor do TOP'
# Tipos do seletor
Tipos:
  Limite:
    Ativar: true
    Nome: 'Limite'
  Compradas:
    Ativar: true
    Nome: 'Máquinas Compradas'
  Colocadas:
    Ativar: true
    Nome: 'Máquinas Colocadas'
  Valor:
    Ativar: true
    Nome: 'Valor das Máquinas'
# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome}'
  Selecionar: ' &f• &7{nome}'
]]>
</code-block>
</chapter>

<chapter title="upgrades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '{maquina}'
Tamanho: 27
Backslot: 18
Itens:
  CapacidadeUpgrade:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: FIREBALL
    Data: 0
    Name: '&aUpgrade de Capacidade'
    Lore:
      - '&7Esta evolução faz com que a'
      - '&7capacidade de combustível da'
      - '&7máquina seja aumentada.'
      - ''
      - ' &fNível: &7{nivel_atual}/{nivel_maximo}&f.'
      - ' &fCapacidade: &7{capacidade_atual}/{capacidade_maximo}&f.'
      - ' &fCusto para próx nível: &7{money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  CapacidadeUpgradeMaximo:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: FIREBALL
    Data: 0
    Name: '&aUpgrade de Capacidade'
    Lore:
      - '&7Esta evolução faz com que a'
      - '&7capacidade de combustível da'
      - '&7máquina seja aumentada.'
      - ''
      - ' &fNível: &7{nivel_atual}/{nivel_maximo}&f.'
      - ' &fCapacidade: &7{capacidade_atual}/{capacidade_maximo}&f.'
      - ''
      - '&cVocê já está no máximo.'
  DropsUpgrade:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: EYE_OF_ENDER
    Data: 0
    Name: '&aUpgrade de Geração'
    Lore:
      - '&7Esta evolução faz com que a'
      - '&7máquina produza mais drops'
      - '&7por vez.'
      - ''
      - ' &fNível: &7{nivel_atual}/{nivel_maximo}&f.'
      - ' &fDrops gerados por vez: &7{drops_atual}/{drops_maximo}&f.'
      - ' &fCusto para próx nível: &7{money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  DropsUpgradeMaximo:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: EYE_OF_ENDER
    Data: 0
    Name: '&aUpgrade de Geração'
    Lore:
      - '&7Esta evolução faz com que a'
      - '&7máquina produza mais drops'
      - '&7por vez.'
      - ''
      - ' &fNível: &7{nivel_atual}/{nivel_maximo}&f.'
      - ' &fDrops gerados por vez: &7{drops_atual}/{drops_maximo}&f.'
      - ''
      - '&cVocê já está no máximo.'
  VelocidadeUpgrade:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: EXP_BOTTLE
    Data: 0
    Name: '&aUpgrade de Velocidade'
    Lore:
      - '&7Esta evolução faz com que o'
      - '&7tempo de geração da máquina'
      - '&7seja reduzido.'
      - ''
      - ' &fNível: &7{nivel_atual}/{nivel_maximo}&f.'
      - ' &fTempo a menos: &7-{velocidade_atual}s/-{velocidade_maximo}s&f.'
      - ' &fCusto para próx nível: &7{money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  VelocidadeUpgradeMaximo:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: EXP_BOTTLE
    Data: 0
    Name: '&aUpgrade de Velocidade'
    Lore:
      - '&7Esta evolução faz com que o'
      - '&7tempo de geração da máquina'
      - '&7seja reduzido.'
      - ''
      - ' &fNível: &7{nivel_atual}/{nivel_maximo}&f.'
      - ' &fTempo a menos: &7-{velocidade_atual}s/-{velocidade_maximo}s&f.'
      - ''
      - '&cVocê já está no máximo.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> VelocidadeUpgradeMaximo:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

</chapter>

<chapter title="shop" collapsible="true">
<chapter title="combustiveis.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Combustiveis:
  1:
    # Item do combustível.
    Item:
      CustomSkull: false
      URL: ''
      ID: COAL
      Data: 0
      Glow: false
      Name: '&8Gasolina'
      Lore:
        - ''
        - '&fPreço: &a1000 coins&f.'
        - '&fLitros: &750 litros&f.'
        - ''
        - '&a&lFORMAS DE COMPRA'
        - ''
        - '&7&l• &fBotão direito: &7Comprar 1&f.'
        - '&7&l• &fBotão esquerdo: &7Escolher quantia&f.'
        - ''
    # Tipo do combustível
    Combustivel: 'gasolina'
    # Data de liberação para comprar
    Libera em: '16/10/2020-10:00'
    # Permissão para comprar o combustível
    # Deixe '' (vazio) para não usar
    Permissao: 'ymaquinas.combustivel.gasolina'
    Comprar:
      Custos:
        Custo1:
          Display: 'Money'
          Tipo: 'Money' #tipos: Money, plugin de pontos
          Custo: 100.0
]]>
</code-block>
</chapter>

<chapter title="maquinas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Maquinas:
  1:
    # Item da máquina.
    Item:
      CustomSkull: false
      URL: ''
      ID: IRON_BLOCK
      Data: 0
      Glow: false
      Name: '&fMáquina de Ferro'
      Lore:
        - ''
        - '&fPreço: &a1000 coins &7e &610 pontos&f.'
        - '&fPreço p/ drop: &7100 coins&f.'
        - ''
        - '&a&lFORMAS DE COMPRA'
        - ''
        - '&7&l• &fBotão direito: &7Comprar 1&f.'
        - '&7&l• &fBotão Q: &7Comprar limite&f.'
        - '&7&l• &fBotão esquerdo: &7Escolher quantia&f.'
        - '&7&l• &fBotão shift+direito: &7Preview do drop&f.'
        - ''
    # Preview do drop da máquina
    Drop:
      CustomSkull: false
      URL: ''
      ID: IRON_INGOT
      Data: 0
      Name: '&fFerro'
      Lore:
        - ' &fValor por drop: &a100 coins&f.'
    # Tipo da maquina
    Maquina: 'ferro'
    # Data de liberação para comprar
    Libera em: '16/10/2020-10:00'
    # Placeholder {rank} na lore da compra indisponível
    Rank: '&7[Membro]'
    Comprar:
      Custos:
        Custo1:
          Display: 'Money'
          Tipo: 'Money' #tipos: Money, plugin de pontos
          Custo: 1000.0
        Custo2:
          Display: 'Pontos'
          Tipo: 'PlayerPoints'
          Custo: 10.0
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bonus:
  membro:
    Ordem: 1
    # Permissão para ser reconhecido
    Permissao: 'ymaquinas.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Item dos boosters
Booster:
   CustomSkull: false
   URL: ''
   ID: 384
   Data: 0
   Glow: true
   Name: '&aBônus de venda'
   Lore:
      - ''
      - '&aTempo: &e{tempo}'
      - '&aPorcentagem: &e{bonus}%'
      - ''

Boosters:
   Booster1:
      Tempo: 60 #em segundos
      Bonus: 10.0 #porcentagem a mais
]]>
</code-block>
</chapter>

<chapter title="combustiveis.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Combustiveis:
  gasolina:
    Nome: '&7Gasolina'
    # Deixar a máquina infinita ao abastecer
    Infinito: false
    # Consumir o combustível ao abastecer uma máquina
    Consumir: true
    # Abastecer a máquina completamente sem deixar ela infinita
    CombustivelInfinito: false
    Litros: 50
    Item:
      CustomSkull: false
      URL: ''
      ID: COAL
      Data: 0
      Name: '&7Gasolina'
      Lore:
        - '&7Utilize este item para abastecer'
        - '&7as suas máquinas.'
        - ''
        - '&fLitros: &b{litros} litros&f.'
        - ''
        - '&aClique com o combustível em uma máquina.'
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
  Maquina:
    Comando: 'maquinas'
    Aliases: [ maquina, machine, machines ]
  Combustivel:
    Comando: 'combustiveis'
    Aliases: [ combustivel, fuel, fuels ]
  Limite:
    Comando: 'limite'
    Aliases: [ maquinalimite ]
  Drops:
    Comando: 'drops'
    Aliases: [ ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Opções gerais do plugin
Opcoes:
  # Sistema de bolsa de valores (yBolsa ou HeroBolsa)
  Bolsa: true
  # Raio de checagem de maquinas perto
  # em blocos.
  Raio: 5
  # Ativar o holograma do maquinas
  # pode elevar o timings um *pouco*
  Holograma: true
  # Tempo de atualização da task do holograma
  # Quanto menor o tempo, mais lag poderá ser gerado
  # em ticks; 20 ticks = 1 segundo
  TaskTempo: 5
  # Quando ativo, só poderá colocar máquinas no plot (PlotSquared)
  Plot: true
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Limite máximo de amigos que uma máquina pode ter
  # deixe 0 para ser infinito
  Maximo amigo: 0
  # Quebrar somente com silk touch
  Silk: true
  # Quantia máxima que pode ter de multiplicador
  Multiplicador max: 10
  # Ativar a compra usando o limite disponível com o botão "Q"
  # Isto só funciona se o limite estiver ativado
  Compra Q: true
  # Ativar a compra via chat
  # caso desativado, comprará apenas 1 unidade (sem contar o multiplicador)
  Compra chat: true
  # Gastar limite ao comprar
  GastarLimite: false
  # Permitir compactar combústiveis do mesmo tipo
  CompactarCombustivel: true
  # Máquinas com combustível infinito gerar apenas com o dono on
  InfinitoDonoOn: false
  # Formato do status da máquina quebrada
  QuebradaStatus: '&cQUEBRADA'
  # Formato do status da máquina sem combustivel
  SemCombustivelStatus: '&cSEM COMBUSTÍVEL'
  # Verificar se há máquinas por perto
  # para colocar um outro tipo
  Verificar perto: true
  # Ativar a máquina automaticamente ao colocá-la no chão
  Ativar colocar: false
  # Rodar a task de limpeza de máquinas inexistentes após 5 segundos do load do servidor
  MaquinaClearTask: true
  # Rodar a task de limpeza de hologramas
  HologramaClearTask:
    Ativar: true
    Delay: 30 # em segundos
  # Fechar inventário dos jogadores que estiverem com a máquina aberta após ela ser quebrada
  FecharQuebrada: true
  # Checar se a máquina possui combustível infinito para poder colocar somente em um stack que for combustível infinito
  ChecarInfinito: true
  # Dár máquina com combustível infinito se a quebrada possuir
  QuebrarInfinito: true
  # Mostrar máquinas de amigos no /maquina drops
  DropsMostrarAmigo: true
  # Zerar o combústivel quando a máquina quebrar
  ZerarQuebrar: false
  # Permitir o jogador colocar apenas 1 stack de spawner de cada tipo
  ApenasUm: false
  # Delay da compra com Q
  # em segundos
  DelayQ: 10
  # Blocos que não podem colocar máquinas em cima
  BlockCima blacklist:
    - 'SANDSTONE:0'
  # Configuração da barra de progresso
  Progress bar:
    Quantia: 10
    Simbolo: ':'
    Cor sim: '&a'
    Cor nao: '&7'
  # Formatador de mensagens
  Formatador:
    Bonus tem: '&fBônus: &a{bonus}%&7 ({display}&7)'
    Bonus nao tem: ''

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  StackMax: '&cO stack máximo desta máquina é {stackmax}.'
  Deu: '&aVocê deu &7x{quantia} {maquina}&a para o jogador &7{player}&a.'
  Deu combustivel: '&aVocê deu &7x{quantia} {combustivel}&a para o jogador &7{player}&a.'
  Deu todos: |
    &aO staff &f{player}&a deu &7x{quantia} {maquina}&a para todos online&a.
  Deu todos combustivel: |
    &aO staff &f{player}&a deu &7x{quantia} {combustivel}&a para todos online&a.
  Maquinas: '&cMáquinas disponíveis: &7{maquinas}'
  Combustiveis: '&cCombustiveis disponíveis: &7{combustiveis}'
  Help: |
    &bComandos disponíveis:
    &b > &3/maquinas &8- &fAbre o menu de máquinas
    &b > &3/maquinas help &8- &fEnvia essa mensagem
    &b > &3/maquinas lista &8- &fMostra a lista de máquinas disponíveis
    &b > &3/maquinas give <player/all> <maquina> <quantia> &8- &fDá máquinas para um jogador / todos os jogadores
  Help combustivel: |
    &bComandos disponíveis:
    &b > &3/combustiveis &8- &fAbre o menu de combustíveis
    &b > &3/combustiveis help &8- &fEnvia essa mensagem
    &b > &3/combustiveis lista &8- &fMostra a lista de combustíveis disponíveis
    &b > &3/combustiveis give <player/all> <combustivel> <quantia> &8- &fDá combustíveis para um jogador / todos os jogadores
  Help limite: |
    &bComandos disponíveis:
    &b > &3/limite &8- &fMostra o seu limite
    &b > &3/limite <player> &8- &fMostra o limite de outro jogador
    &b > &3/limite help &8- &fEnvia essa mensagem
    &b > &3/limite top &8- &fAbre o menu do top limite
    &b > &3/limite give <player> <quantia> &8- &fDá limite em item para um jogador
    &b > &3/limite remove <player> <quantia> &8- &fRemove limite de um jogador
    &b > &3/limite add <player> <quantia> &8- &fAdiciona limite para um jogador
    &b > &3/limite set <player> <quantia> &8- &fSeta o limite de um jogador
  Perm: '&cVocê não tem permissão para abrir esta máquina.'
  Perm maquina: '&cVocê não tem permissão para colocar este tipo de máquina.'
  Perm plot: '&cVocê não tem permissão neste terreno.'
  Colocada: '&a{quantia}x {maquina} &acolocada(s).'
  Removida: '&a{quantia}x {maquina} &aremovida(s).'
  Somente dono: '&cSomente o dono da máquina pode realizar esta ação.'
  Ativou drop: '&aVocê ativou o(s) drop(s) da {maquina}.'
  Gamemode: '&cEssa ação só pode ser realizada no modo survival.'
  Infinito: '&cEsta máquina possui combustível infinito.'
  Cheio: '&cEsta máquina está totalmente abastecida.'
  Abasteceu: '&aVocê abasteceu a máquina com o combustível {combustivel}.'
  Incompativel: '&cEsta máquina não aceita o combustível {combustivel}.'
  Inv cheio: '&cSeu inventário está cheio.'
  Suficiente: '&cEsta máquina não possui drops suficiente.'
  Coletou: '&aVocê coletou &7{quantia}x drops&7.'
  Cancelou: '&cVocê cancelou a operação.'
  Maximo amigo: '&cEsta máquina atingiu o limite máximo de amigos.'
  Adicionou: '&aVocê adicionou o jogador &7{player}&a na sua máquina.'
  Ja adicionado: '&cEste jogador já está adicionado.'
  Adicionar dono: '&cVocê não pode adicionar o dono como amigo na máquina.'
  Toque suave: '&cVocê precisa de uma picareta com toque suave para quebrar esta máquina.'
  Consertou: '&aVocê consertou a máquina e pagou &f{money} coins&a.'
  Consertar: '&cVocê precisa de &f{money} coins&c para consertar essa máquina.'
  MoneyUpgrade: '&cVocê precisa de &f{money} coins&c para comprar esse upgrade.'
  Comprou capacidade: '&aVocê adquiriu &f+1 nível&a do upgrade &fcapacidade &apor &f{money} coins&a.'
  Comprou drops: '&aVocê adquiriu &f+1 nível&a do upgrade &fdrops &apor &f{money} coins&a.'
  Comprou velocidade: '&aVocê adquiriu &f+1 nível&a do upgrade &fvelocidade &apor &f{money} coins&a.'
  Max multiplicador: '&cVocê não pode definir mais que o seu máximo: &7{maximo}&c.'
  Definido: '&aVocê definiu seu multiplicador para &7{multiplicador}&a.'
  Nao possui: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  Cadastrado: '&cEste plugin &f{plugin}&c não está implementado no plugin de shop.'
  Desabilitado: '&cEste plugin &f{plugin}&c não está ligado.'
  Limite insuficiente: '&cVocê não possui limite suficiente. Disponível: &7{limite}&c.'
  Limite alterado: '&aLimite do jogador &7{player}&a alterado para &7{quantia}&a.'
  Deu limite: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Max limite: '&cVocê já chegou no máximo.'
  Ha maquinas: '&cHá máquinas num raio de {raio} blocos.'
  Booster recebeu: '&aVocê recebeu &7{quantia} &a booster(s) de drops.'
  Booster deu: '&aVocê deu &7{quantia} &a booster(s) de drops para o jogador &7{player}&a.'
  Acabou booster: '&cSeu booster de drops acabou.'
  Ja esta booster: '&cVocê já está usando um booster.'
  Ativou booster: '&aVocê ativou um booster de drops. Multiplicador: &e{bonus}&a. Tempo: &e{tempo}&a.'
  Booster nenhum: '&cVocê não está usando nenhum booster.'
  Booster usando: '&aSeu booster de &f{bonus}% &aacaba em &f{tempo}&a.'
  Cheio limite-stack: '&cEsta máquina está no limite de stack máximo ({limite}).'
  Abasteceu limite-stack: '&aVocê aumentou o limite de stack da máquina para {limite}.'
  Recolher insuficiente: '&cEste stack possui apenas {stack} máquinas.'
  BlockBaixo: '&cVocê não pode colocar máquinas em cima deste bloco.'
  Si mesmo: '&cVocê não pode realizar esta ação à si mesmo.'
  Limite enviado: '&bVocê enviou &f{limite} limite&b para o jogador &f{player}&b.'
  Limite recebido: '&bVocê recebeu &f{limite} limite&b do jogador &f{player}&b.'
  Nao possui limite: '&bVocê não possui &f{limite} limite&b.'
  Target max limite: '&bO jogador já possui o máximo de limite permitido: &f{limite}&b.'
  Delay: '&cAguarde &e{time} &cpara adquirir novamente.'
  No-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  Ja colocou: '&cVocê já colocou uma máquina deste tipo.'
  Seu limite:
    - '&bQuantidade de limite que você possui: &f{limite}&b.'
  Limite jogador:
    - '&bQuantidade de limite que &7{player}&b possui: &f{limite}&b.'
  Adicionar:
    - ''
    - '&aDigite no chat o nome do seu amigo que quer adicionar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Coletar:
    - ''
    - '&aDigite a quantia que você quer coletar.'
    - ''
    - '&8| &fVocê possui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara coletar tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''
  Digite:
    - ''
    - '&aDigite a quantia de máquinas que deseja.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite combustivel:
    - ''
    - '&aDigite a quantia de combustíveis que deseja.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite multiplicador:
    - ''
    - '&8| &aDigite no chat a quantia de multiplicador que deseja.'
    - ''
    - '&f> &7Atual: &b{atual}&7.'
    - '&f> &7Máximo: &b{maximo}&7.'
    - ''
  Comprou:
    - '&bObrigado por adquirir máquinas na loja de máquinas. Confira as informações da compra:'
    - ''
    - '&7&l| &fMáquina: &7{maquina}&f.'
    - '&7&l| &fQuantia: &7{quantia}&f.'
    - ''
  Comprou combustivel:
    - '&bObrigado por adquirir combustíveis na loja de combustível. Confira as informações da compra:'
    - ''
    - '&7&l| &fCombustível: &7{combustivel}&f.'
    - '&7&l| &fQuantia: &7{quantia}&f.'
    - ''
  Digite remover:
    - ''
    - '&aDigite a quantia de máquinas que deseja remover.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''

# Limite de compra de máquinas na loja.
Limite:
  # Quantia de limite que o jogador ganhar ao se registrar.
  Default: 1
  # Máximo de limite que o jogador pode ter.
  # Deixe 0 para ser infinito.
  Max: 100
  # Ativar o limite
  Ativar: true
  # Item do limite que será ativável
  Item:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    ID: 0
    Data: 0
    Glow: true
    Name: '&bLimite de compra'
    Lore:
      - ''
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
      - ''

# Limite de stack de máquinas.
Limite stack:
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  ID: 0
  Data: 0
  Glow: true
  Name: '&bLimite de stack'
  Lore:
    - ''
    - '&fQuantia: &a{quantia}'
    - ''
    - '&7Clique com botão direito na máquina para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
    - ''

# Configurações gerais dos itens
Items:
  # Quando a máquina não foi liberado na data ainda.
  Nao pode:
    CustomSkull: false
    URL: ''
    ID: BARRIER
    Data: 0
    Glow: true
    Name: '{maquina}'
    Lore:
      - ''
      - '&cVocê não pode comprar esta máquina.'
      - '&7Ela será liberado em: &f{data} - &f{hora}'
      - '&7Tempo para liberar: &f{time_formatted}'
      - ''
  # Quando o jogador não tiver permissão de comprar aquela máquina.
  Permissao:
    CustomSkull: false
    URL: ''
    ID: BARRIER
    Data: 0
    Glow: true
    Name: '{maquina}'
    Lore:
      - ''
      - '&cVocê não pode comprar esta máquina.'
      - '&7Você não possui permissão.'
      - ''
  # Quando o item não foi liberado na data ainda.
  Nao pode combustivel:
    CustomSkull: false
    URL: ''
    ID: BARRIER
    Data: 0
    Glow: true
    Name: '{combustivel}'
    Lore:
      - ''
      - '&cVocê não pode comprar este combustível.'
      - '&7Ele será liberado em: &f{data} - &f{hora}'
      - '&7Tempo para liberar: &f{time_formatted}'
      - ''
  # Quando o jogador não tiver permissão de comprar aquela máquina.
  Permissao combustivel:
    CustomSkull: false
    URL: ''
    ID: BARRIER
    Data: 0
    Glow: true
    Name: '{combustivel}'
    Lore:
      - ''
      - '&cVocê não pode comprar este combustível.'
      - '&7Você não possui permissão.'
      - ''
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

# Formatos de money e quantia
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

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
  membros:
    Ordem: 1
    Permissao: 'ymaquinas.membro'
    Display: '&7[Membro]'
    Desconto: 10.0 # em % do valor total
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
    permission: 'yminas.provider.money'
  yMinas:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yMinas'
    # Formato inteiro
    display: 'Blocos'
    # Formato abreviado
    abbreviated: 'blocos'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yminas.provider.yminas'
]]>
</code-block>
</chapter>

<chapter title="maquinas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Maquinas:
  ferro:
    # Nome que irá aparecer nas mensagens
    Nome: '&fMáquina de Ferro'
    # Permissão para poder por o spawner
    # deixe '' (vazio) para não usar
    Permissao: ''
    # Stack máximo de máquinas (total)
    StackMax: 2
    # Limite padrão de stack de máquinas
    # Deixe 0 para não usar
    LimiteStackPadrao: 30
    # Velocidade de geração
    Velocidade: 10
    # Chance da máquina quebrar a cada onda (deixe 0 para não usar)
    QuebrarChance: 10.0
    # Preço para consertar a máquina
    ConsertarPreco: 1000.0
    # Quantia de combustível que irá gastar por onda
    CombustivelOnda: 10
    # Gastar combustível apenas se o dono estiver offline?
    GastarApenasOff: false
    # Combustíveis que a máquina aceita
    Combustiveis:
      - 'gasolina'
    # A máquina vai gerar um vidro com uma cabeça dentro?
    Glass: false
    # Tipo do vidro
    GlassType: 'STAINED_GLASS'
    # Data da cor do vidro
    GlassData: 11
    # Ajuste a cabeça dentro do vidro
    Glass-offset: -1.2
    # Mensagem de venda
    Mensagens:
      Vendeu: '&aVocê vendeu &7{quantia}x {drop}&a por &6{money} coins &8{bonus}&a.'
    # Item da máquina
    Item:
      CustomSkull: false
      URL: ''
      ID: IRON_BLOCK
      Data: 0
      Name: '&fMáquina de Ferro'
      Lore:
        - ''
        - '&f Stack: &7{stack}'
        - '&f Combustível atual: &c{combustivel_tem}'
        - '&f Drops armazenados: &c{drops_armazenados}'
        - '&f Preço por drop: &a100 coins'
        - ''
        - '&f Upgrades:'
        - '&f  > Capacidade de combustível: &b{capacidade}'
        - '&f  > Drops gerados por rodada: &b{drops}'
        - '&f  > Velocidade de geração: &b{velocidade}s'
        - ''
    # Holograma que irá aparecer em cima da máquina
    Holograma:
      Altura: 3.5
      Holograma:
        - '&fMáquina de Ferro'
        - '&fDono: &7{dono}&f.'
        - '&fStack: &bx{quantia}&f.'
        - '&fDrops armazenados: &bx{drops}&f.'
        - '&fCombustível: &7{combustivel_tem}/{capacidade} &8{progressbar} &a{porcentagem}%'
        - '&fStatus: &r{status}'
        # '&fDrops p/ rodada: &b{drops_rodada}'
        # '&fVelocidade de geração: &b{velocidade_upgrade}s'
        - ''
        - '[item]IRON_INGOT:0'
    # Upgrades da máquina
    Upgrades:
      # Capacidade de combústivel da máquina
      Capacidade:
        PrecoPorLevel: 10.0
        Maximo: 9
        Padrao: 3
        AdicionarPorLevel: 25
        # Multiplicar a capacidade pelo stack
        MultiplicarStack: true
        Prices-PerLevel:
          price1:
            provider: 'yeconomias-token'
            price: 10000.0
      # Quantidade de drops por rodada da máquina
      Drops:
        PrecoPorLevel: 20.0
        Maximo: 5
        Padrao: 1
        AdicionarPorLevel: 2
        Prices-PerLevel:
          price1:
            provider: 'yeconomias-token'
            price: 10000.0
      # Velocidade de geração de drops da máquina
      Velocidade:
        PrecoPorLevel: 15.0
        Maximo: 5
        Padrao: 0
        RemoverPorLevel: 1
        Prices-PerLevel:
          price1:
            provider: 'yeconomias-token'
            price: 10000.0
    # Drop da máquina
    Drop:
      Nome: '&fFerro'
      # ícone que irá ficar no menu de drops
      Icone:
        CustomSkull: false
        URL: ''
        ID: IRON_INGOT
        Data: 0
        Name: '&fFerro'
        Lore:
          - ''
          - ' &fDrops armazenados: &a{drops_armazenados}&f.'
          - ' &fValor por drop: &a100 coins&f.'
          - ' &fValor total: &a{money} coins&f.'
          - ' &fBolsa: &7{bolsa}%&f.'
          - ' &fSeu bônus: &b{bonus_raw}%&f.' # bonus formatado: {bonus}
          - ''
          - '&aBotão &fESQUERDO&a para vender.'
          - '&aBotão &fDIREITO&a para recolher.'
      # ícone que irá ficar no menu de all_drops
      Icone-All:
        CustomSkull: false
        URL: ''
        ID: IRON_INGOT
        Data: 0
        Name: '&fMáquina de Ferro'
        Lore:
          - '&7Dono da Máquina: &f{player}'
          - ''
          - ' &fDrops armazenados: &a{drops_armazenados}&f.'
          - ' &fValor por drop: &a100 coins&f.'
          - ' &fValor total: &a{money} coins&f.'
          - ' &fBolsa: &7{bolsa}%&f.'
          - ' &fSeu bônus: &b{bonus_raw}%&f.' # bonus formatado: {bonus}
          - ''
          - '&aBotão &fESQUERDO&a para vender.'
          - '&aBotão &fDIREITO&a para recolher.'
      Item:
        CustomSkull: false
        URL: ''
        ID: IRON_INGOT
        Data: 0
        Name: '&fFerro'
        Lore: [ ]
      # Ativar o armazém de drops
      Armazem: true
      # Possibilitar recolher o drop no armazém
      Recolher: true
      # Possibilitar vender o drop no armazém
      Vender: true
      # Botão que será realizada a venda (LEFT | RIGHT)
      Vender botao: 'LEFT'
      # Botão que será realizado recolher (LEFT | RIGHT)
      Recolher botao: 'RIGHT'
      # Permissão para recolher drops (deixe vazio '' para não usar)
      Recolher perm: 'ymaquinas.ferro.coletar'
      # Permissão para vender drops (deixe vazio '' para não usar)
      Vender perm: 'ymaquinas.ferro.vender'
      # Preço por drop (para o comando)
      Preco: 100
      # Economias que a máquina irá dar
      Currencies:
        preco1:
          Provider: 'money'
          Amount: 100.0
      # O Drop vai executar um comando ao ser recolhido?
      # Caso seja um comando e o armazem estiver desativado
      # a máquina irá dropar itens que ao serem ativados
      # executarão o comando
      Comando:
        Ativar: false
        UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
        MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
        InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
        ColetarChatBypass: true # coletar diretamente, sem precisar digitar a quantia no chat (apenas quando os comandos tiverem ativos)
        FormatarQuantia: true # formatar a quantia que será executada no comando. Ex: 1k, 10k, 1M
        Comandos:
        - 'give {player} iron_ingot {quantia}'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static MaquinaAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;MaquinaAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(MaquinaAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/86-yMaquinas">Site do plugin yMaquinas</a>
    </category>
</seealso>