---
title: gossip_menu_option
description: 
published: true
date: 2023-04-01T23:40:11.744Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:32:12.004Z
---

<a href="https://trinitycore.info/en/database/master/world/gossip_menu_addon" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'gossip_menu_addon'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/gossip_menu_option_locale" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'gossip_menu_option_locale'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment | Source in sniff |
| --- | --- | --- | :---: | :---: | --- | --- | --- | --- |
| [MenuID](#menuid) | int | unsigned | PRI | NO | 0 |  |  | SMSG_GOSSIP_MESSAGE |
| [GossipOptionID](#gossipoptionid) | int | signed |  | NO | 0 |  |  |  |
| [OptionID](#optionid) | int | unsigned | PRI | NO | 0 |  |  | SMSG_GOSSIP_MESSAGE |
| [OptionNpc](#optionnpc) | tinyint | unsigned |  | NO | 0 |  |  | SMSG_GOSSIP_MESSAGE |
| [OptionText](#optiontext) | mediumtext |  |  | YES | NULL |  |  | SMSG_GOSSIP_MESSAGE |
| [OptionBroadcastTextID](#optionbroadcasttextid) | int | unsigned |  | NO | 0 |  |  | fetched from hotfixes db (via wpp) |
| [Language](#language) | int | unsigned |  | NO | 0 |  |  |  |
| [Flags](#flags) | int | signed |  | NO | 0 |  |  |  |
| [ActionMenuID](#actionmenuid) | int | unsigned |  | NO | 0 |  |  | CMSG_GOSSIP_SELECT_OPTION |
| [ActionPoiID](#actionpoiid) | int | unsigned |  | NO | 0 |  |  | SMSG_GOSSIP_POI |
| [GossipNpcOptionID](#gossipnpcoptionid) | int | signed |  | YES | NULL |  |  |  |
| [BoxCoded](#boxcoded) | tinyint | unsigned |  | NO | 0 |  |  | SMSG_GOSSIP_MESSAGE |
| [BoxMoney](#boxmoney) | int | unsigned |  | NO | 0 |  |  | SMSG_GOSSIP_MESSAGE |
| [BoxText](#boxtext) | mediumtext |  |  | YES | NULL |  |  | SMSG_GOSSIP_MESSAGE |
| [BoxBroadcastTextID](#boxbroadcasttextid) | int | unsigned |  | NO | 0 |  |  | fetched from hotfixes db (via wpp) |
| [SpellID](#spellid) | int | signed |  | YES | NULL |  |  |  |
| [OverrideIconID](#overrideiconid) | int | signed |  | YES | NULL |  |  |  |
| [VerifiedBuild](#verifiedbuild) | int | signed |  | NO | 0 |  |  | generated |
&nbsp;
## Description of fields

### MenuID
Gossip entry from [`gossip_menu.MenuID`](/database/master/world/gossip_menu#MenuID) this option is associated with.
&nbsp;

### GossipOptionID
*- no description -*
&nbsp;

### OptionID
The id associated with this gossip_menu_option. Must be unique for a given menu starting from 0 (zero).
Value increments by 1 if there are multiple options in the same gossip_menu.
&nbsp;

### OptionNpc
*- no description -*
&nbsp;

### OptionText
This is the text that you want to be displayed in the player selectable option. Examples would be: "Please train me.", "I would like to browse your goods.", "Learn Dual Spec".
If field `OptionBroadcastTextID` contains a valid [`broadcast_text.ID`](/database/master/world/broadcast_text#ID), it links to broadcast_text so the content from broadcast_text is displayed directly.
&nbsp;

### OptionBroadcastTextID
The ID of the `OptionText` text in [`broadcast_text.ID`](/database/master/world/broadcast_text#ID). Responsible for locales.
&nbsp;

### Language
*- no description -*
&nbsp;

### Flags
*- no description -*
&nbsp;

### ActionMenuID
*- no description -*
&nbsp;

### ActionPoiID
*- no description -*
&nbsp;

### GossipNpcOptionID
*- no description -*
&nbsp;

### BoxCoded
*- no description -*
&nbsp;

### BoxMoney
*- no description -*
&nbsp;

### BoxText
Text displayed in a box after selecting the gossip option.
&nbsp;

### BoxBroadcastTextID
The ID of the `BoxText` text in [`broadcast_text.ID`](/database/master/world/broadcast_text#ID). Responsible for locales.
&nbsp;

### SpellID
*- no description -*
&nbsp;

### OverrideIconID
*- no description -*
&nbsp;

### VerifiedBuild
This field is used by the TrinityDB Team to determine whether a template has been verified from WDB files.

If value is 0 then it has not been parsed yet.

If value is above 0 then it has been parsed with WDB files from that specific client build.

If value is -1 then it is just a place holder until proper data are found on WDBs.

If value is -Client Build then it was parsed with WDB files from that specific client build and manually edited later for some special necessity.

&nbsp;

<a href="https://trinitycore.info/en/database/master/world/gossip_menu_addon" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'gossip_menu_addon'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/gossip_menu_option_locale" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'gossip_menu_option_locale'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
