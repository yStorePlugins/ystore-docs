# yBossesVirtuais
<secondary-label ref="rankup"/>

### Descrição
Crie vários bosses, com diferenciados nomes e léveis, mate-o em GUI e receba recompensas.

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
<video src="//www.youtube.com/watch?v=gvZpSOd9edw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/boss - Abrir o menu de bosses.
/boss giveboss  - Dar um boss para um jogador.
/boss givematadora - Dar uma matadora para um jogador.
/boss givematadoraauto - Dar uma matadora automática para um jogador.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ybosses.usar - Permissão para o /bossybosses.giveboss - Permissão para o /boss givebossybosses.givematadora - Permissão para o /boss givematadora e /boss givematadoraauto</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yBossesVirtuais/
    ├── menus/
    │    ├── bossarmazenados.yml
    │    ├── bossprincipal.yml
    │    ├── bossspawnados.yml
    │    ├── loja.yml
    │    ├── lojabosses.yml
    │    ├── lojamatadoras.yml
    │    ├── preview.yml
    │    ├── principal.yml
    │    ├── recompensas.yml
    │    ├── top.yml
    │    ├── topmatadora.yml
    │    ├── topmatados.yml
    │    └── upgrades.yml
    ├── bosses.yml
    ├── config.yml
    ├── matadoraAuto.yml
    ├── matadoras.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="bossarmazenados.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Bosses armazenados'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cVazio'
   Lore:
   - ''
   - '&7Você não possui nenhum boss armazenado.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="bossprincipal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Bosses Principal'
Tamanho: 27
BackSlot: 18
Itens:
   Bosses:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/3857d6b17901fd3f0109bd9bdcc28021b65947fce0a958327247d26d92915b85'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aBosses Armazenados'
      Lore:
      - ''
      - '&7Clique para gerenciar seus bosses armazenados.'
      - ''
   Spawnados:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/8ddd74dfcc447bc2e787d5ba17361f27d910decafd275d60bd2aeaf83270'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aBosses Spawnados'
      Lore:
      - ''
      - '&7Clique para gerenciar seus bosses spawnados.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="bossspawnados.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Bosses Spawnados'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cVazio'
   Lore:
   - ''
   - '&7Você não possui nenhum boss spawnado.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="loja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Loja'
Tamanho: 27
BackSlot: 18
Itens:
   Bosses:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/3857d6b17901fd3f0109bd9bdcc28021b65947fce0a958327247d26d92915b85'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aBosses'
      Lore:
      - ''
      - '&7Clique para comprar bosses.'
      - ''
   Matadoras:
      Slot: 13
      CustomSkull: false
      URL: ''
      ID: 276
      Data: 0
      Glow: true
      Name: '&aMatadoras'
      Lore:
      - ''
      - '&7Clique para comprar matadoras.'
      - ''
   Upgrades:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aUpgrades'
      Lore:
      - ''
      - '&7Clique para comprar upgrades.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="lojabosses.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Loja de Bosses'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 18
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="lojamatadoras.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Loja de Matadoras'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 18
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Principal'
Tamanho: 27
Itens:
   Loja:
      Slot: 10
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aLoja'
      Lore:
      - ''
      - '&7Clique para comprar bosses e/ou upgrades.'
      - ''
   Top:
      Slot: 11
      CustomSkull: false
      URL: ''
      ID: 425
      Data: 0
      Glow: true
      Name: '&5TOP'
      Lore:
      - ''
      - '&7Clique para ver o TOP Bosses e o TOP Matadoras.'
      - ''
   Matadora automatica:
      Slot: 12 #para desativar deixe -1
      CustomSkull: false
      URL: ''
      ID: 425
      Data: 0
      Glow: true
      Name: '&aMatadora automática'
      Lore:
      - ''
      - '&7Clique para gerenciar sua matadora automatica.'
      - ''
   Bosses:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/8321bd865442f7af8f3aae159cb42d78e8fe63b21f51b367dfb0a4e642273ec3'
      ID: 0
      Data: 0
      Glow: true
      Name: '&cBosses'
      Lore:
      - ''
      - '&7Clique para ver e matar seus Bosses.'
      - ''
   Armazem:
      Slot: 14
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/d218cc1941492939ffbeccacca3a3342e8c260c333cea1b6dbfdd5e3bebd2f'
      ID: 0
      Data: 0
      Glow: true
      Name: '&6Armazém'
      Lore:
      - ''
      - '&7Clique para gerenciar suas recompensas.'
      - ''
   Perfil:
      Slot: 16
      Name: '&b{player}'
      Lore:
      - ''
      - '&fBosses matados: &a{matados}'
      - '&fBosses Spawnados: &a{min}&f/&a{max}'
      - '&fNível da Matadora: &a{matadora}'
      - '&fDano da Matadora: &a{danomatadora}'
      - ''
      - '&fAnti-Regressor: &a{regressor}%'
      - '&fAnti-Inviabilizador: &a{inviabilizador}%'
      - ''
      - '&fXP de evolução: &a{xptenho}&f/&a{xpnecessario}'
      - ''
      - '&fAcréscimo de Dano: &a{dano}%'
      - ''
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Recolher todos:
   Slot: 49
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&6Recolher todos'
   Lore:
   - ''
   - '&7Clique para recolher todas as recompensas.'
   - ''

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cVazio'
   Lore:
   - ''
   - '&7Você não possui nenhuma recompensa armazenada.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - TOP'
Tamanho: 27
BackSlot: 18
Itens:
   Matadora:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/3857d6b17901fd3f0109bd9bdcc28021b65947fce0a958327247d26d92915b85'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aTOP Matadoras'
      Lore:
      - ''
      - '&7Clique para ver o top matadoras.'
      - ''
   Matados:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aTOP Bosses matados'
      Lore:
      - ''
      - '&7Clique para ver o top bosses matados.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="topmatadora.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - TOP Matadoras'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Item:
   Name: '&b{player}'
   Lore:
   - ''
   - '&fJogador: &e{player}'
   - '&fPosição: &e{pos}º'
   - '&fLével da matadora: &a{matadora}'
   - ''
]]>
</code-block>
</chapter>

<chapter title="topmatados.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - TOP Matados'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Item:
   Name: '&b{player}'
   Lore:
   - ''
   - '&fJogador: &e{player}'
   - '&fPosição: &e{pos}º'
   - '&fBosses matados: &a{matados}'
   - ''
]]>
</code-block>
</chapter>

<chapter title="upgrades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bosses - Loja de Upgrades'
Tamanho: 27
BackSlot: 18
Itens:
   Max bosses spawnados:
      Slot: 10
      Usar: true
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aMáx bosses spawnados'
      Lore:
      - ''
      - '&fSeu level: &b{playerlevel}.'
      - '&fPróximo: &b{proximolevel}'
      - '&fPreço: &b{preco} &aem Money.'
      - ''
      - '&7Clique para comprar.'
      - ''
      Lore max:
      - ''
      - '&cVocê já atingiu o máximo desse upgrade.'
      - ''
   Anti-Regressor:
      Slot: 12
      Usar: true
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aAnti-Regressor'
      Lore:
      - ''
      - '&fSeu level: &b{playerlevel}%'
      - '&fPróximo: &b{proximolevel}%'
      - '&fPreço: &b{preco} &aem Money.'
      - ''
      - '&7Clique para comprar.'
      - ''
      Lore max:
      - ''
      - '&cVocê já atingiu o máximo desse upgrade.'
      - ''
   Anti-Inviabilizador:
      Slot: 13
      Usar: true
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aAnti-Inviabilizador'
      Lore:
      - ''
      - '&fSeu level: &b{playerlevel}%'
      - '&fPróximo: &b{proximolevel}%'
      - '&fPreço: &b{preco} &aem Money.'
      - ''
      - '&7Clique para comprar.'
      - ''
      Lore max:
      - ''
      - '&cVocê já atingiu o máximo desse upgrade.'
      - ''
   Acrescimo de dano:
      Slot: 14
      Usar: true
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aAcréscimo de dano'
      Lore:
      - ''
      - '&fSeu level: &b{playerlevel}%'
      - '&fPróximo: &b{proximolevel}%'
      - '&fPreço: &b{preco} &aem Money.'
      - ''
      - '&7Clique para comprar.'
      - ''
      Lore max:
      - ''
      - '&cVocê já atingiu o máximo desse upgrade.'
      - ''
   Matadora:
      Slot: 16
      Usar: true
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/564a91433d66bfc6ef1c9ac4e371a886a1c462c975ff8127761d703e0a3e7306'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aMatadora'
      Lore:
      - ''
      - '&fSeu level: &b{playerlevel}'
      - '&fPróximo: &b{proximolevel}'
      - ''
      - '&fSeu dano: &b{playerdano}'
      - '&fDano da próxima: &b{proximodano}'
      - ''
      - '&fPreço: &b{preco} &aem {tipo}.'
      - ''
      - '&7Clique para comprar.'
      - ''
      Lore max:
      - ''
      - '&cVocê já atingiu o máximo desse upgrade.'
      - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bosses.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bosses:
   1:
      Ovo:
         CustomSkull: false
         URL: ''
         ID: 383
         Data: 50
         Glow: true
         Name: '&aBoss Creeper'
         Lore:
         - ''
         - '&fVida: &c{vida}'
         - '&fLevel mínimo da Matadora: &b{matadora}'
         - ''
         - '&fRegredir: &c{regredir}%'
         - '&fInviabilizar: &c{inviabilizar}%'
         - ''
         - '&7Clique com botão direito para armazenar.'
         - ''
      Vida: 1000
      Matadora minimo: 0
      XP: 50
      Sons:
         Usar: true
         Dano: 'CREEPER_HISS'
         Matar: 'CREEPER_DEATH'
      Comprar:
         Tipo: 'Money'
         Preco: 100.0
         Compravel: true
      Efeitos:
         Regredir: #regredir 1 nível da matadora do player
            Usar: true
            Chance: 10.0
         Inviabilizar: #inviabilizar o player de dar dano no boss
            Usar: true
            Chance: 10.0
            Tempo: 10 #em segundos
      Recompensas:
      - '100,Reco1' #chance,recompensa
]]>
</code-block>
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

#Coloque yPoints, PlayerPoints ou JH_Shop ou yCash ou AtlasEconomiaSecundaria
Plugin de Pontos: 'PlayerPoints'

Um de cada tipo: false #permitir spawnar só 1 boss de cada tipo por vez
Tempo matadora automatica: 20 #em segundos

Comando:
   Comando: 'bosses'
   Aliases: []

Mensagens:
   Nao tem pontos: '&cDesculpe, mas você não possui a quantia necessária de pontos, &7{pontos} pontos&c.'
   Nao tem money: '&cDesculpe, mas você não possui a quantia necessária de money, &7{money} money&c.'
   Comprou boss: '&aObrigado pela sua compra, você adquiriu 1x &7Boss ( {boss} &7)&a com sucesso.'
   Comprou matadora: '&aObrigado pela sua compra, você adquiriu 1x &7Matadora nível {matadora}&a com sucesso.'
   Comprou upgrade: '&aVocê adquiriu este upgrade com sucesso.'
   Maximo: '&cVocê atingiu o máximo de bosses spawnados.'
   Ja spawnado: '&cVocê já tem um boss desse tipo spawnado, mate-o primeiro antes de spawnar outro.'
   Spawnado: '&aVocê spawnou um boss do tipo &7( {boss} &7)&a.'
   Minimo: '&cSua matadora não tem o level mínimo para este boss.'
   Regredido: '&cVocê teve sua matadora regredida, ou seja, perdeu um nível.'
   Inviabilizado: '&cVocê foi antingido pelo efeito de inviabilizar. Você não pode bater em bosses por {tempo} segundos.'
   Nao bater: '&cVocê está impossibilitado de bater em bosses durante {tempo} segundos.'
   Evoluiu: '&aVocê alcançou o XP necessário para evolução da matadora, como consequência, teve sua matadora evoluida.'
   Inv cheio: '&cSeu inventário está cheio.'
   Matadora maior: '&cVocê possui uma matadora melhor ou equivalente a essa.'
   Matadora ativa: '&aVocê ativou uma matadora melhor.'
   Nao compravel: '&cEsta matadora não pode ser comprada.'
   MatadoraAuto ja: '&cVocê já possui a matadora automática.'
   MatadoraAuto ativa: '&aVocê ativou sua matadora automática.'
   Armazenou: '&aVocê armazenou seu(s) boss(es).'
   Nao e numero: '&cO argumento não é um número.'
   Cancelou: '&cVocê cancelou a compra.'
   Quantia insuficiente: '&cVocê não tem bosses suficiente.'
   Recolheu: '&aVocê recolheu &7{quantia}x &abosses de &7( {boss} )&a.'
   Digite:
   - ''
   - '&aDigite a quantia de bosses que deseja.'
   - '&7para cancelar digite &ncancelar&7.'
   - ''
   
Formatador:
   Money: 'Money'
   Points: 'Cash'
   Vida: true

Sons:
   Usar: true
   Comprar upgrade: 'LEVEL_UP'
   Comprar boss: 'VILLAGER_YES'

Upgrades:
   Valores default:
      Max boss spawnados: 1
      Anti-Regressor: 0.0
      Anti-Inviabilizador: 0.0
      Acrescimo de dano: 0.0
      
   Valores maximos:
      Max boss spawnados: 2
      Anti-Regressor: 5.0
      Anti-Inviabilizador: 4.0
      Acrescimo de dano: 3.0
   
   Precos:
      Max boss spawnados:
         Tipo: 'MONEY'
         Preco: 100.0
         Porcentagem por level: 30.0
         Acrescentar: 1
      Anti-Regressor:
         Tipo: 'MONEY'
         Preco: 120.0
         Porcentagem por level: 50.0
         Acrescentar: 1.0
      Anti-Inviabilizador:
         Tipo: 'MONEY'
         Preco: 110.0
         Porcentagem por level: 10.0
         Acrescentar: 1.0
      Acrescimo de dano:
         Tipo: 'MONEY'
         Preco: 100.0
         Porcentagem por level: 30.0
         Acrescentar: 1.0
         
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
      Name: '&cVoltar'
      Lore:
      - '&7Clique para voltar à página anterior.'
   Proximo:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&aPróximo'
      Lore:
      - '&7Clique para ir à próxima página.'

Lores:
   Lore bater:
   - ''
   - '&fVida: &c{vida}'
   - '&fLevel mínimo da Matadora: &b{matadora}'
   - ''
   - '&fRegredir: &c{regredir}% &e- {playerregredir}%'
   - '&fInviabilizar: &c{inviabilizar}% &e- {playerinviabilizar}%'
   - '&fDano da matadora: &c{danomatadora}'
   - ''
   - '&fQuantidade spawnada: &b{quantia}'
   - ''
   - '&7Clique com botão esquerdo para dar dano.'
   - '&7Clique com botão direito para de-spawnar.'
   - '&7Clique com botão do meio para ver as recompensas.'
   - ''
   Lore comprar:
   - ''
   - '&fVida: &c{vida}'
   - '&fLevel mínimo da Matadora: &b{matadora}'
   - ''
   - '&fRegredir: &a{regredir}%'
   - '&fInviabilizar: &a{inviabilizar}%'
   - ''
   - '&fPreço: &a{preco} em {tipo}'
   - ''
   - '&7Clique com o botão esquerdo para comprar.'
   - '&7Clique com o botão direito para ver as recompensas.'
   - ''
   Lore ativar:
   - ''
   - '&fVida: &c{vida}'
   - '&fLevel mínimo da Matadora: &b{matadora}'
   - ''
   - '&fRegredir: &a{regredir}%'
   - '&fInviabilizar: &a{inviabilizar}%'
   - ''
   - '&7Clique com o botão direito para armazenar.'
   - ''
   Lore spawnar:
   - ''
   - '&fVida: &c{vida}'
   - '&fLevel mínimo da Matadora: &b{matadora}'
   - ''
   - '&fRegredir: &a{regredir}% &e- {playerregredir}%'
   - '&fInviabilizar: &a{inviabilizar}% &e- {playerinviabilizar}%'
   - ''
   - '&fQuantidade armazenada: &a{quantia}'
   - ''
   - '&7Clique com botão esquerdo para spawnar.'
   - '&7Clique com botão direito para recolher em forma de item.'
   - '&7Clique com botão do meio para ver as recompensas.'
   - ''
      
Formats:
 - ''
 - ''
 - 'K'
 - 'M'
 - 'B'
]]>
</code-block>
</chapter>

<chapter title="matadoraAuto.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Matadora automatica'
Tamanho: 27
BackSlot: 18

Default: false

Comprar:
   Compravel: true
   Tipo: 'MONEY'
   Preco: 100.0
   Comprou: '&aObrigado pela sua compra, você adquiriu a matadora automática com sucesso.'
   
Item fisico:
   CustomSkull: false
   URL: ''
   ID: 276
   Data: 0
   Glow: true
   Name: '&aMatadora automática'
   Lore:
   - '&7Clique com botão direito para ativar.'
   
Item:
   Slot: 13
   CustomSkull: false
   URL: ''
   ID: 276
   Data: 0
   Glow: true
   Name: '&aMatadora automática'
   Lore:
   - ''
   - '&fPreço: &7100 money'
   - ''
   - '&7Clique para comprar.'
   - ''
   Lore on:
   - ''
   - '&fEstado: &aON'
   - ''
   - '&7Clique para desativar.'
   - ''
   Lore off:
   - ''
   - '&fEstado: &cOFF'
   - ''
   - '&7Clique para ativar.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="matadoras.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Matadoras:
   Default:
      Ordem: 1
      Nivel: 0
      Dano: 20
      Regredir: true
      Evoluir: false #evolucao com xp
      Comprar:
         Compravel: true
         Tipo: 'MONEY'
         Preco: 0.0
         XP: 0
      Item:
         CustomSkull: false
         URL: ''
         ID: 276
         Data: 0
         Glow: true
         Name: '&aMatadora Default'
         Lore:
         - ''
         - '&fDano: &c20'
         - ''
         - '&7Clique com botão direito para ativar.'
         - ''
      Loja:
         CustomSkull: false
         URL: ''
         ID: 276
         Data: 0
         Glow: true
         Name: '&aMatadora Default'
         Lore: #esta matadora é a default, portanto não irá aparecer.
         - ''
   Nivelado:
      Ordem: 2
      Nivel: 0
      Dano: 50
      Regredir: true
      Evoluir: false #evolucao com xp
      Comprar:
         Compravel: true
         Tipo: 'MONEY'
         Preco: 5000.0
         XP: 20
      Item:
         CustomSkull: false
         URL: ''
         ID: 276
         Data: 0
         Glow: true
         Name: '&aMatadora Nivelado'
         Lore:
         - ''
         - '&fDano: &c50'
         - ''
         - '&7Clique com botão direito para ativar.'
         - ''
      Loja:
         CustomSkull: false
         URL: ''
         ID: 276
         Data: 0
         Glow: true
         Name: '&aMatadora Nivelado'
         Lore:
         - ''
         - '&fDano: &c50'
         - ''
         - '&fPreço: &a5K em money.'
         - ''
         - '&7Clique para comprar.'
   Avancada:
      Ordem: 3
      Nivel: 1
      Dano: 9999999 #deixe 9999999 para hitkill
      Regredir: false
      Evoluir: false #evolucao com xp
      Comprar:
         Compravel: false
         Tipo: 'MONEY'
         Preco: 10000.0
         XP: 100
      Item:
         CustomSkull: false
         URL: ''
         ID: 276
         Data: 0
         Glow: true
         Name: '&aMatadora Avançada'
         Lore:
         - ''
         - '&fDano: &cHitKill'
         - ''
         - '&7Clique com botão direito para ativar.'
         - ''
      Loja: #se não for comprável, não irá aparecer
         CustomSkull: false
         URL: ''
         ID: 276
         Data: 0
         Glow: true
         Name: '&aMatadora Avançada'
         Lore:
         - ''

]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   Reco1:
      Preview:
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         - '&aTu vais ganhar uma pedra.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         - '&aTu ganhou uma pedra.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/23-yBossesVirtuais">Site do plugin yBossesVirtuais</a>
    </category>
</seealso>