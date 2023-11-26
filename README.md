Zpěvník 6. oddílu Mustangové

Pro stažení zpěvníku jednoduše rozklikněte zpevnik.pdf a vpravo najděte tlačítko Download.

Úpravy (pouze pro přihlášené):
Máte-li návrh na úpravu, připiště ji do návrhy_a_připomínky.txt - nejjednodušší je rozkliknout a vpravo najít ikonku tužky (Edit). 
Po připsání zmáčkněte Ctrl+S. Vyskočí okno, zde můžete popsat co jste změnili, nicméně v tomto přípdě nechte základní zprávu ("Updated návrhy_a_připomínky.txt") 

Přidání písničky:
Přidání má dva kroky - vytvoření textového souboru a přidání písničky do seznamu. 
Ve složce songs vytvořte nový soubor, pojmenujte nazev-pisnicky.tex (tak aby formát seděl k tomu co už ve složce je). Písničku je potřeba naformátovat následovně:
(příkazy píšu kurzívou abych je zde odlišil od textu)\n
  -nahoře *\beginsong{Název písničky}[by=Autor]*, úplně na konci *\endsong*\n
  -každá sloka začíná příkazem *\\beginverse*, končí *\\endverse*\n
  -každý refrén začíná *\\beginchorus*, končí *\endchorus*\n
  -když se refrén opakuje, napište ho prázdný, tj.  *\beginchorus \endchorus*, to vytvoří jenom "R:"\n
  -Akordy vložíte jako \\[Ami] \\[Dsus4] \\[F#]\n
  -Repetice se udělá pomocí *\\lrep* (to co je v repetici) *\\rrep*\n
  -opakování je pomocí *\\rep{3}* - vypíše "(3x)"\n
  -kurzíva pomocí *\\textit{text v kurzívě}*, tučné písmo *\\teftbf{tučný text}*\n
  -další příkazy je možné najít v dokumentaci, na https://songs.sourceforge.net/songsdoc/songs.html\n
Když budete hotoví, zmáčkněte Ctrl+s, commit message nechte defaultní. Dále je potřeba upravit soubor songlist-cz.tex.\n
  -Zde přidejte řádek *\\input{nazev-pisnicky.tex}*, na správné místo (aby byly písničky řazené abecedně).\n
  -Pak opět Ctrl+s, commit message můžete přepsat na "Přidána písnička XY" nebo něco podobného (ale není to nutné)\n 
  -Důležité - tento krok udělejte až potom co vytvoříte textový soubor s písničkou podle minulého kroku(a jste si přiměřeně jistí že má správnou syntaxi), jinak po commitu vznikne error!\n
Když vznikne chyba, přijde na mail upozornění. V takovém případě to můžete buď zkusit sami opravit (typicky to bude nějaká zapomenutá závorka nebo podobně), nebo počkejte na Jirku či Nutriho.
