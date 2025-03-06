# yBoosters
<secondary-label ref="utility"/>

### Descrição
Crie boosters para habilidades do mcmmo

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
<video src="//www.youtube.com/watch?v=nMREPQWK0LM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/booster - Abre o menu principal
/booster agradecer - Agradece o booster global
/booster removerglobal - Remove o booster global ativo
/booster removerplayer - Remove o booster global ativo
/booster givemcmmo - Dá um booster pessoal para um jogador
/booster givemcmmoglobal - Dá um booster global para um jogador
/booster ajuda - Mostra todos os comandos
/booster reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yboosters.agradecer - Permissão para o /booster agradecer
yboosters.removerglobal - Permissão para o /booster removerglobal
yboosters.removerplayer - Permissão para o /booster removerplayer
yboosters.givemcmmo - Permissão para o /booster givemcmmo
yboosters.givemcmmoglobal - Permissão para o /booster givemcmmoglobal
yboosters.ajuda - Permissão para o /booster ajuda
yboosters.usar - Permissão para o /booster
yboosters.pausar - Permissão para pausar um booster pessoal
yboosters.reload - Permissão para o /booster reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yboosters_pessoal_skill% - Retorna o nome da skill do booster pessoal
%yboosters_pessoal_multiplicador% - Retorna o multiplicador do booster pessoal
%yboosters_pessoal_tempo% - Retorna o tempo do booster pessoal
%yboosters_global_skill% - Retorna o nome da skill do booster global
%yboosters_global_multiplicador% - Retorna o multiplicador do booster global
%yboosters_global_tempo% - Retorna o tempo do booster global
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yBoosters/
    ├── menus/
    │    ├── habilidadeSelect.yml
    │    ├── preview.yml
    │    └── principal.yml
    ├── anuncios.yml
    ├── config.yml
    ├── habilidades.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="habilidadeSelect.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Booster - Habilidades'
Tamanho: 27
# Você pode adicionar mais habilidades
Itens:
  Espadas:
    # A skill que o booster irá ativar.
    Skill: 'SWORDS'
    Skill display: 'Espadas'
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: 276
    Data: 0
    Glow: true
    Name: '&aEspadas'
    Lore:
      - '&7Ganhe bônus de xp na evolução'
      - '&7da skill espadas.'
      - ''
      - '&aClique para ativar o booster.'
  Escavacao:
    # A skill que o booster irá ativar.
    Skill: 'EXCAVATION'
    Skill display: 'Escavação'
    Slot: 12
    CustomSkull: false
    URL: ''
    ID: 277
    Data: 0
    Glow: true
    Name: '&aEscavação'
    Lore:
      - '&7Ganhe bônus de xp na evolução'
      - '&7da skill escavação.'
      - ''
      - '&aClique para ativar o booster.'
# Enfeite o menu com estes itens
Itens custom: {}
  #Enfeite1:
  #  Slot: 11
  #  CustomSkull: false
  #  URL: ''
  #  ID: 1
  #  Data: 0
  #  Glow: true
  #  Name: ''
  #  Lore: []
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Recompensa Misteriosa'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Booster - Principal'
Tamanho: 27
Actionbar slot: 12
HabilidadeGlobal slot: 14
Habilidade slot: 16
Itens:
  Pontos:
    Slot: 10
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
    ID: 1
    Data: 0
    Glow: true
    Name: '&aPontos'
    Lore:
      - '&7Você ganha pontos quando um jogador lhe agradecer'
      - '&7por você ter ativado um booster global.'
      - ''
      - '&f > Você possui: &b{pontos} pontos&f.'
      - '&f > Custo da "Recompensa Misteriosa": &b1 ponto&f.'
      - ''
      - '&fEsquerdo&a para comprar a "Recompensa Misteriosa".'
      - '&fDireito&a para ver as recompensas da "Recompensa Misteriosa".'
  Actionbar sim:
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 5
    Glow: true
    Name: '&aActionbar'
    Lore:
      - '&aVocê está recebendo a notificação'
      - '&ado tempo restante do seu booster na'
      - '&aactionbar.'
  Actionbar nao:
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 14
    Glow: true
    Name: '&cActionbar'
    Lore:
      - '&cVocê não está recebendo a notificação'
      - '&cdo tempo restante do seu booster na'
      - '&cactionbar.'
  HabilidadeGlobal sim:
    CustomSkull: false
    URL: ''
    ID: 384
    Data: 0
    Glow: true
    Name: '&aBooster Global de Habilidades'
    Lore:
      - '&fSkill: &7{skill}&f.'
      - '&fMultiplicador: &7{multiplicador}&f.'
      - '&fDuração: &7{duracao}&f.'
  HabilidadeGlobal nao:
    CustomSkull: false
    URL: ''
    ID: 374
    Data: 0
    Glow: true
    Name: '&cBooster Global de Habilidades'
    Lore:
      - '&7Não há nenhum booster global'
      - '&7de habilidades ativo.'
  Habilidade sim:
    CustomSkull: false
    URL: ''
    ID: 384
    Data: 0
    Glow: true
    Name: '&cBooster de Habilidades'
    Lore:
      - '&fSkill: &7{skill}&f.'
      - '&fMultiplicador: &7{multiplicador}&f.'
      - '&fDuração: &7{duracao}&f.'
      - ''
      - '&7Estado: &r{estado}&7.'
      - ''
      - '&7Clique para pausar/retomar o booster.'
  Habilidade nao:
    CustomSkull: false
    URL: ''
    ID: 374
    Data: 0
    Glow: true
    Name: '&cBooster de Habilidades'
    Lore:
      - '&7Não há nenhum booster de'
      - '&7habilidades ativo.'
# Enfeite o menu com estes itens
Itens custom: {}
  #Enfeite1:
  #  Slot: 11
  #  CustomSkull: false
  #  URL: ''
  #  ID: 1
  #  Data: 0
  #  Glow: true
  #  Name: ''
#  Lore: []
]]>
</code-block>
</chapter>

</chapter>

<chapter title="anuncios.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Mensagem:
  - ''
  - '&8[Upgrade] &eO jogador &6{player} &eatingiu o lével &a{level} &ena skill &6{skill}&f.'
  - ''
# Leveis que serão anunciados
Leveis:
  - 1
  - 2
  - 3
  - 4
  - 5
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
  Booster:
    Comando: 'booster'
    Aliases: [ boosters ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Opções gerais do plugin
Opcoes:
  # Stackar o booster global com o booster proprio
  Stack: true
  # Actionbar do booster individual
  Actionbar: '&cBooster de &f{skill}&c, restante: &f{tempo}&c.'
  # Preço da recompensa misteriosa
  RecoMisteriosa preco: 1.0
  # Sistema de agradecer
  Agradecer:
    # Pontos mínimos a serem dados
    Min: 1.0
    # Pontos máximos a serem dados
    Max: 5.0

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Nao encontrado: '&cJogador não encontrado.'
  Nao e numero: '&cO argumento não é um número.'
  Recebeu habilidade: '&aVocê recebeu um booster de habilidades.'
  Deu habilidade: '&aVocê deu um booster de habilidades para o jogador &7{player}&a.'
  Nao global: '&cNão há nenhum booster global ativado.'
  Online: '&cEste jogador não está mais online.'
  Ja agradeceu: '&cVocê já agradeceu este booster.'
  Agradeceu: '&aVocê agradeceu o jogador &f{player}&a pelo booster.'
  Removeu global: '&cVocê removeu o booster global.'
  Possui: '&cVocê deve ter 1 ponto para comprar a "Recompensa Misteriosa".'
  Comprou: '&aVocê comprou a &f"Recompensa Misteriosa"&a por &f1 ponto&a.'
  Si mesmo: '&cVocê não pode agradecer a si mesmo.'
  Nao player: '&cO jogador {player} não tem nenhum booster ativado.'
  Removeu player: '&cVocê removeu o booster do player {player}.'
  Acabou habilidade:
    - ''
    - '&cSeu booster de habilidades encerrou.'
    - ''
  Acabou habilidade global:
    - ''
    - '&cO booster global de habilidades encerrou.'
    - ''
  Ja usando habilidade:
    - '&cVocê já está usando um booster de habilidades, use &7&n/boosters&c para checar.'
  Ja global habilidade:
    - '&cUm booster global de habilidades já está ativo, use &7&n/boosters&c para checar.'
  Ativou habilidade global:
    - '&eO jogador &8{player}&e ativou um booster &8Global&e de habilidades.'
    - '&f > &eSkill: &a{skill}&e.'
    - '&f > &eDuração: &a{duracao}&e.'
    - '&f > &eMultiplicador: &a{multiplicador}&e.'
  Ativou habilidade:
    - '&eVocê ativou um booster de habilidades&e.'
    - '&f > &eSkill: &a{skill}&e.'
    - '&f > &eDuração: &a{duracao}&e.'
    - '&f > &eMultiplicador: &a{multiplicador}&e.'

# Item do booster
# A lore do item é configurada em cada booster
# na habilidades.yml
Item:
  Habilidade:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
    ID: 0
    Data: 0
    Glow: true
    Name: '&8Booster de habilidades'
  Habilidade global:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/ff778f72eaca452ee013893e2bc53d8d5b1fca44cfe2703865b054c28a3dd7'
    ID: 0
    Data: 0
    Glow: true
    Name: '&8Booster Global de habilidades'
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

# Formatos de quantia
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

<chapter title="habilidades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Boosters:
  Booster1:
    # Duração do booster
    # em segundos
    Duracao: 10
    # Multiplicador do booster
    # em multiplicador direto (vezes).
    Multiplicador: 1.2
    Lore:
      - '&fDuracao: &710s&f.'
      - '&fMultiplicador: &71.2x&f.'
      - ''
      - '&aClique para escolher a habilidade'
      - '&ae ativar o booster.'
    Lore todas:
      - '&fDuracao: &710s&f.'
      - '&fMultiplicador: &71.2x&f.'
      - ''
      - '&e | Este booster vale para'
      - '&e | todas as skills.'
      - ''
      - '&aClique para ativar o booster.'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    Chance: 100.0
    # Item que aparecerá no preview do boss.
    Preview:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&fChance: &6100%'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será dado o item se os comandos estiverem em false.
    # Item que será dado ao jogador.
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEu valho muito!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: false
      List:
        - 'give {player} stone 1'

]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static BoosterAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;BoosterAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(BoosterAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/54-yBoosters">Site do plugin yBoosters</a>
    </category>
</seealso>