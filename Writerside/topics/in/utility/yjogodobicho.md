# yJogoDoBicho
<secondary-label ref="utility"/>

### Descrição
O famoso jogo do bicho agora no minecraft!

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
<video src="//www.youtube.com/watch?v=1IGWu2LwNQs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/jogodobicho - Abre o menu principal
/jogodobicho reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yjogodobicho.use - Permissão para o /jogodobicho
yjogodobicho.admin.reload - Permissão para o /jogodobicho reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yJogoDoBicho/
    ├── animals.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="animals.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
animals:
  avestruz:
    # Ordem do bicho conforme a tabela
    order: 1
    # Nome do bicho para as mensagens
    name: '&fAvestruz'
    # Item no menu da tabela
    display:
      material: 'c40e7551843f1c416da50dd82eaba165ae7ca843db9d17ab5a8cc279050059b3'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    # Item no menu da tabela (selecionado)
    display-selected:
      material: 'c40e7551843f1c416da50dd82eaba165ae7ca843db9d17ab5a8cc279050059b3'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  aguia:
    order: 2
    name: '&fÁguia'
    display:
      material: '21f829d84d0e87112f685e7d234bef010964debb7a86f38d9f7072c8a4468527'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '21f829d84d0e87112f685e7d234bef010964debb7a86f38d9f7072c8a4468527'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  burro:
    order: 3
    name: '&fBurro'
    display:
      material: '46dcda265e57e4f51b145aacbf5b59bdc6099ffd3cce0a661b2c0065d80930d8'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '46dcda265e57e4f51b145aacbf5b59bdc6099ffd3cce0a661b2c0065d80930d8'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  borboleta:
    order: 4
    name: '&fBorboleta'
    display:
      material: '9fd806defdfdf59b1f2609c8ee364666de66127a623415b5430c9358c601ef7c'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '9fd806defdfdf59b1f2609c8ee364666de66127a623415b5430c9358c601ef7c'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  cachorro:
    order: 5
    name: '&fCachorro'
    display:
      material: '6c537dc81d1279459d485fa9a9d33e0ff60a1cc26a62bcb4ca2f4cc55369a423'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '6c537dc81d1279459d485fa9a9d33e0ff60a1cc26a62bcb4ca2f4cc55369a423'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  cabra:
    order: 6
    name: '&fCachorro'
    display:
      material: '6c537dc81d1279459d485fa9a9d33e0ff60a1cc26a62bcb4ca2f4cc55369a423'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '6c537dc81d1279459d485fa9a9d33e0ff60a1cc26a62bcb4ca2f4cc55369a423'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  carneiro:
    order: 7
    name: '&fCarneiro'
    display:
      material: '88170c84a763f8d3ac345c913d54a8654b20e35ec291844f16ebd386a7b0023d'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '88170c84a763f8d3ac345c913d54a8654b20e35ec291844f16ebd386a7b0023d'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  camelo:
    order: 8
    name: '&fCamelo'
    display:
      material: 'ba4c95bfa0b61722255389141b505cf1a38bad9b0ef543de619f0cc9221ed974'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'ba4c95bfa0b61722255389141b505cf1a38bad9b0ef543de619f0cc9221ed974'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  cobra:
    order: 9
    name: '&fCobra'
    display:
      material: '60503b81ac020c67c37787b45c9a26223f9bc26bca27f81af32f2cf55e2440b7'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '60503b81ac020c67c37787b45c9a26223f9bc26bca27f81af32f2cf55e2440b7'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  coelho:
    order: 10
    name: '&fCoelho'
    display:
      material: '9dcb88ed79bf3bd93ed57d18e0d2d8ce1039719d82cf413404cd6f0d83d81208'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '9dcb88ed79bf3bd93ed57d18e0d2d8ce1039719d82cf413404cd6f0d83d81208'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  cavalo:
    order: 11
    name: '&fCavalo'
    display:
      material: 'e335e31961713353a76401e00c3454b7ca885b7784d5288d3227222d9b48d393'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'e335e31961713353a76401e00c3454b7ca885b7784d5288d3227222d9b48d393'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  elefante:
    order: 12
    name: '&fElefante'
    display:
      material: '25ce762bc8e7ad5e16b35354f7d9341cbccd2de61791a7a6882ac43c38cc8e'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '25ce762bc8e7ad5e16b35354f7d9341cbccd2de61791a7a6882ac43c38cc8e'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  galo:
    order: 13
    name: '&fGalo'
    display:
      material: '1caea4b7a0b2f1c6a8b0eb71f9c8e143cf1ad0e6bd859567d6cbd4d8b45aad15'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '1caea4b7a0b2f1c6a8b0eb71f9c8e143cf1ad0e6bd859567d6cbd4d8b45aad15'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  gato:
    order: 14
    name: '&fGato'
    display:
      material: 'c67b2b6a9c75168b50776ff002739002c84fc8217f739fb185018ffe77b0b5ed'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'c67b2b6a9c75168b50776ff002739002c84fc8217f739fb185018ffe77b0b5ed'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  jacaré:
    order: 15
    name: '&fJacaré'
    display:
      material: 'fc2391da81052360007623c749a23b74dd1773f8c1ea0d1156682a3e97ab5989'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'fc2391da81052360007623c749a23b74dd1773f8c1ea0d1156682a3e97ab5989'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  leao:
    order: 16
    name: '&fLeão'
    display:
      material: '73987090cb8641f55d8320f05ff896b9afc1c36c8c54a960dadaec42d2e86a6d'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '73987090cb8641f55d8320f05ff896b9afc1c36c8c54a960dadaec42d2e86a6d'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  macaco:
    order: 17
    name: '&fMacaco'
    display:
      material: 'a6b856d923ca6f40013832af51370196db541b8c5209f4ea80e2eadf658d7949'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'a6b856d923ca6f40013832af51370196db541b8c5209f4ea80e2eadf658d7949'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  porca:
    order: 18
    name: '&fPorca'
    display:
      material: '75a9e8ee9361c99255df509db11d1a464a1c6f2f6e5c51d8cad86e3892d38e9a'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '75a9e8ee9361c99255df509db11d1a464a1c6f2f6e5c51d8cad86e3892d38e9a'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  pavao:
    order: 19
    name: '&fPavão'
    display:
      material: '7fd6ab3f0324190d8c8f73221791510c2fc406c4a7ddb7301d3e14b313a12de2'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '7fd6ab3f0324190d8c8f73221791510c2fc406c4a7ddb7301d3e14b313a12de2'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  peru:
    order: 20
    name: '&fPeru'
    display:
      material: '231251c8da0eb52d6578c57a22c2df15d101becfbddd19752cecafe9bfc7f517'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '231251c8da0eb52d6578c57a22c2df15d101becfbddd19752cecafe9bfc7f517'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  touro:
    order: 21
    name: '&fTouro'
    display:
      material: '81096384fa719d1a94b3b2a502289ed385aa54e45fcb58b83878552ad5066ee'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: '81096384fa719d1a94b3b2a502289ed385aa54e45fcb58b83878552ad5066ee'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  tigre:
    order: 22
    name: '&fTigre'
    display:
      material: 'b2609ea8464153f86e957a7425f16e4ff7060a0b5f0bbebdfa4f7eee703f08b4'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'b2609ea8464153f86e957a7425f16e4ff7060a0b5f0bbebdfa4f7eee703f08b4'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  urso:
    order: 23
    name: '&fUrso'
    display:
      material: 'bdc22f6eb9d8227d5b402f2cf0bae6fd7f270ec46742580c92f7ff4537324f5c'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'bdc22f6eb9d8227d5b402f2cf0bae6fd7f270ec46742580c92f7ff4537324f5c'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  veado:
    order: 24
    name: '&fVeado'
    display:
      material: 'c14af5ac6a96bfdee1b83c7e33c874a268936284384d66c9c61c18c9fc366bc6'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'c14af5ac6a96bfdee1b83c7e33c874a268936284384d66c9c61c18c9fc366bc6'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
  vaca:
    order: 25
    name: '&fVaca'
    display:
      material: 'f88be57af6d248c297b3cae676f45cc2a438f15a9ef26cdf5f035fb842d86dd9'
      name: '&f&l{order} {name}'
      lore:
        - '&6{numbers}'
        - ''
        - '&aClique para selecionar este bicho'
    display-selected:
      material: 'f88be57af6d248c297b3cae676f45cc2a438f15a9ef26cdf5f035fb842d86dd9'
      name: '&f&l{order} {name}'
      lore:
        - '&aApostando com: &f{name}'
        - '&6{numbers}'
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
  animal: 'jogodobicho|jdb'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#            _                   ____        ____  _      _
#  _   _    | | ___   __ _  ___ |  _ \  ___ | __ )(_) ___| |__   ___
# | | | |_  | |/ _ \ / _` |/ _ \| | | |/ _ \|  _ \| |/ __| '_ \ / _ \
# | |_| | |_| | (_) | (_| | (_) | |_| | (_) | |_) | | (__| | | | (_) |
#  \__, |\___/ \___/ \__, |\___/|____/ \___/|____/|_|\___|_| |_|\___/
#  |___/             |___/
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

# Sistemas gerais
general:
  # Números que cada bicho possuirá
  numbers-total: 4
  # Mínimo por aposta
  bet-minimum: 100.0
  # Multiplicador da aposta simples
  simple-multiplier: 4.0
  # Multiplicador da aposta em dezenas
  dozens-multiplier: 6.0
  # Multiplicador da aposta em centenas
  hundreds-multiplier: 11.0
  # Multiplicador da aposta em milhar
  thousands-multiplier: 50.0
  # Delay para apostar novamente
  # em segundos
  delay: 5

# Sistema de anúncios
announces:
  dozens:
    chat: |

      &eO jogador &f{player}&e acertou a DEZENA no &fJOGO DO BICHO&e!
      &eAposta: &f{amount}
      &eRecebeu: &f{total} (&lx{odd}&f)

    actionbar: ''
    title: ''
  hundreds:
    chat: |

      &eO jogador &f{player}&e acertou a CENTENA no &fJOGO DO BICHO&e!
      &eAposta: &f{amount}
      &eRecebeu: &f{total} (&lx{odd}&f)

    actionbar: ''
    title: ''
  thousands:
    chat: |

      &eO jogador &f{player}&e acertou o MILGAR no &fJOGO DO BICHO&e!
      &eAposta: &f{amount}
      &eRecebeu: &f{total} (&lx{odd}&f)

    actionbar: ''
    title: ''
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
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yjogodobicho.provider.money'
    # ‘Item’ que aparecerá para os jogadores no menu do jogo
    item:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &aVocê está apostando com &fMoney&a.'
        - ''
    # ‘Item’ que aparecerá para os jogadores no menu do jogo
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ''
        - '&aClique para alterar'
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
  name: '&8Jogo do Bicho'
  size: 45
  slots: [ 0, 1, 2, 3, 4, 9, 10, 11, 12, 13, 18, 19, 20, 21, 22, 27, 28, 29, 30, 31, 36, 37, 38, 39, 40 ]
  previous-slot: 33
  next-slot: 35
  items:
    amount-slot: 17
    number-slot: 34
    animal-slot: 6
    provider-slot: 8
    simple-slot: 15
    dozens-slot: 42
    hundreds-slot: 43
    thousands-slot: 44
    info-slot: 25
    info:
      material: '{player}'
      name: '&eSuas Informações'
      lore:
        - ''
        - '&7Gasto: &c{spent}'
        - '&7Ganho: &a{obtained}'
        - ''
    amount:
      material: '90584175f5f57b75e1447da97ad30f8cceb2dd0c89c8dfddeb8c5c9c2736fff4'
      name: '&aQuantia apostada'
      lore:
        - '&7Quantia que você irá por na'
        - '&7sua aposta.'
        - ''
        - '&7Atual: &f{amount}'
        - ''
        - '&aClique para alterar a quantia'
    number:
      material: 'f78c7778b3ec796f8e04399e613623135130ad5418aacce4cb3587984f1ae'
      name: '&aNúmero da Aposta'
      lore:
        - '&7Número que você irá apostar.'
        - ''
        - '&7Válido apenas nas apostas:'
        - '&f Dezenas, Centenas e Milhar'
        - ''
        - '&7Atual: &f{number}'
        - ''
        - '&aClique para alterar o número'
    provider:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aMoeda apostada'
      lore:
        - '&7Moeda que será utilizada na'
        - '&7sua aposta.'
        - ''
        - '&7Atual: &fNenhuma'
        - ''
        - '&aClique para alterar a moeda'
    animal-no:
      material: '1b9c45d6c7cd0116436c31ed4d8dc825de03e806edb64e9a67f540b8aaae85'
      name: '&cBicho'
      lore:
        - '&cNenhum bicho selecionado.'
    simple:
      material: '137dcfb66a61c529f2a128aeef93c25f9d0b0439b59fb199d2b04acfe0b85aac'
      name: '&eAposta Simples &f&l{odd}x'
      lore:
        - '&7Ela vai cobrir os {total_numbers} números que'
        - '&7o bicho representa.'
        - ''
        - '&7Você ganha se o número sorteado cai dentro'
        - '&7do grupo de números associados ao bicho em'
        - '&7que você apostou.'
        - ''
        - '&aClique para relizar a aposta.'
    dozens:
      material: 'e467a7b9d76ba6d0fed743602533fc98c87af0c60f80f38da774f7a01a2093fa'
      name: '&eDezenas &f&l{odd}x'
      lore:
        - '&7Você aposta em uma das dezenas possíveis.'
        - ''
        - '&7Você ganha se as duas últimas cifras do número'
        - '&7sorteado coincidirem com a dezena escolhida.'
        - ''
        - '&7Número escolhido: &f{number}'
        - ''
        - '&aClique para relizar a aposta.'
    hundreds:
      material: '3324a7d61ccd44b031744b517f911a5c461614b953b17f648282e147b29d10e'
      name: '&eCentenas &f&l{odd}x'
      lore:
        - '&7Você aposta em uma das centenas possíveis.'
        - ''
        - '&7Você ganha se as duas primeiras cifras do número'
        - '&7sorteado coincidirem com a centena escolhida.'
        - ''
        - '&7Número escolhido: &f{number}'
        - ''
        - '&aClique para relizar a aposta.'
    thousands:
      material: '4d11109f4ab03aa6c5b76cad129176ffb1fce8c174e69c9e8ba06b9f8061e5ad'
      name: '&eMilhar &f&l{odd}x'
      lore:
        - '&7Você aposta um número específico.'
        - ''
        - '&7Você ganha se o número sorteado é exatamente'
        - '&7o mesmo número em que você apostou.'
        - ''
        - '&7Número escolhido: &f{number}'
        - ''
        - '&aClique para relizar a aposta.'
  facing:
    e1:
      slot: 5
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e2:
      slot: 7
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e3:
      slot: 14
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e4:
      slot: 16
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e5:
      slot: 23
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e6:
      slot: 24
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e8:
      slot: 26
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e9:
      slot: 32
      material: 'STAINED_GLASS_PANE:7'
      name: ''
    e10:
      slot: 41
      material: 'STAINED_GLASS_PANE:7'
      name: ''

# Menu de seleção de economias
providers:
  name: '&8Selecionar economia'
  size: 27
  previous: 9
  next: 17
  back: 18
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
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
  help: |

    &aJogo do Bicho comandos:

    &a> /jogodobicho
    &a> /jogodobicho top

  provider-permission: '&cVocê não tem permissão para utilizar esta economia.'
  select-economy: '&cSelecione uma moeda para apostar.'
  select-animal: '&cSelecione um bicho para apostar.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  win: '&aVocê obteve um sucesso de saldo de &f{amount} ({odd})&a.'
  lose: '&cVocê perdeu.'
  lose-other: '&cVocê perdeu. Número sorteado: {sorted}.'
  minimum: '&cVocê precisa apostar no mínimo {amount}.'
  digit-amount: |

    &aDigite a quantia que deseja apostar.
    &7para cancelar digite &ncancelar&7.

  digit-number: |

    &aDigite o número que deseja apostar.
    &7para cancelar digite &ncancelar&7.

  number-syntax: '&cVocê precisa selecionar um número entre 1 e 9999.'
  number-syntax-dozen: '&cVocê precisa selecionar um número entre 01 e 99 na aposta em dezenas.'
  number-syntax-hundred: '&cVocê precisa selecionar um número entre 001 e 999 na aposta em centenas.'
  number-syntax-thousand: '&cVocê precisa selecionar um número entre 0001 e 9999 na aposta em milhar.'
  delay: '&cAguarde &e{time} &cpara apostar novamente.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/127-yJogoDoBicho">Site do plugin yJogoDoBicho</a>
    </category>
</seealso>