# yAlmas
<secondary-label ref="rankup"/>

### Descrição
Mobs e jogadores no teu servidor possam dropar suas almas ao morrer e, com a possibilidade de ele renascer em forma de um boss Morto Vivo

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
<video src="//www.youtube.com/watch?v=-nZtSwrlKW0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/almas - Abre o menu principal
/almas  - Vê a quantia de almas de um jogador
/almas pagar - Envia almas para um jogador usando teu saldo de almas
/almas setar - Seta uma quantia de almas para um jogador
/almas remover - Remove uma quantia de almas de um jogador
/almas add - Dá uma quantia de almas para um jogador
/almas givebooster - Dá boosters para um jogador
/almas givelivro - Dá o livro do ceifador para um jogador
/almas giveboss - Dá o boss para um jogador
/almas setnpc - Seta o NPC de almas
/almas delnpc - Deleta o NPC de almas
/almas reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yalmas.usar - Permissão para o /almas
yalmas.olhar - Permissão para o /almas
yalmas.pagar - Permissão para o /almas pagar
yalmas.setar - Permissão para o /almas setar
yalmas.remover - Permissão para o /almas remover
yalmas.add - Permissão para o /almas add
yalmas.givebooster - Permissão para o /almas givebooster
yalmas.givelivro - Permissão para o /almas givelivro
yalmas.giveboss - Permissão para o /almas giveboss
yalmas.setnpc - Permissão para o /almas setnpc
yalmas.delnpc - Permissão para o /almas delnpc
yalmas.reload - Permissão para o /almas reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yalmas_almas% - Retorna a quantia de almas.
%yalmas_formatado% - Retorna a quantia de almas formatado (K, M, B, T...)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static AlmasAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;AlmasAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(AlmasAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/30-yAlmas">Site do plugin yAlmas</a>
    </category>
</seealso>