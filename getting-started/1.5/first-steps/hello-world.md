# Send a "hello world" transaction

**In this tutorial, you send your first transaction to an IOTA node. At the end of this tutorial, you will have your own transaction in the Tangle that everyone can see.**

## Prerequisites

To complete this tutorial, you need a [developer environment for Node.js](../first-steps/set-up-env.md).

In this tutorial, you will connect to a node that's run by the IOTA Foundation in the Devnet: A development network.

## Send a message to the tangle

In this step, you create a message that contains a "Hello world" message and send it to your connected node to attach to the Tangle.

1. Require the library and connect to a node.

    Create a Javascript file
    ```bash
    touch index.js
    ```

    Input this to your new file.
    ```js
    // Require everything you need here from the library.
    const { sendData, SingleNodeClient, Converter } = require("@iota/iota.js");
    ```

2. Create a async functions and send a message

    ```js
    const API_ENDPOINT = "http://localhost:14265";
    const client = new SingleNodeClient(API_ENDPOINT);
    const myIndex = "MY-DATA-INDEX";
    const message = Converter.asciiToBytes("Hello World!")

    await sendData(client, myIndex, message)
        .then((res) => {
            console.log("Received Message Id: ", res.messageId);
        })
        .catch((err) => console.error(err));
    ```

    You'll find out more about what these are in the next topic.

2. Call the method and start the programm.

   
    To run the code, execute this in your terminal.

    ```bash
    node index.js
    ```

    You can watch the message on the [Tangle Explorer](https://explorer.iota.org/). 

:::success:Congratulations :tada:
You've just sent your first transaction. Your transaction is attached to the Tangle, and will be gossiped around the rest of the network.
:::

<!-- 
## Run the code

We use the [REPL.it tool](https://repl.it) to allow you to run sample code in the browser.

Click the green button to run the sample code in this tutorial and see the results in the window.

<iframe height="600px" width="100%" src="https://repl.it/@jake91/Send-a-hello-world-transaction?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

 -->

## Next steps

Take an in-depth look at how your transaction made it to the Tangle by [examining the steps that were involved](../first-steps/sending-transactions.md).

You can also use the client library to [search for your transaction in the Tangle](root://core/1.0/tutorials/js/read-transactions.md).

Examples of this tutorial are also available in the following languages:

- [C](root://core/1.0/tutorials/c/send-your-first-bundle.md)
- [Go](root://core/1.0/tutorials/go/send-your-first-bundle.md)
- [Python](root://core/1.0/tutorials/python/send-your-first-bundle.md)
- [Java](root://core/1.0/tutorials/java/send-your-first-bundle.md)
