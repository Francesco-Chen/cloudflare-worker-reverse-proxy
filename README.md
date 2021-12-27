# cloudflare-worker-reverse-proxy

Reverse proxy a web page using Cloudflare worker.

### How to use:
copy and insert your hostname that you want to do reverse proxy on Cloudflare worker

```js
addEventListener(
	"fetch",event => {
		let url=new URL(event.request.url);
		url.hostname="";
		let request=new Request(url,event.request);
		event. respondWith(
			fetch(request)
		)
	}
)
```

![alt text](Screenshot.png)
