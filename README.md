# Goblin Run

In deze repository vind je de informatie over het project Goblin Run.

De opdracht is om een hypercasual game te ontwikkelen. Het doel voor de klant (VooDoo Games) is om een nieuwe hypercasual game aan hun portfolio toe te voegen.
Het idee van onze game is dat je een goblin bent die in een vat door een medieval wereld rolt om te ontsnappen aan ridders van een kasteel. Je moet zo lang mogelijk overleven en tegenstanders ontwijken. Dit geeft je punten, en je kunt een highscore krijgen. 

We gaan een verdienmodel met advertenties gebruiken die terugkomen op de deathscreen.

# Geproduceerde Game Onderdelen

Patricia Kuipers:
  * [Wereldgenerator](https://github.com/mennoweerman/ExamenGoblinRun/tree/develop/GoblinRun/Content/Features/TileSpawner)
    
Menno Weerman:
  * [Player Movement](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Menno/PlayerMovement)
  * [Score System](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Menno/ScoreSystem)
  * [Player Death](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Menno/PlayerDeath)
  * [Main Menu](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Menno/UI/MainMenu)
  * [Pause Menu](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Menno/UI/PauseMenu)
  * [Miniature Camera Effect](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Menno/VFX/MiniatureEffect)

Bart de Boer:
  * [Enemy AI Spawner & Movement](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Bart/EnemySpawner/GoblinRun/Content/Blueprints)

## Wereldgenerator door Patricia Kuipers

Patricia heeft een wereldgenerator gemaakt die de omgeving willekeurig uit verschillende tiles creëert. Hieronder zie je een afbeelding van een wereld die ermee is gemaakt.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/5e453e84-9c10-4fa9-9d6a-7df72a606fff)

De tiles spawnen normaal alleen om de speler heen. Zodra de speler een tile aanraakt, spawnen er op de vrije plekken nieuwe tiles omheen. 

Tiles hebben bepaalde limitaties zodat ze aan alle kanten goed op elkaar aansluiten. De limitaties kun je per tile in de editor instellen, door middel van een map met een Enumerator van "boven", "rechts", "onder" en "links" en een Struct van 3 booleans, "land", "weg" en "water". Hier kun je er dus één van aanvinken, om aan te geven per kant dat dat hetgene is wat er tegenaan mag spawnen. 

De pijl geeft de "boven" richting van een tile aan, zie het plaatje hieronder.

![Tile_01](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/5b921e7a-d8f1-49f4-b552-92830975bb31)

In de scene staat een object genaamd Tile Manager. Deze bevat een lijst met alle tiles die ingespawnt kunnen worden. Hij wordt ook daadwerkelijk bij het inspawnen van nieuwe tiles gebruikt. 

Dit zijn niet alle tiles van de game, want de kasteeltiles willen we niet willekeurig in de wereld spawnen. 

Als er nieuwe tiles aan de game toegevoegd worden, hoeven er maar twee dingen gedaan te worden om ze werkend te krijgen: een nieuwe blueprint van elke tile aanmaken met de juiste instellingen per kant, en de blueprint in deze lijst toevoegen. Daarna kan hij automatisch goed in de wereld gezet worden.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/546196d5-1916-4446-b972-e5b7c31df021)

Tiles die ver van de speler zitten worden weer verwijderd. Dit doen we om goede performance in de game te behouden. De afstand waarop tiles van de speler despawnen kan makkelijk worden ingesteld door middel van een float in de engine.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/74f103bf-703f-4ef2-8a60-0ec7411dba7e)

Hieronder zie je hoe de tiles despawnen met de variabele "Despawn Distance" op de waarde 5000. 

https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/d206ba7b-284d-4a4b-a272-c754d27833c3

Dit is hoe ze despawnen als die waarde op 25000 staat.

https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/00b51436-a4ea-48d6-b5c7-2291ae66b85c

Ten slotte staat er een "Backup Tile" variabele in de Tile blueprint. Deze is voor de zeldzame gevallen waarin er geen passende tile tussen andere tiles in gespawnt kan worden, en er voor een andere optie gekozen moet worden. Dit omdat het spawnsysteem erg complex geworden is, en er niet met alles rekening gehouden kon worden.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/9ddc0e1a-0887-4cfa-a714-7d9e391a10a9)


## Enemy AI Spawner & Movement door Bart de Boer

Het enemy spawnsysteem zorgt ervoor dat in de 4 hoeken van het scherm vijanden worden ingespawnt.
Je kan in de editor aangeven hoever die hoeken zijn en je kan de frequentie aangeven van hoe vaak de vijanden inspawnen.

![SpawnerVariables](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/bf197041-4f77-40c9-9313-72082e3a497c)

De enemy AI zorgt ervoor dat vijanden naar je toe kunnen lopen. Ze gebruiken de navmesh in het level om een pad naar de speler
te zoeken en die dan te achtervolgen.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/818a6e31-7f83-4def-929f-45890a6dace9)

## Playermovement door Menno Weerman

De playermovement zorgt ervoor dat de speler automatisch vooruit gaat en je met behulp van de knoppen links en rechts op het scherm naar de bijbehorende richtingen kunt draaien. 

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b752cdfb-65ca-4637-839b-90a77fca538e)

Je versnelt langzaam naar de topsnelheid zodat het spel uitdagender is. Ook hebben we een goede middenweg gevonden voor de turnradius, zodat het niet te makkelijk maar ook niet te moeilijk manoeuvreren is.

## Score System door Menno Weerman

Je krijgt gebaseerd op je snelheid punten. Je krijgt gemiddeld 1 punt per seconde als je niet stil staat. Als je de maximum snelheid rijd word je tekst goud en krijg je 3 keer zoveel punten. 

![Afbeelding van WhatsApp op 2024-03-14 om 10 21 14_387a9f90](https://github.com/mennoweerman/ExamenGoblinRun/assets/70953228/eef0f5d2-c61b-4ec8-a038-13cb09c6b407)
![Afbeelding van WhatsApp op 2024-03-14 om 10 20 59_5dc20b12](https://github.com/mennoweerman/ExamenGoblinRun/assets/70953228/41f0d89d-54bc-41a9-95f8-efb9957867f5)

## Player Death door Menno Weerman

Als je dood gaat krijg je een death screen voor je met je highscore en je uiteindelijke score. Hier kan je de game opnieuw spelen of terug naar de main menu gaan.

![Afbeelding van WhatsApp op 2024-03-14 om 10 29 22_fe4dd0ed](https://github.com/mennoweerman/ExamenGoblinRun/assets/70953228/91e3bd64-ecdc-4363-915b-ca830ba69a60)

## Main Menu door Menno Weerman

Als je de game opstart kom je op de main menu terecht zodat je de game niet gelijk hoeft te starten. Hierin kan je de game beginnen of de game afsluiten. 

![Afbeelding van WhatsApp op 2024-03-14 om 10 30 16_68051b76](https://github.com/mennoweerman/ExamenGoblinRun/assets/70953228/a2914477-3b21-4989-a5e2-2c5547d5859f)

## Pause Menu door Menno Weerman

Het pause menu kun je bereiken door de pause knop rechts boven in je scherm te drukken tijdens het spelen. Hierdoor zou je game pauzeren en zal je je score niet kwijtraken als je de game niet afsluit.

![Afbeelding van WhatsApp op 2024-03-14 om 10 27 01_36a33ccf](https://github.com/mennoweerman/ExamenGoblinRun/assets/70953228/eeb660bc-5c52-4d9c-a697-0b56f254daa9)

Door het pause scherm kan je de game verder laten gaan, en terug naar de main menu gaan.
