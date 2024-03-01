# Goblin Run

In deze repository vind je de informatie over het project Goblin Run.

De opdracht is om een hypercasual game te ontwikkelen. Het doel voor de klant (VooDoo Games) is om een nieuwe hypercasual game aan hun portfolio toe te voegen.
Het idee van onze game is dat je een goblin bent die in een vat door een medieval wereld rolt om te ontsnappen aan ridders van een kasteel. Je moet zo lang mogelijk overleven en tegenstanders ontwijken.

# Geproduceerde Game Onderdelen

Geef per teammember aan welke game onderdelen je hebt geproduceerd. Doe dit met behulp van omschrijvingen visual sheets en screenshots.
Maak ook een overzicht van alle onderdelen met een link naar de map waarin deze terug te vinden zijn.

Patricia Kuipers:
  * [Tilespawner](https://github.com/mennoweerman/ExamenGoblinRun/tree/develop/GoblinRun/Content/Features/TileSpawner)
    
Menno Weerman:
  * [Playermovement](https://github.com/mennoweerman/ExamenGoblinRun/tree/develop/GoblinRun/Content/Blueprints)

Bart de Boer:
  * [Enemy AI Spawner & Movement](https://github.com/mennoweerman/ExamenGoblinRun/tree/feature/Bart/EnemySpawner/GoblinRun/Content/Blueprints)

Xavi Fijnhaar:
  * [Placeholder Art](https://github.com/mennoweerman/ExamenGoblinRun/tree/develop/GoblinRun/Content/Art/Placeholders)

## Tilespawner door Patricia Kuipers

Patricia heeft een tilespawner gemaakt die een map willekeurig kan genereren. Zodra de speler een tile aanraakt, spawnen er nieuwe tiles omheen met bepaalde limitaties zodat ze goed op elkaar aansluiten. Ook worden tiles die ver van de speler zitten weer verwijderd, zodat het de performance niet vermindert.

![TileGif](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/9fc4873f-e159-425a-bda0-f2682bcb9ddf)

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

## Placeholders door Xavi Fijnhaar

Xavi heeft placeholders gemaakt voor de speler en de wereld zodat de developers zo snel mogelijk konden beginnen met het ontwikkelen en testen van de game.

![image](https://github.com/mennoweerman/ExamenGoblinRun/assets/54790202/46b8a3fa-8a18-48b6-84d0-7390dc2c6b2d)



