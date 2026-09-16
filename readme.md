# samajammin.com (archived)

> **This site is no longer online.** The `samajammin.com` domain is no longer
> registered and the content is no longer pinned to IPFS, so the links and
> commands below will not resolve.
>
> My current site is **[samrichards.dev](https://samrichards.dev/)**.
>
> This repo is kept public as a historical reference — the IPFS walkthrough
> still holds up if you want to publish a static site the same way.

This was my personal website: a simple, static site hosted on
[IPFS](https://ipfs.io/) via
[Cloudflare's gateway](https://www.cloudflare.com/distributed-web-gateway/).

## Deploy your own site to IPFS

1. [Download IPFS](https://docs.ipfs.io/introduction/install/#installing-from-a-prebuilt-package)

2. Connect your local IPFS node to the network

```
ipfs daemon
```

3. Add your content to IPFS

```
ipfs add -r /path/to/folder-with-your-content
```

That's about it! Read [this excellent walkthrough](https://developers.cloudflare.com/distributed-web/ipfs-gateway/connecting-website/) for detailed instructions, including how to set up a custom domain and SSL.

## Be a benevolent peer

One advantage of IPFS is that the more popular the content, the faster it will load. The more any content is shared across nodes, the more peer nodes that can serve it to our browsers.

If you add IPFS sites to your own node, you help the IPFS community!

Follow these steps, substituting a site that is actually published:

```
cd ~/ && mkdir ipfs-files # Create folder to download ipfs content
cd ipfs-files
ipfs get /ipns/<the-site-you-want-to-pin>
ipfs add -r <the-site-you-want-to-pin>
```

Thanks for your contribution to the peer-to-peer revolution :)
