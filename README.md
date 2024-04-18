
# Getting-Started-with-.env-in-React-Vite

![0_RROwM5fuF-Sc6pPb](https://github.com/BeWithSohail/Getting-Started-with-.env-in-React-Vite/assets/26677709/0aa11b82-1294-4752-ab83-4e545cd3343e)

Today, I will create React application using Vite because of his good performance in building and running web applications, and initialize environment variable.

(1) Let’s create our project:

$ npm create vite@latest
#or
$ yarn create vite 
#or
$ pnpm create vite


(2) Install dependencies: 

$ cd my-project
$ npm install
#or
$ yarn
#or
$ pnpm install
Add .env dependency:

(3) Install dotenv file 

npm install dotenv OR

$ yarn add dotenv  OR 

$ npm install dotenv


(4) Create ‘.env’ file in the main directory of my-project:

$ touch .env

.env :

API_URL=http://localhost:3030 


(5) Edit ‘vite.config.ts’ file

// import dotenv package

import dotenv from 'dotenv';

import { defineConfig } from 'vite';

import react from '@vitejs/plugin-react-swc';


(6) // Run package config

// https://vitejs.dev/config/

dotenv.config();


export default defineConfig({
  plugins: [react()],

// define process env

  define: {
    'process.env': process.env
  }

});

(7) Now you can use environment variable in your project

// process.env.[env-var]

console.log(process.env.API_URL)


Thanks In Advance 
