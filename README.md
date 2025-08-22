# extendclean
Here is how to extend zeppelin bot's cleaning! First, we need to make sure you are building your own code. By default, it will use prebuilt images so the --build argument can be omitted from the following commands, unless if you have changed the source code locally, in which case, replace

image: dragory/zeppelin

with

build:
  context: .

for the migrate, bot, api, and dashboard containers in your respective docker-compose (standalone/lightweight). Make sure to run the below command every time you update/change the source code.

Next, go to fetchmessagestoclean.ts and change the MAX_CLEAN_AMOUNT ans MAX_CLEAN_TIME to any amount you want (Max clean time has to be 14=<)

If you filled in the Standalone section in the env file:
docker compose -f docker-compose.standalone.yml up -d --build
If you filled in the Lightweight section in the env file:
docker compose -f docker-compose.lightweight.yml up -d --build

