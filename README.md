# matchcutfc.de

Website von Matchcut nach CI und Markenkonzept. Claim: „Fußball ist nie nur Fußball.“ / „Football is never just football.“ Alles steckt in `index.html`: Schriften, Styles und Skript sind eingebettet, es werden keine externen Inhalte geladen.

## Vor dem Livegang ausfüllen

- **Impressum** (`#impressum`) und **Datenschutz** (`#datenschutz`): die Peach-markierten Platzhalter in `index.html`
- **Kontaktadresse (optional):** `email` im Block `CONFIG` am Ende von `index.html`

## Social-Links

Im Block `CONFIG` unter `editions`: Deutsche Ausgabe (@matchcutfc.de) und English Edition (@matchcutfc, auf YouTube @matchcutfc.en). Kopf und Fuß zeigen die Ausgabe der aktuellen Sprache, der Community-Bereich zeigt beide.

## Sprache

- matchcutfc.de zeigt Deutsch, matchcutfc.com Englisch
- `?lang=en` oder `?lang=de` an der Adresse erzwingt eine Sprache, z. B. für die Weiterleitung von matchcutfc.com auf `https://matchcutfc.de/?lang=en`
- sonst entscheidet die Browsersprache

## Quellen pro Video ergänzen

Im Block `<script type="application/json" id="quellen-daten">` einen Eintrag pro Video anlegen. Die Nummer erscheint als „Nr. 001“ und ist suchbar. Jeder Eintrag ist direkt verlinkbar: `https://matchcutfc.de/#video-001`.

```json
{
  "nummer": 1,
  "datum": "2026-11-14",
  "titel": { "de": "Haaland gegen Mbappé: Wer steht öfter im Abseits?", "en": "Haaland vs Mbappé: who gets caught offside more?" },
  "tags": ["Haaland", "Mbappé", "Abseits"],
  "videos": { "tiktok": "https://…", "instagram": "https://…", "youtube": "https://…" },
  "quellen": [
    { "name": "Opta Analyst", "url": "https://…", "beleg": { "de": "Abseitsstellungen 2025/26", "en": "Offsides 2025/26" } }
  ]
}
```

Der Beispiel-Eintrag (`"beispiel": true`) verschwindet automatisch, sobald der erste echte Eintrag drin ist.

## Dateien

- `index.html`: die Seite
- `favicon.svg`, `apple-touch-icon.png`: Profilbild dunkel aus dem Logo-Paket
- `og-image.jpg`: Vorschaubild, wenn der Link geteilt wird
- `CNAME`: Domain für GitHub Pages
- `.nojekyll`: GitHub Pages liefert die Dateien unverändert aus
