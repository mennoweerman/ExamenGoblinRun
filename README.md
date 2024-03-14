# Goblin Run

In deze repository vind je de informatie over het project Goblin Run.

De opdracht is om een hypercasual game te ontwikkelen. Het doel voor de klant (VooDoo Games) is om een nieuwe hypercasual game aan hun portfolio toe te voegen.
Het idee van onze game is dat je een goblin bent die in een vat door een medieval wereld rolt om te ontsnappen aan ridders van een kasteel. Je moet zo lang mogelijk overleven en tegenstanders ontwijken.

# Geproduceerde Game Onderdelen

Geef per teammember aan welke game onderdelen je hebt geproduceerd. Doe dit met behulp van omschrijvingen visual sheets en screenshots.
Maak ook een overzicht van alle onderdelen met een link naar de map waarin deze terug te vinden zijn.

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

Xavi Fijnhaar:
  * [Placeholder Art](https://github.com/mennoweerman/ExamenGoblinRun/tree/develop/GoblinRun/Content/Art/Placeholders)

## Wereldgenerator door Patricia Kuipers

Patricia heeft een wereldgenerator gemaakt die de ongeving willekeurig uit verschillende tiles creëert. Zodra de speler een tile aanraakt, spawnen er nieuwe tiles omheen met bepaalde limitaties zodat ze goed op elkaar aansluiten (wegen, water en land). Ook worden tiles die ver van de speler zitten weer verwijderd, zodat het de performance niet vermindert. De afstand hiervan is instelbaar.

![ezgif-5-73ddc364c8](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/2175bbe4-ec23-43a6-bb06-98921f04f4d2)

De radius van tiles die om de speler heen gegenereerd moeten worden is aan te passen door middel van een cijfer in de engine. Ook heeft elke kant van een tile (boven, rechts, onder en links) een vinkje waar je kan aangeven of er een weg, water of land tile aan vast mag zitten. Op basis daarvan wordt er bepaald welke tiles er ingespawnt mogen worden.

![VisualSheetMapGeneration](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b49048cc-c0e5-4f1e-ac07-dc7679c3be2f)

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

Het score systeem zorgt ervoor dat de speler een uitdaging in de game heeft. Je krijgt gebaseerd op je snelheid punten en kan daarmee proberen je highscore te verbreken als vorm van voldoening in de game. Je kan ook je highscore delen met je vrienden voor een vorm van competitie.

![image](![alt text](<Afbeelding van WhatsApp op 2024-03-14 om 10.20.59_c097a755.jpg>))
![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b752cdfb-65ca-4637-839b-90a77fca538e)

## Player Death door Menno Weerman

De player death zorgt ervoor dat de speler dood kan gaan en het spel niet opeindig door gaat. Als je dood gaat krijg je een death screen voor je met je highscore en je uiteindelijke score. 

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b752cdfb-65ca-4637-839b-90a77fca538e)

Dit zorgt voor korte speelsessies, maar ook dat je steeds beter kan worden in de game om steeds een betere highscore te krijgen.

## Main Menu door Menno Weerman

De main menu zorgt ervoor dat je niet gelijk de game hoeft te spelen als je de game opstart. Hierin kan je de game beginnen of de game afsluiten. 

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b752cdfb-65ca-4637-839b-90a77fca538e)

## Pause Menu door Menno Weerman

Het pause menu is bedoelt om tijdens het spel even de game te kunnen stoppen om iets anders te kunnen doen zonder je score kwijt te raken.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b752cdfb-65ca-4637-839b-90a77fca538e)

Door het pause scherm kan je de game verder laten gaan, en terug naar de main menu gaan.

## Miniature Camera effect door Menno Weerman

Het camera effect zit op de speler om het effect te geven dat de speler heel klein is en een soort speelgoed is.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/b752cdfb-65ca-4637-839b-90a77fca538e)

## Placeholders door Xavi Fijnhaar

Xavi heeft placeholders gemaakt voor de speler en de wereld zodat de developers zo snel mogelijk konden beginnen met het ontwikkelen en testen van de game.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/46b8a3fa-8a18-48b6-84d0-7390dc2c6b2d)



