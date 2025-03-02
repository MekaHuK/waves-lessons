# Web3

Before we go into some more technical details, let's talk about some of the basic aspects of the web, its history, and the future.

- [Short history of Web evolution](#short-history-of-web-evolution)
- [Web services now and Web3 architecture](#web-services-now-and-web3-architecture)
- [Digital signatures](#digital-signatures)
- [Managing keys](#managing-keys)

## Short history of Web evolution

The Internet as a technology was born in 1969 (more than 50 years ago!), on 2nd September 1969. This was the first time two computers communicated with each other. But the World Wide Web was invented by Tim Berners-Lee in 1989. The World Wide Web in those days was completely different, not like it is now. There were no social networks like Facebook, e-commerce websites like Amazon, or even search engines and websites with memes.

Web pages were mostly “read-only” services. Universities and big companies were the main content creators, and pages were static only, without any way to interact with them. We call this Web 1.0.
 
**Web 1.0 – the “read-only” internet.**

Internet adoption and penetration grew extremely fast, and in the mid-2000s new interactive web services started to appear — forums, social networks and many other platforms for user-generated content. The Web became a “read” and “write” service. Pages became interactive and dynamic. We still live in the era of Web 2.0.

**Web 2.0 – user-generated content and p2p interactions/**

Web 3.0 is the future of the Internet, but what will this future look like?

We can see that the internet is becoming more and more intelligent over time. A large number of users are communicating, creating and sharing content. The complexity of these users’ behavior is also increasing dramatically. There are many challenges too, especially concerning data breaches and privacy. So we believe that the future of the internet should be decentralized, secure and user-centric. It will also make use of the benefits of major emerging technologies like the Internet of Things, Artificial Intelligence, Big Data, Virtual and Augmented Reality.

![](./_static/web3.png)


## Web services now and Web3 architecture

Web3 is different from the previous shift from Web1 to Web2. At its core, Web3 isn’t about speed, performance, or convenience. Instead, Web3 is about power. It’s about who has control over the technologies and applications that we use every day. It’s about breaking the dynamic that has shaped the last decade of the web: the tradeoff between convenience and control.

One of the pioneers of Web3 and the co-founder of the Ethereum blockchain, Gavin Wood, described Web3 in 2014 as “a reimagination of the sorts of things that we already use the Web for, but with a fundamentally different model for the interactions between parties. Information that we assume to be public, we publish. Information that we assume to be agreed upon, we place on a consensus-ledger. Information that we assume to be private, we keep secret and never reveal. Communication always takes place over encrypted channels and only with pseudonymous identities as endpoints; never with anything traceable (such as IP addresses). In short, we engineer the system to mathematically enforce our prior assumptions, since no government or organization can reasonably be trusted.”

**We can describe Web3 as a fully decentralized web with new models of interaction for users, based on trustless infrastructure** — such as a blockchain.

Traditional web services have “server” and “client” elements. When a user opens a page in his browser the server responds with a Web Page with static content, HTML, various assets (e.g. images and fonts) and JavaScript code.

Once the user interacts with the UI components of the web page – for example, buttons and forms – the JavaScript code creates a new request to the server: to fetch data to display or to write some data to the database on the server.

The server processes the request and returns as a response HTML, XML, or JSON data. The JavaScript in a browser uses this data to change the client’s application state and view.

![](./_static/web3-2.png)

Web3 works in a different way. Of course, a Web3 app also requires HTML and JavaScript code to run in a browser. So, the logic of server and client are still needed.

A “Read” request is created when a user interacts with a client application. In a Web3 app, the request is processed by a node from a Blockchain Network. The main difference here is that the data can be read by anyone and is public on popular opened distributed ledgers.

**The most important thing is to know how to write a piece of information into the blockchain network. Here we use the terms “transaction” and “digital signature”.**

All updates to the blockchain network must be submitted using transactions. The blockchain network determines that a transaction is valid only if a valid digital signature is provided. You may not be familiar with digital signatures, so let’s dive deeper into it.

![](./_static/web3-3.png)

## Digital signatures

Imagine that Bob creates two keys, a **private** and a **public** key. These keys are connected by a mathematical formula in a way that for each public key there is only one private key, and vice versa.

When Bob creates a message or transaction, he signs it using his private key. Bob must keep his private key secret. But Bob can share the public key with anyone who will validate the signed message or transaction. Anyone with Bob’s public key is able to verify that a certain transaction was signed by Bob’s private key – **verifying that Bob was the only one able to create and sign that message/transaction.**

![](./_static/keys.png)

This is known as asymmetric cryptography.

Here is an important note:

> A private key can be generated from some random seed phrase using hashing functions. The public key is obtained from the private key by using an elliptic curve multiplication. The network address, on the other hand, is obtained directly from the public key by using hashing functions.

All these transformations are **one-directional**. The opposite direction is very hard in terms of required computations.

Actually, it implies an astronomical value (~2^**256**) of computations required!

![](./_static/curve.png)

Seed phrases usually look like a random list of words (usually 15 or 16), for example: ‘couple remind obey mind core window talk maid small crisp card sure valve position sword’.

## Managing keys

Seed phrases and private keys **must be stored securely**. But at the same time they should be easy to use in order to sign transactions. The main software for the web is a browser, so one of the best solutions is to keep seeds and keys in browser extension applications. Browser extensions are secure by design (web pages do not have access to extensions’ storage and only can make requests to it). At the same time, they are convenient for users and developers (because of the WebExtensions standard). The main idea is that 3rd party application developers will not request that users use their private key directly with their apps, so they don’t expose this sensitive data to the web.

Many blockchains have browser extensions as secure key storage and as a tool to sign transactions. In the Waves ecosystem, there is [Keeper Wallet](https://keeper-wallet.app/#get-keeper) for these purposes. Here’s what the workflow looks like: 

1. Users store their private keys in a browser extension.
2. 3rd party applications like wallets and decentralized applications can request an extension to sign a transaction.
3. When apps request something, the user sees it and can approve or reject it.
4. If he approves it, the transaction goes to the blockchain network.

Well, let’s summarize this lesson and the most important things we’ve learned. We’ve talked about the Web’s evolution, about Web 1, 2 and 3 and their differences. We can describe Web3 as a fully decentralized web with new models of interaction for users, based on trustless infrastructure. We also talked about digital signatures and how they affect user experience with Web3 services. In the next lessons, we will start exploring the technical aspects of Web3: decentralization, blockchains and their consensus algorithms.