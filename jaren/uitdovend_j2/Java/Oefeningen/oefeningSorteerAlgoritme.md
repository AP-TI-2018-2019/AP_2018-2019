# Oefeningen sorteeralgoritmen

1) Controleer de tijdscomplexiteit van de bubblesort. Pas de bubble sort aan zodat het algoritme stopt als er niets meer te sorteren is. Dit zal het algoritme veel efficiënter maken bij gedeeltelijk gesorteerde array’s.
   1) > De complexiteit van bubblesort in de average- en worst-case is O(N²). In de best-case scenario is dit O(N).
   2) > De performantie kan geoptimaliseerd worden indien we een boolean bijhouden om te zien of er een swap is gedaan of niet. Indien er geen swap is gedaan, betekent dit dat de input al gesorteerd staat. Hierdoor is er geen nood om meer dan eenmaal over de array te loopen.
   3) > [Voor code zie theorie](../Theorie/sorteeralgoritmen.md)
2) Wat is de best case tijdscomplexiteit nu de bubble sort geoptimaliseerd is ? Best case is (in het geoptimaliseerde algoritme) wanneer de array reeds gesorteerd aangeboden wordt aan de bubble sort.
   1) > Zoals eerder vermeld zal de best-case scenario een complexiteit van T(N)=O(N) kennen.

3) Is de bubblesort een in-place algoritme ?
   1) > Ja. Het gebruikt O(1) extra geheugengebruik (een int voor de swap) en volgens de classificatie is elk algoritme dat <= O(log(n)) geheugen gebruikt een in-place algoritme.

4) Is de selection sort een in-place algoritme ?
   1) > Ja. Het gebruikt O(1) extra geheugengebruik (een int voor de swap en een int voor de min idx) en volgens de classificatie is elk algoritme dat <= O(log(n)) geheugen gebruikt een in-place algoritme.

5) Wat is de complexiteit van de selection sort bij een volledig gesortereerde array ? Waarom heeft dit deze complexiteit ?
   1) > Selection sort heeft net als mergesort de unieke eigenschap dat de complexiteit in zowel de best-, worst- als average-case hetzelfde blijft. Het heeft een complexiteit van O(N²) doordat het, ongeacht of de array gesorteerd is of niet, telkens over de array zal loopen om de min. value vooraan te plaatsen gevolgd door de 2de kleinste etc. Het is dus een **NIET** adaptief algoritme.

6) Wat is de best en worst case van de insertion sort ? En wat is hun bijhorende complexiteit ?
   1) > De best-case scenario van dit algoritme is als het algoritme een gesorteerde lijst ingevoerd krijgt. Hierdoor moet het slechts eenmaal over de array loopen aangezien het enkel swaps doet om het getal op de huidige index op zijn juiste positie te zetten. Dit geeft dit algoritme een best-case complexiteit van O(N).
   2) > De worst-case scenario is als dit algoritme een omgekeerd gesorteerde lijst ingevoerd krijgt (gesorteerd van groot naar klein). Dit zorgt er voor dat élk value geswapped meot worden om op de juiste plaatst geswapped te worden. Dit geeft een complexiteit van O(N²) in de worst-case-scenario.

7) Is de insertion sort een in-place algoritme ?
   1) > Ja. Het gebruikt O(1) extra geheugengebruik (een int voor de swap) en volgens de classificatie is elk algoritme dat <= O(log(n)) geheugen gebruikt een in-place algoritme.

8) Pas de quicksort aan zodat hij voor een reeks van 5 elementen of minder, insertionsort gebruikt i.p.v. quicksort.
   1) > Dit kan men zeer eenvodudig aanpakken door een if-statement in het begin van het algoritme te plaatsen die checkt of end-start <= 5 of niet. Indien dit klopt, wordt deze kleine array door een custom versie van insertion sort gesorteerd.
   2) > [Voor code zie theorie](../Theorie/sorteeralgoritmen.md)

9) Hoeveel extra geheugenopslag heeft een merge sort nodig ? Wat is de geheugen complexiteit  voor de merge sort?
   1) > Mergesort is een simpel algoritme dat een lijst telkens blijft opdelen in verschillende lijsten tot er meerdere lijsten overblijven met elks één waarde in. Nadien merget het 2 arrays per keer **DIRECT** in de juiste volgorde tot er weer één grote array is. Doordat dit algoritme een ingevoerde array opsplitst in meerdere arrays waar telkes 1 value in steekt, heeft dit een extra geheugengebruik van O(N). Dit betekent dat dit algoritme hierdoor **NIET** in-place is.
