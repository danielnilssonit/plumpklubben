# Plumpklubben

Plump, det svenska kortspelet där man bjuder på hur många stick man tar. För mobil, surfplatta och dator. Spela mot
datorn eller mot vänner och familj över internet.

**Spela:** https://danielnilssonit.github.io/plumpklubben/

- **Mot datorn:** två till sex spelare, datorn på lätt, medel eller svår.
- **Online:** tryck på *Spela online*, skapa ett bord och dela länken eller QR-koden. Lediga platser kan fyllas med datorer. Var och en spelar i sin egen telefon, platta eller dator.
- **Svenska regler:** tio kort i första given och sedan ett mindre varje giv, alla bjuder i tur och ordning och den som ger får inte bjuda så att det går jämnt ut, högsta budet spelar ut, man måste bekänna färg, exakt rätt antal stick ger 10 poäng plus budet (nollbud 5), annars en plump i protokollet. Husregler: trumf, vem som spelar ut, nollbudets poäng, partiets längd.
- **Lugnt och tydligt:** ett läge med lugnare tempo, större kort och en röst som säger när det är din tur.
- På iPhone och iPad: *Dela → Lägg till på hemskärmen*, så startar spelet som en app. Mot datorn fungerar det även utan internet.

Spelarna hittar varandra via öppna MQTT-servrar (inga konton, ingen egen server). Den som skapar bordet är värd och
blandar korten. Varje spelares hand och drag krypteras (ECDH och AES-GCM), så att ingen annan som lyssnar på servrarna
kan se korten. Namnen man väljer syns för andra i lobbyn.

Kortbilderna är ritade i koden (SVG). Rösterna är inspelade med ElevenLabs och musiken är gjord i Suno. Den här mappen
byggs automatiskt (tools/build-pages.mjs i projektet).
