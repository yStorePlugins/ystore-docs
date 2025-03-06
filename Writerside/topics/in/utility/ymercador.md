# yMercador
<secondary-label ref="utility"/>

### Descrição
Venda itens de tempos em tempos com estoque limitado

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
<video src="//www.youtube.com/watch?v=GyAtQuxEAhs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mercador setmercador [mercador] - Seta o NPC do mercador especificado
/mercador delmercador [mercador] - Deleta o NPC do mercador especificado
/mercador forcar [mercador] [duracao] - Força a vinda do mercador
/mercador forcarsaida [mercador] - Força a saída do mercador
/mercador reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymercador.setmercador - Permissão para o /mercador setmercador
ymercador.delmercador - Permissão para o /mercador delmercador
ymercador.forcar - Permissão para o /mercador forcar
ymercador.forcarsaida - Permissão para o /mercador forcarsaida
ymercador.reload - Permissão para o /mercador reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMercador/
    ├── menus/
    │    └── confirmacao.yml
    ├── mercadores/
    │    └── padrao.yml
    ├── config.yml
    └── descontos.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmacao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de compra'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: WOOL
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser comprada: &a{quantia}&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a compra.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: WOOL
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a compra.'

]]>
</code-block>
</chapter>

</chapter>

<chapter title="mercadores" collapsible="true">
<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comando para abrir o menu
Comando: 'pirata'

# Permissao para abrir
Permissao: ''

# Quantidade de itens que o mercador irá trazer
item-amount: 1

# Horários que o mercador irá trazer mercadorias
Horarios:
  # todos, segunda, terca, quarta, quinta, sexta, sabado, domingo
  # dia-hora-minuto-segundo;duração
  # duração = Duração do mercador (quanto tempo ele vai ficar disponível até o novo horário; em segundos)
  - 'todos-00:00:00,60'
  - 'todos-02:00:00,60'
  - 'todos-04:00:00,60'
  - 'todos-06:00:00,60'
  - 'todos-08:00:00,60'
  - 'todos-10:00:00,60'
  - 'todos-12:00:00,60'
  - 'todos-14:00:00,60'
  - 'todos-16:00:00,60'
  - 'todos-18:00:00,60'
  - 'todos-20:00:00,60'
  - 'todos-22:00:00,60'

# Opções de configuração do inventário
Inventario:
  Nome: '&6Mercador Pirata'
  Tamanho: 54
  Paginado:
    Ativar: true
    Slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
  Enfeites:
    exemplo:
      Slot: 0
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: STONE
      Data: 0
      Glow: false
      Name: '&7Exemplo de enfeite'
      Lore: []

# Opcoes de configuração do NPC
NPCS:
  ID: 2425235
  Indisponivel:
    Ativar: true
    Skin: 'NoLongerAPirate'
    Holograma:
      Altura: 3.1
      Holograma:
        - '&6&lMERCADOR'
        - '&7Estou em viagem no momento!'
        - '&7Volte mais tarde.'
  Disponivel:
    Skin: 'NoLongerAPirate'
    Holograma:
      Altura: 3.1
      Holograma:
        - '&6&lMERCADOR'
        - '&aVim com várias mercadorias para você!'

# Mensagens
Mensagens:
  NaoChegou: |
    §l§f §a
    &cOps! Parece que o pirata ainda não chegou com novos itens.
    &cQuando ele chegar, um anúncio será enviado a todos, fique esperto.
    §l§f §a
  Chegou: |
    §l§f §a
    &6&lMERCADOR PIRATA
    &fO mercador chegou!
    &fVeja suas mercadorias no &6/pirata&f agora mesmo.
    §l§f §a
  Foi: |
    §l§f §a
    &6&lMERCADOR PIRATA
    &fO mercador se foi!
    §l§f §a
  ChegouTitle: ''
  FoiTitle: ''
  ChegouActionbar: '&6O MERCADOR PIRATA chegou!'
  FoiActionbar: '&6O MERCADOR PIRATA se foi!'
  Setou: '&aVocê setou o NPC do mercador padrão.'
  Deletou: '&aVocê deletou o NPC do mercador padrão.'
  NaoSetado: '&cO NPC do mercador padrão não está setado.'

# itens que o mercador irá trazer
Itens:
  item1:
    Display:
      Slot: 10 # apenas se a opção de paginação estiver desabilitada
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: SOUL_SAND
      Data: 0
      Glow: false
      Name: '&5Farinha de Almas'
      Lore:
        - '&fCusto: &a{Money} coins&f.'
        - '&fSeu desconto: &7{desconto}%&f.'
        - ''
        - '&fEstoque atual: &b{estoque}&f.'
    Comprar:
      # Deixe Comandos: [] para não usar
      Comandos: []
      # Ao ativar, cada comando será 1 slot
      # Ele poderá comprar só a quantia de slots disponíveis.
      Contabilizar comandos: true
      # Se essa opção estiver true, ele irá executar o comando pela quantidade que o player escolheu na hora na compra, se estiver false, irá adicionar a placeholder {quantia} no comando.
      Repetir comandos: false
      # Usar o menu de confirmação
      Confirmacao: false
      # Habilitar a compra com botão esquerdo
      CompraEsquerdo: true
      # Habilitar a compra com botão direito
      CompraDireito: true
      # Mensagem de compra
      Msg: |
        §l§f §a
        &6&lMERCADOR PIRATA
        &fVocê comprou &6x{quantia} &5Farinha de Almas &fpelo preço de &a{Money} coins&f.
        §l§f §a
      Digite: |
        §l§f §a
        &6&lMERCADOR PIRATA
        &fDigite a quantia que deseja comprar de &5Farinha de Almas&f.
        §l§f §a
        &fCusto: &a{Money} coins&f.
        &fSeu desconto: &b{desconto}%&f.
        §l§f §a
        &fPara cancelar digite &ncancelar&f.
        §l§f §a
      # Apague para não usar
      Item:
        CustomSkull: false
        URL: ''
        ID: SOUL_SAND
        Data: 0
        Amount: 64
        Name: '&5Farinha de Almas'
        Glow: false
        Lore: []
        Enchants:
          - '' #deixe vazio para não usar
      # chance do mercador trazer este item
      Chance: 100.0
      # Opções do estoque
      Estoque:
        Min: 1
        Max: 10
      # Custos de compra
      Custos:
        Custo1:
          Display: 'Money'
          Tipo: 'Money' #tipos: Money, plugin de pontos
          Custo: 1000.0

#
Tempo restante: 0 # NÃO MEXER AQUI
Local: 'none' # NÃO MEXER AQUI
EstoqueAtual: [] # NÃO MEXER AQUI
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Mercador:
    Comando: 'mercador'
    Aliases: [ mercadores ]
# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'
# Opções gerais do plugin
Opcoes:
  # Maximo de itens por compra
  Maximo por compra: 64
  # Formatador de mensagens
  Formatador:
    Desconto: ' &7( {desconto}% )'
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Lista: '&cMercadores disponíveis: &7{lista}&c.'
  Cancelou: '&cVocê cancelou a compra.'
  Nao e numero: '&cO argumento não é um número.'
  Maximo: '&cDesculpe, o valor máximo por compra é de {maximo}.'
  Inv cheio: '&cSeu inventário não tem espaço suficiente.'
  Nao possui: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  Cadastrado: '&cEste plugin &f{plugin}&c não está implementado no plugin de shop.'
  Desabilitado: '&cEste plugin &f{plugin}&c não está ligado.'
  Estoque: '&cEste item não possui esta quantia em estoque.'
  Forcou: '&aVocê forçou a vinda do mercador &7{mercador}.'
  ForcouSaida: '&aVocê forçou a saída do mercador &7{mercador}.'
  NaoChegou: '&cEste mercador ainda não chegou de viagem.'
  Ajuda: |
    &bComandos disponíveis:
    &b-> &3/mercador setmercador <mercador>
    &b-> &3/mercador delmercador <mercador>
    &b-> &3/mercador forcar <mercador> <duracao>
    &b-> &3/mercador forcarsaida <mercador>
    &b-> &3/mercador reload
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

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Ordem: 1
      Permissao: 'ymercador.vip'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/88-yMercador">Site do plugin yMercador</a>
    </category>
</seealso>