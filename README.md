# node-red-openai-api #

a replication of the Open AI API for Node-RED

This repository contains flows for [Node-RED](https://nodered.org/) which replicate the [Open AI API](https://platform.openai.com/docs/api-reference/introduction). This allows users to route requests to Open AI products through their own (or a hosted) Node-RED server, giving them full control over all requests.

Possible use cases could be:

* log any requests to the Open AI - either for reporting reasons or just to learn how other scripts (like [Auto-GPT](https://github.com/Significant-Gravitas/Auto-GPT) or [BabyAGI](https://github.com/yoheinakajima/babyagi)) use this API to reach their goals;
* don't give your Open AI API key to potentially dangerous scripts! Instead, add it to these flows only and configure your untrusted scripts to use these endpoints as a proxy;
* replace some (or all) requests to the Open AI API by your own implementations - e.g., based on other flows which use [LLaMA](https://github.com/rozek/node-red-flow-llama), [Stanford Alpaca](https://github.com/rozek/node-red-flow-alpaca), or GPT4All [filtered](https://github.com/rozek/node-red-flow-gpt4all-filtered) or [unfiltered](https://github.com/rozek/node-red-flow-gpt4all-unfiltered) or [GPT4All-J](https://github.com/rozek/node-red-flow-gpt4all-j) models.

In any case, this proxy gives you much more control over Open AI API requests with respect to

* data privacy,
* safety and
* costs.

![a small detail of the whole Open AI API replica](OpenAI-API_detail.png)

> Nota bene: this work is currently in progress, a first release is planned for monday, April 24th, 2023 - stay tuned.

## Installation ##

To install these flows, simply open the Flow Editor of your Node-RED server and import the contents of file [OpenAI-API.json](./OpenAI-API.json) - best into a new workspace.

## Usage ##

By default, any incoming request is logged into the Node-RED Flow Editor's debug pane and simply passed to the Open AI API.

![pre-implemented Open AI API Handlers](OpenAI-API-Handlers.png)

## Configuring Python Scripts to use this Proxy ##


## Credits ##

The Node-RED HTTP entry points are based on the [Open AI API documentation](https://platform.openai.com/docs/introduction) and an [OpenAPI specification for the Open AI API](https://github.com/openai/openai-openapi) (please use the [author's fork of that specification](https://github.com/rozek/openai-openapi) if you plan to create other clients from it as that fork contains updated installation instructions)

## License ##

[MIT License](LICENSE.md)
