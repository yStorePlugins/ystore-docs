# yCheques
<secondary-label ref="rankup"/>

### Descrição
Crie cheques utilizando várias economias!

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
<video src="//www.youtube.com/watch?v=xXrVqR9EBDw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/cheque - Abre o menu principal
/cheque setnpc - Seta o NPC do cheque.
/cheque delnpc - Deleta o NPC do cheque.
/cheque criar - Cria um cheque sem gastar saldo.
/cheque reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycheques.usar - Permissão para o /cheque
ycheques.admin - Permissão para o /cheque setnpc e /cheque delnpc
ycheques.taxa.bypass - Permissão para não ter taxa de criação</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCheques/
    ├── menus/
    │    └── principal.yml
    ├── cheques.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Gerenciar cheques'
Tamanho: 27
Itens:
  Informacoes:
    Slot: 11
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSuas informações'
    Lore:
      - '&7Veja suas informações'
      - '&7referente aos cheques.'
      - ''
      - ' &fCheques criados: &a{criados}&f.'
      - ''
# Caso queira enfeitar seu menu, poderá criar itens nesta seção:
Itens custom: {}
  #Enfeite1:
  #  Slot: 0
  #  CustomSkull: false
  #  URL: ''
  #  ID: 1
  #  Data: 0
  #  Glow: true
  #  Name: ''
  #  Lore: []
# Tipos de cheques que irão aparecer no menu.
# Você poderá checar os tipos além do "Money" na página do plugin
# em nosso site.
Cheques:
  Cheque1:
    Tipo: 'Money'
    Slot: 13
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/8381c529d52e03cd74c3bf38bb6ba3fde1337ae9bf50332faa889e0a28e8081f'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aCheque de Money'
    Lore:
      - ''
      - ' &fLimite usado: &c{usado}&f/&a{limite}&f.'
      - ' &fVocê possui &7{quantia}&f disponível.'
      - ''
      - '&aClique para criar um cheque de money.'
  Cheque2:
    Tipo: 'yPoints'
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    ID: 0
    Data: 0
    Glow: true
    Name: '&6Cheque de Cash'
    Lore:
      - ''
      - ' &fLimite usado: &c{usado}&f/&a{limite}&f.'
      - ' &fVocê possui &7{quantia}&f disponível.'
      - ''
      - '&aClique para criar um cheque de cash.'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="cheques.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Cheques:
  Cheque1:
    Tipo: 'Money'
    material: 'http://textures.minecraft.net/texture/8381c529d52e03cd74c3bf38bb6ba3fde1337ae9bf50332faa889e0a28e8081f'
    name: '&aCheque de Money'
    lore:
      - ''
      - '&7Criado por: &a{player}&7.'
      - '&7Criado em: &f{data} &8- &f{hora}&7.'
      - ''
      - '&bValor do cheque: &a{quantia}&b.'
      - ''
      - '&aClique para ativar este cheque.'
    Mensagem:
      Title: '&a{quantia} coins<nl>&erecebidos!'
      Actionbar: '&aVocê ativou um cheque de &e{quantia}&a coins.'
      Chat: |
        &aVocê ativou um cheque de &e{quantia}&a coins.
      Chat-criou: |
        &aVocê criou um cheque de &e{quantia} coins&a com sucesso.
  Cheque2:
    Tipo: 'yPoints'
    material: 'http://textures.minecraft.net/texture/667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    name: '&6Cheque de Cash'
    lore:
      - ''
      - '&7Criado por: &a{player}&7.'
      - '&7Criado em: &f{data} &8- &f{hora}&7.'
      - ''
      - '&bValor do cheque: &a{quantia}&b.'
      - ''
      - '&aClique para ativar este cheque.'
    Mensagem:
      Title: '&a{quantia} cash<nl>&erecebidos!'
      Actionbar: '&aVocê ativou um cheque de &e{quantia}&a cash.'
      Chat: |
        &aVocê ativou um cheque de &e{quantia} cash&a.
      Chat-criou: |
        &aVocê criou um cheque de &e{quantia} cash&a com sucesso.
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
  Tabela: 'ycheques.players'
  Debug: true

# Comandos e aliases do plugin
Comando:
  Cheque:
    Comando: 'cheque'
    Aliases: [ cheques ]

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Opcoes de configuração do NPC
NPC:
  ID: 923283
  Skin: 'TheThunderGod063'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Cheques'
      - '&7Gerenciador de cheques.'

# Opções gerais do plugin
Opcoes:
  # Limite de criação de cada cheque
  # Deixe 0 para não ter limite
  Limite: 10
  # Tempo para resetar o limite
  # em segundos
  Resetar com: 60
  # Minimo para criar um cheque
  Minimo: 2000.0
  # Caso true, o comando /cheque criar será apenas executado pelo console
  Criar console: true
  # Quando ativo, o jogador poderá juntar todos os cheques do mesmo tipo em 1 só
  Juntar: true
  # Taxa para criar cheque (em %)
  # permissão de bypass: ycheques.taxa.bypass
  Taxa: 20
  # Ativar o sistema de UUID - ANTI-DUPE
  # **** Cuidado ao desativar
  UUID: true

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Cancelou: '&cVocê cancelou a operação.'
  Nao e numero: '&cO argumento não é um número.'
  Menor minimo: '&cEsta operação requer um mínimo de &7{quantia}&c.'
  Inv cheio: '&cSeu inventário está cheio.'
  Nao possui: '&cVocê não possui a quantia &7{quantia}&c.'
  Setado: '&aNPC do cheque setado com sucesso.'
  Removido: '&aNPC do cheque removido com sucesso'
  Nao setado: '&cO NPC não está setado.'
  Nao encontrado: '&cJogador não encontrado.'
  Cadastrado: '&cEste plugin &f{plugin}&c não está implementado no plugin de cheques.'
  Desabilitado: '&cEste plugin &f{plugin}&c não está ligado.'
  Configurado: '&cNão foi encontrado nenhum cheque configurado na cheques.yml para o plugin &f{plugin}&c.'
  Aguarde: '&cVocê atingiu seu limite diário deste cheque, aguarde &7{tempo}&c para realizar essa operação novamente.'
  Criou: '&aVocê criou um cheque de &7{quantia}&a com sucesso.'
  Converteu: '&aVocê juntou seus cheques com sucesso.'
  UUID: '&cEste cheque está duplicado e já utilizado.'
  Cheque:
    - ''
    - '&aDigite no chat a quantia que quer criar um cheque.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/53-yCheques">Site do plugin yCheques</a>
    </category>
</seealso>