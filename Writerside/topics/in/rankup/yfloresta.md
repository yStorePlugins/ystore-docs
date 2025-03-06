# yFloresta
<secondary-label ref="rankup"/>

### Descrição
Crie plantações de árvores que dão dinheiro ao quebrá-las

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
<video src="//www.youtube.com/watch?v=ruLdcff_UK0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/floresta - Abre o menu principal
/floresta ajuda - Envia a mensagem de ajuda
/floresta ir - Vai até a área de floresta
/floresta sair - Sai da área de floresta
/floresta blocos - Abre o menu de blocos cadastrados
/floresta armazem - Abre o menu de recompensas armazenadas
/floresta top - Abre o menu de top
/folhas - Vê a quantia de corais
/folhas [player] - Vê a quantia de folhas de um jogador
/folhas enviar - Envia suas folhas para um jogador
/folhas add - Adiciona folhas para um jogador
/folhas give - Dá folhas em forma de itens para um jogador
/folhas set - Seta folhas para um jogador
/folhas remove - Remove folhas de um jogador
/floresta setspawn - Seta o local de spawn da área da floresta.
/floresta setareaspawn - Seta o local de spawn da área customizada da floresta.
/floresta setsaida - Seta a saída da área da floresta.
/floresta givebooster - Dá um booster à um jogador.
/floresta giveskin - Dá uma skin à um jogador em forma de item.
/floresta giveskindireto - Dá uma skin à um jogador
/floresta removerskin - Remove a skin de um jogador.
/floresta addclasse - Adiciona classe a um jogador.
/floresta removerclasse - Remove a classe de um jogador.
/floresta setarclasse - Seta a classe de um jogador.
/floresta resetarclasse - Reseta a classe de um jogador.
/floresta reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yfloresta.use - Permissão para o /floresta, /floresta blocos, /floresta armazem, /floresta top
yfloresta.go - Permissão para o /floresta ir
yfloresta.exit - Permissão para o /floresta sair
yfloresta.coin.use - Permissão para o /folhas
yfloresta.coin.look - Permissão para o /folhas [player]
yfloresta.coin.send - Permissão para o /folhas enviar
yfloresta.coin.help - Permissão para o /folhas ajuda
yfloresta.coin.add - Permissão para o /floresta add
yfloresta.coin.remove - Permissão para o /floresta remove
yfloresta.coin.set - Permissão para o /floresta set
yfloresta.coin.give - Permissão para o /floresta give
yfloresta.setspawn - Permissão para o /floresta setspawn
yfloresta.setexit - Permissão para o /floresta setexit
yfloresta.givebooster - Permissão para o /floresta givebooster
yfloresta.setareaspawn - Permissão para o /floresta setareaspawn
yfloresta.admin.giveskin - Permissão para o /floresta giveskin
yfloresta.admin.giveskindireto - Permissão para o /floresta giveskindireto
yfloresta.admin.removeskin - Permissão para o /floresta removeskin
yfloresta.admin.addclasse - Permissão para o /floresta addclasse
yfloresta.admin.removeclasse - Permissão para o /floresta removeclasse
yfloresta.admin.setclasse - Permissão para o /floresta setclasse
yfloresta.admin.resetclasse - Permissão para o /floresta resetclasse
yfloresta.reload - Permissão para o /floresta reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yfloresta_time% - Retorna o tempo que o jogador ficou na floresta
%yfloresta_time_raw% - Retorna o tempo que o jogador ficou na floresta sem formatar
%yfloresta_broken% - Retorna a quantia de blocos que o jogador quebrou
%yfloresta_broken_raw% - Retorna a quantia de blocos que o jogador quebrou sem formatar
%yfloresta_coin% - Retorna a quantia de folhas do jogador
%yfloresta_coin_raw% - Retorna a quantia de folhas do jogador sem formatar
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yFloresta/
    ├── enchantments/
    │    ├── custom_enchants.yml
    │    └── enchants.yml
    ├── areas.yml
    ├── blocks.yml
    ├── boosters.yml
    ├── bungeecord.yml
    ├── classes.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    ├── rewards.yml
    └── skins.yml
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
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    commands: ['100.0,give {player} STONE 1']
    displays:
      can:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: TRIPWIRE_HOOK
        name: '&aChaveiro'
        lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Apague apenas os encantamentos que não for usar
enchants:
  efficiency: # Não mude este nome, ou o encantamento não será reconhecido
    name: 'Eficiência'
    # Nível da picareta necessário para poder evoluir o encantamento
    pickaxe-level: 0
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
      default: 0.0 # deixe um valor alto aqui (pra não bugar os packets)
      maximum: 25.0 # Use -1 para ser infinito
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
      # Ativar dar blocos
      blocks: true
      # Ativar os custom enchant
      custom-enchant: true
      # Ativar os mine_rewards
      rewards: true
    prices-default:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
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
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
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
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
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
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: GOLD_INGOT
        name: '&aFortuna'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
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
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na floresta.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na floresta.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: FEATHER
        name: '&aVelocidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na floresta.'
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
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na floresta.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na floresta.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        name: '&aPressa'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na floresta.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - ''
          - '&cVocê já está no máximo.'

  lucky:
    name: 'Sortudo'
    pickaxe-level: 0
    order: 8
    show-menu: true
    can-buy: true
    show-infinity: false
    animation: true
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        name: '&aSortudo'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte ao achar recompensas.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        name: '&aSortudo'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte ao achar recompensas.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        name: '&aSortudo'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte ao achar recompensas.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
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
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
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
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
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
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
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
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
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
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
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
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
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

  multiplier:
    name: 'Multiplicador'
    pickaxe-level: 0
    order: 12
    show-menu: true
    can-buy: true
    show-infinity: false
    level-multiplier: 0.15
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Multiplicador Atual: &b{multiplier}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Multiplicador Atual: &b{multiplier}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        name: '&aMultiplicador'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Multiplicador Atual: &b{multiplier}%&f.'
          - ''
          - '&cVocê já está no máximo.'

  eletricity:
    name: 'Eletricidade'
    pickaxe-level: 0
    order: 13
    show-menu: true
    can-buy: true
    show-infinity: false
    level-percentage: 0.15
    level:
      default: 0.0
      maximum: 10.0
    prices-default:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: '9ac52419b99025828c89fa825945e6948e45bb5a22e4425a59e9096e4c1ac38'
        name: '&aEletricidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais energia ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      cant:
        material: '9ac52419b99025828c89fa825945e6948e45bb5a22e4425a59e9096e4c1ac38'
        name: '&aEletricidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais energia ao desmatar.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: '9ac52419b99025828c89fa825945e6948e45bb5a22e4425a59e9096e4c1ac38'
        name: '&aEletricidade'
        lore:
          - '&7Este encantamento permite que você'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - '&7ganhe mais energia ao desmatar.'
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
        provider: 'yfloresta'
        price: 10000.0
    prices-per-level:
      price1:
        provider: 'yfloresta'
        price: 10000.0
    prices-disenchanter:
      price2:
        provider: 'yfloresta'
        price: 100.0
    displays:
      can:
        material: '7ff91e15b31fe4cfda13fb44634da87a75ba2c17fce7b524a55a314f5aa99d9f'
        name: '&aEsfera'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma esfera.'
          - '&7de blocos.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
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
          - '&7de blocos.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&f > Custo: &a{yfloresta} folhas&f.'
          - '&f > Nível necessário: &a{level}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      maximum:
        material: '7ff91e15b31fe4cfda13fb44634da87a75ba2c17fce7b524a55a314f5aa99d9f'
        name: '&aEsfera'
        lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar uma esfera.'
          - '&7de blocos.'
          - ''
          - '&f > Nível: &b{actual}&f/&b{maximum}&f.'
          - '&f > Porcentagem Atual: &b{percentage}%&f.'
          - ''
          - '&cVocê já está no máximo.'

]]>
</code-block>
</chapter>

</chapter>

<chapter title="areas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
areas:
  area1:
    # Ordem da área para compra
    order: 1
    # Permissão para comprar a área
    permission: ''
    # NÃO ALTERAR
    location: 'none'
    # Preços para comprar a área
    costs:
      price1:
        provider: 'money'
        amount: 1000.0
    # Itens do menu
    icon:
      buy:
        material: 'LOG:1'
        name: '&aÁrea {order} &8(Savana)'
        lore:
          - '&7Área: &b{order}'
          - '&7Floresta: &bSavana'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aClique para comprar'
      previous:
        material: 'LOG:1'
        name: '&aÁrea {order} &8(Savana)'
        lore:
          - '&7Área: &b{order}'
          - '&7Floresta: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&cVocê precisa comprar a anterior'
      has:
        material: 'LOG:1'
        name: '&aÁrea {order} &8(Savana)'
        lore:
          - '&7Área: &b{order}'
          - '&7Floresta: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aVocê já possui esta area'
      equipped:
        material: 'LOG:1'
        name: '&aÁrea {order} &8(Savana)'
        lore:
          - '&7Área: &b{order}'
          - '&7Floresta: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aVocê está nessa area'
]]>
</code-block>
</chapter>

<chapter title="blocks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
blocks:
  log:
    # Permissão para quebrar o bloco
    permission-break: ''
    # Mensagem de permissão
    permission-message: '&cVocê ainda não pode quebrar a MADEIRA BRUTA.'
    # Delay para resetar
    # em segundos
    delay: 10
    materials:
      # material que deverá ser quebrado
      break-material: 'LOG:0'
      # material que vai virar ao quebrar
      to-material: 'BEDROCK:0'
      # material que vai virar ao resetar
      reset-material: 'LOG:0'
    effects:
      # efeito ao quebrar
      break-particle: ''
      # som ao quebrar
      break-sound: ''
      # efeito ao resetar
      reset-particle: 'HAPPY_VILLAGER'
      # som ao resetar
      reset-sound: ''
    sells:
      sell1:
        order: 1
        permission: ''
        # holograma de venda
        hologram: [ '&a+{money}' ]
        # Altura que o holograma vai spawnar no bloco
        hologram-off-set: 0.6
        # mensagens de venda
        message:
          actionbar: '&e&lFLORESTA: &a+{money} coins &7(+{bonus}%)'
          title: ''
          chat: ''
        # quantidade de folhas que será dada
        coin: 1.0
        # quantidade que será dada em outras economias
        prices:
          price1:
            provider: 'money'
            price: 1.0
        # As recompensas são cadastradas na rewards.yml
        # Use: chance,recompensa
        # Quantia de recompensas que serão dadas
        reward-amount: 1
        # Dropar as recompensas no chão
        reward-ground: false
        rewards: [ '100,reward1' ]
]]>
</code-block>
</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
boosters:
   booster1:
      # Duração do booster em segundos
      time: 60
      # Bônus de venda
      bonus: 10.0
      # Bônus de folhaws
      bonus-leaves: 10.0
      # Item do booster
      item:
         material: EXP_BOTTLE
         glow: true
         name: '&aBônus de Floresta'
         lore: [ '', '&aTempo: &e{time}', '&aBônus de coins: &e{bonus}%', '&aBônus de folhas: &e{bonus-leave}%', '' ]
]]>
</code-block>
</chapter>

<chapter title="bungeecord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     ___                                               _
#    / __\_   _ _ __   __ _  ___  ___  ___ ___  _ __ __| |
#   /__\// | | | '_ \ / _` |/ _ \/ _ \/ __/ _ \| '__/ _` |
#  / \/  \ |_| | | | | (_| |  __/  __/ (_| (_) | | | (_| |
#  \_____/\__,_|_| |_|\__, |\___|\___|\___\___/|_|  \__,_|
#                     |___/
#
# Sistema de múltiplos servidores.

# Ativar o sistema de bungeecord
enabled: false

# Modo deste servidor
# LOBBY (ex: servidor de RankUP)
# SERVER (ex: servidor que contém a floresta)
mode: 'LOBBY'

# Nome do servidor na config do BungeeCord em que o jogador vai ao sair da floresta
exit: 'rankup'

# Nome do servidor na config do BungeeCord em que o jogador vai ao entrar na floresta
entry: 'mina'

# Delay para enviar a vara ao trocar para o servidor da floresta
# em ticks
delay: 3

# Bloquear ações neste servidor caso esteja fora da floresta
# Somente caso o "Modo" for "SERVER"
# permissão de bypass: yfloresta.blocked.bypass
block-actions: true
]]>
</code-block>
</chapter>

<chapter title="classes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
classes:
  class1:
    # O padrão é a ordem 0
    order: 0
    display: '&fQuartzo'
    # Cor da armadura
    # Formato: RED:GREEN:BLUE (255:255:255)
    # deixe RAINBOW para ser colorido
    color: '255:255:255'
    # Permissão para evoluir à esta classe
    # Deixe '' (vazio) para não usar
    permission: ''
    # Efeito:Nível
    effects: ['SPEED:1']
    # Bônus que serão dados
    bonus:
      leaves: 5
      coin: 10
    # Custos de evolução
    prices:
      price1:
        provider: 'money'
        price: 1000.0
      price2:
        provider: 'money'
        price: 1000.0
    # Itens da armadura
    armor:
      helmet:
        material: LEATHER_HELMET
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
      chestplate:
        material: LEATHER_CHESTPLATE
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
      leggings:
        material: LEATHER_LEGGINGS
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
      boots:
        material: LEATHER_BOOTS
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
    # Itens do menu de classes
    menu:
      buy:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - ''
          - '&aClique para evoluir'
      has:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
          - '&aClique para equipar.'
      equipped:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
          - '&aVocê está usando este.'
      need:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - ''
          - '&cVocê não possui os custos para evoluir.'
      previous:
        material: LEATHER_CHESTPLATE
        color: '255:255:255'
        name: '&fClasse Quartzo'
        lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7chance e coins na floresta!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{leaves}% de folhas'
          - '&7- +{coin}% de coins'
          - ''
          - '&cVocê não possui a classe anterior.'
]]>
</code-block>
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
  floresta: 'floresta'
  coin: 'folhas|folha'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _____ _                     _
#  _   _|  ___| | ___  _ __ ___  ___| |_ __ _
# | | | | |_  | |/ _ \| '__/ _ \/ __| __/ _` |
# | |_| |  _| | | (_) | | |  __/\__ \ || (_| |
#  \__, |_|   |_|\___/|_|  \___||___/\__\__,_|
#  |___/
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

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Altura do void do seu servidor
void-detect: 0

general:
  # Acumular os bônus que tiver permissão
  accumulate-bonus: false
  formatter-bonus-has: '&a+{bonus}% por ser {display}&a.'
  formatter-bonus-no-has: ''
  # Ativar a invisibilidade na área da floresta
  invisibility: false
  # Esconder o encantamento na lore da ferramenta caso o player desative ele
  # caso esteja false, o encantamento ficará riscado na lore da ferramenta
  hide-deactivated: false
  # Fazer com que a ferramenta nunca quebre
  tool-unbreakable: true
  # Permitir a troca de itens via numkeys
  numkeys: false
  # Habilitar o menu de evolução ao interagir com a ferramenta sem shift
  no-shfit-evolution: true
  # Habilitar o menu de evolução ao interagir com a ferramenta com shift
  shfit-evolution: true
  # Para evoluir as classes ele deverá seguir a ordem delas?
  classes-order: true
  # Evoluir a picareta com a ação do botão direito
  evolute-right: true
  # Evoluir a picareta com a ação do botão Q
  evolute-q: true
  # Máximo permitido para evoluir com Q
  evolute-q-max: 0
  # Skin default da picareta
  skin-default: ''
  # Necessitar estar com o inv vazio
  inv-empty: false
  # Materiais que irão ser reconhecidos na skin
  skin-materiais:
    - 'WOOD'
    - 'STONE'
    - 'IRON'
    - 'GOLD'
    - 'DIAMOND'
  # Lista de comandos permitidos na floresta
  commands-allowed:
    - '/g'
    - '/l'
    - '/floresta'
    - '/florestas'
  # Lista de comandos para sair da floresta
  commands-exit:
    - '/sair'
    - '/spawn'
    - '/exit'

# Sistema de energia
energy:
  # Ativar o sistema de energia
  enabled: true
  # Quantia de energia por bloco quebrado
  amount: 1
  # Quantia de energia que irá aumentar a cada nível
  per-level: 1000
  # Ativar o sistema de dar encantamento aleatório
  give-enchant: true
  # Comandos que irá dar quando evoluir (com enchant)
  enchant-commands: []
  # Comandos que irá dar quando evoluir (sem enchant)
  no-enchant-commands: []
  # Enchants que poderão ser dados
  # chance,encantamento
  enchants:
    - '10.0,efficiency'
    - '10.0,nuclear'
    - '10.0,destructor'
    - '10.0,explosion'
    - '10.0,laser'
    - '10.0,drill'
    - '10.0,inverted-destructor'
    - '10.0,linear'
    - '10.0,sphere'
    - '10.0,x'
    - '10.0,fortune'
    - '10.0,summoner'
    - '10.0,speed'
    - '10.0,haste'
    - '10.0,lucky'
    - '10.0,multiplier'
    - '10.0,eletricity'
  # Mensagens
  enchant-evolved: |
    &r
    &bSua ferramenta evoluiu de nível!
    &bEncantamento adquirido: &f+1 nível de {enchantment}&b.
    &r
  no-enchant-evolved: |
    &r
    &bSua ferramenta evoluiu de nível!'
    &cInfelizmente todos seus encantamentos estão no máximo.'
    &r
  # Comandos que serão executados ao alcançar determinado nível
  # nível-necessário,cmd
  specific-rewards: [ '100,give {player} diamond 2' ]

# Sistema de encantamento aleatório por chance
random:
  chance: 0
  title: ''
  actionbar: ''
  chat: |
    &r
    &bEncantamento adquirido: &f+1 nível de {enchantment}&b.
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

# Item da ferramenta
tool:
  material: WOOD_AXE
  name: '&bMachado &6[{blocks_broken}]'
  lore:
    - '&7Inquebrável ∞'
    - '{enchants}'
    - ''
    - ' &fNível: &7{level}'
    - ' &fEnergia: &7{energy}/{energy_next} &f({progressbar}&f)'

# Item de folha ativável
leave:
  material: '1ba16c3890af39c3f2d576586cff443de07dad32b2315e2ff6f0d5d6a3c663dd'
  name: '&b+{amount} Folhas'
  lore:
    - ''
    - '&fQuantia: &b{amount}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus blocos no inventário em 1 só.'
    - ''

scoreboard:
  enabled: true
  title: '&b&lyStore'
  lines:
    - '&7     Área de Floresta'
    - ''
    - '&f B. quebrados: &7{blocks_broken}'
    - ''
    - '&e Machado'
    - '&8  ❘&f Nível: &7{level}'
    - '&8  ❘&f Energia: &7{energy}/{energy_next}'
    - ''
    - '&f Folhas: &e⛃{leaves}'
    - '&f Coins: &2$&a{money}'
    - ''
    - '&b    ystoreplugins.com.br'

# Itens padrões definidos para o jogador.
items:
  tool-slot: 2
  # Item utilizado para que o jogador saia da pesca.
  exit:
    material: 'BARRIER:0'
    slot: 8
    name: '&cSair da Ferramenta'
    lore:
      - '&7Clique para sair da'
      - '&7área de floresta.'
  # Item utilizado para que o jogador saia da pesca.
  classes:
    material: 'LEATHER_CHESTPLATE:0'
    slot: 6
    name: '&bClasses'
    lore:
      - ' &7As classes irão te dar mais'
      - ' &7chance e coins na floresta!'
      - ''
      - '&fSua classe: &7{classe}'
      - ''
      - '&aClique para upar sua classe'
  # Siga o exemplo abaixo para criar itens custom
  #custom:
  #  material: BARRIER:0
  #  slot: 0
  #  name: ''
  #  lore: []
  #  left-command: ''
  #  right-command: ''
  #  left-perm: 'yfloresta.left-perm.custom'
  #  right-perm: 'yfloresta.right-perm.custom'

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'

# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender as platanções.
bonus:
  membros:
    order: 1
    # Permissão para ser reconhecido
    permission: 'yfloresta.bonus.membro'
    # Nome que irá aparecer nas mensagens
    display: '&7[Membro]'
    # Quantia do bônus em %
    bonus: 10.0
    bonus-leave: 10.0

# Sistema de anúncios ao chegar em um nível específico
specific-level:
  level10:
    # Nível necessário
    level: 10
    # Mensagem que será enviada
    message: |
      &r
      &c&lNÍVEL! &cO jogador &f{player} &cevoluiu para o nível &f&l{level}&c.
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
    permission: 'yfloresta.provider.money'
  yFloresta:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yFloresta'
    # Formato inteiro
    display: 'Folhas'
    # Formato abreviado
    abbreviated: 'folhas'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yfloresta.provider.yfloresta'
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

# Ativar o sistema de atualizar o menu principal automaticamente enquanto estiver aberto
menu-updater: true
# Tempo para atualizar o menu automaticamente
# em ticks -> 20 ticks = 1s
menu-updater-time: 200

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
  name: '&8Floresta'
  size: 36
  items:
    profile-slot: 10
    go-slot: 26
    rewards-slot: 12
    blocks-slot: 14
    top-slot: 16
    booster-slot: 20
    areas-slot: 22
    classe-slot: 24
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7jogador na floresta.'
        - ''
        - ' &8▶ &fTempo na Floresta: &7{time}'
        - ''
        - ' &8▶ &fFlores quebradas: &7{broken}'
        - ' &8▶ &fRecompensas no armazém: &7{rewards}'
        - ' &8▶ &fFolhas: &a✿&f{coin}'
        - ''
    rewards:
      material: 'CHEST'
      name: '&6Recompensas'
      lore:
        - '&7Gerencie as recompensas'
        - '&7que você ganhou.'
        - ''
        - ' &8▶ &fRecompensas: &7{rewards}'
        - ''
        - '&6Clique para gerenciar!'
    blocks:
      material: 'LOG'
      name: '&dBlocos'
      lore:
        - '&7Consulte as possíveis'
        - '&7recompensas dos blocos.'
        - ''
        - '&dClique para acessar!'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em nossa floresta.'
        - ''
        - '&aClique para acessar!'
    booster-no:
      material: GLASS_BOTTLE
      name: '&aBooster'
      lore: [ '&cNenhum booster ativo' ]
    booster:
      material: EXP_BOTTLE
      name: '&aBooster'
      lore:
        - '&aSeu booster de drops está ativo!'
        - '&f> &bTempo: &7{time}&f.'
        - '&f> &bBônus venda: &7{bonus}%&f.'
        - '&f> &bBônus folhas: &7{bonus-leave}%&f.'
    go:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aIr à Floresta'
      lore:
        - '&7Clique para entrar na'
        - '&7área da floresta'
    leave:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cSair da Floresta'
      lore:
        - '&7Clique para sair da'
        - '&7área da floresta'
    areas:
      material: TNT
      name: '&bÁreas'
      lore:
        - '&7Evolua sua área da floresta'
        - '&7e tenha blocos diferenciados.'
        - ''
        - '&aClique para fazer o upgrade'
    classe:
      material: LEATHER_CHESTPLATE
      name: '&bClasses'
      lore:
        - '&7Upando sua classe você irá ganhar'
        - '&7bônus na floresta, no ganho de'
        - '&7coins e folhas.'
        - ''
        - '&fSua classe: &7{classe}'
        - ''
        - '&aClique para gerenciar as classes'

# Menu de recompensas
main-rewards:
  name: '&8Floresta'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  #
  empty-slot: 22
  collect-slot: 50
  #
  items:
    empty:
      material: 'WEB'
      name: '&eVazio...'
      lore: [ '&7Nenhuma recompensa para', '&7coletar.' ]
    collect:
      material: 'a6cc486c2be1cb9dfcb2e53dd9a3e9a883bfadb27cb956f1896d602b4067'
      name: '&eRecolher tudo'
      lore: [ '&7Clique para recolher', '&7todas as recompensas.' ]

# Preview de blocos
blocks:
  name: '&8Floresta'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  lore:
    - '&7Clique para ver as recompensas'

# Preview de recompensas
rewards-preview:
  name: '&8Floresta'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu de top
top:
  name: '&8Floresta'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 30
  previous-slot: 9
  next-slot: 17
  # Seletor dos tops
  selector:
    slot: 31
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor do TOP'
    # Tipos do seletor
    types:
      broken:
        enabled: true
        name: 'Blocos quebrados'
      coin:
        enabled: true
        name: 'Folhas'
      time:
        enabled: true
        name: 'Tempo na floresta'
    # Formatos do seletor
    formats:
      seeing: ' &8• &f{name}'
      select: ' &8• &7{name}'
  items:
    # Item do top flores quebradas
    broken:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fBlocos quebrados: &7{amount}'
        - '&fPosição: &7{pos}'
    # Item do top coin
    coin:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fFolhas: &7{amount}'
        - '&fPosição: &7{pos}'
    # Item do top tempo na floresta
    time:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fTempo na Floresta: &7{amount}'
        - '&fPosição: &7{pos}'

# Menu de evolução
evolution:
  name: '&8Floresta'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 45
  items:
    tool-slot: 47
    profile-slot: 50
    skin-slot: 48
    filter-slot: 52
    disenchanter-slot: 53
    profile:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&fFolhas: &b{leaves}'
        - '&fBlocos quebrados: &b{broken_blocks}'
        - ''
    skin:
      material: '731f3279fc112b7f18bd0a2229934fcb5605c62823ce698b8b503ecccf0a3ac4'
      name: '&aSkins'
      lore:
        - '&7Configure a skin da sua ferramenta'
        - '&7e ganhe alguns bônus.'
        - ''
        - '&aClique para acessar'
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

# Menu de skins
skins:
  name: '&8Floresta'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  items:
    tool-slot: 31

# Menu de filtro
filter:
  name: '&8Floresta'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  items:
    tool-slot: 31
    enchant:
      name: '&a{enchant}'
      lore:
        - ''
        - '&fEncantamento: &7{enchant}'
        - '&fDesativado: &7{status}'
        - ''

# Menu de desencantador
disenchanter:
  name: '&8Floresta'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  items:
    tool-slot: 31
    enchant:
      name: '&a{enchant}'
      lore:
        - ''
        - '&fEncantamento: &7{enchant}'
        - '&fNíveis: &7{level}'
        - ''
        - '&fIrá ganhar &a{yfloresta} folhas&f.'
        - ''
        - '&aBotão &fESQUERDO &apara desencatar 1 nível'
        - '&aBotão &fDIREITO &apara desencatar {level} níveis'

# Menu de upgrade de área
upgrade-areas:
  name: '&8Floresta'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 31
  previous-slot: 18
  next-slot: 26

# Menu de classes
classes:
  name: '&8Floresta'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  items:
    classe-slot: 50
    classe:
      material: 'LEATHER_CHESTPLATE'
      name: '&eClasse'
      lore:
        - '&7Upando sua classe você irá ganhar'
        - '&7bônus na floresta, no ganho de'
        - '&7coins e folhas.'
        - ''
        - '&fSua classe: &7{classe}'
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
# Mensagens a serem enviadas pelo plugin.

# Mensagens e ações ao entrar
enter:
  title: '&bBem vindo à área da floresta'
  actionbar: '&bVocê entrou na área da floresta.'
  chat: |

    &bBem vindo à área da floresta.

  sound: 'ORB_PICKUP'

# Mensagens e ações ao sair
leave:
  title: ''
  actionbar: '&bVocê saiu da área de floresta.'
  chat: |

    &bVocê saiu da área da floresta.

  sound: 'ORB_PICKUP'

evolved:
  title: '&aFerramenta evoluída<nl>&apara &e{level}!'
  actionbar: '&aSua ferramenta evoluiu para o nível &e{level}!'
  chat: ''

actionbar:
  cant-break: '&cEssa ferramenta não consegue quebrar essa árvore!'
  break-log: '&cUse sua ferramenta para quebrar troncos de árvore!'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/floresta &8- &7Abre o menu principal.
    &a/floresta ir &8- &7Vai até a floresta.
    &a/floresta blocos &8- &7Abre o menu de blocos disponíveis.
    &a/floresta armazem &8- &7Abre o menu de armazém de recompensas.
    &a/floresta top &8- &7Abre o menu de top.
    &a/floresta sair &8- &7Sai da floresta.
    &a/floresta setspawn &8- &7Seta o local de spawn da floresta.
    &a/floresta setareaspawn &8- &7Seta o local de spawn de uma área da floresta.
    &a/floresta setsaida &8- &7Seta o local de saída da floresta.
    &a/floresta givebooster &8- &7Dá um booster à um jogador.
    &a/floresta giveskin &8- &7Dá uma skin à um jogador.
    &a/floresta giveskindireto &8- &7Adiciona uma skin à um jogador.
    &a/floresta removerskin &8- &7Remove uma skin de um jogador.
    &a/floresta addclasse &8- &7Adiciona uma classe à um jogador.
    &a/floresta removerclasse &8- &7Remove uma classe de um jogador.
    &a/floresta setarclasse &8- &7Define uma classe à um jogador.
    &a/floresta resetarclasse &8- &7Reseta a classe de um jogador.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  not-in: '&cVocê não está na área da floresta.'
  spawn: '&cO spawn da área da floresta não foi setado.'
  exit: '&cA saída da área da floresta não foi setada.'
  set-exit: '&aLocal de saída setado com sucesso.'
  set-spawn: '&aLocal de spawn setado com sucesso.'
  command: '&cVocê não pode usar este comando na área da floresta. Utilize /spawn para sair dela.'
  coin-help: |

    &a/folhas &8- &7Ver os seus folhas.
    &a/folhas <player> &8- &7Ver os folhas de alguém.
    &a/folhas enviar <player> <quantia> &8- &7Envia seus folhas para alguém.
    &a/folhas give <player/all> <quantia> &8- &7Dar folhas a alguém.
    &a/folhas add <player> <quantia> &8- &7Adiciona folhas a alguém.
    &a/folhas set <player> <quantia> &8- &7Remove folhas de alguém.
    &a/folhas remove <player> <quantia> &8- &7Seta folhas a alguém.

  coin: '&bVocê possui &f{coin} folhas&b.'
  coin-player: '&bO jogador &f{player}&b possui &f{coin} folhas&b.'
  coin-added: '&bVocê adicionou &f{coin} folhas&b ao jogador &f{player}&b.'
  coin-removed: '&bVocê removeu &f{coin} folhas&b do jogador &f{player}&b.'
  coin-set: '&bVocê setou &f{coin} folhas&b para o jogador &f{player}&b.'
  coin-sent: '&bVocê enviou &f{coin} folhas&b para o jogador &f{player}&b.'
  coin-received: '&bVocê recebeu &f{coin} folhas&b do jogador &f{player}&b.'
  coin-has: '&cVocê não possui a quantia de &f{coin}&c folhas.'
  converted: '&bVocê compactou todos seus folhas em 1.'
  activated: '&bVocê ativou &f{coin} folhas&b.'
  give: '&bVocê deu &f{coin} &bfolhas para o jogador &f{player}&b.'
  give-all: |

    &bO usuário &f{player}&b deu &f{coin} &bfolhas para todos os jogadores online&b.

  coin-added-all: '&bVocê adicionou &f{coin} folhas&b para todos os jogadores&b.'
  holding: '&cVocê não está segurando uma ferramenta.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  booster-null: |
    &cEste booster não existe.
    &cDisponíveis: &7{list}
  booster-give: '&aVocê deu x{amount} Booster(s) &8(+{bonus}%) &apara o jogador &f{player}&a.'
  booster-received: '&aVocê recebeu x{amount} Booster(s) &8(+{bonus}%)&a.'
  booster-finished: '&aCampo: &cSeu booster acabou.'
  booster-has: '&cVocê já está com um booster ativado.'
  booster-activated: '&aVocê ativou um booster da floresta. Multiplicador: &e{bonus}% coins &ae &e{bonus-leave}% folhas&a. Tempo: &e{time}&a.'
  booster-already: '&cVocê já está usando um booster.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  evolute: '&aO encantamento &f{enchant}&a foi evoluído para o nível &f{level}&a.'
  digit: |

    &aDigite a quantia de níveis que você quer adquirir ao encantamento &f{enchantment}&a.
    &7para cancelar digite &ncancelar&7.

  exceeds: '&cEstes níveis excedem o nível máximo do encantamento.'
  area-found: '&cÁrea não encontrada. Disponíveis: {list}'
  area-set-spawn: '&aLocal de spawn da área setado com sucesso.'
  area-bought: '&aVocê comprou a área.'
  slot-empty: '&cO slot {slot} deve estar vazio para poder receber a ferramenta. Por favor, re-entre na floresta.'
  digit-enchant: |

    &aDigite a quantia de níveis que você quer adquirir ao encantamento &f{enchantment}&a.
    &7para cancelar digite &ncancelar&7.

  enchantment-evolved: '&aO encantamento &f{enchantment}&a foi evoluido para o nível &f{level}&a.'
  enchantment-cant-buy: '&cVocê não pode comprar esse encantamento.'
  enchantment-exceeds: '&cEstes níveis excedem o nível máximo do encantamento.'
  enchantment-has-level: '&cVocê não possui a quantia de &f{level}&c níveis necessários.'
  enchantment-disenchanted: '&aVocê desencantou &f{level} níveis &ado encantamento &f{enchant}&a.'
  skin-found: '&cEsta skin não existe. Disponíveis: &7{list}'
  skin-give: '&bVocê deu uma skin para o jogador &f{player}&b.'
  skin-has: '&aVocê já possui esta skin ativada.'
  skin-activated: '&aSkin ativada com sucesso.'
  skin-no-has: '&cA ferramenta não possui essa skin.'
  skin-removed: '&aSkin removida com sucesso.'
  skin-has-player: '&aO jogador já possui esta skin.'
  classe-bought: '&aVocê evoluiu para a classe &7{classe}&a.'
  classe-permission: '&cVocê não tem permissão para evoluir para esta classe.'
  classe-previous: '&cVocê deve possuir a classe anterior primeiro.'
  classe-reset: '&aVocê resetou a classe do jogador &f{player}&a.'
  classe-set: '&aVocê definiu a classe {classe} ao jogador &f{player}&a.'
  classe-found: '&aEsta classe não existe. Disponíveis: {classes}'
  cant-break: ''
  break-log: ''
  inv-full: '&cSeu inventário está cheio.'
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
      lore: [ '&aEsta pedra vale muito dinheiro!', '', '&6Chance: {chance}%' ]
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
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', '&6Chance: {chance}%' ]
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
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', '&6Chance: {chance}%' ]
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
]]>
</code-block>
</chapter>

<chapter title="skins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
skins:
  default:
    order: 0
    type: 'WOOD'
    item:
      material: 'WOOD_AXE'
      name: '&aMachado de Madeira'
      lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '', '&fBônus: &a0%', '', '&aClique para ativar' ]
    menu:
      equip:
        material: 'WOOD_AXE'
        name: '&aMachado de Madeira'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '', '&fBônus: &a0%', '', '&aClique para equipar' ]
      equipped:
        material: 'WOOD_AXE'
        name: '&aMachado de Madeira'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '', '&fBônus: &a0%', '', '&aJá está equipada' ]
      has:
        material: 'WOOD_AXE'
        name: '&aMachado de Madeira'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '', '&fBônus: &a0%', '', '&cVocê não possui esta skin' ]
    name: '&fMachado de Madeira &6[{blocks_broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{level}'
      - ' &fEnergia: &7{energy}/{energy_next} &f({progressbar}&f)'
      - ''
    bonus: 0.0
    bonus-blocks: 0.0
    whitelist-blocks: [ 'LOG:0', 'LOG:4', 'LOG:8' ]
    trail:
      particle: 'REDSTONE'
      item: 'LOG:0,REDSTONE:0'
  stone:
    order: 1
    type: 'STONE'
    item:
      material: 'STONE_AXE'
      name: '&aMachado de Pedra'
      lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '', '&fBônus: &a10%', '', '&aClique para ativar' ]
    menu:
      equip:
        material: 'STONE_AXE'
        name: '&aMachado de Pedra'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '', '&fBônus: &a10%', '', '&aClique para equipar' ]
      equipped:
        material: 'STONE_AXE'
        name: '&aMachado de Pedra'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '', '&fBônus: &a10%', '', '&aJá está equipada' ]
      has:
        material: 'STONE_AXE'
        name: '&aMachado de Pedra'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '', '&fBônus: &a10%', '', '&cVocê não possui esta skin' ]
    name: '&fMachado de Pedra &6[{blocks_broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{level}'
      - ' &fEnergia: &7{energy}/{energy_next} &f({progressbar}&f)'
      - ''
      - '&a+10% &7(pedra)'
      - ''
    bonus: 10.0
    bonus-blocks: 10.0
    whitelist-blocks: [ 'LOG:0', 'LOG:4', 'LOG:8', 'LOG:1', 'LOG:5', 'LOG:9' ]
    trail:
      particle: 'REDSTONE'
      item: 'STONE:0,REDSTONE:0'
  iron:
    order: 2
    type: 'IRON'
    item:
      material: 'IRON_AXE'
      name: '&aMachado de Ferro'
      lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '', '&fBônus: &a15%', '', '&aClique para ativar' ]
    menu:
      equip:
        material: 'IRON_AXE'
        name: '&aMachado de Ferro'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '', '&fBônus: &a15%', '', '&aClique para equipar' ]
      equipped:
        material: 'IRON_AXE'
        name: '&aMachado de Ferro'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '', '&fBônus: &a15%', '', '&aJá está equipada' ]
      has:
        material: 'IRON_AXE'
        name: '&aMachado de Ferro'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '', '&fBônus: &a15%', '', '&cVocê não possui esta skin' ]
    name: '&fMachado de Ferro &6[{blocks_broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{level}'
      - ' &fEnergia: &7{energy}/{energy_next} &f({progressbar}&f)'
      - ''
      - '&a+15% &7(ferro)'
      - ''
    bonus: 15.0
    bonus-blocks: 15.0
    whitelist-blocks: [ 'LOG:0', 'LOG:4', 'LOG:8', 'LOG:1', 'LOG:5', 'LOG:9', 'LOG:2', 'LOG:6', 'LOG:10' ]
    trail:
      particle: 'REDSTONE'
      item: 'IRON_INGOT:0,REDSTONE:0'
  gold:
    order: 3
    type: 'GOLD'
    item:
      material: 'GOLD_AXE'
      name: '&aMachado de Ouro'
      lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '', '&fBônus: &a20%', '', '&aClique para ativar' ]
    menu:
      equip:
        material: 'GOLD_AXE'
        name: '&aMachado de Ouro'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '', '&fBônus: &a20%', '', '&aClique para equipar' ]
      equipped:
        material: 'GOLD_AXE'
        name: '&aMachado de Ouro'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '', '&fBônus: &a20%', '', '&aJá está equipada' ]
      has:
        material: 'GOLD_AXE'
        name: '&aMachado de Ouro'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '', '&fBônus: &a20%', '', '&cVocê não possui esta skin' ]
    name: '&fMachado de Ouro &6[{blocks_broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{level}'
      - ' &fEnergia: &7{energy}/{energy_next} &f({progressbar}&f)'
      - ''
      - '&a+20% &7(ouro)'
      - ''
    bonus: 20.0
    bonus-blocks: 20.0
    whitelist-blocks: [ 'LOG:0', 'LOG:4', 'LOG:8', 'LOG:1', 'LOG:5', 'LOG:9', 'LOG:2', 'LOG:6', 'LOG:10', 'LOG_2:0', 'LOG_2:4', 'LOG_2:8' ]
    trail:
      particle: 'REDSTONE'
      item: 'GOLD_INGOT:0,REDSTONE:0'
  diamond:
    order: 4
    type: 'DIAMOND'
    item:
      material: 'DIAMOND_AXE'
      name: '&aMachado de Diamante'
      lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '&8> &f Madeira da Selva', '', '&fBônus: &a25%', '', '&aClique para ativar' ]
    menu:
      equip:
        material: 'DIAMOND_AXE'
        name: '&aMachado de Diamante'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '&8> &f Madeira da Selva', '', '&fBônus: &a25%', '', '&aClique para equipar' ]
      equipped:
        material: 'DIAMOND_AXE'
        name: '&aMachado de Diamante'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '&8> &f Madeira da Selva', '', '&fBônus: &a25%', '', '&aJá está equipada' ]
      has:
        material: 'DIAMOND_AXE'
        name: '&aMachado de Diamante'
        lore: [ '&7Essa skin lhe permite quebrar', '&7os seguintes tipos de madeiras:', '', '&8> &f Madeira de Carvalho', '&8> &f Madeira de Pinheiro', '&8> &f Madeira de Eucalipto', '&8> &f Madeira de Acácia', '&8> &f Madeira da Selva', '', '&fBônus: &a25%', '', '&cVocê não possui esta skin' ]
    name: '&fMachado de Diamante &6[{blocks_broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{level}'
      - ' &fEnergia: &7{energy}/{energy_next} &f({progressbar}&f)'
      - ''
      - '&a+20% &7(diamante)'
      - ''
    bonus: 25.0
    bonus-blocks: 25.0
    whitelist-blocks: [ 'LOG:0', 'LOG:4', 'LOG:8', 'LOG:1', 'LOG:5', 'LOG:9', 'LOG:2', 'LOG:6', 'LOG:10', 'LOG_2:0', 'LOG_2:4', 'LOG_2:8', 'LOG:3', 'LOG:7', 'LOG:11' ]
    trail:
      particle: 'REDSTONE'
      item: 'DIAMOND:0,REDSTONE:0'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/143-yFloresta">Site do plugin yFloresta</a>
    </category>
</seealso>