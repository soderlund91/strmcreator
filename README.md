This code is created with the use of ChatGPT, and it may therefore be some buggs. 
I'm no coder so i'm lacking the ability to streamline the code.

I made this for my own use and my specific needs, feel free to use and develop!

======HOW TO USE======



```
services:
  strm-creator:
    image: soderlund91/strm-creator:latest
    container_name: strm-creator
    ports:
      - "8585:8000"
    volumes:
      - ./config:/config
      - ./data:/data
      - ./media:/media
    restart: unless-stopped
```



Web UI at
```
http://localhost:8585/ui
```
