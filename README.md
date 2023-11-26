Zpěvník 6. oddílu Mustangové

Pro stažení zpěvníku jednoduše rozklikněte zpevnik.pdf a vpravo najděte tlačítko Download.

Úpravy (pouze pro přihlášené):
Máte-li návrh na úpravu, připiště ji do návrhy_a_připomínky.txt - nejjednodušší je rozkliknout a vpravo najít ikonku tužky (Edit). 
Po připsání zmáčkněte Ctrl+S. Vyskočí okno, zde můžete popsat co jste změnili, nicméně v tomto přípdě nechte základní zprávu ("Updated návrhy_a_připomínky.txt") 

Přidání písničky:
Přidání má dva kroky - vytvoření textového souboru a přidání písničky do seznamu. 
Ve složce songs vytvořte nový soubor, pojmenujte nazev-pisnicky.tex (tak aby formát seděl k tomu co už ve složce je). Písničku je potřeba naformátovat následovně:
  (příkazy píšu mezi hvězdičkami, do texťáku je dáváte bez hvězdiček)
  nahoře *\beginsong{Název písničky}[by=Autor]*, úplně na konci *\endsong*
  každá sloka začíná příkazem *\beginverse*, končí *\endverse*
  každý refrén začíná *\beginchorus*, končí *\endchorus*
  když se refrén opakuje, napište ho prázdný, tj.  *\beginchorus \endchorus*, to vytvoří jenom "R:"
  Akordy vložíte jako \[Ami] \[Dsus4] \[F#]
  Repetice se udělá pomocí *\lrep* (to co je v repetici) *\rrep*
  opakování je pomocí *\rep{3}* - vypíše "(3x)"
  kurzíva pomocí *\textit{text v kurzívě}*, tučné písmo *\teftbf{tučný text}*
  další příkazy je možné najít v dokumentaci, na https://songs.sourceforge.net/songsdoc/songs.html
Když budete hotoví, zmáčkněte Ctrl+s, commit message nechte defaultní. Dále je potřeba upravit soubor songlist-cz.tex.
  Zde přidejte řádek *\input{nazev-pisnicky.tex}*, na správné místo (aby byly písničky řazené abecedně).
  Pak opět Ctrl+s, commit message můžete přepsat na "Přidána písnička XY" nebo něco podobného (ale není to nutné) 
  Důležité - tento krok udělejte až potom co vytvoříte textový soubor s písničkou podle minulého kroku(a jste si přiměřeně jistí že má správnou syntaxi), jinak po commitu vznikne error!
Když vznikne chyba, přijde na mail upozornění. V takovém případě to můžete buď zkusit sami opravit (typicky to bude nějaká zapomenutá závorka nebo podobně), nebo počkejte na Jirku či Nutriho.
