# yReparacao
<secondary-label ref="factions"/>

### Descrição
Uma nova forma de reparar, ficando mais caro a cada vez que o item fica mais danificado e se contém encantamentos.

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
<video src="//www.youtube.com/watch?v=_t1wId-8gjI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/reparar&nbsp;- Reparar o item
/inventário.
/reparar giveitemrepair&nbsp;- Dar o item reparador.
/reparar reload&nbsp;- Recarregar as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yreparacao.usar - Permissão para o /reparar
yreparacao.giveitemrepair - Permissão para o /reparar giveitemrepair
yreparacao.admin.reload - Permissão para o /reparar reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yReparacao/
    ├── commands.yml
    ├── config.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="commands.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     ___                                          _
#    / __\___  _ __ ___  _ __ ___   __ _ _ __   __| |___
#   / /  / _ \| '_ ` _ \| '_ ` _ \ / _` | '_ \ / _` / __|
#  / /__| (_) | | | | | | | | | | | (_| | | | | (_| \__ \
#  \____/\___/|_| |_| |_|_| |_| |_|\__,_|_| |_|\__,_|___/
#
# Lista de comandos do plugin.

# Utilize "comando|comando" para criar aliases.
# Por exemplo: "gm|gamemode"
# Você pode criar quantas aliases quiser.
commands:
  repair: 'repair|reparar'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Opcoes:
   Nao cadastrado:
      Bloquear: true

Preco durabilidade base: 10.0 #caso não esteja cadastrado e o bloquear estiver false.
Preco encantamento base: 10.0 #caso não esteja cadastrado e o bloquear estiver false.

Preco durabilidade base xp: 5 #caso não esteja cadastrado e o bloquear estiver false.
Preco encantamento base xp: 5 #caso não esteja cadastrado e o bloquear estiver false.

Menu:
   Nome: '&8Reparação'
   Confirmar:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/c641682f43606c5c9ad26bc7ea8a30ee47547c9dfd3c6cda49e1c1a2816cf0ba'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aConfirmar'
      Lore:
      - ''
      - '&7Clique para confirmar a reparação.'
      - ''
   Cancelar:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/c641682f43606c5c9ad26bc7ea8a30ee47547c9dfd3c6cda49e1c1a2816cf0ba'
      ID: 0
      Data: 0
      Glow: true
      Name: '&cCancelar'
      Lore:
      - ''
      - '&7Clique para cancelar a reparação.'
      - ''
   Item:
      Slot: 13
      Lore:
      - ''
      - '&aSeu item possui {quantiaenc} encantamentos. Isto lhe custa: &e{moneyenc} & &e{xpenc} xp'
      - '&aO seu item está danificado e irá lhe custar: &e{moneydurabilidade} & &e{xpdurabilidade} xp'
      - '&aDesconto: &e{desconto}'
      - ''
      - '&fTotal: &e{money} & {xp} xp'
      - ''
      
Descontos:
   VIP:
      Permissao: 'yreparacao.vip'
      Desconto: 100.0

Encantamentos:
   Afiacao:
      ID: DAMAGE_ALL
      Preco por level: 10.5
      Preco por level xp: 5
   Repulsao:
      ID: KNOCKBACK
      Preco por level: 40.0
      Preco por level xp: 20

Durabilidade:
   Item1:
      ID: DIAMOND_SWORD
      Preco por level: 3.0
      Preco por level xp: 1

Repair-item:
   material: 'ANVIL'
   name: '&aReparador'
   lore: [ '&7Clique em um item para', '&7reparar ele totalmente.' ]
]]>
</code-block>
</chapter>

<chapter title="messages.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___  ___ ___  __ _  __ _  ___  ___
#   /    \ / _ \/ __/ __|/ _` |/ _` |/ _ \/ __|
#  / /\/\ \  __/\__ \__ \ (_| | (_| |  __/\__ \
#  \/    \/\___||___/___/\__,_|\__, |\___||___/
#                              |___/
#
# Plugin messages

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  inv-full: '&cO seu inventário está cheio.'
  help: |

    &aReparação comandos:

    &a> /reparar
    &a> /reparar giverepairitem

  item-none: '&cVocê deve estar segurando algum item.'
  item-cant: '&cEste item não pode ser reparado.'
  item-maximum: '&cEste item já está na durabilidade máxima.'
  repair: '&aVocê reparou este item e gastou &e{money} & {xp} xp'
  no-balance: '&cVocê não tem money suficiente, necessário: &e{money}'
  no-balance-xp: '&cVocê não tem xp suficiente, necessário: &e{xp}'
  enchant-found: '&cVocê não pode reparar este item pois contém encantamentos não cadastrados.'
  item-found: '&cVocê não pode reparar este item pois ele não está cadastrado.'
  item-give: '&bVocê deu &f{amount}x item reparador&b ao jogador &f{player}&b.'
  item-received: '&bVocê recebeu &f{amount}x item reparador&b.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/15-yReparacao">Site do plugin yReparacao</a>
    </category>
</seealso>