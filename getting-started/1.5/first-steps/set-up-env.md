# Set up a developer environment

**In this tutorial, you set up your device with all the tools you need to write and run code in JavaScript. These tools are called a developer environment.**

In this tutorial, you will learn how to:

- Install your tools
- Create your first coding project
- Install the IOTA core client library

## Why JavaScript

IOTA supports many programming languages, including C, Go, Java, and Python. While all these languages have their own benefits, JavaScript is one of the most popular languages.

As such, these tutorials use a server-side version of JavaScript called Node.js.

If you have never used JavaScript or Node.js before, reference the beginner tutorials at [w3schools.com](https://www.w3schools.com/).

## Step 1. Install your tools

In this step, install the programming tools that make up your developer environment. 

1. Install the [latest long-term support (LTS) version of Node.js](https://nodejs.org/en/download/).

    Node.js is an open-source server environment that allows you to run JavaScript on the server.

2. Install [Visual Studio Code](https://code.visualstudio.com/Download).

    :::info:
    Installing Visual Studio Code is a suggestion as it is a simple code editor that makes it easy to write and run code.

    Feel free to use any other as a preference.
    :::

## Step 2. Create your first coding project

In this step, create a project using the [npm package manager](https://www.npmjs.com/) that comes with Node.js. This project is used throughout the tutorials in this section.

1. Open a command-line interface.

    Depending on your operating system, a command-line interface could be [PowerShell in Windows](https://docs.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6), the [Linux Terminal](https://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/) or [Terminal for macOS](https://macpaw.com/how-to/use-terminal-on-mac).

2. Create a new directory to use for your project and change into it.

    ```bash
    mkdir iota-tutorial
    cd iota-tutorial
    ```

3. Initialize a new Node.js project.

    ```bash
    npm init
    ```

Now you have a `package.json` file, which includes the packages and applications the project depends on, and specific metadata like the project's name, description, and author. Whenever you install packages, those packages will be added to this file as a dependency. For more information, see this excellent [package.json guide](https://flaviocopes.com/package-json/).

## Step 3. Install the IOTA core client library


The IOTA core client library contains the main functionality that you need to develop applications on IOTA. Implemeted in TypeScript to strongly type the objects sent and received from the API.


Install the [iots.js](https://github.com/iotaledger/iota.js/tree/chrysalis) library via npm. 

```bash
npm install iotaledger/iota.js#chrysalis
```

After installing a package, you'll have a `node_modules` directory, which contains the `@iota/iota.js` package code and its dependencies.

:::success: Congratulations :tada:
You've got all the tools you need and now you're ready to start learning and coding!
:::

## Next steps

Complete your first IOTA project by [sending a "hello world" transaction](../first-steps/hello-world.md).

