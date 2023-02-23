<style>
    code {
        color: #ffffff;
        background-color: #333333;
    }
</style>

<h1>General Format</h1>

<b>This is how every event will be structured. When writing a new event, copy and paste this into a .json file before making any changes. </b>

<pre><code>
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
</code></pre>

<h1>Name</h1>
<p>The title of the event. Displayed in bold at the top of the event<br>Example:</p>

<pre><code>
{
    "name": "Supply Shortage"
}
</code></pre>

<h1>Description</h1>
<p>Flavor text that appears in smaller text.<br>Example:</p>

<pre><code>
{
    "description": "Lack of manpower to work the forges has made us unable to create enough supplies to fully equip our armies!"
}
</code></pre>

<h1>Image</h1>
<p>Image that accompanies the event. (Shamelessly ripped from EU4). A list of all the images is available here at <a href="github.com/inkunzi-m/inkunzi-m.github.io/tree/main/events">github.com/inkunzi-m/inkunzi-m.github.io/tree/main/events</a><br>Example:</p>

<pre><code>
{
    "image": "EUROPEAN_city_view.png"
}
</code></pre>

<h1>Weight</h1>
<p>How likely the event is to happen (higher number = more likely).<br>Example:</p>

<pre><code>
{
    "weight": 30
}
</code></pre>

<h1>Predicates</h1>
<p>Things that must be true for this event to be able to trigger.<br>Here's a table showing an example of usage for every predicate:</p>

 <table>
  <tr>
    <th>Examples:</th>
  </tr><tr>
    <td><pre><code style="background-color: #666666">"trait": "warlike"</code></pre></td>
  </tr><tr>
    <td><pre><code>"at_war": "true"</code></pre></td>
  </tr><tr>
    <td><pre><code>"ruler_condition": "Sick"</code></pre></td>
  </tr><tr>
    <td><pre><code>[
    {"trait": "warlike"},
    {"trait": "isolationist"},
]</code></pre></td>
  </tr>
</table> 

    PREDICATE_NAME      VALUE_TYPE      EXAMPLE_VALUE
    ------------------------------------------------------

    trait               string          "Isolationist"
    at_war              boolean         true
    ruler_condition     string          "Sick"

    either:             predicate_list  ([{"trait": "warlike"}, {"trait", "isolationist"}])






Effects <-> <br>

    EFFECT_NAME             VALUE_TYPE          EXAMPLE_VALUE
    -----------------------------------------------------------'

    dummy                   string              "you suck (for one session)"

    add_warsupport          decimal             20.5
    add_income              decimal | percent   20.5 | 13%
    add_legitimacy          integer             1
    add_army_upkeep         decimal             20.5
    add_units               dictionary          {"Strongmen": 2000, "Horsemen": 500}

    set_ruler_condition     string              "Sick"
