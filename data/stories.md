stories:
- story: collect restaurant booking info  # name of the story - just for debugging
  steps:
  - intent: greet                         # user message with no entities
  - action: utter_ask_howcanhelp
  - intent: inform                        # user message with entities
    entities:
    - location: "rome"
    - price: "cheap"
  - action: utter_on_it                  # action that the bot should execute
  - action: utter_ask_cuisine
  - intent: inform
    entities:
    - cuisine: "spanish"
  - action: utter_ask_num_people
<!-- ## Happy path 1
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Happy path 2
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Happy path 3
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Happy path 4
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Happy path 5
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Happy path 6
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Happy path 7
* greet
  - utter_greet
* query_knowledge_base
  - action_query_database
* query_knowledge_base
  - action_query_database
* goodbye
  - utter_goodbye

## Hello
* greet
- utter_greet

## Query Knowledge Base
* query_knowledge_base
- action_query_database

## Bye
* goodbye
- utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot -->
