# Como usar o yPlugins

### Primeiros passos para utilizar o yPlugins
<procedure title="Passos para utilizar o yPlugins">
   <p>Confira os primeiros passos para utlizar o yPlugins</p>
   <step>Ir para a Área do Cliente > Plugins e baixar o yPlugins</step>
   <step>Após isso, mova o yPlugins para a pasta Plugins do seu servidor;</step>
    <code-block lang="Plain Text">
    [14:02:50] [Server thread/INFO]: [yPlugins] Loading server plugin yPlugins v2.5.0
    [14:02:52] [Server thread/WARN]: [yPlugins] Falha na autenticação (not_found: 0.0.0.0:25565), desligando servidor...`
    </code-block>  
    <step>Ao ligar o servidor, aparecerá uma mensagem parecida com essa, onde o IP apresentado deve ser colocado no site da yStore (Área do Cliente > Servidor e copie o IP apresentado) em seguida, clique em Plugins e selecione os plugins que vão funcionar no IP cadastrado e clique em Atualizar.</step>
    <p>Parabéns, o seu servidor está liberado para usar o yPlugins.</p>
</procedure>

### Primeiros passos para utilizar as APIs do yPlugins
<procedure title="Passos para utilizar as APIs do yPlugins">
   <p>Confira os primeiros passos para utlizar as APIs do yPlugins</p>
   <step>Baixar o yPlugins</step>
   <step>Adicione ele no seu projeto</step>
   <step>Após fazer isso, você terá como gerir os plugins que você possui com a API podendo fazer modificações mais específicas.</step>
   <step>Exemplo de uso (com o yClans, porém cada plugin possui a sua APIHolder)</step>
   <code-block lang="java" ignore-vars="true">
public static ClanAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;ClanAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(ClanAPIHolder.class);
        return rsp == null ? null : rsp.getProvider();
    } catch (Throwable var1) {
        return null;
    }
}
</code-block>
    <p>Parabéns, o seu projeto agora consegue utilizar as APIs da yStore.</p>
</procedure>

<seealso style="cards">
    <category ref="wrs">
        <a href="rankup.md"/>
        <a href="factions.md"/>
        <a href="management.md"/>
        <a href="utility.md"/>
        <a href="addons.md"/>
        <a href="discord.md"/>
    </category>
</seealso>