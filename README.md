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
<p>Things that must be true for this event to be able to trigger.<br>Here's a table showing an example of usage for every predicate:</p>

 <table>
  <tr>
    <th>Examples:</th>
  </tr><tr>
    <td><pre><code>"trait": "warlike"</code></pre></td>
  </tr><tr>
    <td><pre><code>"at_war": "true"</code></pre></td>
  </tr><tr>
    <td><pre><code>"ruler_condition": "Sick"</code></pre></td>
  </tr><tr>
    <td><pre><code>"either": [
    {"trait": "warlike"},
    {"trait": "isolationist"},
]</code></pre></td>
  </tr>
</table> 

<h1>Effects</h1>
<p>Things that will happen when the event fires</p>

 <table>
  <tr>
    <th>Examples:</th>
  </tr><tr>
    <td><pre><code>"dummy": "Anything custom/manual goes here"</code></pre></td>
  </tr><tr>
    <td><pre><code>"add_warsupport": 20.5</code></pre></td>
  </tr><tr>
    <td><pre><code>"add_income": 20.5</code></pre></td>
    <td><pre><code>"add_income": "13%"</code></pre></td>
  </tr><tr>
    <td><pre><code>"add_legitimacy": 1</code></pre></td>
  </tr><tr>
    <td><pre><code>"add_army_upkeep": 20.5</code></pre></td>
  </tr><tr>
    <td><pre><code>"set_ruler_condition": "Sick"</code></pre></td>
  </tr><tr>
    <td><pre><code>"add_units": {
        {"Strongmen": 2000},
        {"Horsemen": 500}
}</code></pre></td>
  </tr>
</table> 
