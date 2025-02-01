# FSDB (FIRST Slovenia Discord Bot)

Bot za FIRST Slovenia Discord server (atm samo reaction role)

## Usage

### Creation

Bot dela na special sintaksi, ki ga user pošlje v channel (CHANNEL_ID_FOR_SETTING v .env):

```
content
---
<emoji> <roleId>
<emoji2> <roleId2>
...
```

Torej, pred `---` je content sporočila, npr. reaction role vprašanje ("Koliko si star?")

Pod `---` so emojiji (custom ali builtin) in role id, ločena sta s presledkom. Torej npr. `🔞 123456789012345678`, kjer je številka role id

Več emojijev ima lahko isti role id, samo emojiji morajo biti drugačni (ker ne moreš reactati z dvema istima emojima).

Nato bot pošlje sporočilo z contentom (pred `---`) v CHANNEL_ID_FOR_SENDING (env variable) in reacta z emojiji.

### Editing

Sporočilo v CHANNEL_ID_FOR_SETTING lahko editaš in bot bo uveljavil spremembe. Npr. lahko 
- spremeniš content ("Koliko časa si na svetu?")
- spremeniš katerikoli emoji (`🍞 123456789012345678`)
- spremeniš katerikoli role id (`🔞 098765432109876543`)
- oboje (`🍞 098765432109876543`)
- all of the above, za katerikoli emoji

### Deletion

Če zbrišeš tvoje sporočilo, bo bot tudi zbrisal svoje sporočilo. (Ni zelo uporabno ampak obstaja)
