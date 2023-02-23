General Format
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

<h>This is how every event will be structured.</h>

Name <-> <br>
    • The title of the event. Displays in bold at the top
    • Example:
        "name": "Supply Shortage"

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
