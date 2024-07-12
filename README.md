# Music Player (With Play & Pause Functionality)
Language Uses: HTML, CSS, JAVASCRIPT
## ScreenShots
![Main Music Player](https://github.com/user-attachments/assets/480be9f4-f825-4786-bd06-6f4bcbf0331b)
![Ss](https://github.com/user-attachments/assets/09c32890-10cc-4c59-9a6b-3ed45914323e)

JavaScript Code For User Interaction 👨‍💻
```javascript
<script>
      let progress = document.getElementById("progress");
      let song = document.getElementById("song");
      let ctrlIcon = document.getElementById("ctrlIcon");

      song.onloadedmetadata = function () {
        progress.max = song.duration;
        progress.value = song.currentTime;
      };

      function playPause() {
        if (ctrlIcon.classList.contains("fa-pause")) {
          song.pause();
          ctrlIcon.classList.remove("fa-pause");
          ctrlIcon.classList.add("fa-play");
        } else {
          song.play();
          ctrlIcon.classList.add("fa-pause");
          ctrlIcon.classList.remove("fa-play");
        }
      };

      if (song.play()) {
        setInterval(() => {
          progress.value = song.currentTime;
        }, 500);
      };
      progress.onchange = function () {
        song.play();
        song.currentTime = progress.value;
        ctrlIcon.classList.add("fa-pause");
        ctrlIcon.classList.remove("fa-play");
      };
    </script>
```
## Check Out The Website 👇

Visit The Website🌐 [Music Player](https://shayanshahdeveloper.github.io/Project-2-Music-Player/)

## Developed By Shayan Shah
Social media Handles 👉
[Linkdin](https://www.linkedin.com/in/shayan-shah-b31439296/)


