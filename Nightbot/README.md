# Nightbot Commands:

## !ptranslate
This command translates Pokemon between their English and Japanese names.<br/>
Usage: *!poketranslate Snorlax* will output *Snorlax is カビゴン (kabigon)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/poketranslate.txt)'.split('§');q='$(query)';if(!q){'Usage: !ptranslate Snorlax'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b='getting away! Usage: !ptranslate Mr.Mime (no space chars)';}q+' is '+b;})
```
## !ptype
This command returns Pokemon type for an entered species.<br/>
```
$(eval a='$(urlfetch json https://github.com/nmillerche/chatbot_commands/raw/main/Nightbot/textfiles/pokemontypes.txt)'.split('§');q='$(query)';if(!q){'Usage: !ptype snorlax'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=q+' '+a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b=q+' is not recognized! Usage: !ptype mr.mime (no spaces)';}b;})
```
## !pattack
This command returns Pokemon attack type effectiveness.<br/>
Usage: *!pattack fire* will output *Fire attacks are super effective against Grass, Ice, Bug, and Steel types. They are not very effective against Fire, Water, Rock, or Dragon types.*
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/pokemon_strengths.txt)'.split('§');q='$(query)';if(!q){'Usage: !pattack fire'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b=q+' is not recognized! Usage: !pattack psychic';}b;})
```
## !pweak
This command returns Pokemon type weaknesses, including dual-types.<br/>
Usage: *!pweak psychic* will output *Psychic attacks are super effective against Fighting and Poison types. They are not very effective against Psychic or Steel types. They have no effect against Dark types.*
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/pokemon_weakness.txt)'.split('§');q='$(query)';if(!q){'Usage: !pweak normal/fire'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query):')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b=q+' is not recognized! Usage: !pweak psychic/bug';}b;})
```

## !mariotranslate
This command translates Mario names between their English and Japanese names.<br/>
Usage: *!mariotranslate Bowser* will output *Bowser is クッパ (kuppa)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/mariotranslate.txt)'.split('§');q='$(query)';if(!q){'Usage: !mariotranslate Goomba'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b='Thank you  $(user), but $(query) might be in another castle! Usage: !mariotranslate KoopaTroopa (no space chars)';}q+' is '+b;})
```

## !masu
This command will conjugate a Japanese verb from dictionary form to masu form.<br/>
Usage: *!masu いく* will output *いきます (go)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/masuVerbs.txt)'.split('§');q='$(query)';if(!q){'Usage: !masu suru'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];}}if(b==''){b='$(query) is not in my database.';}b;})
```
