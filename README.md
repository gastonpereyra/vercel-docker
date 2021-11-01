# Vercel + Docker

![template](https://user-images.githubusercontent.com/39351850/139603463-31eba860-db3f-48cd-b9f6-918dc95d13ae.png)

---

The idea 💡 is to keep the files somewhere with easy access, and let open to everyone to colaborate.

> ❕ **IMPORTANT** I will call _"service"_ to some project/repository deploy in 🔼 [Vercel](https://vercel.com)

## Intro

When you are using 🔼 [Vercel](https://vercel.com) to create "service", it is easy, is simple, is automatic in most cases. They offers not only multiple templates, especially for frontend projects, and has his own CLI with multiple options.

Using the CLI is useful to develop in local, it link the local service with the deployed, for example use the env variables.

## Problem

When it's about a frontend project nothing happens..

When it's about a backend proeject, a **REST API** for example, at first is wondefull.. If you wanted to deploy multiple "services" which interact can used `--listen` option to setup different ports, Ok!.

> ❔ **What happened if you wanted to use different accounts?**

Well, you must login with the different accounts each time, or use `--token` option to start the local Env.

> ❕ **IMPORTANT** You can setup a token in Vercel to login, can do it [here](https://vercel.com/account/tokens)

But.. wait..

> ❔ **Why you must use different accounts?**

Well, if you are in a team and don't want or cannot paid for a Team account, or colaborators in Vercel. You can create a main account in Github, to use it as a single user, only must give access to everybody to push branches and manage that account. So you have a Free-Account for a Team.

> ❔ **What happened if you have different dependencies, like databases?**

## Solution

Docker is a great in this cases, write a docker-compose file, add every service necesary, like Mongodb, and develop it.

Also Works with everyelse.. incluiding to keep the Token in Secret.

So, with Docker, we can have serveral "services", with differents tokens (for different accounts), and several differents ports, with databases (or whatever we need).. and develop in Vercel.

To see more, look en [`/example`]('https://github.com/gastonpereyra/vercel-docker/tree/main/example') folder.

