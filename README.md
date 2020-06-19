# nginx-vod-module-prebuilt

This repository contains a single GitHub Actions script that build a dynamic module of [`nginx-vod-module`](https://github.com/kaltura/nginx-vod-module), together with [`nginx`](https://github.com/nginx/nginx) and [`ffmpeg`](https://github.com/FFmpeg/FFmpeg).

## Why?
I am a very amateur developer, and I do it for learning how to compile Nginx. I understand my current process may not be most efficient. If you spot any issue or want to give me suggestions, feel free to open a [PR](https://github.com/nixklai/nginx-vod-module-prebuilt/pulls)!

## How?
1. Enable `universe` repository with `sudo add-apt-repository universe`
2. Copy unzip the prebuilt in `/usr/share/nginx/modules/nginx-vod-module` (or other location), and create a file `/etc/nginx/modules-enabled/nginx-vod-module.conf` (or other name) with the following:
```
load_module modules/nginx-vod-module/ngx_http_vod_module.so;
```
3. Follow the rest of the set-up instruction of nginx-vod-module