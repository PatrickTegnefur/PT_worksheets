# Uppgiftsbanken

En utskriftsvänlig uppgiftsbank i matematik. Du väljer uppgifter ur banken, samlar ett urval och bygger arbetsblad på A4 som du skriver ut eller sparar som PDF. Allt är vanliga textfiler (JSON och SVG), så materialet ligger hos dig och kan versionshanteras på GitHub.

## Kom igång

**Publicera på GitHub Pages**
1. Skapa ett nytt repo på GitHub och ladda upp innehållet i den här mappen (så att `index.html` ligger i repots rot).
2. Gå till *Settings → Pages*, välj *Deploy from a branch*, grenen `main` och mappen `/ (root)`.
3. Efter någon minut finns verktyget på `https://<användare>.github.io/<repo>/`.

**Köra lokalt (Windows)**
Dubbelklicka på `starta-lokalt.bat`. Den startar en liten lokal server (kräver Python) och öppnar `http://localhost:8000`. Verktyget fungerar inte om `index.html` öppnas direkt från mappen, eftersom webbläsaren då blockerar inläsningen av filerna.

Använd Chrome eller Edge på dator. Då kan verktyget spara filer rakt in i din mapp.

## Så arbetar du

1. **Bank:** bläddra bland uppgifterna med kategoriträdet till vänster. Klicka på ett färgat chip för att se uppgifter som testar liknande saker. Lägg de du gillar i samlingen. Välj gärna fler än du behöver och gallra senare.
2. **Samling:** sortera om, ta bort uppgifter som är för lika varandra och lägg dem i arbetsbladet.
3. **Arbetsblad:** dra uppgifterna på plats, ändra bredd och skrivutrymme, välj numrering, typsnitt och storlek. Sidorna visas som riktiga A4-sidor. *Skriv ut* ger papper eller PDF ("Spara som PDF").
4. **Skapa:** skriv egna uppgifter eller generera rutinuppgifter från mallar. Det går att redigera allt efteråt.
5. **Spara:** *Spara arbetsblad* och *Spara samling* skriver en JSON-fil. Nya och ändrade uppgifter listas under *Filer att spara i repot* i fliken Skapa. Spara varje fil i sin mapp i din lokala kopia av repot och gör sedan commit och push (GitHub Desktop räcker).

Tills du har sparat filerna ligger ändringarna bara i webbläsaren.

## Mappar
```
index.html        verktyget
index.json        register över filerna
kategorier.json   arbetsområde › delområde › uppsättning
uppgifter/        uppgifterna, en fil per delområde
figurer/          SVG-figurer (filnamn = uppgiftens id)
generatorer/      mallar som slumpar fram rutinuppgifter
samlingar/        sparade urval
arbetsblad/       sparade arbetsblad
docs/dataformat.md  beskrivning av alla filformat
```

## Bidra
Kollegor kan använda verktyget direkt via länken. För att lägga till uppgifter eller generatorer skapas filerna enligt `docs/dataformat.md` och skickas som pull request, så att du kan granska innan de blir en del av banken.

## Att tänka på
- Facit ligger i samma filer som uppgifterna. Om repot är publikt kan alla som hittar det läsa facit.
- Kopiera inte uppgifter ur läromedel till ett publikt repo. Egna uppgifter är fria att dela.
