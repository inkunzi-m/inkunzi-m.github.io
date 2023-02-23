<h1>General Format</h1>

<p>This is how every event will be structured. When writing a new event, copy and paste this into a .json file before making any changes. Personally (this is totally optional), I would recommend using <a href="https://vscode.dev">vscode.dev</a> to make it as it will point out some common formatting errors. Just click "New File" -> "Text File" -> "Select a Language" -> "JSON", and paste the stuff in. </p>

```json
{
    "name": "",
    "description": "",
    "image": "",

    "weight": 0,
    "predicates": {

    },
    "effects": {

    }
}
```

<h1>Name</h1>
<p>The title of the event. Displayed in bold at the top of the event.</p>

Example:
```json
"name": "Supply Shortage"
```

<h1>Description</h1>
<p>Flavor text that appears in smaller text.</p>

Example:
```json
"description": "Lack of manpower to work the forges has made us unable to create enough supplies to fully equip our armies!"
```

<h1>Image</h1>
<p>Image that accompanies the event. (Shamelessly ripped from EU4). A list of all the images is available here at <a href="/events">.../events</a></p>

Example:
```json
"image": "EUROPEAN_city_view.png"
```

<h1>Weight</h1>
<p>How likely the event is to happen (higher number = more likely).</p>

Example:
```json
"weight": 30
```

<h1>Predicates</h1>
<p>Things that must be true for this event to be able to trigger.<br>Here's a code block showing an example of usage for every predicate:</p>

```json
"name": "Alzha",
"culture": "Alzhaic",
"religion": "Bytos",
"trait": "Warlike",
"at_war": true,
"ruler_condition": "Sick",
"min_ruler_age": 18,
"max_ruler_age": 60,
"min_infamy": 10,
"max_infamy": 20,
"min_legitimacy": "None",
"max_legitimacy": "Absolute",
"min_centralization": "None",
"max_centralization": "Absolute",
"either": {
    {"trait": "warlike"},
    {"trait": "isolationist"}
}
```

<h1>Effects</h1>
<p>Things that will happen when the event fires. <br>Here's a code block showing an example of usage for every effect:</p>

```json
"dummy": "Anything custom/manually edited would go here",
"add_warsupport": 10,
"add_stability": 10,
"add_infamy": 10,
"add_income": 20000,
"add_income": "15%",
"add_legitimacy": 1,
"add_centralization": -1,
"add_army_upkeep_cost": "10%",
"add_revolt_sentiment": "10%",
"set_ruler_condition": "Sick",
"add_cultural_stability": 0.5,
"add_religious_strength": 1.0,
"add_religious_authority": 0.75,
"add_units": {
    {"Infantry": 2000},
    {"Archers": 500}
}
"add_ruler_stats": {
    {"Rulership": 1},
    {"Intrigue": 2}
}
```
