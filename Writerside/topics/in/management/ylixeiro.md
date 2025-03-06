# yLixeiro
<secondary-label ref="management"/>

### Descrição
Plugin de lixeiro um pouco diferente.

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
<video src="//www.youtube.com/watch?v=fyYF8cAx2b8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/lixeiro - Ver informações da coleta anterior.
/lixeiro forcar&nbsp;- Força a coleta de entidades e itens.
/lixeiro historico&nbsp;- Abre o menu de histórico de itens limpos (3)
/lixeiro reload&nbsp;- Recarrega as configurações
/lixeira - Abre uma lixeira virtual.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ylixeiro.use - Permissão para o /lixeiro
ylixeiro.historic - Permissão para o /lixeiro historico
ylixeiro.force - Permissão para o /lixeiro forcar
ylixeiro.admin.reload - Permissão para o /lixeiro reload
ylixeiro.trash - Permissão para o /lixeira</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLixeiro/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Lixeiro:
    Comando: 'lixeiro'
    Aliases: []
  Lixeira:
    Comando: 'lixeira'
    Aliases: [ trashcan, lixo ]

# Tempo para realizar a limpeza
# em segundos
Tempo: 130

# Limpar os itens
Itens: true

# Limpar as entidades
Entidades: true

# Limpar os mobs do ySpawners
YSpawners: false

# Som que será enviado ao executar o /lixeiro
Lixeiro som: 'NOTE_PLING'

# Volume e pitch dos sons
Sound-volume: 20
Sound-pitch: 20

# Blacklist de items para não serem removidos
# ID:DATA
Items blacklist:
  - 'nenhum'

# Blacklist de entidades para não serem removidas
Entidades blacklist:
  - 'ZOMBIE'
# Mundos que não serão limpos

World blacklist:
  - 'nenhum'

# Entidades que mesmo renomeadas serão limpas
# colocar a METADATA
Metadata whitelist:
  - 'ySpawners-MobStacked'
  - 'ySpawnersV2-MobStacked'

# Mensagens gerais
Mensagens:
  Permissao: '&cVocê não tem permissão para fazer isto.'
  Limpou: '&aVocê limpou todos os itens do chão.'
  Proxima:
    - ' &eTempo para a próxima limpeza: {tempo}.'
    - ' &8♻ &fNa última limpeza foram limpos &7{total}&f itens.'

# Mensagem que irá ser enviada no chat
# Formato: tempo,<mensagem>
# Utilize <nl> para uma nova linha
Chat:
  - '120, &eTodos os itens no chão serão removidos em 2 minutos!<nl> &8♻ &fPara visualizar o tempo, digite &7/lixeiro&f.'
  - '60, &eTodos os itens no chão serão removidos em 1 minuto!<nl> &8♻ &fPara visualizar o tempo, digite &7/lixeiro&f.'
  - '10, &eTodos os itens no chão serão removidos em 10 segundos!'
  - '5, &eTodos os itens no chão serão removidos em 5 segundos!'
  - '4, &eTodos os itens no chão serão removidos em 4 segundos!'
  - '3, &eTodos os itens no chão serão removidos em 3 segundos!'
  - '2, &eTodos os itens no chão serão removidos em 2 segundos!'
  - '1, &eTodos os itens no chão serão removidos em 1 segundo!'
  - '0, &eForam removidos &e&l{total}&e itens do chão!' # a placeholder {total} retorna itens e entidades.

# Mensagem que irá ser enviada no actionbar
# Formato: tempo,<mensagem>
Actionbar:
  - '120, &eTodos os itens no chão serão removidos em 2 minutos!'
  - '60, &eTodos os itens no chão serão removidos em 1 minuto!'
  - '30, &eTodos os itens no chão serão removidos em 30 segundos!'
  - '10, &eTodos os itens no chão serão removidos em 10 segundos!'
  - '5, &eTodos os itens no chão serão removidos em 5 segundos!'
  - '4, &eTodos os itens no chão serão removidos em 4 segundos!'
  - '3, &eTodos os itens no chão serão removidos em 3 segundos!'
  - '2, &eTodos os itens no chão serão removidos em 2 segundos!'
  - '1, &eTodos os itens no chão serão removidos em 1 segundo!'
  - '0, &eForam removidos &e&l{total}&e itens do chão!' # a placeholder {total} retorna itens e entidades.

# Titles que serão enviados a cada x segundos
Title:
  - '30,&eLixeiro<nl>&7Limpando em 30 segundos.'
  - '10,&eLixeiro<nl>&7Limpando em 10 segundos.'
  - '0,&eLixeiro<nl>&7{total} itens limpos.'

# Sons que serão enviados a cada x segundos.
Sons:
  - '120,NOTE_STICKS'
  - '60,NOTE_STICKS'
  - '30,NOTE_STICKS'
  - '10,NOTE_STICKS'
  - '5,NOTE_STICKS'
  - '4,NOTE_STICKS'
  - '3,NOTE_STICKS'
  - '2,NOTE_STICKS'
  - '1,NOTE_STICKS'
  - '0,NOTE_PLING'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/45-yLixeiro">Site do plugin yLixeiro</a>
    </category>
</seealso>