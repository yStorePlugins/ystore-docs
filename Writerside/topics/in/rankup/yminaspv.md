# yMinasPv
<secondary-label ref="rankup"/>

### Descrição
O melhor da mineração agora na sua plot

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
<video src="//www.youtube.com/watch?v=9VtLD5Gw7bM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/minapv&nbsp;- Abre o menu principal
/minapv give&nbsp;- Dá uma mina privada para um jogador
/minapv&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yminaspv.use - Permissão para o /minapv
yminaspv.give - Permissão para o /minapv give
yminaspv.admin.reload - Permissão para o /minapv reload</code-block>
</chapter>



## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMinasPv/
    ├── enchantments/
    │    ├── custom_enchants.yml
    │    └── enchantments.yml
    ├── mines/
    │    └── redstone.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="enchantments" collapsible="true">
<chapter title="custom_enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos quiser
enchants:
  chaveiro:
    name: 'Chaveiro'
    pickaxe-level: 0
    order: 14
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    commands: ['100.0,give {player} STONE 1']
    displays:
      can:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="enchantments.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Apague apenas os encantamentos que não for usar
enchants:
  efficiency: # Não mude este nome, ou o encantamento não será reconhecido
    name: 'Eficiência'
    # Ordem do ícone no menu
    order: 1
    # Aparecer no menu de evolução
    show-menu: true
    # Poder evoluir pagando no menu de evolução
    can-buy: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    show-infinity: false
    level:
      default: 0
      maximum: 1000.0 # Use -1 para ser infinito
    # Opções de give do encantamento
    options:
      # Delay para ativar o encantamento novamente
      # em segundos
      delay: 0
      # Ativar dar EXP Vanilla
      xp: true
      # Ativar dar XP mcMMO
      xp-mcmmo: true
      # Ativar dar economias
      economy: true
      # Ativar os custom enchant
      custom-enchant: true
      # Ativar os mine_rewards
      rewards: true
      # Permissão para usar o encantamento
      # Deixe vazio para não usar
      permission: ''
    price-multiplier: 1.00
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays: # Item que aparecerá no menu de evolução
      can: # quando puder evoluir
        material: DIAMOND_PICKAXE
        name: '&aEficiência'
        lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant: # quando não puder evoluir
        material: DIAMOND_PICKAXE
        name: '&aEficiência'
        lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission: # quando não puder evoluir
        material: DIAMOND_PICKAXE
        name: '&aEficiência'
        lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum: # quando já estiver no máximo
        material: DIAMOND_PICKAXE
        name: '&aEficiência'
        lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&cVocê já está no máximo.'

  fortune:
    name: 'Fortuna'
    pickaxe-level: 0
    order: 2
    show-menu: true
    can-buy: true
    show-infinity: false
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&cVocê já está no máximo.'

  nuclear:
    name: 'Nuclear'
    pickaxe-level: 0
    order: 3
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cNuclear<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        name: '&aNuclear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant: # quando não puder evoluir
        material: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        name: '&aNuclear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission: # quando não puder evoluir
        material: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        name: '&aNuclear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum: # quando já estiver no máximo
        material: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        name: '&aNuclear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  destructor:
    name: 'Destruidor'
    pickaxe-level: 0
    order: 4
    show-menu: true
    can-buy: true
    show-infinity: false
    animation: true
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cDestruidor<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        name: '&aDestruidor'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        name: '&aDestruidor'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        name: '&aDestruidor'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        name: '&aDestruidor'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  speed:
    name: 'Velocidade'
    pickaxe-level: 0
    order: 6
    show-menu: true
    can-buy: true
    show-infinity: false
    level:
      default: 0.0
      maximum: 1.0
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&cVocê já está no máximo.'

  haste:
    name: 'Pressa'
    pickaxe-level: 0
    order: 7
    show-menu: true
    can-buy: true
    show-infinity: false
    level:
      default: 0.0
      maximum: 1.0
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&cVocê já está no máximo.'

  explosion:
    name: 'Explosão'
    pickaxe-level: 0
    order: 9
    show-menu: true
    can-buy: true
    show-infinity: false
    animation: true
    radius: 2
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cExplosão<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        name: '&aExplosao'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        name: '&aExplosao'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        name: '&aExplosao'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        name: '&aExplosao'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  laser:
    name: 'Laser'
    pickaxe-level: 0
    order: 10
    show-menu: true
    can-buy: true
    show-infinity: false
    animation: true
    radius: -1
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cLaser<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        name: '&aLaser'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        name: '&aLaser'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        name: '&aLaser'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        name: '&aLaser'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  drill:
    name: 'Furadeira'
    pickaxe-level: 0
    order: 11
    show-menu: true
    can-buy: true
    show-infinity: false
    animation: true
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cFuradeira<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        name: '&aFuradeira'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        name: '&aFuradeira'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        name: '&aFuradeira'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        name: '&aFuradeira'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  sphere:
    name: 'Esfera'
    pickaxe-level: 0
    order: 14
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    animation: true
    radius: 5
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cEsfera<nl>&cativada'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '7ff91e15b31fe4cfda13fb44634da87a75ba2c17fce7b524a55a314f5aa99d9f'
        name: '&aEsfera'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma esfera.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '7ff91e15b31fe4cfda13fb44634da87a75ba2c17fce7b524a55a314f5aa99d9f'
        name: '&aEsfera'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma esfera.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: '7ff91e15b31fe4cfda13fb44634da87a75ba2c17fce7b524a55a314f5aa99d9f'
        name: '&aEsfera'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma esfera.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: '7ff91e15b31fe4cfda13fb44634da87a75ba2c17fce7b524a55a314f5aa99d9f'
        name: '&aEsfera'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma esfera.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  x:
    name: 'x'
    pickaxe-level: 0
    order: 15
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    animation: true
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&xC<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '91b7a0c210e6cdf5a35fd8197e6e24a038315bbe3bdcd1bcc3630bf26f59ec5c'
        name: '&aX'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um X.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '91b7a0c210e6cdf5a35fd8197e6e24a038315bbe3bdcd1bcc3630bf26f59ec5c'
        name: '&aX'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um X.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: '91b7a0c210e6cdf5a35fd8197e6e24a038315bbe3bdcd1bcc3630bf26f59ec5c'
        name: '&aX'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um X.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: '91b7a0c210e6cdf5a35fd8197e6e24a038315bbe3bdcd1bcc3630bf26f59ec5c'
        name: '&aX'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um X.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  linear:
    name: 'Linear'
    pickaxe-level: 0
    order: 16
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    animation: true
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cLinear<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: 'a8259df25c9de155b063cbef86646574d694eff3ad8d4d0cc64c4abc84d1441f'
        name: '&aLinear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma cruz.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: 'a8259df25c9de155b063cbef86646574d694eff3ad8d4d0cc64c4abc84d1441f'
        name: '&aLinear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma cruz.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: 'a8259df25c9de155b063cbef86646574d694eff3ad8d4d0cc64c4abc84d1441f'
        name: '&aLinear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma cruz.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: 'a8259df25c9de155b063cbef86646574d694eff3ad8d4d0cc64c4abc84d1441f'
        name: '&aLinear'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma cruz.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  inverted-destructor:
    name: 'Destruidor Invertido'
    pickaxe-level: 0
    order: 17
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    animation: true
    level:
      default: 0.0
      maximum: 10.0
    messages:
      title: '&cDestruidor Invertido<nl>&cativado'
      actionbar: ''
      chat: ''
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '4f824d1622d00457816ba02c7fa6602d7d6d11dfa3c9684e0d94412ed59e8424'
        name: '&aDestruidor Invertido'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a coluna inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '4f824d1622d00457816ba02c7fa6602d7d6d11dfa3c9684e0d94412ed59e8424'
        name: '&aDestruidor Invertido'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a coluna inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: '4f824d1622d00457816ba02c7fa6602d7d6d11dfa3c9684e0d94412ed59e8424'
        name: '&aDestruidor Invertido'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a coluna inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: '4f824d1622d00457816ba02c7fa6602d7d6d11dfa3c9684e0d94412ed59e8424'
        name: '&aDestruidor Invertido'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a coluna inteira.'
          - '&7de coins.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  multiplier:
    name: 'Multiplicador'
    pickaxe-level: 0
    order: 12
    show-menu: true
    can-buy: true
    show-infinity: false
    level-multiplier: 0.15
    providers-multiplier:
      - 'money'
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'money'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'money'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'money'
        price: 100.0
    displays:
      can:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem coins suficientes.'
      permission:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem permissão para evoluir este.'
      maximum:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="mines" collapsible="true">
<chapter title="redstone.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome da ESTRUTURA
display-name: '&aTorre de Cacto'

# Bloco que irá aparecer no preview caso esteja bloqueado de por
preview-block: 'STAINED_GLASS:14'

# Tempo de reset da mina
# em segundos
reset-time: 600

# Porcentagem de blocos restantes para resetar a mina
percentage-reset: 10.0

# Alterar a altura do y ao colocar (se quiser colocar pra setar no ar/setar dentro do solo)
y-offset: 0

# Blocos que serão desconsiderados e removidos ao setar a estrutura
block-blacklist: [ 'GRASS', 'STONE' ]

# Colocar de modo gradual
gradual: false

# Item que o jogador irá receber
item:
  material: f9033bbf23a40e409cd0c1eaecab6b1c0dc6b3c31e253a06550b22bce9899575
  name: '&aMina Privada'
  lore:
    - '&7Para iniciar a minerar nessa'
    - '&7mina coloque-a em sua plot!'
    - ''
    - '&fTamanho: &77x6'
    - ''
    - '&fSHIFT + Direito'

# Preços dos blocos da mina
mine-block-prices:
  block1:
    type: 'REDSTONE_ORE:0'
    # EXP do minecraft vanilla
    xp: 1
    # EXP do mcMMO (MINING)
    xp-mcmmo: 1
    # Valores de economias
    prices:
      price1:
        provider: 'money'
        amount: 100.0
  block2:
    type: 'GLOWING_REDSTONE_ORE:0'
    xp: 1
    xp-mcmmo: 1
    prices:
      price1:
        provider: 'money'
        amount: 100.0
  block4:
    type: 'REDSTONE_BLOCK:0'
    xp: 1
    xp-mcmmo: 1
    prices:
      price1:
        provider: 'money'
        amount: 500.0

# Recompensas dos blocos da mina
mine-block-rewards:
  block1:
    type: 'REDSTONE_ORE:0'
    rewards:
      - '10.0,reward1'
  block4:
    type: 'REDSTONE_BLOCK:0'
    rewards:
      - '50.0,reward2'

# Sistema de resetar a própria mina
manual-reset:
  enabled: true
  # em segundos
  delay: 600
  # Permissão para resetar
  permission: 'yminaspv.reset.self'
  # Preços para resetar
  prices:
    price1:
      provider: 'money'
      amount: 100.0

# Mensagens
messages:
  # Mensagens ao quebrar um bloco
  sell:
    title: ''
    actionbar: '&a+{money} coins adicionados ┃ &r{bonus}&a.'
    chat: ''
  # Mensagens ao resetar
  reset:
    title: '&aMINA<nl>&aRESETADA'
    actionbar: '&aMINA RESETADA'
    chat: ''

# Siglas de cada bloco para identificação no pattern
blocks:
  - '1,STONE:0'
  - '4,REDSTONE_ORE:0'
  - 'X,AIR:0'
  - '2,COBBLESTONE:0'
  - '3,REDSTONE_BLOCK:0'
  - '0,SPONGE:0'

# Modelagem da estrutura
patterns:
  layer_1:
    y: 1
    pattern:
      - '00000000'
      - '01111120'
      - '01111110'
      - '01111110'
      - '01111110'
      - '01111110'
      - '01111110'
      - '01111110'
      - '00000000'
  layer_2:
    y: 2
    pattern:
      - 'XXXXXXXX'
      - 'X333334X'
      - 'X444444X'
      - 'X433344X'
      - 'X444433X'
      - 'X434443X'
      - 'X344433X'
      - 'X334334X'
      - 'XXXXXXXX'
  layer_3:
    y: 3
    pattern:
      - 'XXXXXXXX'
      - 'X443343X'
      - 'X343344X'
      - 'X334333X'
      - 'X443333X'
      - 'X444333X'
      - 'X333333X'
      - 'X343443X'
      - 'XXXXXXXX'
  layer_4:
    y: 4
    pattern:
      - 'XXXXXXXX'
      - 'X443333X'
      - 'X344433X'
      - 'X443344X'
      - 'X433433X'
      - 'X434344X'
      - 'X343434X'
      - 'X434434X'
      - 'XXXXXXXX'
  layer_5:
    y: 5
    pattern:
      - 'XXXXXXXX'
      - 'X334344X'
      - 'X433434X'
      - 'X334334X'
      - 'X344444X'
      - 'X444444X'
      - 'X344434X'
      - 'X334334X'
      - 'XXXXXXXX'
  layer_6:
    y: 6
    pattern:
      - 'XXXXXXXX'
      - 'X434343X'
      - 'X343433X'
      - 'X434334X'
      - 'X334434X'
      - 'X344333X'
      - 'X433443X'
      - 'X343444X'
      - 'XXXXXXXX'
  layer_7:
    y: 7
    pattern:
      - 'XXXXXXXX'
      - 'X344334X'
      - 'X343444X'
      - 'X333343X'
      - 'X433443X'
      - 'X343434X'
      - 'X433343X'
      - 'X434444X'
      - 'XXXXXXXX'
  layer_8:
    y: 8
    pattern:
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
      - 'XXXXXXXX'
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
  minepv: 'minepv|minapv|minaspv'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         __  __ _                 ____
#  _   _|  \/  (_)_ __   __ _ ___|  _ \__   __
# | | | | |\/| | | '_ \ / _` / __| |_) \ \ / /
# | |_| | |  | | | | | | (_| \__ \  __/ \ V /
#  \__, |_|  |_|_|_| |_|\__,_|___/_|     \_/
#  |___/
#
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

# Modo de depuração para correção de problemas no plugin.
debug-mode: false

#      ___      _        _
#     /   \__ _| |_ __ _| |__   __ _ ___  ___
#    / /\ / _` | __/ _` | '_ \ / _` / __|/ _ \
#   / /_// (_| | || (_| | |_) | (_| \__ \  __/
#  /___,' \__,_|\__\__,_|_.__/ \__,_|___/\___|
#
# Configurações do banco de dados.

database:
  # Determina o tipo de banco de dados. Valores válidos: [SQLITE, MYSQL, HIKARI (recomendado)]
  storage-type: SQLITE

  # Dados para conexão ao banco de dados MYSQL.
  data:
    # Endereço de conexão do banco de dados. [EX: 127.0.0.1]
    host: localhost
    # Porta de conexão do banco de dados. [EX: 3306]
    port: 3306
    # Nome do banco de dados a ser conectado. [EX: minecraft]
    database: ''
    # Usuário de conexão. [EX: root]
    username: ''
    # Senha do usuário de conexão: [EX: 123]
    password: ''

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Coloque o identificador da sua skill de mineração do mcMMO ou AuraSkills
mining-skill-identify: 'MINING'

general:
  # Acumular os bônus que tiver permissão
  accumulate-bonus: false
  formatter-bonus-has: '&a+{bonus}% por ser {display}&a.'
  formatter-bonus-no-has: ''
  # Ativar o preview no shift
  shift-preview-enabled: true
  # Ativar o preview sem shift
  no-shift-preview-enabled: true
  # Ativar o place no shift
  shift-place: true
  # Ativar o place sem shift
  no-shift-place: false
  # Tempo que levará para atualizar o preview
  # em ticks (20 ticks = 1 segundo)
  refresh-time: 5
  # Distância do preview
  # em blocos
  preview-distance: 7
  # Máximo de minas privadas que um jogador poderá ter
  player-max-mines: 1
  # Máximo de amigos que uma mina privada poderá ter
  mine-max-friends: 10
  # Habilitar o menu de evolução ao interagir com a picareta sem shift
  no-shfit-evolution: true
  # Habilitar o menu de evolução ao interagir com a picareta com shift
  shfit-evolution: true
  # Habilitar o price-multiplier de maneira exponencial
  # Vai multiplicar sempre o x pelo valor do nível anterior já multiplicado
  # Caso false, vai apenas multiplicar o valor atual do encantamento x o multiplicador
  price-multiplier-exponential: true
  # Evoluir a picareta com a ação do botão direito
  evolute-right: true
  # Evoluir a picareta com a ação do botão Q
  evolute-q: true
  # Máximo permitido para evoluir com Q
  evolute-q-max: 1000
  # Máximo permitido para evoluir com Direito
  evolute-right-max: 1000
  # Esconder o encantamento na lore da picareta caso o player desative ele
  # caso esteja false, o encantamento ficará riscado na lore da picareta
  hide-deactivated: false

# Item da picareta customizada
pickaxe:
  unbreakable: true
  material: DIAMOND_PICKAXE
  name: '&bPicareta &7(Mina Privada)'
  lore:
    - '&7Inquebrável ∞'
    - '{enchants}'

# Você pode criar quantos bônus quiser
# Será dado o bônus ao minerar.
bonus:
  membros:
    order: 1
    # Permissão para ser reconhecido
    permission: 'yminaspv.bonus.membro'
    # Nome que irá aparecer nas mensagens
    display: '&7[Membro]'
    # Quantia do bônus em %
    bonus: 10.0

# Enviar a mensagem de recompensas ganhas a cada x tempo
reward-message:
  enabled: true
  # delay para enviar a mensagem
  # em segundos
  delay: 60
  message: |
    &r
    &eMina Privada
    &7Suas recompensas do último minuto.
    &r
    {chat}
    &r

# Enviar a mensagem de montantes ganhos a cada x tempo
earns-message:
  enabled: true
  # delay para enviar a mensagem
  # em segundos
  delay: 60
  chat-format: '&6&l|&f {provider_display}: &2{provider_symbol}&f{provider_value}'
  message: |
    &r
    &e&lGG! &eVocê quebrou &e&l{blocks}&e blocos no último minuto.
    &r
    &6Confira o lucro dos blocos quebrados:
    {chat}
    &r
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
  money:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'Money'
    # Formato inteiro
    display: 'Dinheiro'
    # Formato abreviado
    abbreviated: 'coins'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permitir a fortuna multiplicar essa economia
    allow-fortune: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yminaspv.provider.money'
    # Formato do símbolo
    symbol: '$'
]]>
</code-block>
</chapter>

<chapter title="menus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___ _ __  _   _ ___
#   /    \ / _ \ '_ \| | | / __|
#  / /\/\ \  __/ | | | |_| \__ \
#  \/    \/\___|_| |_|\__,_|___/
#
# Sistema de menus.

# Setas dos menus.
arrows:
  back:
    material: 'ARROW:0'
    name: '&cVoltar'
    lore: ['&7Clique para voltar ao menu anterior.']
  previous:
    material: 'ARROW:0'
    name: '&cAnterior'
    lore: ['&7Clique para ir à página anterior.']
  next:
    material: 'ARROW:0'
    name: '&aPróximo'
    lore: ['&7Clique para ir à próxima página.']

# Menu principal
main:
  name: '&8Mineração'
  size: 27
  items:
    reset-slot: 10
    info-slot: 11
    pickaxe-slot: 13
    friends-slot: 15
    remove-slot: 16
    info:
      material: 'PAPER'
      name: '&aInformações'
      lore:
        - '&7Visualize o status e informações'
        - '&7gerais da sua mina privada.'
        - ''
        - ' &8> &fBlocos: &c{blocks_mined}&7/&a{blocks_total}'
        - ' &8> &fAmigos: &a{friends}'
        - ' &8> &fTempo para resetar: &a{time}'
        - ''
    pickaxe:
      material: 'DIAMOND_PICKAXE'
      name: '&aPicareta'
      lore:
        - '&7Garanta sua picareta e comece já'
        - '&7a sua jornada de mineração.'
        - ''
        - '&aClique para pegar.'
    friends:
      material: 'EMERALD'
      name: '&aAmigos'
      lore:
        - '&7Gerencie quem pode minerar junto'
        - '&7contigo nessa mina.'
        - ''
        - '&f> Quantia: &a{friends}'
        - ''
        - '&aClique para gerenciar.'
    # icon to remove mine
    remove:
      material: 'BARRIER'
      name: '&cRemover'
      lore:
        - '&7Remova sua estrutura de mina e'
        - '&7pegue ela em item novamente.'
        - ''
        - '&aClique para remover.'
    reset-permission:
      material: 924757bc9a3171f9d0fdfbd209ac42e15f7744eb5f2db31920ff8af8d94567c6
      name: '&aResetar'
      lore: [ '&cVocê não tem permissão para isso.' ]
    reset-time:
      material: 924757bc9a3171f9d0fdfbd209ac42e15f7744eb5f2db31920ff8af8d94567c6
      name: '&aResetar'
      lore: [ '&cAguarde {time} para resetar novamente.' ]
    reset:
      material: 924757bc9a3171f9d0fdfbd209ac42e15f7744eb5f2db31920ff8af8d94567c6
      name: '&aResetar'
      lore:
        - '&7Resete sua mina por completo'
        - '&7e minere mais blocos.'
        - ''
        - '&fPreço: &a{money}'
        - ''
        - '&aClique para resetar.'

# Menu de evolução
evolution:
  name: '&8Mineração'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  items:
    pickaxe-slot: 47
    filter-slot: 49
    disenchanter-slot: 51
    filter:
      material: HOPPER
      glow: true
      name: '&aFiltro'
      lore:
        - '&7Desabilite encantamentos que não'
        - '&7queira utilizar no momento.'
        - ''
        - '&aClique para acessar'
    disenchanter:
      material: ANVIL
      glow: true
      name: '&aDesencantador'
      lore:
        - '&7Desencante encantamentos que não'
        - '&7queira utilizar e receba o valor'
        - '&7de volta.'
        - ''
        - '&aClique para acessar'

# Menu de filtro
filter:
  name: '&8Mineração'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  items:
    pickaxe-slot: 31
    enchant:
      name: '&a{enchant}'
      lore:
        - ''
        - '&fEncantamento: &7{enchant}'
        - '&fDesativado: &7{status}'
        - ''

# Menu de desencantador
disenchanter:
  name: '&8Mineração'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  items:
    pickaxe-slot: 31
    enchant:
      name: '&a{enchant}'
      lore:
        - ''
        - '&fEncantamento: &7{enchant}'
        - '&fNíveis: &7{level}'
        - ''
        - '&fIrá ganhar &a{money} coins&f.'
        - ''
        - '&aBotão &fESQUERDO &apara desencatar 1 nível'
        - '&aBotão &fDIREITO &apara desencatar {level} níveis'

# Menu de amigos
friends:
  name: '&8Mineração'
  size: 54
  slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
  previous-slot: 9
  next-slot: 17
  back-slot: 18
  items:
    add-slot: 27
    add:
      material: '8e9b27fccd80921bd263c91dc511d09e9a746555e6c9cad52e8562ed0182a2f'
      name: '&aAdicionar amigo'
      lore:
        - '&7Clique aqui para adicionar'
        - '&7amigos para poder usar'
        - '&7esta mina.'
    friend:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&aBotão &fDIREITO&a para deletar.'
        - ''
]]>
</code-block>
</chapter>

<chapter title="messages.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___  ___ ___  __ _  __ _  ___  ___
#   /    \ / _ \/ __/ __|/ _` |/ _` |/ _ \/ __|
#  / /\/\ \  __/\__ \__ \ (_| | (_| |  __/\__ \
#  \/    \/\___||___/___/\__,_|\__, |\___||___/
#                              |___/
#
# Plugin messages

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  inv-full: '&cO seu inventário está cheio.'
  help: |

    &a/minaspv give &8- &7Dar uma mina para um/todos os jogadores.
    &a/minaspv reload &8- &7Recarrega as configurações.

  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  mine-give: '&aVocê deu &7{amount}x {mine}&a para o jogador &7{player}&a.'
  mine-received: '&aVocê recebeu &7{amount}x {mine}&a.'
  mine-list: |
    &cMina não encontrada.
    &cMinas disponíveis: &f{list}
  mine-max: '&cVocê já possui o máximo de minas privadas ativas. &7({max})'
  mine-activated: '&aVocê ativou &7{amount}x {mine}&a.'
  mine-found: '&cVocê não está em nenhuma mina privada.'
  mine-reset-time: '&cVocê deve aguardar {time} para resetar esta mina novamente.'
  mine-reset-permission: '&cVocê não tem permissão para resetar esta mina.'
  mine-reset-full: '&cNão há blocos para resetar nessa mina.'
  mine-reset: '&aVocê resetou sua mina.'
  mine-remove-empty: '&cA mina precisa está resetada para conseguir removê-la.'
  mine-remove-owner: '&cSomente o dono da mina consegue removê-la.'
  mine-removed: '&aMina removida com sucesso.'
  mine-just-owner: '&cSomente o dono da mina consegue realizar essa ação.'
  mine-friend-digit-add: |

    &aDigite no chat o nome do seu amigo que quer adicionar.'
    &7para cancelar digite &ncancelar&7.'

  digit-enchant: |

    &aDigite a quantia de níveis que você quer adquirir ao encantamento &f{enchantment}&a.
    &7para cancelar digite &ncancelar&7.

  mine-friend-max: '&cEsta mina privada atingiu o limite máximo de amigos.'
  mine-friend-add-owner: '&cVocê não pode adicionar o dono como amigo na mina privada.'
  mine-friend-already-added: '&cEste jogador já está adicionado.'
  mine-friend-added: '&aVocê adicionou o jogador &7{player}&a na sua mina privada.'
  mine-pickaxe-has: '&cVocê já possui uma picareta no inventário.'
  enchantment-evolved: '&aO encantamento &f{enchantment}&a foi evoluido para o nível &f{level}&a.'
  enchantment-cant-buy: '&cVocê não pode comprar esse encantamento.'
  enchantment-exceeds: '&cEstes níveis excedem o nível máximo do encantamento.'
  enchantment-has-level: '&cVocê não possui a quantia de &f{level}&c níveis necessários.'
  enchantment-disenchanted: '&aVocê desencantou &f{level} níveis &ado encantamento &f{enchant}&a.'
  enchantment-permission: '&cVocê não tem permissão para evoluir este encantamento.'
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
    # Mensagens que serão enviadas ao receber a recompensa
    messages:
      # Quantia que irá multiplicar na placeholder de recompensas no chat
      amount-placeholder: 64
      title: '&a+64 Pedras'
      actionbar: ''
      chat: '&a+{amount} Pedras'
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
    messages:
      amount-placeholder: 1
      title: '&a+1 Diamante'
      actionbar: ''
      chat: '&a+{amount} Diamante'
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
    messages:
      amount-placeholder: 1
      title: '&a+1 Esmeralda'
      actionbar: ''
      chat: '&a+{amount} Esmeralda'
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/162-yMinasPv">Site do plugin yMinasPv</a>
    </category>
</seealso>