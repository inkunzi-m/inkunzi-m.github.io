General Format <->
    {
        "name": "",
        "description": "",
        "autofill": [

        ],
        "image": "",

        "weight": 0,
        "predicates": {

        },
        "effects": {

        }
    }

    <h>THIS IS HOW EVERY</h>

Name <->
    • The title of the event. Displays in bold at the top
    • Example:
        "name": "Supply Shortage"

Description <->


Predicates <->

    PREDICATE_NAME      VALUE_TYPE      EXAMPLE_VALUE
    ------------------------------------------------------

    trait               string          "Isolationist"
    at_war              boolean         true
    ruler_condition     string          "Sick"

    either:             predicate_list  ([{"trait": "warlike"}, {"trait", "isolationist"}])






Effects <->

    EFFECT_NAME             VALUE_TYPE          EXAMPLE_VALUE
    -----------------------------------------------------------'

    dummy                   string              "you suck (for one session)"

    add_warsupport          decimal             20.5
    add_income              decimal | percent   20.5 | 13%
    add_legitimacy          integer             1
    add_army_upkeep         decimal             20.5
    add_units               dictionary          {"Strongmen": 2000, "Horsemen": 500}

    set_ruler_condition     string              "Sick"
