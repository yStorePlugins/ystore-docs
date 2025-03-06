# ySpawnersVirtuais
<secondary-label ref="rankup"/>

### Descrição
Spawners totalmente inovadores, permitindo que os jogadores armazenem seus spawners virtualmente enquanto, os mesmos geram mobs em um local físico.

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
<video src="//www.youtube.com/watch?v=Tlv55luGQHg"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/spawner - Abrir o menu principal
/spawner setspawn - Seta o local de spawn do mob
/spawner delspawn - Deleta o local de spawn do mob
/limite - Vê os limites
/limite [player] - Vê os limites de um jogador
/spawner givespawner  - Dar spawners para um jogador
/spawner givelimite - Dar limite de compra para um jogador
/spawner givelimitespawners - Dar limite de spawner para um jogador
/spawner givelimitedrops - Dar limite de drops para um jogador
/spawner espada  - Pegar a espada custom</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yspawners.usar - Permissão para o /spawneryspawners.setspawn - Permissão para o /spawner setspawnyspawners.delspawn - Permissão para o /spawner delspawnyspawners.limite - Permissão para o /limiteyspawners.limite.outros - Permissão para o /limite [player]yspawners.espada - Permissão para o /spawner espadayspawners.givespawner - Permissão para o /spawner givespawneryspawners.givelimite - Permissão para o /spawner givelimite, /spawner givelimitespawners e /spawner givelimitedrops</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yspawners_limite% - Retorna os limites de compra do jogador.
%yspawners_limite_spawner% - Retorna os limites de spawner do jogador.
%yspawners_limite_drops% - Retorna os limites de drops do jogador.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── ySpawnersVirtuais/
    ├── menus/
    │    ├── armazem.yml
    │    ├── evolucao.yml
    │    ├── loja.yml
    │    ├── lojamelhorias.yml
    │    ├── lojaspawners.yml
    │    ├── principal.yml
    │    ├── spawners.yml
    │    └── top.yml
    ├── bonus.yml
    ├── config.yml
    ├── descontos.yml
    ├── mobs.yml
    ├── precos.yml
    ├── recompensas.yml
    └── spawners.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="armazem.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Armazém'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26
# Se não houver nada no armazém.
Vazio:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: 408
  Data: 0
  Glow: true
  Name: '&cVazio'
  Lore:
    - '&7Você não possui nenhum drop.'
# Item que está armazenado.
Item:
  Nome: '&b{item}'
  Lore:
    - ''
    - '&fQuantidade: &b{quantia}'
    - '&fPreço unitário: &a{preco}'
    - '&fPreço total: &a{precototal} &f+ (&a{playerbonus}% &f+ {bonus})%f.'
    - ''
    - '&7Clique com botão esquerdo para vender.'
    - '&7Clique com botão direito para recolher.'
]]>
</code-block>
</chapter>

<chapter title="evolucao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Evolucao da espada'
Tamanho: 36
# Itens do menu de evolução.
Itens:
  Perfil:
    Slot: 4
    Lore:
      - ''
      - '&eQuantia de XP: &a{xp}&e.'
  Looting:
    Slot: 20
    CustomSkull: false
    URL: ''
    ID: 388
    Data: 0
    Glow: true
    Name: '&eLooting'
    Lore:
      - ''
      - '&7Este encantamento permite multiplicar seus drops.'
      - ''
      - '&7Seu nivel: &f{agora} &7(&e{porcentagem_agora}%&7)'
      - '&7Próximo nivel: &f{proximo} &f / &7{max} &7(&e{porcentagem_prox}%&7)'
      - '&7Custo: &f{preco}'
      - ''
      - '&7Clique para encantar.'
    Lore max:
      - ''
      - '&7Este encantamento permite multiplicar seus drops.'
      - ''
      - '&cVocê chegou ao nível máximo.'
  Dano:
    Slot: 22
    CustomSkull: false
    URL: ''
    ID: 331
    Data: 0
    Glow: true
    Name: '&eDano'
    Lore:
      - ''
      - '&7Este encantamento permite aumentar seu dano.'
      - ''
      - '&7Seu nivel: &f{agora} &7(&e{dano_agora}&c❤&7)'
      - '&7Próximo nivel: &f{proximo} &f / &7{max} &7(&e{dano_prox}&c❤&7)'
      - '&7Custo: &f{preco}'
      - ''
      - '&7Clique para encantar.'
    Lore max:
      - ''
      - '&7Este encantamento permite aumentar seu dano.'
      - ''
      - '&cVocê chegou ao nível máximo.'
  Sortudo:
    Slot: 24
    CustomSkull: false
    URL: ''
    ID: 399
    Data: 0
    Glow: true
    Name: '&eSortudo'
    Lore:
      - ''
      - '&7Este encantamento permite aumentar sua chance de'
      - '&7ganhar recompensas.'
      - ''
      - '&7Seu nivel: &f{agora} &7(&e{porcentagem_agora}%&7)'
      - '&7Próximo nivel: &f{proximo} &f / &7{max} &7(&e{porcentagem_prox}%&7)'
      - '&7Custo: &f{preco}'
      - ''
      - '&7Clique para encantar.'
    Lore max:
      - ''
      - '&7Este encantamento permite aumentar sua chance de'
      - '&7ganhar recompensas.'
      - ''
      - '&cVocê chegou ao nível máximo.'
]]>
</code-block>
</chapter>

<chapter title="loja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Geradores - Loja'
Tamanho: 27
BackSlot: 9
# Itens da loja principal.
Itens:
  Spawners:
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4faaf642babf93f96e146e2bb7b3cd70a4ec9d17f4a2957a99e2d8ed5bc8306d'
    ID: 0
    Data: 0
    Glow: false
    Name: '&eGeradores'
    Lore:
      - '&7Clique para abrir a loja de geradores.'
  Melhorias:
    Slot: 15
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/e9e4bdcf172d5dc77c2bd4e37ad985399a9f2cdebf72463929ea4b666ef6f80'
    ID: 0
    Data: 0
    Glow: false
    Name: '&aMelhorias'
    Lore:
      - '&7Clique para comprar melhorias para'
      - '&7os seus geradores.'
]]>
</code-block>
</chapter>

<chapter title="lojamelhorias.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Geradores - Melhorias'
Tamanho: 27
BackSlot: 9
# Itens da loja de melhorias.
Itens:
  Drop bonus:
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4cb3acdc11ca747bf710e59f4c8e9b3d949fdd364c6869831ca878f0763d1787'
    ID: 0
    Data: 0
    Glow: false
    Name: '&aDrop bônus'
    Lore:
      - ''
      - '&fSeu nível: &e{playerlevel}&f.'
      - '&fPróximo: &e{proximolevel} &f- &7(&a{preco}c &7(&e-{desconto}%&7) &7)&f.'
      - ''
      - '&aClique para comprar.'
      - ''
    Lore max:
      - ''
      - '&aVocê ja está no nível'
      - '&amáximo do drop bônus.'
      - ''
  Spawnar:
    Slot: 13
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/81359b8150b25cca5dc3a92ece02f2dfb6a5235d4f7bffacc3934880033a7'
    ID: 0
    Data: 0
    Glow: false
    Name: '&aSpawnar mais rápido'
    Lore:
      - ''
      - '&fSeu nível: &e{playerlevel}%'
      - '&fPróximo: &e{proximolevel}% &f- &7(&a{preco}c &7(&e-{desconto}%&7) &7)&f.'
      - ''
      - '&aClique para comprar.'
      - ''
    Lore max:
      - ''
      - '&aVocê ja está no nível'
      - '&amáximo de spawnar rápido.'
      - ''
  Bonus de venda:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
    ID: 0
    Data: 0
    Glow: false
    Name: '&aBônus de venda'
    Lore:
      - ''
      - '&fSeu nível: &b{playerlevel}%'
      - '&fPróximo: &b{proximolevel}% &f- &7(&a{preco}c &7(&e-{desconto}%&7) &7)&f.'
      - ''
      - '&aClique para comprar.'
      - ''
    Lore max:
      - ''
      - '&aVocê ja está no nível'
      - '&amáximo do bônus de venda.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="lojaspawners.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Geradores - SLoja'
Tamanho: 27
Slots: [ 11, 12, 13, 14, 15 ]
BackSlot: 9
VoltarSlot: 9
ProximoSlot: 17
# Item de perfil da loja.
Limite:
  Slot: 4
  Name: '&b{player}'
  Lore:
    - '&fVocê possui &a{limite} &fem limite.'
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Geradores - Principal'
Tamanho: 27
# Itens do menu principal
Itens:
  Perfil: # primeiro
    Slot: 10
    Name: '&f{player}'
    Lore:
      - ''
      - '&fGeradores ativos: &a{ativos}&fx.'
      - '&fDrops armazenados: &a{dropsarmazenados}&fx.'
      - ''
      - '&fXP de evolução: &a{xp}&f.'
      - ''
      - '&e⭐ Melhorias'
      - ''
      - '&f > Tempo de spawn: &7({tempomin}/{tempomax}) &e-{tempo}s'
      - '&f > Drop bônus: &7({dropbonusmin}/{dropbonusmax}) &e+{dropbonus}%'
      - '&f > Bônus de venda: &7({bonusvendamin}/{bonusvendamax}) &e+{bonusvenda}%'
      - ''
  Spawners: #segundo
    Slot: 11
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4faaf642babf93f96e146e2bb7b3cd70a4ec9d17f4a2957a99e2d8ed5bc8306d'
    ID: 0
    Data: 0
    Glow: false
    Name: '&eGeradores'
    Lore:
      - '&7Clique para acessar seus geradores.'
      - '&fGeradores sendo usados: &a{geradores}&f.'
      - '&fSeu limite: &a{limite}&f.'
  Armazem: #terceiro
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/95732d3e57b9a62159b35d2754574452a32b4c221fc4fd363bff522ff04a577e'
    ID: 0
    Data: 0
    Glow: false
    Name: '&bArmazém'
    Lore:
      - '&7Clique para acessar seu armazém.'
      - '&fDrops disponíveis: &a{drops}x&f.'
      - '&fSeu limite: &a{limite}&f.'
  Loja: #quarto
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: 266
    Data: 0
    Glow: false
    Name: '&aLoja'
    Lore:
      - '&7Clique para comprar geradores e melhorias'
  Top: #quinto
    Slot: 16
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/15a7ee9a86de203674a93b570bc8992e500363dd32f2b9813daaeeabccf92151'
    ID: 0
    Data: 0
    Glow: true
    Name: '&eTOP Geradores'
    Lore:
      - '&7Clique para ver os jogadores com o maior'
      - '&7valor de geradores acumulados.'
]]>
</code-block>
</chapter>

<chapter title="spawners.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Spawners - Armazenados'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26
# Quando não houver spawners.
Vazio:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: 408
  Data: 0
  Glow: true
  Name: '&cVazio'
  Lore:
    - '&7Você não possui nenhum spawner.'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Geradores'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26
# Item do Top geradores.
Item:
  Name: '&b{player}'
  Lore:
    - ''
    - '&fPosição: &e{pos}º'
    - '&fGeradores comprados: &e{geradores}'
    - '&fValor atual dos geradores: &e{valor}'
    - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Este bônus servirá na hora de vender drops.
# Você pode criar quantos quiser.
Bonus:
  VIP:
    Permissao: 'yspawners.vip'
    Bonus: 10.0
    Ordem: 1
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
Comandos:
  Spawners:
    Comando: 'spawners'
    Aliases: [ geradores, spawner, gerador ]
  Limite:
    Comando: 'limite'
    Aliases: [ limites ]
# Opções das melhorias disponíveis para o jogador.
Melhorias:
  # Esta melhoria serve para diminuir o tempo de spawnar um mob
  # de todos os spawners.
  Delay:
    # Preço de cada lével.
    Preco: 10.0
    # Porcentagem que irá aumentar no preço a cada lével que comprar.
    # Por exemplo: Level 1 = 10.0, Level 2 = 10 + 30% ( que seria, 13 )
    Porcentagem acrescida: 30.0
    # Segundos que irá diminuir por cada lével adquirido.
    # Por exemplo: Spawner de porco (delay 10segundos). Level 1 irá diminuir 1 segundo,
    # ou seja, irá spawnar com 9 segundos. O level 2 irá diminuir 2 segundos, ou seja,
    # irá spawnar com 8 segundos.
    Segundos por level: 1
    # Máximo de léveis que o jogador pode comprar deste upgrade.
    Max: 3
    # Quantia de léveis que o jogador ganha ao se registrar.
    Default: 1
  Drop bonus:
    # Preço de cada lével.
    Preco: 10.0
    # Porcentagem que irá aumentar no preço a cada lével que comprar.
    # Por exemplo: Level 1 = 10.0, Level 2 = 10 + 30% ( que seria, 13 )
    Porcentagem acrescida: 30.0
    # Porcentagem que irá aumentar de drops por cada lével.
    # Por exemplo: 10 drops no lével 1 se tornariam 10 drops + 5%, ou seja, 10,5 drops.
    Porcentagem por level: 5.0
    # Máximo de léveis que o jogador pode comprar deste upgrade.
    Max: 3
    # Quantia de léveis que o jogador ganha ao se registrar.
    Default: 0.0
  Bonus de venda:
    # Preço de cada lével.
    Preco: 10.0
    # Porcentagem que irá aumentar no preço a cada lével que comprar.
    # Por exemplo: Level 1 = 10.0, Level 2 = 10 + 30% ( que seria, 13 )
    Porcentagem acrescida: 30.0
    # Porcentagem que irá aumentar no money ao vender drops.
    # Por exemplo: 100 em money no lével 1 se tornariam 100 + 5%, ou seja 105 em money.
    Porcentagem por level: 5.0
    # Máximo de léveis que o jogador pode comprar deste upgrade.
    Max: 3
    # Quantia de léveis que o jogador ganha ao se registrar.
    Default: 0.0
# Opções do armazém de drops.
Armazem:
  # Ativar o armazem
  Ativar: true
  # Permitir a venda direta de drops
  Venda: true
  # Permitir a coleta de drops.
  Coleta: true
# Opções de geração de mobs.
Gerar:
  # Gerar quando o jogador estiver offline.
  Offline: true
  # Gerar quando a chunk do spawner estiver descarregada. ( Pode gerar lag )
  Chunk descarregada: true
  # Raio de verificação do stack mobs
  Raio: 5
  # Nome do mob no stackmobs
  Nome: '&7{quantia}x &c{mob}'
  # Desativar a AI dos mobs
  NoAI: true
# Opções gerais do plugin
###
# O limite de spawners vai ser geral ou por cada spawner
Limite geral: false
# Acumular os bônus que tiver permissão
Acumular bonus: false
# Multiplicar o xp com a quantidade de mobs
XP multiplicar: false
# Limite máximo do stackmobs
# Deixe 0 para ser infinito
MobStack max: 0
# Ativar a variação de 20% para menos ou para mais da quantia de spawners.
# Por exemplo: 10 spawners com a variação em true. Gerariam entre 8 a 12 mobs.
Variacao: false
# Multiplicação fixa da looting de acordo ao nível e a quantia de mobs.
# Caso esteja ativado, será (drops x mobs x looting)
Fixo: true
# Ao matar segurando shift, irá matar apenas 1 mob do stackmobs.
Shift unitario: true
# Ativar a coleta de spawners armazenados
Spawners coleta: true
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
# Limite de spawners armazenados de cada tipo.
Limite spawners:
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
    Name: '&bLimite de spawners'
    Lore:
      - ''
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
      - ''
# Limite de drops armazenados de cada tipo.
Limite drops:
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
    Name: '&bLimite de drops'
    Lore:
      - ''
      - '&fQuantia: &a{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
      - ''
# Configuração da matadora de mobs.
Matadora:
  # Ativar a matadora.
  Usar: true
  # Item da matadora.
  Item:
    CustomSkull: false
    URL: ''
    ID: 276
    Data: 0
    Glow: true
    Name: '&bEspada matadora'
    Lore:
      - '&7Use para matar os mobs spawnados.'
      - '&7Clique com shift+botão direito para abrir a evolução.'
  # Encantamentos que vem por padrão na matadora.
  Default:
    # Multiplicador de drops. (Looting própria, infinita)
    Looting: 1
    # Encantamento para dropar recompensas.
    Sortudo: 0
    # Dano acrescido da matadora. ( Irá somar o encantamento dano + o dano vanilla do item)
    Dano: 1
  # Preços de cada encantamento.
  Precos:
    # Acréscimo de valor para cada nível.
    # Por exemplo: Nivel 1 custa 10, já o Nivel 2 custa 10 + 20%, ou seja, 12.
    Acrescimo: 20.0
    Looting: 20
    Sortudo: 20
    Dano: 20
  # Máximo de léveis para cada encantamento.
  Maximo:
    Looting: 3
    Sortudo: 5
    Dano: 10
  # Atributos de cada encantamento.
  Atributos por level:
    Looting: 10.0 # Recomendo deixar assim para um calculo mais proximo do vanilla.
    Sortudo: 5.0 # 5% de chance a cada nível para dropar recompensas.
    Dano: 1 # 1 de dano acrescido a cada nível.
# Interação ao clicar com botão direito em um mob do stackmobs.
Interacao:
  # Ativar a interação.
  Ativar: true
  # Mensagem que será enviada ao clicar no mob.
  Mensagem:
    - ''
    - '&cTipo do mob: &7{mob}'
    - '&cXP de evolução dropável: &7{xp}'
    - '&cSpawnado por: &7{spawner}'
    - '&cDono do spawner: &7{dono}'
    - '&cQuantidade stackada: &7{quantidade}'
    - ''
# Mensagens do plugin.
Mensagens:
  Permissao: '&cVocê não tem permissão para usar isto.'
  Help: '&cSub-comandos: givelimite, givelimitespawners, givelimitedrops, givespawner, espada, setspawn, delspawn.'
  Matadora desativada: '&cO sistema de matadora foi desativado.'
  Matadora dada: '&cMatadora dada ao jogador {player}.'
  Nao tem money: '&cDesculpe, mas você não possui a quantia necessária de money, &7{money} money&c.'
  Comprou spawner: '&aObrigado pela sua compra, você adquiriu {quantia}x &7Spawner ( {spawner} &7)&a com sucesso.'
  Comprou melhoria: '&aVocê adquiriu esta melhoria com sucesso.'
  Nao e numero: '&cO argumento não é um número.'
  Cancelou: '&cVocê cancelou a compra.'
  Local nao setado: '&cO local de spawn deste spawner não foi setado.'
  Local setado: '&aVocê setou o local de spawn deste spawner.'
  Local removido: '&aVocê removeu o local de spawn deste spawner.'
  Nao pode vender: '&cA venda foi bloqueada.'
  Nao pode coletar: '&cA coleta foi bloqueada.'
  Vendeu: '&aVocê vendeu &7{quantia}x {item} &apor &7{preco}&a.'
  Inv cheio: '&cSeu inventário está cheio.'
  XP insuficiente: '&cVocê não possui xp suficiente para isso.'
  Limite insuficiente: '&cVocê não possui limite suficiente. Disponível: &7{limite}&c.'
  Nao encontrado: '&cJogador não encontrado.'
  Deu: '&aVocê deu &e{quantia} &ade limite para o jogador &e{player}&a.'
  Converteu: '&cVocê compactou todos seus limites em 1.'
  Ativou: '&aVocê ativou &e{quantia} &ade limites.'
  Espada: '&cVocê necessita da espada matadora para isto.'
  Armazenou: '&aVocê armazenou &7{quantia}x &aspawners de &7( {spawner} )&a.'
  Deu spawner: '&aVocê deu &7{quantia}x &aspawner(s) de &7( {spawner} ) &apara o jogador &7{player}&a.'
  Quantia insuficiente: '&cVocê não tem spawners suficiente.'
  Recolheu: '&aVocê recolheu &7{quantia}x &aspawners de &7( {spawner} )&a.'
  Max limite: '&cVocê já chegou no máximo.'
  Seus spawners:
    - ''
    - '&cVocê não possui este spawner.'
    - '&7Disponíveis: {spawners}'
    - ''
  Digite:
    - ''
    - '&aDigite a quantia de spawners que deseja.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Seu limite:
    - '&bInformações sobre seus limites:'
    - ''
    - '&bLimite de compra: &7{limite_compra}&b.'
    - '&bLimite de spawners: &7{limite_spawners}&b.'
    - '&bLimite de drops: &7{limite_drops}&b.'
    - ''
  Limite jogador:
    - '&bInformações sobre os limites do jogador &f{player}&b:'
    - ''
    - '&bLimite de compra: &7{limite_compra}&b.'
    - '&bLimite de spawners: &7{limite_spawners}&b.'
    - '&bLimite de drops: &7{limite_drops}&b.'
    - ''
# Sons gerais do plugin.
Sons:
  # Ativar os sons.
  Usar: true
  # Som ao comprar uma melhoria.
  Comprar melhoria: 'LEVEL_UP'
  # Som ao comprar um spawner.
  Comprar spawner: 'VILLAGER_YES'
# Setas dos menu.
Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - ''
      - '&7Clique para voltar.'
      - ''
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróximo'
    Lore:
      - ''
      - '&7Clique para ir à próxima página.'
      - ''
# Itens que substituirá o spawner na loja de spawners.
Items:
  # Quando o item não foi liberado na data ainda.
  Nao pode:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 0
    Data: 0
    Glow: true
    Name: '{spawner}'
    Lore:
      - ''
      - '&cVocê não pode comprar este spawner.'
      - '&7Ele será liberado em: &f{data} - &f{hora}'
      - ''
  # Quando o jogador não tiver permissão de comprar aquele spawner.
  Permissao:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 0
    Data: 0
    Glow: true
    Name: '{spawner}'
    Lore:
      - ''
      - '&cVocê não pode comprar este spawner.'
      - '&7Você não possui permissão.'
      - ''
# Lore que substituirá a dos spawners.
Lores:
  # Lore na loja
  Lore comprar:
    - ''
    - '&fEntidade: &a{entidade}'
    - '&fDelay de spawn: &a{delay}s'
    - '&fPreço: &a{preco} &7(&e-{desconto}%&7)'
    - ''
    - '&7Clique com o botão esquerdo para comprar.'
    - ''
  # Lore para armazenar o spawner
  Lore ativar:
    - ''
    - '&fEntidade: &c{entidade}'
    - '&fDelay de spawn: &a{delay}s'
    - '&fQuantidade: &a{quantidade}'
    - ''
    - '&7Clique com o botão direito para armazenar.'
    - ''
# Formatos de quantia e money
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
# Formatador booleano.
Formatador:
  B true: '&aSim'
  B false: '&cNão'
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Estes descontos servirão para comprar spawners e melhorias.
# Você pode criar quantos quiser.
Descontos:
  VIP:
    Permissao: 'yspawners.vip'
    Desconto: 10.0
    Ordem: 1
]]>
</code-block>
</chapter>

<chapter title="mobs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Cadastro dos mobs e drops dos spawners.
# Obs: Será necessário configurar o drop na precos.yml.
# Lista de entidades (1.8.x): https://helpch.at/docs/1.8.8/org/bukkit/entity/EntityType.html
Mobs:
  CREEPER:
    # Drop que será armazenado ao matar este mob.
    Drop: '289:0'
    # Quantia de XP que será dada ao matar este mob.
    XP: 20
    # Deixe 0 para ser o do vanilla.
    Quantia: 1
]]>
</code-block>
</chapter>

<chapter title="precos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Preço de cada drop anteriormente configurado na mobs.yml
Precos:
  Preco1:
    # Drop configurado na mobs.yml.
    Drop: '289:0'
    # Preço unitário.
    Preco: 10.0
    # Display do drop no menu de armazém.
    Nome: '&cPólvora'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Recompensa que será dada ao matar um mob.
# Você pode criar quantas quiser.
Recompensas:
  Reco1:
    # Se o ( Command -> Use ) tiver true, isso não vai funcionar
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Glow: true
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aTu ganhou uma pedra.'
      # Se não desejar, deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    Chance: 30.0
    Command:
      Use: false
      # Se o ( Use ) tiver false, isso não funcionar.
      List:
        - 'give {player} stone 1'

]]>
</code-block>
</chapter>

<chapter title="spawners.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Spawners:
  1:
    # Esta opção servirá para usar nos comandos de setspawn e delspawn
    # Caso não esteja definida, irá pegar o nome da seção que neste caso é (1)
    # Defina identificadores diferentes para cada spawner
    Identificador: 'Creeper'
    # Item do spawner.
    Item:
      CustomSkull: false
      URL: ''
      ID: 383
      Data: 50
      Glow: true
      Name: '&aSpawner de Creeper'
      Lore:
        - ''
        - '&fAtivo: {ativo}'
        - '&fQuantidade: &b{quantia}'
        - '&fTempo de spawn: &a{tempo} &e-{tempoplayer}s'
        - ''
        - '&7Clique com o botão esquerdo para ativar/desativar.'
        - '&7Clique com o botão direito para setar o local de spawn.'
        - '&7Clique com o scroll para remover o local de spawn.'
        - '&7Clique com shift+botão esquerdo para recolher.'
        - ''
    # Delay para spawnar um mob.
    Delay de spawn: 5 # Em segundos
    # Mob que será spawnado.
    # Lista de entidades (1.8.x): https://helpch.at/docs/1.8.8/org/bukkit/entity/EntityType.html
    Tipo: 'CREEPER'
    # Data que será liberado o spawner para ser comprado na loja.
    Libera em: '01/01/2020-10:00'
    # Opções de compra.
    Comprar:
      # Preço de cada spawner.
      Preco: 100.0
      # Permissão para comprar o spawner.
      Permissao: 'yspawners.creeper'
  2:
    Item:
      CustomSkull: false
      URL: ''
      ID: 383
      Data: 54
      Glow: true
      Name: '&aSpawner de Zumbi'
      Lore:
        - ''
        - '&fAtivo: {ativo}'
        - '&fQuantidade: &b{quantia}'
        - '&fTempo de spawn: &a{tempo} &e-{tempoplayer}s'
        - ''
        - '&7Clique com o botão esquerdo para ativar/desativar.'
        - '&7Clique com o botão direito para setar o local de spawn.'
        - '&7Clique com o scroll para remover o local de spawn.'
        - '&7Clique com shift+botão esquerdo para recolher.'
        - ''
    Delay de spawn: 10 #em segundos
    Tipo: 'ZOMBIE'
    Libera em: '16/10/2020-10:00'
    Comprar:
      Preco: 110.0
      Permissao: 'yspawners.zumbi'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/24-ySpawnersVirtuais">Site do plugin ySpawnersVirtuais</a>
    </category>
</seealso>