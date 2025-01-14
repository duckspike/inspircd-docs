---
title: v3 Extended Bans
---

## Extended Bans

Some [list modes](/3/channel-modes), such as [channel mode `b` (ban)](/3/channel-modes), take a `<nick>!<user>@<host>` mask as their parameter. These list modes can be extended to support alternate forms of matching and actions.

### Acting

Acting extended bans allow restricting actions that users can perform. Such actions can include preventing a user from speaking in a channel (requires [the muteban module](/3/modules/muteban)) or changing their nickname (requires [the nonicks module](/3/modules/nonicks)). Acting extended bans can also be stacked with matching extended bans (see below).

{# use the template defined in mkdocs_inspircd/3/ #}
{% set extbans = acting_module_extbans %}
{% include "3/_extbans_table.md" %}

### Matching

Matching extended bans allow matching against extended user attributes such as account name (requires [the services_account module](/3/modules/services_account)) or TLS (SSL) fingerprint (requires [the sslmodes module](/3/modules/sslmodes)).

{# use the template defined in mkdocs_inspircd/3/ #}
{% set extbans = matching_module_extbans %}
{% include "3/_extbans_table.md" %}
