# yMochilas
<secondary-label ref="utility"/>

### Descrição
Leve baús virtuais em seu próprio inventário

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
<video src="//www.youtube.com/watch?v=QcmUh0ygzkU"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mochila give&nbsp;- Dar uma mochila à um jogador
/mochila reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymochilas.give - Permissão para o /mochila give
ymochilas.reload - Permissão para o /mochila reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMochilas/
    ├── config.yml
    └── mochilas.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Mochila:
    Comando: 'mochila'
    Aliases: [ backpack, mochilas, backpacks ]
# Opções gerais do plugin
Opcoes:
  # Permitir colocar mochila dentro de mochila
  Mochila dentro: true
  # Ativar o uso de shift na mochila
  Shift: false
  # Ativar o uso de teclas numéricas na mochila
  Numkeys: false
  # Abrir a mochila com botão esquerdo
  AbrirEsquerdo: true
  # Abrir a mochila com botão direito
  AbrirDireito: true
  # Blacklist de itens que não poderão ser colocados na mochila
  Item blacklist:
    - 'MOB_SPAWNER'
  # Som ao abrir a mochila
  Som: ''
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isso.'
  Nao encontrado: '&cJogador não encontrado.'
  Deu: '&aVocê deu um(a) &r{mochila}&a para o jogador &7{player}&a.'
  Olhando: '&cHá alguém olhando esta mochila.'
  Encontrada: '&cMochila não encontrada.'
  Coincide: '&cA mochila na sua mão não é a mesma que está aberta.'
  Bloqueado: '&cEste item está bloqueado.'
  Quantia: '&cEsta mochila está agrupada. Desagrupe-a para usar.'
  Shift: '&cVocê não pode usar shift na mochila.'
  Numkeys: '&cVocê não pode usar as teclas numéricas na mochila.'
]]>
</code-block>
</chapter>

<chapter title="mochilas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Mochilas:
  pequena:
    Fileiras: 1
    Menu: '&8Mochila Pequena'
    Item:
      CustomSkull: false
      URL: ''
      ID: 54
      Data: 0
      Glow: false
      Name: '&6Mochila pequena'
      Lore:
        - '&7Fileiras: &f1&7.'
        - ''
        - '&fÚltimo jogador a abrir: &b{player}&f.'
        - '&f > em: &7{data} &f - &7{hora}&f.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/78-yMochilas">Site do plugin yMochilas</a>
    </category>
</seealso>