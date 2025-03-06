# yAntiGrief
<secondary-label ref="management"/>

### Descrição
Autenticação para uso de comandos

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
<video src="//www.youtube.com/watch?v=BhsVJ4UCrFI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/antigrief reload - Recarrega as configurações
/antigrief [senha] - Realiza o login</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yantigrief.staff - Permissão para ser reconhecido como staff</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yAntiGrief/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Antigrief:
    Comando: 'antigrief'
    Aliases: []
  Build:
    Comando: 'build'
    Aliases: []

# Opções gerais do plugin
Opcoes:
  Senha: 'yantigrief'
  # Quantia máxima de tentativas de login
  Tentativas: 3
  # Comandos a serem executados quando exceder as tentativas
  Comandos:
    - 'kick {player} você errou o login do AntiGrief.'
  # Comandos que serão bloqueados
  Comandos bloqueados:
    - '//'
    - '/worldedit:'
    - '/build'
  # Itens que o jogador não poderá interagir com ele na mão sem logar
  # https://helpch.at/docs/1.8.8/org/bukkit/Material.html
  Interagir bloqueados:
    - 'FLINT_AND_STEEL'
    - 'LAVA_BUCKET'
    - 'LAVA'
    - 'WATER'
    - 'WATER_BUCKET'
    - 'FIREBALL'
    - 'ARMOR_STAND'
    - 'ITEM_FRAME'
  # Mundos em que o plugin não irá funcionar
  World blacklist: []

# Configuração das logs
Logs:
  Ativar: true
  # Formato da log
  Formato: '[ [{data}] - ({hora}) ] {action}'
  # Tipos de ações
  Tipos:
    Errou: '{player} errou a senha, tentativa: {tentativa}.'
    Excedeu: '{player} foi kickado por errar 3x o login do antigrief.'
    Logou: '{player} logou ao antigrief.'
    Comando: '{player} executou o comando {comando}.'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isso.'
  Bloqueado: '&cEste comando foi bloqueado pelo AntiGrief.'
  Logar: '&cPara usar este comando, você deve logar-se ao antigrief. /antigrief <senha>'
  Logou: '&aVocê logou com sucesso, já pode executar normalmente os comandos bloqueados.'
  Build: '&cVocê deve desativar a restrição: /build.'
  Build ativado: '&aVocê agora pode quebrar livremente.'
  Build desativado: '&cVocê agora não pode mais quebrar blocos.'
  Logado: '&cVocê já está logado.'
  Tentativa: '&cVocê errou a senha, tentativas restantes: {tentativas}.'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static AntiGriefAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;AntiGriefAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(AntiGriefAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/77-yAntiGrief">Site do plugin yAntiGrief</a>
    </category>
</seealso>