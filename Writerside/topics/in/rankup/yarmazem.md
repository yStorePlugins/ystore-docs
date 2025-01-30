# yArmazem
<secondary-label ref="rankup"/>

### Descrição
Armazene plantações por plots!

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
<video src="//www.youtube.com/watch?v=K6kI8VV4F-g"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/armazem - Abrir o menu do armazem
/armazem givelimitevenda - Dá limite de venda a um jogador.
/armazem givelimitearmazem - Dá limite de armazenamento a um jogador.
/armazem add - Adiciona limite de venda a um jogador.
/armazem remove - Remove limite de venda a um jogador.
/armazem set - Seta limite de venda a um jogador.
/armazem ajuda - Envia a mensagem de ajuda
/armazem reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yarmazem.usar - Permissão para o /armazem
yarmazem.vender - Permissão para vender itens.
yarmazem.coletar - Permissão para coletar itens.
yarmazem.vendertudo - Permissão para o vender tudo.
yarmazem.givelimite - Permissão para o /armazem givelimitevenda e /armazem givelimitearmazem
yarmazem.add - Permissão para o /armazem add
yarmazem.remove - Permissão para o /armazem remove
yarmazem.set - Permissão para o /armazem set
yarmazem.help - Permissão para o /armazem ajuda
yarmazem.reload - Permissão para o /armazem reload
yarmazem.autosell - Permissão para o auto - sell</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yarmazem_limite% - Retorna a quantia de limite do jogador com formatação (1K, 1M...)
%yarmazem_limite_raw% - Retorna a quantia de limite do jogador sem formatação.
%yarmazem_limite_armazem% - Retorna a quantia de limite do armazém atual com formatação (1K, 1M...)
%yarmazem_limite_armazem_raw% - Retorna a quantia de limite do armazém atual&nbsp;sem formatação.
%yarmazem_armazenado% - Retorna a quantia de plantações armazenadas no plot com formatação
%yarmazem_armazenado_raw% - Retorna a quantia de plantações armazenadas no plot sem formatação
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static ArmazemAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;ArmazemAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(ArmazemAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/8-yArmazem">Site do plugin yArmazem</a>
    </category>
</seealso>