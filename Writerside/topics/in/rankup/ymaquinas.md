# yMaquinas
<secondary-label ref="rankup"/>

### Descrição
Blocos que geram drops ao consumir combustível

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
<video src="//www.youtube.com/watch?v=vTKsVokRwi4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/maquinas - Abre a loja de máquinas
/maquinas top - Abre o menu de top
/maquinas help - Envia a mensagem de ajuda
/maquinas booster - Vê o tempo restante do booster
/maquinas lista - Mostra a lista de máquinas disponíveis
/maquinas give - Dá máquinas para um jogador
/maquinas givebooster - Dá boosters para um jogador
/maquinas reload - Recarrega as configurações
/combustiveis - Abre a loja de combustíveis
/combustiveis help - Envia a mensagem de ajuda
/combustiveis lista - Mostra a lista de combustíveis disponíveis
/combustiveis give - Dá combustíveis para um jogador
/limite - Mostra o seu limite
/limite [player] - Mostra o limite de outro jogador
/limite help - Envia a mensagem de ajuda
/limite top - Abre o menu do top limite
/limite enviar - Envia limite para outro jogador
/limite give - Dá limite em item para um jogador
/limite remove - Remove limite de um jogador
/limite add - Adiciona limite para um jogador
/limite set - Seta o limite de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymaquinas.admin - Permissão para ser reconhecido como admin
ymaquinas.maquina.usar - Permissão para o /maquina e /maquina top
ymaquinas.maquina.booster - Permissão para o /maquina booster
ymaquinas.multiplicador.[quantia] - Permissão para ter uma x quantia de multiplicador
ymaquinas.maquina.give - Permissão para o /maquina give
ymaquinas.maquina.givebooster - Permissão para o /maquina givebooster
ymaquinas.maquina.lista - Permissão para o /maquina lista
ymaquinas.maquina.reload - Permissão para o /maquina reload
ymaquinas.combustivel.usar - Permissão para o /combustivel
ymaquinas.combustivel.give - Permissão para o /combustivel give
ymaquinas.combustivel.lista - Permissão para o /combustivel lista
ymaquinas.limite.usar - Permissão para o /limite
ymaquinas.limite.outros - Permissão para o /limite [player]
ymaquinas.limite.enviar - Permissão para o /limite enviar
ymaquinas.limite.set - Permissão para o /limite set
ymaquinas.limite.add - Permissão para o /limite add
ymaquinas.limite.remove - Permissão para o /limite remove
ymaquinas.limite.give - Permissão para o /limite give
ymaquinas.limite.remove - Permissão para o /limite remove
ymaquinas.place.bypass - Permissão para colocar todas as máquinas</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ymaquinas_limite% - Retorna o limite do jogador formatado (1K, 1M, 1T...)
%ymaquinas_limite_raw% - Retorna o limite do jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static MaquinaAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;MaquinaAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(MaquinaAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/86-yMaquinas">Site do plugin yMaquinas</a>
    </category>
</seealso>