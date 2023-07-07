---
layout: default
title: Pre-workshop Material
nav_order: 3
---

# Pre-workshop Material

We will start by providing a brief introduction to the programming languages, frameworks and tools used in this workshop. We will also guide you through the process of cloning and setting up the workshop single-page application on your local machine.

![NextJS-MUI](assets/img/nextjs-mui.png)_Image retrieved from [itnext.io](https://itnext.io/next-js-with-material-ui-7a7f6485f671)_

## Terminology 

- **JavaScript (JS):** a programming language used to create dynamic and interactive websites. JavaScript enables web developers to creates web pages that include animated graphics, interactive forms, dynamic content feeds, etc. Websites created using JavaScript can respond to the user's actions and change the content layout in real time. As the language grew in popularity, JavaScript developers created libraries, frameworks, and programming practices to facilitate and streamline the process of web development. Today, you can use JavaScript for both client-side and server-side development with a variety of frameworks and tools that enhance its functionality.
- **TypeScript (TS):** a strongly typed programming language that builds on JavaScript. As a superset of JavaScript, TypeScript adds additional syntax and support for types, which helps developer catch type-related bugs early on in the development process. TypeScript code is converted to JavaScript, and thus runs anywhere that JavaScript is supported.
- **Library:** In the context of programming and computer science, a library is defined as a set of prewritten code that performs a specified function and helps developers simplify their code and build programs faster by reducing the need to write code for every single action from scratch. A library can include programmatic functions or visual components.
- **Framework:** In the programming world, a framework a structure that you can build software on. It serves as a foundation, so developers are not starting entirely from scratch. Frameworks are often associated with a specific programming language. A framework combines reusable pieces of code written to perform common tasks and user-provided code to create a custom application or website with new capabilities. Using a framework allows developers to focus on implementing high-level functionalities, while the low-level functions of the program are handled by the framework itself.
- **React:** a free, open-source JavaScript library used to build websites by combining reusable components to form an application's user interface. React’s primary role is to handle the view layer of the web application by providing an efficient rendering execution. Rather than dealing with the whole user interface as a single unit, React separates complex UI elements into individual components that form the building blocks of the whole UI. By using the React library, developers can build websites faster compared to vanilla JavaScript. Note that React is considered a library and not a framework because it does not include all the tools needed to build a website. There are many React-based frameworks that augment React with the additional tools needed to build a full-fledged website such as Angular (created by Google), Vue.js, Next.js, etc. 
- **Single-Page Application (SPA):** a website that dynamically rewrites a single webpage with new data from the web server, thus allowing the user to navigate the entire website with the need to reload the page. An SPA differs from a traditional website where the server re-renders a full page with every click the user makes and sends an entire new page to the browser.
- **Next.js**: a flexible React framework that gives developers building blocks to create fast single-page web applications. Next.js gives developers all the tools they need to handle the functionalities of a modern website including rendering, routing, data fetching, integrations, etc. Next.js is compatible with JavaScript as well as TypeScript and can be combined with numerous other libraries.  
- **Material UI (MUI):** a widely used open-source React component library that implements Google’s [Material Design](https://m2.material.io/). The library includes an extensive collection of prebuilt components (e.g., buttons, dropdown menus, data grids, cards, etc.) that are ready for use in production right out of the box. Material UI offers comprehensive styling tools that allow you to customize the design system of its components. Material UI allows you to build websites faster and enjoys a great deal of support in the React community given that it is the largest UI community in the React ecosystem.
- **Node Package Manage (`npm`):** an open-source repository of JavaScript tools and software packages that developers use to create applications and websites. `npm` also acts as a package manager that allows the users to add or remove packages using a command line interface.
- **Visual Studio Code:** a source-code editor developed by Microsoft that support numerous programming languages and extensions that augment it with additional functionalities and allow it to work seamlessly with other software development tools.  
- **WebStorm:** a JavaScript/TypeScript integrated development environment (IDE) developed by JetBrains. WebStorm helps developers create websites by highlighting syntax and semantic errors as they type code into the editor. WebStorm also includes a slew of built-in developer tools that can detect duplicate code fragments, common errors or redundancies and refactor the code to address these issues.

## Pre-workshop Setup

Please follow these steps to install Node.js and create a Next.js application **before** starting the workshop.

If you are using Windows or MacOS, use one of the installers from the [Node.js download page](https://nodejs.org/en/download/). Be sure to install the version labeled **LTS** (Long-Term Support). Other versions have not yet been tested with `npm`.

If you are using a Linux distribution, you can install Node.js using the `apt` package manager.
1. Start by refreshing your local package index: 
~~~
sudo apt update
~~~
2. Install Node.js: 
~~~
sudo apt install nodejs
~~~
3. Verify that the installation was successful: 
~~~
node -v
~~~
  You should be presented with the version of Node.js that you just installed.
4. Install the `npm` package manager:
~~~
sudo apt install npm
~~~

### Clone the Next.js Workshop SPA
Make sure you have Git installed on your system. If you need help installing Git on your system please consult the [official Git documentation](https://github.com/git-guides/install-git) or follow the [Introduction to Git and GitHub](https://ubc-library-rc.github.io/intro-git/) workshop provided by the UBC Library Research Commons.

Once you have Node.js and Git installed, you can clone the demo SPA used in this workshop by opening a terminal window and running the following command:
```git clone https://github.com/McMasterRS/wsr_web-design-guide.git```

You will now have an `wsr_web-design-guide` repo on your local machine.

### Start the Development Server
1. `cd` into the your project directory: 
~~~
cd wsr_web-design-guide
~~~

2. Checkout the `mac-branding` branch using the following command:
```
git checkout mac-branding
```
Alternatively, you can switch branches using your IDE's GUI:
![checkout-vsc](assets/img/checkout-vsc.png)
_Checking out  the `styling` branch using Visual Studio Code_

![checkout-webstorm](assets/img/checkout-webstorm.png)

_Checking out  the `styling` branch using WebStorm_

3. Install `next` using the following command:
```
npm i next
```

4. Start the development server:
~~~
npm run dev
~~~

### View the the Single-Page Application
Open your browser of choice and navigate to `localhost:3000`.
You should be presented with the following page:
![landing](assets/img/landing.png)
