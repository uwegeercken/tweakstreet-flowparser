#### Data processing with Tweakstreet

Files are for the ETL tool from Twineworks: https://tweakstreet.io/

The controlflow is processing all dataflows and controlflows which were found in the given path (and subfolders). 
The idea is to show controlflows, dataflows, steps, services and their relationships - specifically which step or services types are used.

The data is sent to a Neo4j database and stored as nodes:
- Controlfows (.cfl files)
- Dataflows (.dfl files)
- Steps
- Services

Steps is a distinct list of steps (not all steps found). Relations are created between
- Dataflows and Steps
- Controlflows and Steps
- Controlflows and other controlflows
- Controlflows and Services
- Dataflows and Services

The module.tsm file defines the relevant keys in the flowfile and is required. In the Tweakstreet GUI select "File" >> "Choose Config Module" from the menu. When using the commandline engine.sh script, 
pass the module like this: ./engine.sh -g module.tsm 

You will need a Neo4j database running, so you can run the flow.


last update: uwe geercken - 2021-03-20