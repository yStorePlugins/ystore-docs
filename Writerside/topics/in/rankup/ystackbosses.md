# yStackBosses
<secondary-label ref="rankup"/>

### Descrição
Agrupe bosses no melhor sistema da atualidade

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
<video src="//www.youtube.com/watch?v=dSRzcTK8J-M"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/boss - Abre o menu principal
/boss shop - Abre o menu do shop
/boss armazem - Abre o menu do armazem
/boss top - Abre o menu do top
/boss amuletos - Abre o menu dos amuletos
/boss bosses - Abre o menu dos bosses do servidor
/boss giveboss - Dar bosses para um jogador
/boss givematadora - Dar matadoras para um jogador
/boss giveamuleto - Dar amuletos para um jogador
/boss givebookdamage - Dar livro de dano ao jogador
/boss givestackdamage - Dar livro de stack ao jogador
/boss reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ystackbosses.use - Permissão para o /boss, /boss armazem, /boss top, /boss amuletos, /boss bosses
ystackbosses.shop - Permissão para o /boss shop
ystackbosses.giveboss - Permissão para o /boss giveboss
ystackbosses.giveamulet - Permissão para o /boss giveamuleto
ystackbosses.givesword - Permissão para o /boss givematadora
ystackbosses.givedamagebook - Permissão para o /boss givebookdamage
ystackbosses.givestackbook - Permissão para o /boss givestackdamage</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ystackbosses_killed% - Retorna a quantia de bosses mortos do jogador formatado (1K, 1M, 1T...)
%ystackbosses_killed_raw% - Retorna&nbsp;a quantia de bosses mortos&nbsp;do&nbsp;jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static StackBossAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;StackBossAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(StackBossAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/106-yStackBosses">Site do plugin yStackBosses</a>
    </category>
</seealso>