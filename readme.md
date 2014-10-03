# DigitalOcean Droplet Concept

These are my thoughts on what it should and could look like for a user to create a DigitalOcean Droplet.

### Setup

My local development process may seem over the top but running a few simple scripts will run

- Jekyll Server (watching for updates)
- Compass Watch compiling sass
- LiveReload

### LiveReload Browser Plugins
- **[Safari extension ](http://download.livereload.com/2.0.9/LiveReload-2.0.9.safariextz)** — 2.0.9 Note: due to Safari API limitations, browser extension does not work with file: URLs; if you're working with local files via file: URL, please use Chrome or insert the snippet
- **[Chrome extension](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei)** on the Chrome Web Store — if you want to use it with local files, be sure to enable “Allow access to file URLs” checkbox in Tools > Extensions > LiveReload after installation.
- **[Firefox extension](http://download.livereload.com/2.0.8/LiveReload-2.0.8.xpi)** 2.0.8

### Setting up development:

Set up your machine (using bundler) to run the jekyll server and gems needed to run it well:
```
script/bootstrap
```  

Run that server:

```
script/sever
```  
