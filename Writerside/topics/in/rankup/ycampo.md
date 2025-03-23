# yCampo
<secondary-label ref="rankup"/>

### Descrição
Plantas agora dão dinheiro aos jogadores

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
<video src="//www.youtube.com/watch?v=E1e3fqp8GNM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/campo - Abre o menu principal
/tesoura - Recebe uma tesoura
/campo ajuda - Envia a mensagem de ajuda
/campo ir - Vai até a área de campo
/campo sair - Sai da área de campo
/campo flores - Abre o menu de flores
/campo armazem - Abre o menu de recompensas armazenadas
/campo top - Abre o menu de top
/fertilizantes - Vê a quantia de corais
/fertilizantes [player] - Vê a quantia de fertilizantes de um jogador
/fertilizantes enviar - Envia seus fertilizantes para um jogador
/fertilizantes add - Adiciona fertilizantes para um jogador
/fertilizantes give - Dá fertilizantes em forma de itens para um jogador
/fertilizantes set - Seta fertilizantes para um jogador
/fertilizantes remove - Remove fertilizantes de um jogador
/campo setspawn - Seta o local de spawn da área de campo
/campo setsaida - Seta a saída de campo
/campo givebooster - Dá um booster à um jogador
/campo give - Dá uma tesoura à um jogador
/campo reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycampo.use - Permissão para o /campo, /campo flores, /campo armazem, /campo top
ycampo.tool - Permissão para o /tesoura
ycampo.go - Permissão para o /pesca ir
ycampo.exit - Permissão para o /pesca sair
ycampo.coin.use - Permissão para o /fertilizantes
ycampo.coin.look - Permissão para o /fertilizantes [player]
ycampo.coin.send - Permissão para o /fertilizantes enviar
ycampo.coin.help - Permissão para o /fertilizantes ajuda
ycampo.coin.add - Permissão para o /fertilizantes add
ycampo.coin.remove - Permissão para o /fertilizantes remove
ycampo.coin.set - Permissão para o /fertilizantes set
ycampo.coin.give - Permissão para o /fertilizantes give
ycampo.setspawn - Permissão para o /campo setspawn
ycampo.setexit - Permissão para o /campo setexit
ycampo.givebooster - Permissão para o /campo givebooster
ycampo.give - Permissão para o /campo give
ycampo.reload - Permissão para o /campo reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ycampo_time% - Retorna o tempo que o jogador ficou no campo
%ycampo_time_raw% - Retorna o tempo que o jogador ficou no campo sem formatar
%ycampo_broken% - Retorna a quantia de plantas que o jogador quebrou
%ycampo_broken_raw% - Retorna a quantia de plantas que o jogador quebrou sem formatar
%ycampo_pvp% - Retorna se o player está com o pvp ativo
%ycampo_pvp_raw% - Retorna se o player está com o pvp ativo sem formatar
%ycampo_coin% - Retorna a quantia de fertilizantes do jogador
%ycampo_coin_raw% - Retorna a quantia de fertilizantes&nbsp;do jogador sem formatar
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCampo/
    ├── addons/
    │    └── enchants.yml
    ├── enchants/
    │    ├── custom_enchants.yml
    │    ├── enchants.yml
    │    └── thunderEnchants.yml
    ├── areas.yml
    ├── boosters.yml
    ├── bungee.yml
    ├── bungeecord.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── flowers.yml
    ├── menus.yml
    ├── messages.yml
    ├── plugin.yml
    ├── rewards.yml
    └── skins.yml
</code-block>
</chapter>

<chapter title="addons" collapsible="true">
<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Explosao:
  Ordem: 6
  Display: 'Explosao'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 3 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Laser:
  Ordem: 7
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 10 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aLaser<nl>&eativado' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Boomerang:
  Ordem: 8
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&eBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="enchants" collapsible="true">
<chapter title="custom_enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Encantamentos:
  Chaveiro:
    Ordem: 5
    Display: 'Chaveiro'
    Padrao: 0
    Maximo: -1
    BonusPorLevel: 10.0 # em porcentagem
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    # chance,comando
    Comandos:
      - '20,give {player} quartz 1'
    Mensagens:
      Title: '&aChave<nl>&eencontrado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        Material: GOLD_INGOT
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Bônus atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} fertilizantes&f.'
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      NaoPode: # quando não puder evoluir
        Material: GOLD_INGOT
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} fertilizantes&f.'
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem valores suficientes.'
      Maximo: # quando já estiver no máximo
        Material: GOLD_INGOT
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Bônus de drop
Fortuna:
  # Ordem do enchant no menu
  Ordem: 2
  Display: 'Bônus'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: GOLD_INGOT
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: GOLD_INGOT
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: GOLD_INGOT
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'
# Aumenta chance nas recompensas
Sortudo:
  Ordem: 3
  Display: 'Sortudo'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'
# Ganhar mais moedas de farm
Multiplicador:
  Ordem: 4
  Display: 'Multiplicador'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Multiplicador Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Velocidade:
  Ordem: 5
  Display: 'Velocidade'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Duracao: 200 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: FEATHER
      Name: '&aVelocidade'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha o efeito de velocidade na mina.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: FEATHER
      Name: '&aVelocidade'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha o efeito de velocidade na mina.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: FEATHER
      Name: '&aVelocidade'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha o efeito de velocidade na mina.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="thunderEnchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Explosao:
  Ordem: 6
  Display: 'Explosao'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 3 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Laser:
  Ordem: 7
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 10 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aLaser<nl>&eativado' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Boomerang:
  Ordem: 8
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&eBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
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
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aClique para comprar'
      previous:
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&cVocê precisa comprar a anterior'
      has:
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aVocê já possui esta area'
      equipped:
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aVocê está nessa area'
]]>
</code-block>
</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Sistema de boosters
# Você pode criar quantos boosters quiser
boosters:
  booster1:
    time: 60 # em segundos
    bonus: 10.0 # porcentagem a mais
    items:
      interact:
        material: 'EXP_BOTTLE:0'
        name: '&aBônus de campo'
        lore:
          - '&7Este booster permite que você ganhe'
          - '&7mais ao quebrar plantas.'
          - ''
          - '&aTempo: &e{time}'
          - '&aPorcentagem: &e{bonus}%'
          - ''
      menu:
        material: 'EXP_BOTTLE:0'
        name: '&aBônus de campo'
        lore:
          - '&aVocê possui um booster ativo'
          - ''
          - '&7Este booster permite que você ganhe'
          - '&7mais ao quebrar plantas.'
          - ''
          - '&aTempo: &e{time}'
          - '&aPorcentagem: &e{bonus}%'
          - ''
]]>
</code-block>
</chapter>

<chapter title="bungee.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: yCampo
version: '${project.version}'
main: com.ystoreplugins.ycampo.bungee.MainBungee
authors: [ yChusy ]
website: https://ystoreplugins.com.br

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
# SERVER (ex: servidor que contém o campo)
mode: 'LOBBY'

# Nome do servidor na config do BungeeCord em que o jogador vai ao sair do campo
exit: 'rankup'

# Nome do servidor na config do BungeeCord em que o jogador vai ao entrar no campo
entry: 'mina'

# Delay para enviar a vara ao trocar para o servidor do campo
# em ticks
delay: 3

# Bloquear ações neste servidor caso esteja fora do campo
# Somente caso o "Modo" for "SERVER"
# permissão de bypass: ycampo.blocked.bypass
block-actions: true
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
  campo: 'campo'
  coin: 'fertilizante|fertilizantes|flores|flor|flower|flowers'
  tool: 'tesoura'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____
#  _   _ / ___|__ _ _ __ ___  _ __   ___
# | | | | |   / _` | '_ ` _ \| '_ \ / _ \
# | |_| | |__| (_| | | | | | | |_) | (_) |
#  \__, |\____\__,_|_| |_| |_| .__/ \___/
#  |___/                     |_|
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
# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Ativar a invisibilidade na área de campo
invisibility: false

# Abrir menu de evolução ao interagir com a tesoura (Shift+Botão direito)
interact-menu: true

# Somar um nível a mais na evolução
sum-evolute: true

# Máximo permitido para evoluir com Q
q-max: 0

# Acumular os bônus que tiver permissão
acumulate-bonus: false

# Limite de plantações quebradas por segundo
limit-broken-second: 5

# Delay para resetar a plantação pro jogador
# em segundos
reset-delay: 5

# Dar a ferramenta ao entrar no campo caso o jogador não tiver ela no inventário
give-enter: true

# Altura do void do seu servidor
void-detect: 0

# Sistemas gerais
general:
  # Slot da ferramenta no inventário
  tool-slot: 2
  # Esconder o encantamento na lore da picareta caso o player desative ele
  # caso esteja false, o encantamento ficará riscado na lore da ferramenta
  hide-deactivated: false
  # Fazer com que a ferramenta nunca quebre
  tool-unbreakable: true
  # Materiais que irão ser reconhecidos na skin
  skin-materiais:
    - 'WOOD'
    - 'STONE'
    - 'IRON'
    - 'GOLD'
    - 'DIAMOND'

# Sistema de pvp
pvp:
  enable: true
  # Lucro com pvp off
  off-receiving: 70.0
  # Lucro com pvp on
  on-receiving: 100.0
  # Delay para executar o comando de pvp
  delay: 60
  # Actionbar persistente
  # deixe '' para não usar
  actionbar-off: '&c&lPVP &cdesativado! &8 - &fLucro {receiving}%  &7/pvp {pvp_time}'
  actionbar-on: '&a&lPVP &aativo! &8 - &fLucro {receiving}%  &7/pvp {pvp_time}'
  # Ativar o PVP por padrão assim que entrar no campo
  default: false

# Sistema de scoreboard
scoreboard:
  enabled: true
  title: '&b&lyStore'
  # Delay para atualizar a scoreboard (em segundos)
  delay: 1
  lines:
    - '&7         Área de campo'
    - ''
    - '&f Plantas quebradas: &7{broken}'
    - '&f Tempo no campo: &7{time}'
    - '&f PVP Ativado: &7{pvp}'
    - ''
    - '&f Coins: &2$&a%yeconomy_money%'
    - ''
    - '&b    ystoreplugins.com.br'

# Sistema de comandos no campo
commands:
  # Lista de comandos permitidos no campo
  allowed: [ '/g', '/l', '/campo' ]
  # Lista de comandos para sair do campo
  exit: [ '/sair', '/spawn', '/exit' ]
  # Lista de comandos para executar o pvp
  pvp: [ '/pvp' ]

# Sistema de bônus
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender para a loja do servidor.
bonus:
  member:
    priority: 1
    # Permissão para ser reconhecido
    permission: 'ycampo.bonus.member'
    # Quantia do bônus em %
    bonus: 10.0

# Sistema de lores
lore:
  chance: ['', '&6Chance: &f{chance}%', '']

# Item de coin ativável
usable-item:
  material: '1ba16c3890af39c3f2d576586cff443de07dad32b2315e2ff6f0d5d6a3c663dd'
  name: '&b+{amount} Fertilizantes'
  lore:
    - ''
    - '&fQuantia: &b{amount}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus fertilizantes no inventário em 1 só.'
    - ''

# Item da tesoura
tool:
    material: SHEARS
    name: '&bTesoura &7[{broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locais: {}
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
    permission: 'ycampo.provider.money'
]]>
</code-block>
</chapter>

<chapter title="flowers.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
flowers:
  red-rose:
    # Permissão para quebrar a planta
    permission-break: ''
    # Mensagem de permissão
    permission-message: '&cVocê ainda não pode quebrar a ROSA.'
    # Definir um item custom para o display preview
    # Deixe '' para usar o padrão do bloco
    preview-display: ''
    # Materiais que serão reconhecidos
    materials:
      # material que deverá ser quebrado
      break-material: 'RED_ROSE:0'
      # material que vai virar ao quebrar
      to-material: AIR
      # material que vai virar ao resetar
      reset-material: 'RED_ROSE:0'
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
        # Altura que o holograma vai spawnar na flor
        hologram-off-set: 0.6
        # mensagens de venda
        message:
          actionbar: '&e&lCAMPO: &a+{money} coins &7(+{bonus}%) &c{receiving}%'
          title: ''
          chat: ''
        # quantidade de flores (coin/fertilizante) que será dada
        flower: 1.0
        # quantidade que será dada em outras economias
        prices:
          price1:
            provider: 'money'
            price: 1.0
        # Recompensas do boss
        # As recompensas são cadastradas na recompensas.yml
        # Use: chance,recompense
        # Quantia de recompensas que serão dadas
        reward-amount: 1
        # Dropar as recompensas no chão
        reward-ground: false
        rewards: [ '100,reward1' ]
  double_plant:
    permission-break: ''
    # Mensagem de permissão
    permission-message: '&cVocê ainda não pode quebrar a ROSA DUPLA.'
    materials:
      break-material: 'DOUBLE_PLANT:0'
      to-material: AIR
      reset-material: 'DOUBLE_PLANT:0'
    effects:
      break-particle: ''
      break-sound: ''
      reset-particle: 'HAPPY_VILLAGER'
      reset-sound: ''
    sells:
      sell1:
        order: 1
        permission: ''
        hologram: [ '&a+{money}' ]
        hologram-off-set: 1.0
        message:
          actionbar: '&e&lCAMPO: &a+{money} coins &7(+{bonus}%) &c{receiving}%'
          title: ''
          chat: ''
        flower: 1.0
        prices:
          price1:
            provider: 'money'
            price: 1.0
        reward-amount: 1
        reward-ground: false
        rewards: [ '100,reward1' ]
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
  name: '&8Campo - Principal'
  size: 36
  items:
    profile-slot: 10
    rewards-slot: 12
    flowers-slot: 14
    top-slot: 16
    booster-slot: 20
    areas-slot: 22
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7jogador no campo.'
        - ''
        - ' &8▶ &fTempo no campo: &7{time}'
        - ''
        - ' &8▶ &fFlores quebradas: &7{broken}'
        - ' &8▶ &fRecompensas no armazém: &7{rewards}'
        - ' &8▶ &fFertilizantes: &a✿&f{coin}'
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
    flowers:
      material: 'RED_ROSE'
      name: '&dFlores'
      lore:
        - '&7Consulte as possíveis'
        - '&7recompensas das flores.'
        - ''
        - '&dClique para acessar!'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em nosso campo.'
        - ''
        - '&aClique para acessar!'
    booster:
      material: 'GLASS_BOTTLE:0'
      name: '&aBooster'
      glow: true
      lore:
        - '&cVocê não possui nenhum booster ativo.'
    go:
      slot: 24
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aIr ao campo'
      lore:
        - '&7Clique para entrar na'
        - '&7área de campo'
    leave:
      slot: 24
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cSair do campo'
      lore:
        - '&7Clique para sair da'
        - '&7área de campo'
    areas:
      material: TNT
      name: '&bÁreas'
      lore:
        - '&7Evolua sua área de campo'
        - '&7e tenha plantações diferenciadas.'
        - ''
        - '&aClique para fazer o upgrade'

# Menu de recompensas
main-rewards:
  name: '&8Campo - Recompensas'
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

# Preview de flores
flowers:
  name: '&8Campo'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  lore:
    - '&7Clique para ver as recompensas'

# Preview de recompensas
rewards-preview:
  name: '&8Campo'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu de top
top:
  name: '&8Campo - Destaques'
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
        name: 'Flores quebradas'
      coin:
        enabled: true
        name: 'Fertilizantes'
      time:
        enabled: true
        name: 'Tempo no campo'
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
        - '&fFlores quebradas: &7{amount}'
        - '&fPosição: &7{pos}'
    # Item do top coin
    coin:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fFertilizantes: &7{amount}'
        - '&fPosição: &7{pos}'
    # Item do top tempo no campo
    time:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fTempo no campo: &7{amount}'
        - '&fPosição: &7{pos}'

evolute:
  name: '&8Campo - Evoluir'
  size: 36
  slots: [ 11, 13, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  # Slot onde ficará a tesoura do jogador
  tool-slot: 31
  profile-slot: 33
  items:
    profile:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&fFertilizantes: &b{coin}'
        - ''

# Menu de upgrade de área
upgrade-areas:
  name: '&8Campo - Áreas'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 31
  previous-slot: 18
  next-slot: 26
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
  title: '&bBem vindo à área de campo'
  actionbar: '&bVocê entrou na área de campo.'
  chat: |

    &bBem vindo à área de campo.

  sound: 'ORB_PICKUP'

# Mensagens e ações ao sair
leave:
  title: ''
  actionbar: '&bVocê saiu da área de campo.'
  chat: |

    &bVocê saiu da área de campo.

  sound: 'ORB_PICKUP'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/campo &8- &7Abre o menu principal.
    &a/campo ir &8- &7Vai até o campo.
    &a/campo flores &8- &7Abre o menu de flores disponíveis.
    &a/campo armazem &8- &7Abre o menu de armazém de recompensas.
    &a/campo top &8- &7Abre o menu de top.
    &a/campo sair &8- &7Sai do campo.
    &a/campo setspawn &8- &7Seta o local de spawn do campo.
    &a/campo setareaspawn &8- &7Seta o local de spawn de uma área do campo.
    &a/campo setsaida &8- &7Seta o local de saída do campo.
    &a/campo givebooster &8- &7Dá um booster à um jogador.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  not-in: '&cVocê não está na área de campo.'
  spawn: '&cO spawn da área de campo não foi setado.'
  exit: '&cA saída da área de campo não foi setada.'
  set-exit: '&aLocal de saída setado com sucesso.'
  set-spawn: '&aLocal de spawn setado com sucesso.'
  command: '&cVocê não pode usar este comando na área de campo. Utilize /spawn para sair dele.'
  coin-help: |

    &a/fertilizantes &8- &7Ver os seus fertilizantes.
    &a/fertilizantes <player> &8- &7Ver os fertilizantes de alguém.
    &a/fertilizantes enviar <player> <quantia> &8- &7Envia seus fertilizantes para alguém.
    &a/fertilizantes give <player/all> <quantia> &8- &7Dar fertilizantes a alguém.
    &a/fertilizantes add <player> <quantia> &8- &7Adiciona fertilizantes a alguém.
    &a/fertilizantes set <player> <quantia> &8- &7Remove fertilizantes de alguém.
    &a/fertilizantes remove <player> <quantia> &8- &7Seta fertilizantes a alguém.

  coin: '&bVocê possui &f{coin} fertilizantes&b.'
  coin-player: '&bO jogador &f{player}&b possui &f{coin} fertilizantes&b.'
  coin-added: '&bVocê adicionou &f{coin} fertilizantes&b ao jogador &f{player}&b.'
  coin-removed: '&bVocê removeu &f{coin} fertilizantes&b do jogador &f{player}&b.'
  coin-set: '&bVocê setou &f{coin} fertilizantes&b para o jogador &f{player}&b.'
  coin-sent: '&bVocê enviou &f{coin} fertilizantes&b para o jogador &f{player}&b.'
  coin-received: '&bVocê recebeu &f{coin} fertilizantes&b do jogador &f{player}&b.'
  coin-has: '&cVocê não possui a quantia de &f{coin}&c fertilizantes.'
  converted: '&bVocê compactou todos seus fertilizantes em 1.'
  activated: '&bVocê ativou &f{coin} fertilizantes&b.'
  give: '&bVocê deu &f{coin} &bfertilizantes para o jogador &f{player}&b.'
  give-all: |

    &bO usuário &f{player}&b deu &f{coin} &bfertilizantes para todos os jogadores online&b.

  coin-added-all: '&bVocê adicionou &f{coin} fertilizantes&b para todos os jogadores&b.'
  holding: '&cVocê não está segurando uma tesoura.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  pvp-on: '&aVocê ativou o modo de combate.'
  pvp-off: '&cVocê desativou o modo de combate.'
  pvp-wait: '&cVocê deve aguardar {time} para alterar o modo de combate.'
  booster-null: |
    &cEste booster não existe.
    &cDisponíveis: &7{list}
  booster-give: '&aVocê deu x{amount} Booster(s) &8(+{bonus}%) &apara o jogador &f{player}&a.'
  booster-received: '&aVocê recebeu x{amount} Booster(s) &8(+{bonus}%)&a.'
  booster-finished: '&aCampo: &cSeu booster acabou.'
  booster-has: '&cVocê já está com um booster ativado.'
  booster-activated: '&aVocê ativou um booster de campo. Bônus: &e{bonus}&a. Tempo: &e{time}&a.'
  give-tool: '&bVocê deu uma tesoura para o jogador &f{player}&b.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  evolute: '&aO encantamento &f{enchant}&a foi evoluído para o nível &f{level}&a.'
  tool: '&aVocê recebeu sua tesoura do campo.'
  digit: |

    &aDigite a quantia de níveis que você quer adquirir ao encantamento &f{encantamento}&a.
    &7para cancelar digite &ncancelar&7.

  exceeds: '&cEstes níveis excedem o nível máximo do encantamento.'
  area-found: '&cÁrea não encontrada. Disponíveis: {list}'
  area-set-spawn: '&aLocal de spawn da área setado com sucesso.'
  area-bought: '&aVocê comprou a área.'
  slot-empty: '&cO slot {slot} deve estar vazio para poder receber a ferramenta. Por favor, re-entre no campo.'
  skin-found: '&cEsta skin não existe. Disponíveis: &7{list}'
  skin-give: '&bVocê deu uma skin para o jogador &f{player}&b.'
  skin-has: '&aA ferramenta já possui esta ou uma melhor skin ativada.'
  skin-activated: '&aSkin ativada com sucesso.'
]]>
</code-block>
</chapter>

<chapter title="plugin.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: yCampo
version: '${project.version}'
main: com.ystoreplugins.ycampo.Main
authors: [ yChusy ]
website: https://ystoreplugins.com.br
depend: [ yPlugins ]
softdepend: [ HolographicDisplays, DecentHolograms, PlaceholderAPI ]

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
      title: '&7+64 Pedras'
      actionbar: ''
      chat: '&7+64 Pedras'
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
    # Mensagens que serão enviadas ao receber a recompensa
    messages:
      title: '&b+1 Diamante'
      actionbar: ''
      chat: '&b+1 Diamante'
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
    # Mensagens que serão enviadas ao receber a recompensa
    messages:
      title: '&a+1 Esmeralda'
      actionbar: ''
      chat: '&a+1 Esmeralda'
]]>
</code-block>
</chapter>

<chapter title="skins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Skins:
  stone:
    order: 1
    type: 'STONE'
    custom-model-data: 0
    name: '&bTesoura &7[{broken}]'
    item:
      material: 'STONE'
      name: '&aSkin de Pedra'
      lore: ['&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&aClique na ferramenta para ativar']
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - '&a+10% ( PEDRA )'
      - ''
    bonus: 10.0
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCampo/
    ├── addons/
    │    └── enchants.yml
    ├── enchants/
    │    ├── custom_enchants.yml
    │    ├── enchants.yml
    │    └── thunderEnchants.yml
    ├── areas.yml
    ├── boosters.yml
    ├── bungeecord.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── flowers.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="addons" collapsible="true">
<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Explosao:
  Ordem: 6
  Display: 'Explosao'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 3 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Laser:
  Ordem: 7
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 10 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aLaser<nl>&eativado' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Boomerang:
  Ordem: 8
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&eBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="enchants" collapsible="true">
<chapter title="custom_enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Encantamentos:
  Chaveiro:
    Ordem: 5
    Display: 'Chaveiro'
    Padrao: 0
    Maximo: -1
    BonusPorLevel: 10.0 # em porcentagem
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    # chance,comando
    Comandos:
      - '20,give {player} quartz 1'
    Mensagens:
      Title: '&aChave<nl>&eencontrado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        Material: GOLD_INGOT
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Bônus atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} fertilizantes&f.'
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      NaoPode: # quando não puder evoluir
        Material: GOLD_INGOT
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} fertilizantes&f.'
          - '&f > Custo: &a{money} coins&f.'
          - ''
          - '&cVocê não tem valores suficientes.'
      Maximo: # quando já estiver no máximo
        Material: GOLD_INGOT
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Bônus de drop
Fortuna:
  # Ordem do enchant no menu
  Ordem: 2
  Display: 'Bônus'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: GOLD_INGOT
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: GOLD_INGOT
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: GOLD_INGOT
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'
# Aumenta chance nas recompensas
Sortudo:
  Ordem: 3
  Display: 'Sortudo'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'
# Ganhar mais moedas de farm
Multiplicador:
  Ordem: 4
  Display: 'Multiplicador'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Multiplicador Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Velocidade:
  Ordem: 5
  Display: 'Velocidade'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Duracao: 200 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: FEATHER
      Name: '&aVelocidade'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha o efeito de velocidade na mina.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: FEATHER
      Name: '&aVelocidade'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha o efeito de velocidade na mina.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: FEATHER
      Name: '&aVelocidade'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha o efeito de velocidade na mina.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="thunderEnchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Explosao:
  Ordem: 6
  Display: 'Explosao'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 3 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aExplosao'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Laser:
  Ordem: 7
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Raio: 10 # em ticks
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aLaser<nl>&eativado' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: BLAZE_ROD
      Name: '&aLaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

Boomerang:
  Ordem: 8
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  NivelPorcentagem: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      Material: TNT
      Name: '&eBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} fertilizantes&f.'
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem valores suficientes.'
    Maximo: # quando já estiver no máximo
      Material: TNT
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre várias plantações ao ativar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance Atual: &b{chance}%&f.'
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
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aClique para comprar'
      previous:
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&cVocê precisa comprar a anterior'
      has:
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aVocê já possui esta area'
      equipped:
        material: 'WHEAT'
        name: '&aÁrea {order} &8(Trigo)'
        lore:
          - '&7Área: &b{order}'
          - '&7Plantação: &bTrigo'
          - ''
          - '&7Preço: &2$&f{money}'
          - ''
          - '&aVocê está nessa area'
]]>
</code-block>
</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Sistema de boosters
# Você pode criar quantos boosters quiser
boosters:
  booster1:
    time: 60 # em segundos
    bonus: 10.0 # porcentagem a mais
    items:
      interact:
        material: 'EXP_BOTTLE:0'
        name: '&aBônus de campo'
        lore:
          - '&7Este booster permite que você ganhe'
          - '&7mais ao quebrar plantas.'
          - ''
          - '&aTempo: &e{time}'
          - '&aPorcentagem: &e{bonus}%'
          - ''
      menu:
        material: 'EXP_BOTTLE:0'
        name: '&aBônus de campo'
        lore:
          - '&aVocê possui um booster ativo'
          - ''
          - '&7Este booster permite que você ganhe'
          - '&7mais ao quebrar plantas.'
          - ''
          - '&aTempo: &e{time}'
          - '&aPorcentagem: &e{bonus}%'
          - ''
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
# SERVER (ex: servidor que contém o campo)
mode: 'LOBBY'

# Nome do servidor na config do BungeeCord em que o jogador vai ao sair do campo
exit: 'rankup'

# Nome do servidor na config do BungeeCord em que o jogador vai ao entrar no campo
entry: 'mina'

# Delay para enviar a vara ao trocar para o servidor do campo
# em ticks
delay: 3

# Bloquear ações neste servidor caso esteja fora do campo
# Somente caso o "Modo" for "SERVER"
# permissão de bypass: ycampo.blocked.bypass
block-actions: true
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
  campo: 'campo'
  coin: 'fertilizante|fertilizantes|flores|flor|flower|flowers'
  tool: 'tesoura'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____
#  _   _ / ___|__ _ _ __ ___  _ __   ___
# | | | | |   / _` | '_ ` _ \| '_ \ / _ \
# | |_| | |__| (_| | | | | | | |_) | (_) |
#  \__, |\____\__,_|_| |_| |_| .__/ \___/
#  |___/                     |_|
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
# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Ativar a invisibilidade na área de campo
invisibility: false

# Abrir menu de evolução ao interagir com a tesoura (Shift+Botão direito)
interact-menu: true

# Somar um nível a mais na evolução
sum-evolute: true

# Máximo permitido para evoluir com Q
q-max: 0

# Acumular os bônus que tiver permissão
acumulate-bonus: false

# Limite de plantações quebradas por segundo
limit-broken-second: 5

# Delay para resetar a plantação pro jogador
# em segundos
reset-delay: 5

# Dar a ferramenta ao entrar no campo caso o jogador não tiver ela no inventário
give-enter: true

# Altura do void do seu servidor
void-detect: 0

# Sistemas gerais
general:
  # Slot da ferramenta no inventário
  tool-slot: 2
  # Esconder o encantamento na lore da picareta caso o player desative ele
  # caso esteja false, o encantamento ficará riscado na lore da ferramenta
  hide-deactivated: false
  # Fazer com que a ferramenta nunca quebre
  tool-unbreakable: true
  # Materiais que irão ser reconhecidos na skin
  skin-materiais:
    - 'WOOD'
    - 'STONE'
    - 'IRON'
    - 'GOLD'
    - 'DIAMOND'

# Sistema de pvp
pvp:
  enable: true
  # Lucro com pvp off
  off-receiving: 70.0
  # Lucro com pvp on
  on-receiving: 100.0
  # Delay para executar o comando de pvp
  delay: 60
  # Actionbar persistente
  # deixe '' para não usar
  actionbar-off: '&c&lPVP &cdesativado! &8 - &fLucro {receiving}%  &7/pvp {pvp_time}'
  actionbar-on: '&a&lPVP &aativo! &8 - &fLucro {receiving}%  &7/pvp {pvp_time}'
  # Ativar o PVP por padrão assim que entrar no campo
  default: false

# Sistema de scoreboard
scoreboard:
  enabled: true
  title: '&b&lyStore'
  # Delay para atualizar a scoreboard (em segundos)
  delay: 1
  lines:
    - '&7         Área de campo'
    - ''
    - '&f Plantas quebradas: &7{broken}'
    - '&f Tempo no campo: &7{time}'
    - '&f PVP Ativado: &7{pvp}'
    - ''
    - '&f Coins: &2$&a%yeconomy_money%'
    - ''
    - '&b    ystoreplugins.com.br'

# Sistema de comandos no campo
commands:
  # Lista de comandos permitidos no campo
  allowed: [ '/g', '/l', '/campo' ]
  # Lista de comandos para sair do campo
  exit: [ '/sair', '/spawn', '/exit' ]
  # Lista de comandos para executar o pvp
  pvp: [ '/pvp' ]

# Sistema de bônus
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender para a loja do servidor.
bonus:
  member:
    priority: 1
    # Permissão para ser reconhecido
    permission: 'ycampo.bonus.member'
    # Quantia do bônus em %
    bonus: 10.0

# Sistema de lores
lore:
  chance: ['', '&6Chance: &f{chance}%', '']

# Item de coin ativável
usable-item:
  material: '1ba16c3890af39c3f2d576586cff443de07dad32b2315e2ff6f0d5d6a3c663dd'
  name: '&b+{amount} Fertilizantes'
  lore:
    - ''
    - '&fQuantia: &b{amount}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus fertilizantes no inventário em 1 só.'
    - ''

# Item da tesoura
tool:
    material: SHEARS
    name: '&bTesoura &7[{broken}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locais: {}
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
    permission: 'ycampo.provider.money'
]]>
</code-block>
</chapter>

<chapter title="flowers.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
flowers:
  red-rose:
    # Permissão para quebrar a planta
    permission-break: ''
    # Mensagem de permissão
    permission-message: '&cVocê ainda não pode quebrar a ROSA.'
    # Definir um item custom para o display preview
    # Deixe '' para usar o padrão do bloco
    preview-display: ''
    # Materiais que serão reconhecidos
    materials:
      # material que deverá ser quebrado
      break-material: 'RED_ROSE:0'
      # material que vai virar ao quebrar
      to-material: AIR
      # material que vai virar ao resetar
      reset-material: 'RED_ROSE:0'
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
        # Altura que o holograma vai spawnar na flor
        hologram-off-set: 0.6
        # mensagens de venda
        message:
          actionbar: '&e&lCAMPO: &a+{money} coins &7(+{bonus}%) &c{receiving}%'
          title: ''
          chat: ''
        # quantidade de flores (coin/fertilizante) que será dada
        flower: 1.0
        # quantidade que será dada em outras economias
        prices:
          price1:
            provider: 'money'
            price: 1.0
        # Recompensas do boss
        # As recompensas são cadastradas na recompensas.yml
        # Use: chance,recompense
        # Quantia de recompensas que serão dadas
        reward-amount: 1
        # Dropar as recompensas no chão
        reward-ground: false
        rewards: [ '100,reward1' ]
  double_plant:
    permission-break: ''
    # Mensagem de permissão
    permission-message: '&cVocê ainda não pode quebrar a ROSA DUPLA.'
    materials:
      break-material: 'DOUBLE_PLANT:0'
      to-material: AIR
      reset-material: 'DOUBLE_PLANT:0'
    effects:
      break-particle: ''
      break-sound: ''
      reset-particle: 'HAPPY_VILLAGER'
      reset-sound: ''
    sells:
      sell1:
        order: 1
        permission: ''
        hologram: [ '&a+{money}' ]
        hologram-off-set: 1.0
        message:
          actionbar: '&e&lCAMPO: &a+{money} coins &7(+{bonus}%) &c{receiving}%'
          title: ''
          chat: ''
        flower: 1.0
        prices:
          price1:
            provider: 'money'
            price: 1.0
        reward-amount: 1
        reward-ground: false
        rewards: [ '100,reward1' ]
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
  name: '&8Campo - Principal'
  size: 36
  items:
    profile-slot: 10
    rewards-slot: 12
    flowers-slot: 14
    top-slot: 16
    booster-slot: 20
    areas-slot: 22
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7jogador no campo.'
        - ''
        - ' &8▶ &fTempo no campo: &7{time}'
        - ''
        - ' &8▶ &fFlores quebradas: &7{broken}'
        - ' &8▶ &fRecompensas no armazém: &7{rewards}'
        - ' &8▶ &fFertilizantes: &a✿&f{coin}'
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
    flowers:
      material: 'RED_ROSE'
      name: '&dFlores'
      lore:
        - '&7Consulte as possíveis'
        - '&7recompensas das flores.'
        - ''
        - '&dClique para acessar!'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em nosso campo.'
        - ''
        - '&aClique para acessar!'
    booster:
      material: 'GLASS_BOTTLE:0'
      name: '&aBooster'
      glow: true
      lore:
        - '&cVocê não possui nenhum booster ativo.'
    go:
      slot: 24
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aIr ao campo'
      lore:
        - '&7Clique para entrar na'
        - '&7área de campo'
    leave:
      slot: 24
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cSair do campo'
      lore:
        - '&7Clique para sair da'
        - '&7área de campo'
    areas:
      material: TNT
      name: '&bÁreas'
      lore:
        - '&7Evolua sua área de campo'
        - '&7e tenha plantações diferenciadas.'
        - ''
        - '&aClique para fazer o upgrade'

# Menu de recompensas
main-rewards:
  name: '&8Campo - Recompensas'
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

# Preview de flores
flowers:
  name: '&8Campo'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  lore:
    - '&7Clique para ver as recompensas'

# Preview de recompensas
rewards-preview:
  name: '&8Campo'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu de top
top:
  name: '&8Campo - Destaques'
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
        name: 'Flores quebradas'
      coin:
        enabled: true
        name: 'Fertilizantes'
      time:
        enabled: true
        name: 'Tempo no campo'
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
        - '&fFlores quebradas: &7{amount}'
        - '&fPosição: &7{pos}'
    # Item do top coin
    coin:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fFertilizantes: &7{amount}'
        - '&fPosição: &7{pos}'
    # Item do top tempo no campo
    time:
      material: '{player}'
      name: '&7{player}'
      lore:
        - '&fTempo no campo: &7{amount}'
        - '&fPosição: &7{pos}'

evolute:
  name: '&8Campo - Evoluir'
  size: 36
  slots: [ 11, 13, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  # Slot onde ficará a tesoura do jogador
  tool-slot: 31
  profile-slot: 33
  items:
    profile:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&fFertilizantes: &b{coin}'
        - ''

# Menu de upgrade de área
upgrade-areas:
  name: '&8Campo - Áreas'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  back-slot: 31
  previous-slot: 18
  next-slot: 26
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
  title: '&bBem vindo à área de campo'
  actionbar: '&bVocê entrou na área de campo.'
  chat: |

    &bBem vindo à área de campo.

  sound: 'ORB_PICKUP'

# Mensagens e ações ao sair
leave:
  title: ''
  actionbar: '&bVocê saiu da área de campo.'
  chat: |

    &bVocê saiu da área de campo.

  sound: 'ORB_PICKUP'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/campo &8- &7Abre o menu principal.
    &a/campo ir &8- &7Vai até o campo.
    &a/campo flores &8- &7Abre o menu de flores disponíveis.
    &a/campo armazem &8- &7Abre o menu de armazém de recompensas.
    &a/campo top &8- &7Abre o menu de top.
    &a/campo sair &8- &7Sai do campo.
    &a/campo setspawn &8- &7Seta o local de spawn do campo.
    &a/campo setareaspawn &8- &7Seta o local de spawn de uma área do campo.
    &a/campo setsaida &8- &7Seta o local de saída do campo.
    &a/campo givebooster &8- &7Dá um booster à um jogador.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  not-in: '&cVocê não está na área de campo.'
  spawn: '&cO spawn da área de campo não foi setado.'
  exit: '&cA saída da área de campo não foi setada.'
  set-exit: '&aLocal de saída setado com sucesso.'
  set-spawn: '&aLocal de spawn setado com sucesso.'
  command: '&cVocê não pode usar este comando na área de campo. Utilize /spawn para sair dele.'
  coin-help: |

    &a/fertilizantes &8- &7Ver os seus fertilizantes.
    &a/fertilizantes <player> &8- &7Ver os fertilizantes de alguém.
    &a/fertilizantes enviar <player> <quantia> &8- &7Envia seus fertilizantes para alguém.
    &a/fertilizantes give <player/all> <quantia> &8- &7Dar fertilizantes a alguém.
    &a/fertilizantes add <player> <quantia> &8- &7Adiciona fertilizantes a alguém.
    &a/fertilizantes set <player> <quantia> &8- &7Remove fertilizantes de alguém.
    &a/fertilizantes remove <player> <quantia> &8- &7Seta fertilizantes a alguém.

  coin: '&bVocê possui &f{coin} fertilizantes&b.'
  coin-player: '&bO jogador &f{player}&b possui &f{coin} fertilizantes&b.'
  coin-added: '&bVocê adicionou &f{coin} fertilizantes&b ao jogador &f{player}&b.'
  coin-removed: '&bVocê removeu &f{coin} fertilizantes&b do jogador &f{player}&b.'
  coin-set: '&bVocê setou &f{coin} fertilizantes&b para o jogador &f{player}&b.'
  coin-sent: '&bVocê enviou &f{coin} fertilizantes&b para o jogador &f{player}&b.'
  coin-received: '&bVocê recebeu &f{coin} fertilizantes&b do jogador &f{player}&b.'
  coin-has: '&cVocê não possui a quantia de &f{coin}&c fertilizantes.'
  converted: '&bVocê compactou todos seus fertilizantes em 1.'
  activated: '&bVocê ativou &f{coin} fertilizantes&b.'
  give: '&bVocê deu &f{coin} &bfertilizantes para o jogador &f{player}&b.'
  give-all: |

    &bO usuário &f{player}&b deu &f{coin} &bfertilizantes para todos os jogadores online&b.

  coin-added-all: '&bVocê adicionou &f{coin} fertilizantes&b para todos os jogadores&b.'
  holding: '&cVocê não está segurando uma tesoura.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  pvp-on: '&aVocê ativou o modo de combate.'
  pvp-off: '&cVocê desativou o modo de combate.'
  pvp-wait: '&cVocê deve aguardar {time} para alterar o modo de combate.'
  booster-null: |
    &cEste booster não existe.
    &cDisponíveis: &7{list}
  booster-give: '&aVocê deu x{amount} Booster(s) &8(+{bonus}%) &apara o jogador &f{player}&a.'
  booster-received: '&aVocê recebeu x{amount} Booster(s) &8(+{bonus}%)&a.'
  booster-finished: '&aCampo: &cSeu booster acabou.'
  booster-has: '&cVocê já está com um booster ativado.'
  booster-activated: '&aVocê ativou um booster de campo. Bônus: &e{bonus}&a. Tempo: &e{time}&a.'
  give-tool: '&bVocê deu uma tesoura para o jogador &f{player}&b.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  evolute: '&aO encantamento &f{enchant}&a foi evoluído para o nível &f{level}&a.'
  tool: '&aVocê recebeu sua tesoura do campo.'
  digit: |

    &aDigite a quantia de níveis que você quer adquirir ao encantamento &f{encantamento}&a.
    &7para cancelar digite &ncancelar&7.

  exceeds: '&cEstes níveis excedem o nível máximo do encantamento.'
  area-found: '&cÁrea não encontrada. Disponíveis: {list}'
  area-set-spawn: '&aLocal de spawn da área setado com sucesso.'
  area-bought: '&aVocê comprou a área.'
  slot-empty: '&cO slot {slot} deve estar vazio para poder receber a ferramenta. Por favor, re-entre no campo.'
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
      title: '&7+64 Pedras'
      actionbar: ''
      chat: '&7+64 Pedras'
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
    # Mensagens que serão enviadas ao receber a recompensa
    messages:
      title: '&b+1 Diamante'
      actionbar: ''
      chat: '&b+1 Diamante'
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
    # Mensagens que serão enviadas ao receber a recompensa
    messages:
      title: '&a+1 Esmeralda'
      actionbar: ''
      chat: '&a+1 Esmeralda'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static CampoAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;CampoAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(CampoAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/107-yCampo">Site do plugin yCampo</a>
    </category>
</seealso>