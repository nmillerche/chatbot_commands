# Nightbot Commands:

## !poketranslate
This command translates Pokemon between their English and Japanese names.<br/>
Usage: *!poketranslate Snorlax* will output *Snorlax is カビゴン (kabigon)*.
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/poketranslate.txt)'.split('§');q='$(query)';if(!q){'Usage: !poketranslate Snorlax'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b='$(query) got away! Usage: !poketranslate Mr.Mime (no space chars)';}q+' is '+b;})
```

## !masu
This command will conjugate a Japanese verb from dictionary form to masu form.<br/>
```
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/masuVerbs.txt)'.split('§');q='$(query)';if(!q){'Usage: !masu suru'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];}}if(b==''){b='$(query) is not in my database.';}b;})
```
