Nightbot Commands:

!poketranslate
$(eval a='$(urlfetch json https://raw.githubusercontent.com/nmillerche/chatbot_commands/main/Nightbot/textfiles/poketranslate.txt)'.split('§');q='$(query)';if(!q){'Usage: !poketranslate Snorlax'}else{b='';for(i=0;i<a.length;i++){if(a[i].startsWith('$(query)')){b=a[i].split(':')[1];q=a[i].split(':')[0];}}if(b==''){b='$(query) got away! Usage: !poketranslate Mr.Mime (no space chars)';}q+' is '+b;})
