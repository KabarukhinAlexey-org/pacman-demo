# pacman-canvas

An old classic, re-written in HTML5.
Visit http://pacman.platzh1rsch.ch to see it live.

Sounds from
http://soundfxcenter.com/ and http://soundfxnow.com/

![Alt text](img/game.jpg?raw=true "Game")

---

# License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/platzhersh/pacman-canvas">pacman-canvas</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/platzhersh">Platzh1rsch</a> is marked with <a href="LICENSE.md" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC0 1.0 Universal<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/zero.svg?ref=chooser-v1"></a></p>

# Get started

1. Build dockerfile with command "podman build -t pacman ."
2. Run container with the command "podman run -d -p 8080:8080 pacman"
3. Enjoy the game =)
4. Change color of the wall:
  Edit file "pacman-canvas.js": Line 538: Change wall color from "Blue" to "Red"
5. Rebuild and recreate the container and see the changes.  

---

