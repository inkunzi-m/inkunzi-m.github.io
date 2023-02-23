<h1>General Format</h1>

<b>This is how every event will be structured. When writing a new event, copy and paste this into a .json file before making any changes. </b>

<pre>
<code>
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
</code>
</pre>

<h1>Name</h1>
<p>The title of the event. Displayed in bold at the top of the event\nExample:\n    "name": "Supply Shortage"</p>

Description <-> <br>


Predicates <-> <br>

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
