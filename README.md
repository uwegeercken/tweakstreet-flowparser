This controlflow is processing all dataflows and controlflows which were found in the given folder (and subfolders). 
The idea is to show controlflows, dataflows, steps and their relationships - specifically which step types are used.

The data is sent to a Neo4j database and stored as nodes:
- Controlfows (.cfl files)
- Dataflows (.dfl files)
- Steps

Steps is a distinct list of steps (not all stpes found). Relations are created between
- Dataflows and Steps
- Controlflows and Steps
- Controlflows and other controlflows

You will need a Neo4j database running, so you can run the flow.


last update: uwe geercken - 2021-03-15