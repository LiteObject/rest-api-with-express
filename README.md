# REST API Using NodeJS & Express

Here are step-by-step instructions to create a basic REST API using Node.js, Express, and TypeScript:

## Step 1: Set up a new Node.js project

- Create a new directory for your project.
- Open a terminal and navigate to the project directory.
- Run npm init to initialize a new Node.js project. Follow the - prompts to set up your project's details.

## Step 2: Install dependencies

Install the required dependencies by running the following command:

    npm install express typescript ts-node @types/express

## Step 3: Set up TypeScript configuration
Create a `tsconfig.json` file in the root of your project directory.

```shell
npx tsc --init
```

Add the following content to the `tsconfig.json` file:

```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "outDir": "dist",
    "strict": true,
    "esModuleInterop": true
  },
  "include": ["src"],
  "exclude": ["node_modules"]
}
```

## Step 4: Create the Express server

- Create a new directory named src in the project root.
- Inside the src directory, create a new file named server.ts.
- Add the following code to `server.ts`:

```typescript
import express, { Request, Response } from 'express';

const app = express();
const port = 3000;

app.get('/', (req: Request, res: Response) => {
  res.send('Hello, World!');
});

app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});

```

## Step 5: Build and run the server
- Open a terminal and navigate to the project directory.
- Run the following command to compile the TypeScript code:

    ```shell
    npx tsc
    ```
- After the compilation is successful, run the following command to start the server:

    ```shell
    node dist/server.js
    ```
## Step 6: Test the API
- Open a web browser or use a tool like Postman.
- Access http://localhost:3000 in the browser or send a GET request to http://localhost:3000 using Postman.
- You should see the response "Hello, World!".