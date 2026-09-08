<p align="center">
  <img src=".github/assets/repository-banner.png" alt="SeriuxMod Server Mappings" width="100%">
</p>

# SeriuxMod Server Mappings

Dieses öffentliche Repository ist das versionierte Verzeichnis der in SeriuxMod dargestellten Minecraft-Server. Pro Server beschreibt ein `manifest.json` Identität, Verbindungsadresse, unterstützte Versionen, Regionen, Sprachen, Kategorien, Spielmodi, Social-Links und die zugehörigen Bildressourcen.

## Verzeichnisstruktur

```text
servers/
  <server-id>/
    manifest.json
    icon.png
    banner.png
```

Ein Manifest folgt inhaltlich diesem Aufbau:

```json
{
  "id": "example",
  "server-address": "play.example.net",
  "names": { "de": "Beispielserver", "en": "Example server" },
  "minecraft-versions": ["1.21.4"],
  "regions": ["EU"],
  "languages": ["de", "en"],
  "categories": ["network"],
  "gamemodes": ["survival"],
  "socials": {},
  "assets": { "icon": "icon.png", "banner": "banner.png" }
}
```

## Libraries und Versionen

Das Repository enthält ausschließlich JSON-Metadaten und statische Assets. Es gibt keine Laufzeitbibliotheken, keinen Paketmanager und keinen Buildschritt. Das verwendete Schema ist derzeit nicht als separat versionierte JSON-Schema-Datei hinterlegt.

## Beitrag hinzufügen oder ändern

1. Einen Ordner unter `servers/<server-id>/` anlegen oder bearbeiten.
2. `manifest.json` als valides UTF-8-JSON pflegen.
3. Referenzierte Assets im selben Serverordner ablegen.
4. Sicherstellen, dass `id`, Ordnername und alle Dateinamen stabil bleiben.
5. JSON lokal validieren, zum Beispiel mit `jq empty servers/<server-id>/manifest.json`.

Da dieses Repository öffentlich ist, dokumentiert es keine internen Backend-Endpunkte oder Zugangsdaten.
