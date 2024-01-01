# Nightbot Commands:

## !poketranslate
This command translates Pokemon between their English and Japanese names.<br/>
Usage: *!poketranslate Snorlax* will output *Snorlax is カビゴン (kabigon)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/poketranslate.txt)'.split('§');q='$(query)';if(!q){'Usage: !poketranslate Snorlax'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b='$(query) got away! Usage: !poketranslate Mr.Mime (no space chars)';}q+' is '+b;})
```
## !pattack
This command returns Pokemon attack type effectiveness.<br/>
Usage: *!poketranslate Snorlax* will output *Snorlax is カビゴン (kabigon)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/pokemon_strengths.txt)'.split('§');q='$(query)';if(!q){'Usage: !pattack fire'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b=q+' is not recognized! Usage: !pattack psychic';}b;})
```
## !pweak
This command returns Pokemon type weaknesses.<br/>
Usage: *!poketranslate Snorlax* will output *Snorlax is カビゴン (kabigon)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/pokemon_weakness.txt)'.split('§');q='$(query)'.toLowerCase();if(!q){'Usage: !pweak fire'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b=q+' is not recognized! Usage: !pweak psychic';}b;})
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
