# yAlmas
<secondary-label ref="rankup"/>

### Descrição
Mobs e jogadores no teu servidor possam dropar suas almas ao morrer e, com a possibilidade de ele renascer em forma de um boss Morto Vivo

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
<video src="//www.youtube.com/watch?v=-nZtSwrlKW0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/almas - Abre o menu principal
/almas  - Vê a quantia de almas de um jogador
/almas pagar - Envia almas para um jogador usando teu saldo de almas
/almas setar - Seta uma quantia de almas para um jogador
/almas remover - Remove uma quantia de almas de um jogador
/almas add - Dá uma quantia de almas para um jogador
/almas givebooster - Dá boosters para um jogador
/almas givelivro - Dá o livro do ceifador para um jogador
/almas giveboss - Dá o boss para um jogador
/almas setnpc - Seta o NPC de almas
/almas delnpc - Deleta o NPC de almas
/almas reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yalmas.usar - Permissão para o /almas
yalmas.olhar - Permissão para o /almas
yalmas.pagar - Permissão para o /almas pagar
yalmas.setar - Permissão para o /almas setar
yalmas.remover - Permissão para o /almas remover
yalmas.add - Permissão para o /almas add
yalmas.givebooster - Permissão para o /almas givebooster
yalmas.givelivro - Permissão para o /almas givelivro
yalmas.giveboss - Permissão para o /almas giveboss
yalmas.setnpc - Permissão para o /almas setnpc
yalmas.delnpc - Permissão para o /almas delnpc
yalmas.reload - Permissão para o /almas reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yalmas_almas% - Retorna a quantia de almas.
%yalmas_formatado% - Retorna a quantia de almas formatado (K, M, B, T...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yAlmas/
    ├── menus/
    │    ├── principal.yml
    │    └── top.yml
    ├── bonus.yml
    ├── boosters.yml
    ├── config.yml
    ├── desconto.yml
    ├── loja.yml
    ├── mobs.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8yAlmas - Principal'
Tamanho: 27
Itens:
   Perfil: # primeiro
      Slot: 11
      CustomSkull: true
      URL: '{player}'
      ID: 0
      Data: 0
      Glow: false
      Name: '&f{player}'
      Lore:
      - ''
      - '&cQuantia de almas: &f{almas}&c.'
      - ''
      - '&fBônus: &b{bonus}%&f.'
      - ''
      Lore booster:
      - ''
      - '&fMultiplicador do booster: &b{boosterprct}%'
      - '&fTempo restante: &b{boostertempo}&f.'
      - ''
      - '&cQuantia de almas: &f{almas}&c.'
      - ''
      - '&fBônus: &b{bonus}%&f.'
      - ''
   Loja: #segundo
      Slot: 13
      CustomSkull: false
      URL: ''
      ID: 266
      Data: 0
      Glow: false
      Name: '&aLoja'
      Lore:
      - '&7Clique para gastar tuas almas.'
      - '&7Desconto: &a{desconto}%&f.'
   Top: #terceiro
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/4ea96c49302132167c81c87b79e06dd343020ff20923fce87d388c462409261c'
      ID: 0
      Data: 0
      Glow: false
      Name: '&aTOP'
      Lore:
      - '&7Clique para ver os jogadores com mais almas.'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Almas'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fAlmas: &6{almas}'
   - '&fPosição: &6{pos}'
   - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bonus:
   VIP:
      Ordem: 1
      Permissao: 'yalmas.vip'
      Bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Boosters:
   Booster1:
      Tempo: 60 #em segundos
      Bonus: 10.0
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
   
Comando:
   Comando: 'almas'
   Aliases: [alma, soul, souls]
      
Actionbar: 
   Ativar: true #ao ganhar almas irá mandar uma msg no actionbar
   Mensagem: '&c[Almas] Você ganhou &7{almas} &calmas. &7({bonus}%)'

# Opcoes de configuração do NPC
NPC:
   ID: 9232912
   Skin: 'ySpeed_'
   Holograma:
      Altura: 3.1
      Holograma:
         - '&5Almas'
         - '&7Clique para gerenciar suas almas.'

Metadata: 'ySpawners-MobStacked' #deixe vazio para não usar
# Ao matar com shift, dar apenas a quantia de almas de 1 mob morto.
Shift unitario: true
# Ao matar com shift, dropar o boss
Boss shift: false
# Ao matar o boss criar um baú
# obs: os itens físicos (sem considerar os comandos),
# irão dropar no chão.
Chest spawn: true
# Acumular os bônus que tiver permissão
Acumular bonus: false
   
Player kill:
   Anti-Anterior: true #o jogador irá precisar aguardar x tempo para poder ganhar almas ao matar aquele mesmo jogador
   Delay: 3 #delay para o anti-anterior
   Quantia: 50.0 #quantia de almas por kill
   Chance: 100.0
   Mundos:
   - 'world'
   
Mensagens:
   Permissao: '&cVocê não tem permissão para isto.'
   Permissao plot: '&cVocê não tem permissão neste terreno.'
   Setado npc: '&aNPC do correio setado com sucesso.'
   Removido npc: '&aNPC do correio removido com sucesso'
   Nao setado npc: '&cO NPC não está setado.'
   Nao encontrado: '&cEste jogador não foi encontrado.'
   Booster recebeu: '&aVocê recebeu &7{quantia} &a booster(s) de drops.'
   Booster deu: '&aVocê deu &7{quantia} &a booster(s) de drops para o jogador &7{player}&a.'
   Nao e numero: '&cO argumento não é um número.'
   Acabou booster: '&cSeu booster de drops acabou.'
   Ja esta booster: '&cVocê já está usando um booster.'
   Ativou booster: '&aVocê ativou um booster de drops. Multiplicador: &e{bonus}&a. Tempo: &e{tempo}&a.'
   Adicionou: '&cVocê adicionou &7{almas} &cpara o jogador &7{player}&c.'
   Pagar si mesmo: '&cVocê não pode pagar a si mesmo.'
   Pagou: '&cVocê pagou ao jogador &7{player} &cuma quantia de &7{almas} &calmas.'
   Pagou player: '&cVocê recebeu do jogador &7{player} &cuma quantia de &7{almas} &calmas.'
   Removeu: '&cVocê removeu &7{almas} &cdo jogador &7{player}&c.'
   Remover mais: '&cVocê não pode remover esta quantia, o jogador &7{player} &ctem apenas &7{almas}&c almas.'
   Setou: '&cVocê setou &7{almas} &cpara o jogador &7{player}&c.'
   Olhar: '&cO jogador &7{player} &cpossui &7{almas} &calmas.'
   Suficiente: '&cVocê não tem almas suficiente &7{almas}&c.'
   Inv cheio: '&cSeu inventário está cheio.'
   Comprou: '&aVocê adquiriu coisas na loja por: &7{almas}&a. Desconto: &7{desconto}%&a.'
   Nao pode enchant: '&cEste encantamento não serve para este item.'
   Ja possui enchant: '&cSeu item já possui este encantamento.'
   Encantado: '&aSeu item foi encantado com sucesso.'
   Livro deu: '&aVocê deu &7{quantia}&a de livros ceifador para o jogador &7{player}&a.'
   Livro recebeu: '&aVocê recebeu &7{quantia} &a de livros ceifador.'
   Boss deu: '&aVocê deu &7{quantia}&a de Bosses para o jogador &7{player}&a.'
   Boss recebeu: '&aVocê recebeu &7{quantia} &a de Bosses.'
   Parte de cima: '&cVocê deve spawnar o boss na face de cima do bloco.'
   Mobs ou spawners: '&cHá mobs ou spawners por perto, spawne-o mais distante.'
   Usando ceifadora: '&cVocê deve estar usando uma ceifadora.'
   
Boss:
   Bloco de spawn: 'SOUL_SAND'
   Raio de checagem: 5 #verifica se há mobs por perto antes de spawnar
   PlotSquared: false #ao ativar, só poderá ser spawnado no plot
   Entidade:
      Tipo: 'WITHER_SKELETON'
      Vida: 1000
      Nome: '&c&lMorto Vivo'
      Actionbar: '&eVida do &7Morto Vivo &8(&c{vida}&8/&c{max}&8)'
      RequerirCeifadora: true
      Dano da ceifadora: 10
      Raio: true #manda um raio quando spawna e quando morre
      Morcegos: true #spawna morcegos quando spawna e quando morre
      Efeitos: #caso não queira deixe ( - '' ) ou ( - 'none' )
      - '30,WITHER:4-1' #chance,EFEITO:TEMPO-LEVEL (em segundos)
      - '70,POISON:4-1'
      - '10,SLOW:4-1'
      Dano:
         Chance: 50.0
         Dano: 4 #deixe 0 para desativar. O dano é calculado a partir da vida total (20)
      Jogar pra cima: 10.0 #deixe 0 para desativar
   Encantamento:
      Nome: 'Ceifador'
      Encanta:
      - 'DIAMOND_SWORD'
      - 'IRON_SWORD'
      - 'STONE_SWORD'
      - 'WOOD_SWORD'
      - 'GOLD_SWORD'
      Item:
         CustomSkull: false
         URL: ''
         ID: 403
         Data: 0
         Glow: false
         Name: '&eLivro de encantamento'
         Lore:
         - '&7Ceifador I'
         - ''
         - '&eClique em cima de uma espada para encantá-la.'
   Item:
      CustomSkull: false
      URL: ''
      ID: 383
      Data: 5
      Glow: true
      Name: '&cSpawn do &7Morto Vivo'
      Lore:
      - ''
      - '&fVida: &c1000 HP'
      - '&fSpawne-o em cima de uma &careia das almas&f.'
      - ''
   Mensagens:
      Title:
         Ativar: true
         Title: '&cVocê recebeu um ovo'
         Subtitle: '&cdo &7Morto Vivo'
      Chat:
         Ativar: true
         Mensagem:
         - ''
         - '&cVocê recebeu um ovo do &7Morto Vivo&c.'
         - ''
      Morrer:
         Title:
            Ativar: true
            Title: '&cVocê matou'
            Subtitle: '&cum &7Morto Vivo'
         Chat:
            Ativar: true
            Mensagem:
            - ''
            - '&cVocê matou um &7Morto Vivo&c.'
            - '&cPegue suas recompensas no baú'
            - ''
         
Booster:
   CustomSkull: false
   URL: ''
   ID: 384
   Data: 0
   Glow: true
   Name: '&aMultiplicador de almas'
   Lore:
   - ''
   - '&aTempo: &e{tempo}'
   - '&aMultiplicador: &e{bonus}%'
   - ''
   
Setas:
   Voltar:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/f84f597131bbe25dc058af888cb29831f79599bc67c95c802925ce4afba332fc'
      ID: 262
      Data: 0
      Glow: true
      Name: '&c&lVoltar'
      Lore:
      - ''
      - '&7Clique para voltar.'
      - ''
   Proximo:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/4ef356ad2aa7b1678aecb88290e5fa5a3427e5e456ff42fb515690c67517b8'
      ID: 262
      Data: 0
      Glow: true
      Name: '&a&lPróximo'
      Lore:
      - ''
      - '&7Clique para ir à próxima página.'
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

<chapter title="desconto.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Ordem: 1
      Permissao: 'yalmas.vip'
      Desconto: 10.0
]]>
</code-block>
</chapter>

<chapter title="loja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Loja:
   Nome: '&8Mercado Negro'
   Tamanho: 54
   Back slot: 27
   Items:
      Pedra preciosa:
         Slot: 10
         Preco: 10000.0
         CustomSkull: false
         URL: ''
         Name: '&cPedra preciosa'
         ID: 1
         Data: 0
         Quantia: 64
         Usar lore: true
         Lore:
         - ''
         - '&cCompre para se tornar um mago.'
         - ''
         Usar lore preco: true
         Lore preco:
          - '&fPreco: 10K'
         Encantamentos:
          - 'DIG_SPEED:1'
         Usar comandos: false
         Comandos:
         - ''
      Diamante:
         Slot: 11
         Preco: 5000.0
         CustomSkull: false
         URL: ''
         Name: '&bDiamantes'
         ID: 56
         Data: 0
         Quantia: 64
         Usar lore: true
         Lore:
         - ''
         - '&cCompre para se tornar rico.'
         - ''
         Usar lore preco: true
         Lore preco:
          - '&fPreco: 5K'
         Encantamentos:
          - ''
         Usar comandos: true
         Comandos:
         - 'give {player} diamond 64'
]]>
</code-block>
</chapter>

<chapter title="mobs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Mobs:
   Mob1:
      Entidade: 'ZOMBIE'
      Quantia: 20.0
      Chance: 60.0
      Boss:
         Chance: 100.0
         Quantia: 1
      Mundos:
      - 'world'
   Mob2:
      Entidade: 'CREEPER'
      Quantia: 20.0
      Chance: 10.0
      Boss:
         Chance: 10.0
         Quantia: 2
      Mundos:
      - 'world'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   Reco1:
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
      Chance: 100.0
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'

]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static AlmasAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;AlmasAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(AlmasAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/30-yAlmas">Site do plugin yAlmas</a>
    </category>
</seealso>