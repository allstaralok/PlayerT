# player.html
One file drop-in video player web app for using MP4 video files served using basic directory listing.

![player.html in action](https://user-images.githubusercontent.com/455424/86303837-de3f6400-bbc1-11ea-8688-7eadc0f1c4d9.jpg)
![player.html on all of your devices](https://user-images.githubusercontent.com/455424/86303229-1645a780-bbc0-11ea-80c9-bc6e099dccd6.jpg)

## Usage
`player.html` is designed to be a drop-in video player that does not require any configuration or other files.

To use it copy the [`./src/player.html`](src/player.html) file into a folder that is served over HTTP using the web server's folder listing functionality. `player.html` basically uses the folder listing as an API for enumerating the files and folders. It should work with almost any web server, but it has only be tested against NGINX, Apache, and IIS.

### Supported features

* Only 1 file with zero external dependencies
* [`SVG images`](https://github.com/microsoft/fluentui-system-icons/) are inlined as data URIs
* May be installed as a PWA (Progressive Web App) app. Dynamically generated inline data URI manifest file.
* Playback of MP4, M4V, MKV, WEBM, and OGG files using the browser video engine
* Sharable URL that will load `player.html` in the same folder location, and video position
* Jump forward/backward 15 seconds
* Video thumbnail generation, with concurrency configuration (default 1)
* Thumbnail caching using localStorage
* Social media metadata (og:\*, twitter:\*)

### Supported Web Servers

* NGINX ([`autoindex`](https://nginx.org/en/docs/http/ngx_http_autoindex_module.html) on)
* Apache ([`mod_autoindex`](https://cwiki.apache.org/confluence/display/HTTPD/DirectoryListings))
* IIS (enable [`Directory Browsing`](https://docs.microsoft.com/en-us/iis/configuration/system.webserver/directorybrowse))

## License

* [MIT](./LICENSE)

&copy; 2020 Paul Ellis
