# Steps for Social Buzz Backend with Node.js

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

- create SocialBuzzServer class in setupServer.ts file

```ts
import { Application } from "express";
import { Server } from "http";

export class SocialBuzzServer {
  private app: Application;

  constructor(app: Application) {
    this.app = app;
  }

  public start(): void {
    this.securityMiddleware(this.app);
    this.standardMiddleware(this.app);
    this.routesMiddleware(this.app);
    this.globalErrorHandler(this.app);
    this.startServer(this.app);
  }

  private securityMiddleware(app: Application): void {}
  private standardMiddleware(app: Application): void {}
  private routesMiddleware(app: Application): void {}
  private globalErrorHandler(app: Application): void {}
  private startServer(app: Application): void {}
  private createSocketIO(httpServer: Server): void {}
  private startHttpServer(httpServer: Server): void {}
}
```
