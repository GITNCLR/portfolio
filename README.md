Afbeeldingen van de test resultaten zijn te vinden in "Test Results".
In de map notebook vind je de notebooks die gebruikt zijn voor training en processing.

De hele dataset is te groot om te uploaden naar git ivm de .LIF files die tot 300 mb kunnen zijn, ik probeer deze naar Lamia te sturen via Teams.

GUI Git: https://github.com/CureQ/Microscopy/tree/Cell_Body_Detection

| Week | Logboeknotities |
|------|-----------------|
| 9 | Start gemaakt met het bekijken van de microscopie-afbeeldingen op de netwerkdrive. Gewoon even alles doorklikken en een gevoel krijgen voor wat voor data er is. Veel .lif-bestanden. Geen analyse gedaan, puur verkennen. |
| 10 | Officiële opdracht gekregen. Focus wordt cellichaamdetectie. Joram’s notebooks doorgenomen – handig om te zien hoe hij Cellpose inzet. Eerste tests met Cellpose gedaan: segmentatie van cellichamen en celkernen apart, en daarna filteren op overlap tussen die twee. Werkt al verrassend goed. |
| 11 | Voortgangspresentatie. Gesprek met Joram gehad, hij noemt Stardist als alternatief. Ook even NN-Unet bekeken. Veel documentatie, maar lastig om snel draaiend te krijgen. Eerst verder met Cellpose. |
| 12 | Plan van aanpak geschreven. op papier gezet met planning, doelen, en aanpak. Geen technische voortgang, maar goed om structuur te hebben. |
| 13 | GUI-workshop gehad met Tkinter. Niet super fancy, maar werkt wel. Ondertussen ook verder gekeken naar klassieke segmentatie in FIJI. Ze gebruiken daar Otsu + Watershed, maar dat ziet er best beperkt uit voor onze afbeeldingen. Veel oversplitsing of juist samensmelting. |
| 14 | Bezoek aan PMC. Carolina legt uit hoe ze FIJI gebruiken en waar het spaak loopt. Handig om te zien wat ze precies bedoelen met "niet goed genoeg". Ook veel duidelijkheid over wat ze precies willen meten. Interessant om de microscoop en kweken in het echt te zien. |
| 15 | Verder in de literatuur en op bioimage.io gekeken naar modellen die kant-en-klaar zijn. Paar modellen getest op hun demo-omgeving, maar Cellpose blijft voorlopig het meest stabiel qua resultaat. Veel modellen lijken heel specifiek voor één type data gemaakt. |
| 16 | Voortgangsgesprek met Lamia. Eindpresentatie voor de lab specefieke opdracht gegeven. Met Carolina besproken waar ze tegenaan loopt met huidige segmentatie. Uitleg gegeven over hoe ze kan annoteren. Eerste test gedaan met SAM-2 in notebook draait lokaal en werkt erg goed voor gewoone afbeeldingen van auto's. er zal veel finetuning nodig zijn om dit model goed te laten presteren op onze data. er zijn ook al modellen voor microscopie afbeeldingen gemaakt met sam waaronder CellSam en MicroSam. |
| 17 | Annotaties binnen, als PDF. Geen verwijzing naar welke originele afbeelding hoort bij welke annotatie. Sommige cellen ontbreken, zijn ook moeilijk te zien. Carolina zegt dat dit het beste is wat lukt, dus dit wordt de 'ground truth' voor nu. |
| 18 | Cellpose 4 is uit Met Cellpose-SAM, en dat werkt verrassend goed. Veel beter dan cyto3 van Cellpose 3. Finetuning lijkt niet per se nodig, maar omdat er toch al annotaties zijn, alsnog gedaan voor vergelijking. Daarnaast begonnen aan het paper prototype, flowdiagrammen en stakeholder mapping. besluit om vol op cellpose te gaan, de volledige package, actieve community en nu state of the art SAM model geintegreerd maken de andere opties een stuk minder interesant.|
| 19 | Gevraagd om originele .tif’s met annotaties krijg alleen losse PDF-pagina’s terug. Niet ideaal. Nogmaals gevraagd om echte bestanden. In de tussentijd gewerkt aan evaluatiepipeline voor IoU-scores en visuele overlays met TP/FP/FN. |
| 20 | Bijna alle originele beelden binnen (op twee na). Annotaties overnemen blijkt flink werk, ~20 minuten per afbeelding. Ondertussen 70%-versie opgezet en opgestuurd naar Lamia voor feedback. Ook Jesse om input gevraagd. |
| 21 | Feedback van Jesse en Lamia verwerkt. Laatste finetuningrondes bezig. Segmentatieresultaten opnieuw geplot, nu met duidelijke kleuren en legenda’s. Resultaten binnen van de Finetuning en nu wordt ook kwantificeerbaar dat cellpose sam met diameter instelling het beste resultaat geeft. |
