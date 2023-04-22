# node-red-openai-api #

a replication of the Open AI API for Node-RED

This repository contains flows for [Node-RED](https://nodered.org/) which replicate the [Open AI API](https://platform.openai.com/docs/api-reference/introduction). This allows users to route requests to Open AI products through their own (or a hosted) Node-RED server, giving them full control over all requests.

In the simplest case, people could just forward any request to Open AI and just log what has been sent. But they could also provide their own implementations - e.g., based on other flows which use [LLaMA](https://github.com/rozek/node-red-flow-llama), [Stanford Alpaca](https://github.com/rozek/node-red-flow-alpaca), or GPT4All [filtered](https://github.com/rozek/node-red-flow-gpt4all-filtered) or [unfiltered](https://github.com/rozek/node-red-flow-gpt4all-unfiltered) or [GPT4All-J](https://github.com/rozek/node-red-flow-gpt4all-j) instead of Open AI models - giving them even more control with respect to

* data privacy
* safety and
* costs.

Being compatible with the Open AI API even allows them to use their Node-RED implementations in software which was initially based on Open AI products.

> Nota bene: this work is currently in progress, a first release is planned for monday, April 24th, 2023 - stay tuned.
