# yBaus
<secondary-label ref="management"/>

### Descrição
Armazene itens virtualmente

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
<video src="//www.youtube.com/watch?v=A7cCeDaPFzo"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/bau - Abre o menu principal
/bau [numero]  - Abre um baú específico
/bau gerenciar [numero]  - Gerencia um baú específico
/bau ajuda - Vê todos os comandos
/bau   - Vê um baú específico do player (ADMIN)
/bau darbau   - Dá um baú extra para um jogador (ADMIN)
/bau setnpc - Seta o NPC do bau (ADMIN)
/bau delnpc - Deleta o NPC do bau (ADMIN)
/bau reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ybaus.usar - Permissão para o /bau, /bau gerenciar [numero]
ybaus.usar.numero - Permissão para o /bau [numero]
ybaus.ajuda - Permissão para o /bau ajuda
ybaus.outros - Permissão para o /bau [numero] [player]
ybaus.darbau - Permissão para o /bau darbau
ybaus.setnpc - Permissão para o /bau setnpc
ybaus.delnpc - Permissão para o /bau delnpc
ybaus.reload - Permissão para abrir o /bau reload
ybaus.enderchest - Permissão para abrir o enderchest
ybaus.quantia.[numero] - Permissão para limitar a quantia de baús que um jogador pode ter (respeitando o limite máximo da config.yml)
ybaus.default_quantia.[numero] - Permissão para dar baús por padrão ao logar</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ybaus_amount% - Retorna a quantidade de baús do jogador formatado (1K, 1M, 1T...)
%ybaus_amount_raw% - Retorna a quantidade de baús do jogador&nbsp;sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yBaus/
    ├── menus/
    │    ├── expandir.yml
    │    ├── gerenciar.yml
    │    ├── mudaricone.yml
    │    └── principal.yml
    ├── config.yml
    ├── custos.yml
    ├── data.yml
    └── descontos.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="expandir.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Expandir baú'
Tamanho: 27
Itens:
  Confirmar:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 5
    Glow: false
    Name: '&aConfirmar'
    Lore:
      - '&7Clique para confirmar e expandir.'
  Cancelar:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 14
    Glow: false
    Name: '&cCancelar'
    Lore:
      - '&7Clique para cancelar e retornar.'
  Expandir:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: 54
    Data: 0
    Glow: false
    Name: '&aExpansão'
    Lore:
      - ''
      - '&7Preços:'
      - '&f > &a{Money} coins.'
      - '&f > &6{PlayerPoints} pontos.'
      - ''
      - '&fSeu desconto: &a{desconto}%&f.'
]]>
</code-block>
</chapter>

<chapter title="gerenciar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Gerenciar baú'
Tamanho: 27
BackSlot: 18
Itens:
  Nome:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: 421
    Data: 0
    Glow: false
    Name: '&aNome do baú'
    Lore:
      - '&7Nome do baú que ficará'
      - '&7no /bau.'
      - ''
      - '&7 Atual: {bau}'
      - ''
      - '&7Clique para renomear.'
  Icone:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: 389
    Data: 0
    Glow: false
    Name: '&aÍcone do baú'
    Lore:
      - '&7Mude o ícone que ficará'
      - '&7no /bau.'
      - ''
      - '&7Clique para alterar o ícone.'
  Expandir:
    Slot: 15
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/3857d6b17901fd3f0109bd9bdcc28021b65947fce0a958327247d26d92915b85'
    ID: 0
    Data: 0
    Glow: false
    Name: '&aExpandir baú'
    Lore:
      - '&7Expanda a quantia de'
      - '&7linhas do baú.'
      - ''
      - '&7 Atual: &b{linhas}&7.'
      - ''
      - '&7Clique para expandir.'
]]>
</code-block>
</chapter>

<chapter title="mudaricone.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Baú - Mudar ícone'
Tamanho: 54
Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 37, 38, 39 ]
BackSlot: 45
VoltarSlot: 41
ProximoSlot: 43
# Item de colocar uma head
Head:
  Slot: 42
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/62d90ad63dd826df02994abdcc6c2306163e1072d1b9e63ad4e7d7d1cf87cdf9'
  ID: 0
  Data: 0
  Glow: false
  Name: '&eDefinir head'
  Lore:
    - '&7Clique para definir uma'
    - '&7cabeça customizada no baú.'
# Itens customizados
Itens: {}
#  Enfeite:
#    Slot: 1
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: false
#    Name: '&aEnfeite'
#    Lore: []
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Lista de baús'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 18
VoltarSlot: 27
ProximoSlot: 35
# Item do baú
Bau:
  Name: '&e{nome}'
  Lore:
    - ''
    - '&f > &bBaú #{id}&f.'
    - '&f > &7Slots: &c{slot_usado}&7/&a{slot_total}&f.'
    - ''
    - '&7Botão &fesquerdo&7 para abrir o baú.'
    - '&7Botão &fdireito&7 para gerenciar o baú.'
# Item para comprar novo baú
Comprar:
  Slot: 30
  CustomSkull: false
  URL: ''
  ID: 54
  Data: 0
  Glow: false
  Name: '&6Comprar baú'
  Lore:
    - '&7Clique para comprar'
    - '&7um novo baú.'
    - ''
    - '&7Preços:'
    - '&f > &a{Money} coins.'
    - '&f > &6{PlayerPoints} pontos.'
    - ''
    - '&fSeu desconto: &a{desconto}%&f.'
# Item para abrir o enderchest
Enderchest:
  Slot: 32
  CustomSkull: false
  URL: ''
  ID: 130
  Data: 0
  Glow: false
  Name: '&aBaú do fim'
  Lore:
    - '&7Clique para abrir seu'
    - '&7baú do fim.'
# Itens customizados
Itens: {}
#  Enfeite:
#    Slot: 1
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: false
#    Name: '&aEnfeite'
#    Lore: []
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
Comando:
  Baus:
    Comando: 'bau'
    Aliases: [ baus, chest, chests, baú, baús ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Opcoes de configuração do NPC
NPC:
  ID: 923288
  Skin: 'ySpeed_'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Baús'
      - '&7Clique para gerenciar seus baús.'

# Opções do plugin
Opcoes:
  # Máximo de baús que um jogador poderá ter
  # O plugin tem um limite para um maximo de 20 baús
  Maximo: 2
  # Quantia default de baús que o jogador vai ganhaar
  Default: 1
  # Quantia de linhas que um baú terá
  Rows default: 1
  # Ativar o uso de shift no baú
  Shift: false
  # Ativar o uso de teclas no baú
  Numkeys: false
  # Ativar o uso de criativo no baú
  Criativo: false
  # Habilitar o uso do /bau <numero>
  Command open: false
  # Abrir o menu principal ao fechar um baú
  Open-close: true
  Default-Item:
    Material: 'CHEST'
    Data: 0
    Name: 'Baú {id}'


# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Nao e numero: '&cO argumento não é um número.'
  Nao encontrado: '&cEste jogador não está online.'
  Possui: '&cVocê não possui este baú.'
  Jogador possui: '&cEste jogador não possui este baú.'
  Olhando: '&cO jogador {player} já está olhando este baú.'
  Mudou nome: '&aVocê alterou o nome do baú para &e{nome}&a.'
  Mudou icone: '&aVocê alterou o ícone do baú.'
  Grande: '&cO nome do baú não pode ser maior que 25 letras.'
  Comprou: '&aVocê adquiriu um novo baú.'
  Expandiu: '&aVocê expandiu seu baú.'
  Nao possui: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  Cadastrado: '&cEste plugin &f{plugin}&c não está implementado no plugin de baús.'
  Desabilitado: '&cEste plugin &f{plugin}&c não está ligado.'
  Maximo: '&cEste baú já está com o máximo de linhas.'
  Setado npc: '&aNPC do chain setado com sucesso.'
  Removido npc: '&aNPC do chain removido com sucesso'
  Nao setado npc: '&cO NPC não está setado.'
  Ativar: '&cVocê não pode ativar um baú extra pois já está no limite de baús.'
  Ativou: '&aVocê ativou um baú extra!'
  # Deixe '' para não usar.
  Deu: '&aVocê deu &7x{quantia} &abaú(s) extra(s) para o jogador &7{player}&a.'
  # Deixe '' para não usar.
  Recebeu: '&aVocê recebeu &7x{quantia} &abaú(s) extra(s).'
  Expansao: '&cNão há nenhuma expansão configurada para um baú com este tamanho.'
  Shift: '&cVocê não pode usar shift no baú.'
  Numkeys: '&cVocê não pode usar as teclas numéricas no baú.'
  Criativo: '&cVocê não pode usar clicar no baú estando no criativo.'
  Digite nome:
    - ''
    - '&aDigite o nome para qual deseja alterar.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite skin:
    - ''
    - '&aDigite o nome da head que você deseja.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Ajuda:
    - '&b-> Comandos disponíveis <-'
    - ''
    - '&f > &7/bau'
    - '&f > &7/bau <numero>'
    - '&f > &7/bau <numero> <player>'
    - '&f > &7/bau ajuda'
    - '&f > &7/bau darbau <player> <quantia>'
    - '&f > &7/bau setnpc'
    - '&f > &7/bau delnpc'

# Item do baú extra
BauExtra:
  CustomSkull: false
  URL: ''
  ID: CHEST
  Data: 0
  Glow: true
  Name: '&6Baú Extra'
  Lore:
    - '&7Clique para ativar e'
    - '&7ganhar &6+1 baú&7.'

# Setas dos menus
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
      - '&7Clique para voltar à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróxima'
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

<chapter title="custos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Custos para comprar um novo baú
Comprar:
  # Porcentagem a + para comprar novos baús
  # será usada a partir da compra do 2º baú
  Porcentagem: 10.0
  Custos:
    Custo1:
      Display: 'Money'
      Tipo: 'Money' #tipos: Money, plugin de pontos
      Custo: 1000.0
    Custo2:
      Display: 'Pontos'
      Tipo: 'PlayerPoints'
      Custo: 10.0
# Custos para expandir um baú
Expandir:
  # Neste exemplo padrão, o baú que tiver 1 linha irá evoluir 1 linha
  Linha2:
    # Número de linhas necessárias para essa evolução
    LinhasPrecisa: 1
    # Número de linhas que dará ao evoluir
    Evolucao: 1
    Custos:
      Custo1:
        Display: 'Money'
        Tipo: 'Money' #tipos: Money, plugin de pontos
        Custo: 2000.0
      Custo2:
        Display: 'Pontos'
        Tipo: 'PlayerPoints'
        Custo: 20.0
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Npc local: 'none'
Data: {}
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Ordem: 1
      Permissao: 'ybaus.vip'
      Desconto: 10.0
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/76-yBaus">Site do plugin yBaus</a>
    </category>
</seealso>