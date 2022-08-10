# Awesome Project Build with TypeORM

Steps to run this project:

1. Run `npm i` command
2. Setup database settings inside `ormconfig.json` file
3. Run `npm start` command

## Development Log:
(TS version have changed. @0.2.4)
1. changed DB credentials.

2. To delete a Sequence => DROP SEQUENCE user_id_seq CASCADE;

3. To delete a table => DROP TABLE "user";

4. Whenever we download something on express, we must also download "npm install -D @types/express morgan @types/morgan"

5. Creating a new Entity => typeorm entity:create --name Post

6. whenever we query something, particularly a column - use index for better performance

NOTE: npm install ts-node
      npm install --save-dev tsconfig-paths - Doubt!
7. npm run typeorm "schema:drop" - dropping all the schema's - to migrate - synchronize: flase.

8. A migration is just a single file with sql queries to update a database schema and apply new changes to an existing database.
   - To migrate => npm run typeorm migration:generate -- --name create-users-table

9. To run a migration -> 
npm run typeorm migration:run

10. To seed with the fake data -> must be configured in ormconfig.js -> "seeds": ["src/seeds/**/*{.ts,.js}"],
&& 
in package.json -> "seed": "ts-node ./node_modules/typeorm-seeding/dist/cli.js seed"
-- npm run seed --
