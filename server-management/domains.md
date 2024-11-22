---
description: Want a custom server address/IP? Look no further!
---

# Domains

### Introduction

By purchasing a domain, you can make your server look more professional and make its connection details far easier to remember! The list of recommended domain registrars are as follows:

[Cloudflare](https://www.cloudflare.com/products/registrar/) | [GoDaddy](https://www.godaddy.com/) | [Namecheap](https://www.namecheap.com) | [Porkbun](https://porkbun.com)

However, the guide below will be using **Cloudflare**'s terminology.

### A Record Setup

Once you have purchased your domain, head over to your registrar and add a new DNS record while selecting `A Record`. Then, put any value in the box under `Name` and put in the server's numerical IP as the `value` it will point to. Remember to leave TTL to `automatic`. If you're using Cloudflare, remember to turn the proxy status (orange cloud) off. That's all! Just wait a while until the DNS propagates and you'll be able to join your server with your very own subdomain!

{% hint style="info" %}
**Subdomains**

The word you choose to put in the `Name` section will decide your subdomain. If you owned `minecraftserver.com`, and you put the word `play` in the `host` box, your subdomain that players can use connect to your server would then be `play.minecaftserver.com`.
{% endhint %}

### SRV Record Setup

Alternatively, if you do not have a dedicated IP, you can follow these steps. Follow the setup instructions above first to setup `A Record`, then add a new DNS record and select `SRV`. Your service should be `_minecraft`, the protocol `TCP`, TTL on `auto`, and priority and weight `0`. Replace the port field with the port that your server uses, and replace the target field with the subdomain/domain your server uses - it should be what you set the `A Record` to be. You're finished! Now you should be able to connect to your server using `anything.example.domainending` - you will also no longer need the port when connecting.

### Ember Host Subdomain

If you do not want to purchase a domain to customise your server join address, you can still do it for free by using our subdomains feature directly in our [panel](https://panel.ember.host)! Simply head to the subdomains section on the sidebar and type in whatever you want to let players to connect with (`xxx.emberhost.net`).

By `@icewaffles`
