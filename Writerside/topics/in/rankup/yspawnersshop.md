# ySpawnersShop
<secondary-label ref="rankup"/>

### Descrição
Simples e eficaz, gerencie a compra de spawners no seu servidor.

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
<video src="//www.youtube.com/watch?v=uiy9j4a3Gfs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/spawners - Abre o menu principal.
/spawners reload - Recarrega as configurações
/spawners givelimite - Dá limite para um jogador.
/limite - Mostra a quantia de limite do jogador.
/limite top - Abre o top limite.
/limite - Mostra a quantia de limite de um jogador.
/limite help - Mostra a quantia de limite de um jogador.
/limite setar - Setar uma quantia de limite para o jogador.
/limite add - Adicionar uma quantia de limite para o jogador.
/limite remove - Remover uma quantia de limite do jogador.
/limite enviar - Enviar uma quantia de limite para um jogador.
/redutor give - Dá um redutor de tempo para um jogador.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yspawnersshop.usar - Permissão para o /spawners e /limite top
yspawnersshop.givelimite - Permissão para o /spawners givelimite
yspawnersshop.reload - Permissão para o /spawners reload
yspawnersshop.limite - Permissão para o /limite
yspawnersshop.limite.outros - Permissão para o /limite
yspawnersshop.limite.setar - Permissão para o /limite setar
yspawnersshop.limite.add - Permissão para o /limite add
yspawnersshop.limite.help - Permissão para o /limite help
yspawnersshop.limite.remove - Permissão para o /limite remove
yspawnersshop.limite.enviar - Permissão para o /limite enviar
yspawnersshop.multiplicador.[quantia] - Permissão para ter uma x quantia de multiplicador
yspawnersshop.giveredutor - Permissão para o /redutor give</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yspawnersshop_limite% - Retorna o limite do jogador formatado (1K, 1M, 1T...)
%yspawnersshop_limite_raw% - Retorna o limite do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yspawnersshop_gasto% - Retorna o valor gasto do jogador formatado (1K, 1M, 1T...)
%yspawnersshop_gasto_raw% - Retorna o valor gasto do jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── ySpawnersShop/
    ├── menus/
    │    ├── multipliers.yml
    │    ├── principal.yml
    │    ├── redutor_select.yml
    │    └── top.yml
    ├── config.yml
    ├── descontos.yml
    ├── redutores.yml
    ├── spawners.yml
    └── upgrades.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="multipliers.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Multiplicadores S-SHOP'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34  ]
AnteriorSlot: 45
ProximoSlot: 53
BackSlot: 40
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja de geradores'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34  ]
AnteriorSlot: 45
ProximoSlot: 53
# Itens da loja
Itens:
  Informacoes:
    Slot: 48
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/1cba7277fc895bf3b673694159864b83351a4d14717e476ebda1c3bf38fcf37'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aInformações gerais'
    Lore:
      - '&7Geradores são uma das partes mais'
      - '&7importantes do servidor! Com'
      - '&7eles, é possível receber muuuitos'
      - '&7coins e itens especiais!'
      - ''
      - '&fCoins: &7{money}&f.'
      - '&fDesconto: &7{desconto}% ( {grupo} &7)&f.'
      - '&fLimite de compra: &7{limite}&f.'
      - '&fGeradores Adquiridos: &7{geradores}&f.'
  Top:
    Slot: 49
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTOP'
    Lore:
      - '&7Clique aqui para acessar'
      - '&7a lista de jogadores com'
      - '&7mais limites do servidor.'
  Multiplicador:
    Slot: 50
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/b73e87235a2f691cf14bb0d414fda2563f040865c74273bf2c8bc095fecb228'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aMultiplicador de compra'
    Lore:
      - '&7Quanto mais limite de compra,'
      - '&7mais geradores é possível comprar'
      - '&7por vez, porém, há mais um jeito'
      - '&7de comprar geradores mais rápido,'
      - '&7que é o multiplicador de compra!'
      - '&7Ele fornece mais geradores a'
      - '&7cada compra feita.'
      - ''
      - ' &fMultiplicador ativo: &7{ativo}&f.'
      - ' &fMultiplicador máximo: &7{maximo}&f.'
      - ''
      - '&aClique para alterar seu multiplicador.'
]]>
</code-block>
</chapter>

<chapter title="redutor_select.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Máq. do Tempo'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34  ]
AnteriorSlot: 45
ProximoSlot: 53
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP SpawnersShop'
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

# Item do top geradores
Item geradores:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fGeradores comprados: &7{geradores}'
    - '&fPosição: &e{pos}º'
    - ''

# Item do top valor gasto
Item gasto:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fValor gasto: &7{amount}'
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
  Geradores:
    Ativar: true
    Nome: 'Geradores'
  Gasto:
    Ativar: true
    Nome: 'Valor gasto'

# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome}'
  Selecionar: ' &f• &7{nome}'
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
# Comandos e aliases do plugin
Comandos:
  Principal:
    Comando: 'sshop'
    Aliases: [spawnersshop, spawners, shopspawners, spawnershop, shopspawner]
  Limite:
    Comando: 'limite'
    Aliases: [ ]
  Redutor:
    Comando: 'redutor'
    Aliases: [ ]

#Coloque yPoints, PlayerPoints, JH_Shop, yCash, TGCash, AtlasEconomiaSecundaria, MageCash, WheavelGems, LegendaryEconomy
Plugin de Pontos: 'PlayerPoints'

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Ativar a compra usando o limite disponível com o botão "Q"
# Isto só funciona se o limite estiver ativado
Compra Q: true

# Ativar a compra via chat
# caso desativado, comprará apenas 1 unidade (sem contar o multiplicador)
Compra chat: true

# Quantia máxima que pode ter de multiplicador
Multiplicador max: 10

# Gastar limite ao comprar
GastarLimite: false

# Verificar se há a mesma quantia da compra disponível no inventário
# Caso esteja false, irá verificar se possui apenas 1 slot disponível (ideal para servidores que vendem spawners stackados)
VerificarInv: false

# Ativar o sistema de atualizar o menu
Menu updater: true

# Delay da compra com Q
# em segundos
DelayQ: 10

# Mensagens gerais do plugin:
Mensagens:
  Permissao: '&cVocê não tem permissão para fazer isto.'
  Cancelou: '&cVocê cancelou a compra.'
  Nao tem money: '&cDesculpe, mas você não possui a quantia necessária de money, &7{money} money&c.'
  Nao e numero: '&cO argumento não é um número.'
  Nao encontrado: '&cJogador não encontrado.'
  Limite insuficiente: '&cVocê não possui limite suficiente. Disponível: &7{limite}&c.'
  Deu: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Max limite: '&cVocê já chegou no máximo.'
  Max multiplicador: '&cVocê não pode definir mais que o seu máximo: &7{maximo}&c.'
  Definido: '&aVocê definiu seu multiplicador para &7{multiplicador}&a.'
  Nao tem cash: '&cDesculpe, mas você não possui a quantia necessária de cash, &7{cash} cash&c.'
  Nao tem almas: '&cDesculpe, mas você não possui a quantia necessária de almas, &7{almas} almas&c.'
  Limite alterado: '&aLimite do jogador &7{player}&a alterado para &7{quantia}&a.'
  InvCheio: '&cSeu inventário não possui espaço suficiente.'
  Deu redutor: '&aVocê deu &e{quantia} &ade &eMáquina do Tempo&a para o jogador &e{player}&a.'
  Recebeu redutor: '&aVocê recebeu &e{quantia} &ade &eMáquina do Tempo&a.'
  Nenhum redutor: '&cNenhum spawner está disponível para reduzir seu tempo de liberação.'
  Ativou redutor: '&aVocê adiantou &f{tempo}&a no horário de liberação do spawner &f{spawner}&a.'
  Nao possui: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  Cadastrado: '&cEste plugin &f{plugin}&c não está implementado no plugin de spawners.'
  Help:
    - ''
    - '&c/sshop'
    - '&c/sshop givelimite'
    - '&c/sshop reload'
    - ''
  Comprou:
    - '&bObrigado por adquirir itens na loja de spawners. Confira as informações da compra:'
    - ''
    - '&7&l| &fTipo: &7{tipo}&f.'
    - '&7&l| &fQuantia: &7{quantia}&f.'
    - ''
  Digite:
    - ''
    - '&aDigite a quantia de spawners que deseja.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite multiplicador:
    - ''
    - '&8| &aDigite no chat a quantia de multiplicador que deseja.'
    - ''
    - '&f> &7Atual: &b{atual}&7.'
    - '&f> &7Máximo: &b{maximo}&7.'
    - ''
  Seu limite:
    - '&bQuantidade de limite que você possui: &f{limite}&b.'
  Limite jogador:
    - '&bQuantidade de limite que &7{player}&b possui: &f{limite}&b.'
  Si mesmo: '&cVocê não pode realizar esta ação à si mesmo.'
  Limite enviado: '&bVocê enviou &f{limite} limite&b para o jogador &f{player}&b.'
  Limite recebido: '&bVocê recebeu &f{limite} limite&b do jogador &f{player}&b.'
  Nao possui limite: '&bVocê não possui &f{limite} limite&b.'
  Target max limite: '&bO jogador já possui o máximo de limite permitido: &f{limite}&b.'
  Delay: '&c&lERRO! &cAguarde &e{time} &cpara adquirir um spawner novamente.'
  Limite ajuda:
    - '&aComandos do /limite'
    - ''
    - '&f-> &b/limite'
    - '&f-> &b/limite set'
    - '&f-> &b/limite add'
    - '&f-> &b/limite remove'
    - '&f-> &b/limite send'
    - '&f-> &b/limite top'
    - '&f-> &b/limite help'
    - '&f-> &b/limite [player]'
    - ''

# Limite de compra de spawners na loja.
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

# Configurações gerais dos itens
Items:
  # Quando o item não foi liberado na data ainda.
  Nao pode:
    CustomSkull: false
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 166
    Data: 0
    Glow: true
    Name: '{spawner}'
    Lore:
      - ''
      - '&cVocê não pode comprar este spawner.'
      - '&7Ele será liberado em: &f{data} - &f{hora}'
      - '&7Tempo para liberar: &f{time_formatted}'
      - ''
  # Quando o jogador não tiver permissão de comprar aquele spawner.
  Permissao:
    CustomSkull: false
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 166
    Data: 0
    Glow: true
    Name: '{spawner}'
    Lore:
      - ''
      - '&cVocê não pode comprar este spawner.'
      - '&7Você não possui permissão.'
      - ''
  # Quando o jogador quiser reduzir o tempo de liberação do spawner
  Redutor:
    Lore:
      - ''
      - '&fTipo: &7{tipo}'
      - ''
      - '&7Ele será liberado em: &f{data} - &f{hora}'
      - '&7Tempo para liberar: &f{time_formatted}'
      - ''
      - '&aClique para reduzir o tempo em &f{tempo}&a.'

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
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
  membros:
    Ordem: 1
    Permissao: 'ysshop.membro'
    Display: '&7[Membro]'
    Desconto: 10.0 # em % do valor total
]]>
</code-block>
</chapter>

<chapter title="redutores.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Redutores:
  1hora:
    # Tempo que irá reduzir da liberação de spawners
    # Em segundos
    Tempo: 3600
    Item:
      CustomSkull: false
      URL: ''
      ID: WATCH
      Data: 0
      Glow: true
      Name: '&eMáquina do tempo'
      Lore:
        - '&7Diminuia a sua espera para'
        - '&7liberar um gerador.'
        - ''
        - ' &fTempo: &71 hora'
        - ''
        - '&cClique para utilizar'
]]>
</code-block>
</chapter>

<chapter title="spawners.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Spawners:
  1:
    # Item do spawner.
    Item:
      CustomSkull: false
      URL: ''
      ID: 383
      Data: 92
      Glow: false
      Name: '&aGerador de Monstros'
      Lore:
        - ''
        - '&fTipo: &7Vaca&f.'
        - '&fPreço p/ drop: &71M&f.'
        - ''
        - '&fPreço: &71000 coins&F.'
        - ''
        - '&a&lFORMAS DE COMPRA'
        - ''
        - '&7&l• &fBotão direito: &7Comprar 1&f.'
        - '&7&l• &fBotão Q: &7Comprar limite&f.'
        - '&7&l• &fBotão esquerdo: &7Escolher quantia&f.'
        - ''
    # Display name do spawner
    Display: '&7Vaca'
    # Data de liberação para comprar
    Libera em: '16/10/2020-10:00'
    # Tempo reduzido (não mexa aqui :) )
    Deduced: 0
    # Valor para somar no gasto do jogador
    Gasto: 1000.0
    # Comando que será executado quando o jogador comprar
    Comandos:
      - 'mobspawner give {player} COW {quantia}' # {quantia} para a quantia digitada
    # Placeholder {rank} na lore da compra indisponível
    Rank: '&7[Membro]'
    Comprar:
      # Preço de cada spawner.
      Custos:
        Custo1:
          Display: 'Money'
          Tipo: 'Money' #tipos: Money, plugin de pontos
          Custo: 1000.0
        Custo2:
          Display: 'Pontos'
          Tipo: 'PlayerPoints'
          Custo: 10.0
      # Permissão para comprar o spawner.
      Permissao: 'ysshop.vaca'
]]>
</code-block>
</chapter>

<chapter title="upgrades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
delay:
  # em milissegundos
  default: 5000
  reduce-per-level: 500
  maximum: 4000
  icon-slot: 51
  icon:
    material: 'GOLD_INGOT'
    name: '&eDelay'
    lore: ['&7Seu delay: &f{delay}', '', '&eCusto {Money} coins. Clique para comprar.']
  icon-max:
    material: 'GOLD_INGOT'
    name: '&eDelay'
    lore: ['&7Seu delay: &f{delay}']
  prices:
    price1:
      provider: 'Money'
      display: 'Money'
      amount: 100.0

multiplier:
  command: 'lp user {player} permission set yspawnersshop.multiplicador.{multiplier}'
  maximum: 10
  icon:
    material: 'STAINED_GLASS_PANE:14'
    name: '&eMultiplicador'
    lore: ['&7Multiplicador: &f{multiplier}', '', '&eCusto {Money} coins. Clique para comprar.']
  icon-has:
    material: 'STAINED_GLASS_PANE:4'
    name: '&eMultiplicador'
    lore: ['&7Multiplicador: &f{multiplier}', '', '&aClique para usar']
  icon-using:
    material: 'STAINED_GLASS_PANE:5'
    name: '&eMultiplicador'
    lore: ['&7Multiplicador: &f{multiplier}']
  prices-default:
    price1:
      provider: 'Money'
      amount: 10000.0
  prices-per-level:
    price1:
      provider: 'Money'
      amount: 10000.0
  prices-displays:
    price1:
      provider: 'Money'
      display: 'Money'

]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static SpawnersShopAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;SpawnersShopAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(SpawnersShopAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/46-ySpawnersShop">Site do plugin ySpawnersShop</a>
    </category>
</seealso>