# yStaffLogin
<secondary-label ref="management"/>

### Descrição
Mantenha seu servidor mais seguro, permitindo que cada staff cadastre uma senha, para um segundo login.

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
<video src="//www.youtube.com/watch?v=Lw9ravPwFGc"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/sl - Autenticar a sessão
/sl reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ystafflogin.staff - Permissão para ser reconhecido como staff
ystafflogin.reload - Permissão para o /sl reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yStaffLogin/
    ├── config.yml
    ├── discord.yml
    ├── log.yml
    └── webhooks.yml
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

# Comandos e aliases do plugin
Comando:
  Stafflogin:
    Comando: 'sl'
    Aliases: [ stafflogin, ls, loginstaff ]

# Será solicitado o loginstaff após logar
# Só é compatível com o nLogin
Depois de logar: true

# Salvar IP ao logar staff e não pedir mais o código pro user+IP
Salvar ip: false

# Forçar gamemode survival?
Forcar gamemode: true

# Quantia de caracteres do código de verificação
Quantia caracteres: 6

# Limpar chat ao entrar no servidor e quando realizar o login staff
Limpar chat: true

# Remover os itens ao logar
Remover itens: true

# Estes são os nomes dos menus caso seu servidor tenha captcha próprio
Menus liberados:
  - '&7Captcha'

# Enviar o embed no privado (somente para quem tem yDiscordHook)
DiscordHook:
  # Ativar o sistema
  Ativar: true
  # Embed configurada no yDiscordHook
  Embed: 'ystafflogin_verificacao'

# Mensagens que irão ser enviadas no chat do servidor, ao entrar e sair
Chatmsg:
 # Deixe vazia para não usar
 Logou: '&7[&a+&7] &a{player}'
 # Deixe vazia para não usar
 Saiu: '&7[&c-&7] &c{player}'

# Lista de comandos liberados no loginstaff (deixe os do próprio plugin também)
Comandos liberados:
- '/login'
- '/sl'
- '/stafflogin'
- '/logar'
- '/registro'
- '/registrar'
- '/register'
- '/autenticar'

Mensagens:
 Use login:
 - '&7O código foi enviado no discord.'
 - '&eUse: /sl <codigo>'
 - ''
 Use: '&cUse: /sl <codigo>'
 Permissao: '&cVocê não tem permissão para isto.'
 Ja logado: '&cVocê já está logado.'
 Logou: '&aVocê logou com sucesso!'
 Errou: '&c&lyStore<nl><nl>     &cVocê errou o login staff.<nl>&cRelogue para tentar novamente.'
 Relogue: '&c&lyStore<nl><nl>     &cO servidor foi recarregado.<nl>&cRelogue para autenticar-se novamente.'

# Enviado quando logar.
Title: '&aSucesso<nl>&eVocê realizou seu login Staff.'
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Options:
  Username: 'yStaffLogin'
  Ativar: false
Embeds:
  verificacao:
    Title: 'Realize seu LoginStaff'
    Thumbnail: ''
    Color: '255;255;255'
    Content: ''
    Footer:
      Text: 'Todos os direitos reservados'
      Image: ''
    Fields:
      usuario:
        Inline: false
        Header: 'Usuário'
        Content: '{player}'
      codigo:
        Inline: false
        Header: 'Código'
        Content: '{codigo}'
      ip:
        Inline: false
        Header: 'IP'
        Content: '{ip}'
      data:
        Inline: false
        Header: 'Data'
        Content: '{data} - {hora}'
]]>
</code-block>
</chapter>

<chapter title="log.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de logs
Ativar: false
# Webhook que irá enviar as logs
Webhook: 'https://discord.com/api/webhooks/746113536740032523/HgpcMhC58oPf3KERKI9zY24OAVXEyEWRh-J1ZGOejyvYXeTvU7KNYqXlEbKqn_hKNV35'
# Formato da log
Formato: '[ [{data}] - ({hora}) ] {action}'
# Usuário da webhook
Username: 'Auditoria'
# Tipos de log
Tipos:
  Entrou: '{player} realizou o login-staff no servidor RankUP'
  Saiu: '{player} saiu do servidor RankUP'
  Errou: '{player} errou o login-staff!'
LogEmbed:
  Color: '255;255;255'
  Footer: 'Todos os direitos reservados'
]]>
</code-block>
</chapter>

<chapter title="webhooks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Webhook para cada grupo
# Será enviada para o canal definido
Webhooks:
  staff:
    Permissao: 'ystafflogin.staff'
    URL: 'https://discord.com/api/webhooks/818193190913572884/Umi4lmG2TnEva3GDWoB6NnAi_oUo3UhLU89q8I1Pj7CbskzHHRoFyMfUk3ICHkrAQ1eW'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static StaffLoginAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;StaffLoginAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(StaffLoginAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/3-yStaffLogin">Site do plugin yStaffLogin</a>
    </category>
</seealso>