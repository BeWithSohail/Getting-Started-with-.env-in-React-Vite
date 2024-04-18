# Getting-Started-with-.env-in-React-Vite

![0_RROwM5fuF-Sc6pPb](https://github.com/BeWithSohail/Getting-Started-with-.env-in-React-Vite/assets/26677709/0aa11b82-1294-4752-ab83-4e545cd3343e)

Today, I will create React application using Vite because of his good performance in building and running web applications, and initialize environment variable.

Let’s create our project:

$ npm create vite@latest
#or
$ yarn create vite 
#or
$ pnpm create vite

<br > 
Install dependencies:

$ cd my-project

$ npm install
#or
$ yarn
#or
$ pnpm install
Add .env dependency:

<br > 
$ npm install dotenv
#or
$ yarn add dotenv
#or
$ pnpm install dotenv
Create ‘.env’ file in the main directory of my-project:

$ touch .env
.env :

API_URL=http://localhost:3030
Edit ‘vite.config.ts’ file

<br > 
// import dotenv package
import dotenv from 'dotenv';
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react-swc';

<br > 
// run package config
dotenv.config();
// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
// define process env
  define: {
    'process.env': process.env
  }
});
Now you can use environment variable in your project
<br > 
// process.env.[env-var]
console.log(process.env.API_URL)
