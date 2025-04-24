<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Media Gallery</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header><h1>My Media Gallery</h1></header>
  <main>
    <section id="gallery">
      <h2>Photos</h2>
      <div class="media-grid" id="photoGrid"></div>

      <h2>Videos</h2>
      <div class="media-grid" id="videoGrid"></div>
    </section>
  </main>
  <footer>&copy; 2025 My Media Gallery</footer>
  <script src="script.js"></script>
</body>
</html>
document.addEventListener("DOMContentLoaded", () => {
  const photoGrid = document.getElementById("photoGrid");
  const videoGrid = document.getElementById("videoGrid");

  const photos = [
    "https://via.placeholder.com/300x200.png?text=Photo+1",
    "https://via.placeholder.com/300x200.png?text=Photo+2"
  ];

  const videos = [
    "https://www.w3schools.com/html/mov_bbb.mp4",
    "https://www.w3schools.com/html/movie.mp4"
  ];

  photos.forEach(src => {
    const img = document.createElement("img");
    img.src = src;
    photoGrid.appendChild(img);
  });

  videos.forEach(src => {
    const video = document.createElement("video");
    video.src = src;
    video.controls = true;
    videoGrid.appendChild(video);
  });
});
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #f9f9f9;
  color: #333;
}

header {
  background: #222;
  color: white;
  padding: 1rem;
  text-align: center;
}

.media-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1rem;
  padding: 1rem;
}

.media-grid img, .media-grid video {
  width: 100%;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

footer {
  background: #eee;
  text-align: center;
  padding: 1rem;
  margin-top: 2rem;
}
