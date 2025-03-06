# ySorteio
<secondary-label ref="utility"/>

### Descrição
Configure sorteios com blacklist, para aquele vip chato não poder participar.

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
<video src="//www.youtube.com/watch?v=sYiUV0cyfIU"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/sorteio - Veja todos os comandos disponíveis.
/sorteio help - Ver todos os comandos do plugin.
/sorteio lista - Ver a lista de sorteios.
/sorteio iniciar - Iniciar um sorteio.
/sorteio parar - Parar um sorteio.
/sorteio reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ysorteio.admin - Permissão para todos os comandos.</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── ySorteio/
    ├── config.yml
    ├── recompensas.yml
    └── sorteios.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Sorteio:
    Comando: 'sorteio'
    Aliases: [ sortear, giveaway ]
# Opções gerais do plugin
Opcoes:
  # Quantia de vezes que irá mandar a mensagem "Sorteando"
  # Deixe 0 para ser a quantia de jogadores no servidor
  Vezes: 5
# Autostart de sorteios
Autostart:
  vip:
    # nome do sorteio
    # deixe 'random' para ser um aleatório
    Sorteio: 'random'
    # todos, segunda, terca, quarta, quinta, sexta, sabado, domingo
    # dia-hora-minuto-segundo
    Horario: 'todos-00:00:01'
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isso.'
  Quantia: '&cNão foi possível realizar o sorteio por falta de jogadores.'
  Parou: '&cO sorteio foi cancelado por um administrador.'
  Ocorrendo: '&cJá existe um sorteio ocorrendo.'
  NaoOcorrendo: '&cNão existe um sorteio ocorrendo.'
  Iniciado: '&aSorteio iniciado com sucesso.'
  Parado: '&aSorteio parado com sucesso.'
  Help: |
     &bLista de &6comandos:
     &f> &3/sorteio help &8- &7Aparece esta mensagem.
     &f> &3/sorteio lista &8- &7Ver os tipos de sorteios disponíveis.
     &f> &3/sorteio iniciar <nome> &8- &7Iniciar um sorteio.
     &f> &3/sorteio parar &8- &7Iniciar um sorteio.
  Existe: |
    &cEste sorteio não existe.
    &cDisponíveis: &7{lista}&c.
  Lista: |
    &bDisponíveis: &7{lista}&c.
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
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

<chapter title="sorteios.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Sorteios:
  VIP:
    # Permissão que caso o jogador a tenha, não irá participar do sorteio
    # ou seja: PERMISSÃO DE BLACKLIST
    # deixe '' (vazio) para não usar
    Permissao: 'ysorteio.vip.naoparticipar'
    # Participar do sorteio apenas se estiver vinculado (yDiscordHook)
    Vinculado: false
    # Mensagens do sorteio
    Mensagens:
      Iniciou:
        Title: '&bIniciando sorteio...'
        Actionbar: '&bIniciando sorteio...'
        Chat: []
      Sorteando:
        Title: '&6Sorteando...<nl>&e{player}'
        Actionbar: '&7Sorteando vencedor...'
        Chat: []
      Ganhou global:
        Title: '&6Vencedor sorteado!<nl>&e{player}'
        Actionbar: '&6Vencedor do sorteio: &8{player}&6.'
        Chat:
          - ''
          - '&6&lSORTEIO: &fO jogador &e{player}&f ganhou o sorteio do &eVIP&f!'
          - ''
      Ganhou player:
        Title: '&6Vencedor sorteado!<nl>&e{player}'
        Actionbar: '&6Vencedor do sorteio: &8{player}&6.'
        Chat:
          - ''
          - '&6&lSORTEIO: &fVocê ganhou o sorteio do &eVIP&f!'
          - ''
    # chance,recompensa
    Recompensas:
      - '100,Reco1'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/11-ySorteio">Site do plugin ySorteio</a>
    </category>
</seealso>