# yLogger
<secondary-label ref="management"/>

### Descrição
Gerencie o que os seus jogadores fazem no servidor.

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


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/logger - Mostra o histórico de morte
/logger [player] - Mostra o histórico de morte de outro jogador
/logger reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ylogger.use - Permissão para o /logger
ylogger.other - Permissão para o /logger [player]
ylogger.admin.reload - Permissão para o /logger reload
ylogger.register.chat - Permissão para ser registrado na log de chat
ylogger.register.break_block - Permissão para ser registrado na log de quebrar blocos
ylogger.register.place_block - Permissão para ser registrado na log de colocar blocos
ylogger.register.collect_item - Permissão para ser registrado na log de coletar itens
ylogger.register.drop_item - Permissão para ser registrado na log de dropar itens
ylogger.register.clone_item - Permissão para ser registrado na log de clonar itens
ylogger.register.command - Permissão para ser registrado na log de comandos
ylogger.register.death - Permissão para ser registrado na log de morte
ylogger.register.login - Permissão para ser registrado na log de login
ylogger.register.quit - Permissão para ser registrado na log de sair
ylogger.register.kill - Permissão para ser registrado na log de matar
ylogger.register.open_chest - Permissão para ser registrado na log de abrir baú
ylogger.register.* - Permissão para ser registrado em todas as logs</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLogger/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Log:
    Comando: 'log'
    Aliases: [ logs, logger ]
#Coloque Legendchat, OpeNChat (ou nChat), UltimateChat, NoxusChat ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'
# Esta opção quando ativa pode gerar lag.
# Caso esteja desativada, só irá registrar logs
# dos jogadores que tiverem a permissão: ylogger.register
Ativar todos: false
# Formato da log
Log: '[ [{data}] - ({hora}) ] {action}'
# Tipos de logs que estarão sendo registrados
Tipos:
  Chat: true
  Comando: true
  Abrir bau: true
  Dropar: true
  Colocar: true
  Quebrar: true
  Logar: true
  Quitar: true
  Clonar: true
  Matar: true
  Morrer: true
  Coletar: true
# Formatos dos tipos de logs
Formatos:
  Chat: "{player} digitou no chat '{chat}' a mensagem '{msg}' no mundo [{mundo}] nas coordenadas ({coords})"
  Comando: "{player} utilizou o comando '{comando}' no mundo [{mundo}] nas coordenadas ({coords})"
  Abrir bau: "{player} abriu um baú no mundo [{mundo}] nas coordenadas ({coords})"
  Dropar: "{player} dropou ({quantia}x) item(s) do tipo ({tipo}) no mundo [{mundo}] nas coordenadas ({coords})"
  Colocar: "{player} colocou um bloco do tipo ({tipo}) no mundo [{mundo}] nas coordenadas ({coords})"
  Quebrar: "{player} quebrou um bloco do tipo ({tipo}) no mundo [{mundo}] nas coordenadas ({coords})"
  Logar: "{player} logou no servidor."
  Quitar: "{player} saiu do servidor."
  Clonar: "{player} clonou ({quantia}x) item(s) do tipo ({tipo}) no mundo [{mundo}] nas coordenadas ({coords})"
  Matar: "{player} matou {tipo} nas coordenadas ({coords})"
  Morrer: "{player} morreu para {tipo} no mundo [{mundo}] nas coordenadas ({coords})"
  Coletar: "{player} coletou ({quantia}x) item(s) do tipo ({tipo}) no mundo [{mundo}] nas coordenadas ({coords})"
# Lista de comandos que não serão registrados
Comandos blacklist:
  - '/login'
  - '/register'
  - '/loginstaff'
  - '/stafflogin'
  - '/ls'
  - '/sl'
# Blocos que serão registrados no Colocar e Quebrar
# Lista de blocos: https://helpch.at/docs/1.8.8/org/bukkit/Material.html
# Coloque TODOS para listar todos.
Blocos:
  - 'TRAPPED_CHEST'
  - 'CHEST'
  - 'ENDER_CHEST'
  - 'MOB_SPAWNER'
  - 'ENDER_STONE'
  - 'OBSIDIAN'
  - 'BEACON'
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Possui: '&cEste jogador {player} não possui logs.'
  Erro: '&cOcorreu um erro ao tentar dar paste nas logs de {player}, erro: {erro}'
  Log: '&aLogs de {player} publicadas com sucesso! Url: {url}'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/71-yLogger">Site do plugin yLogger</a>
    </category>
</seealso>