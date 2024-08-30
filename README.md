# Steps

- create project `mkdir social-buz-backend`

- initialize package.json `npm init`

- change main.js to app.js

- install typescript as dev dependency `npm i typescript -D`

- initialize tsconfig.json `npx tsc --init`

- update tsconfig.json

- create src folder `mkdir src && cd src`

- add files `touch app.ts config.ts routes.ts setupDatabase.ts setupServer.ts`

- create folder structure `mkdir -p features shared/globals shared/services/db shared/services/emails shared/services/queues shared/services/redis shared/sockets shared/workers`

- install express `npm i express && npm i @types/express -D`
  