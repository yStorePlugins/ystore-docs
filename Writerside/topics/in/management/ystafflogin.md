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