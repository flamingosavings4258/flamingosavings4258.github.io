<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>GD YouTuber Stats Viewer</title>
  <style>
    body {
      font-family: Arial;
      background: #111;
      color: white;
      text-align: center;
    }
    input, button {
      padding: 10px;
      margin: 10px;
      font-size: 16px;
    }
    .video {
      margin: 15px;
      display: inline-block;
    }
    img {
      width: 200px;
      border-radius: 10px;
    }
  </style>
</head>
<body>

<h1>GD YouTuber Stats</h1>

<input id="UCZ5Crenfm9hAt5PgXjZMx9w" placeholder="Enter Channel ID">
<button onclick="loadChannel()">Load</button>

<div id="stats"></div>

<h2>Videos</h2>
<div id="videos"></div>

<h2>Shorts</h2>
<div id="shorts"></div>

<script>
const API_KEY = "512289810144-8vsb49m66je8005bb3kvhaensc041m3q.apps.googleusercontent.com";

async function loadChannel() {
  const channelId = document.getElementById("channelId").value;

  // Get channel stats
  const statsRes = await fetch(
    `https://www.googleapis.com/youtube/v3/channels?part=statistics,snippet&id=${channelId}&key=${API_KEY}`
  );
  const statsData = await statsRes.json();

  const channel = statsData.items[0];

  document.getElementById("stats").innerHTML = `
    <h2>${channel.snippet.title}</h2>
    <p>Subscribers: ${channel.statistics.subscriberCount}</p>
    <p>Views: ${channel.statistics.viewCount}</p>
    <p>Videos: ${channel.statistics.videoCount}</p>
  `;

  // Get uploads playlist
  const uploadsId = channel.contentDetails?.relatedPlaylists?.uploads;

  const videoRes = await fetch(
    `https://www.googleapis.com/youtube/v3/search?key=${API_KEY}&channelId=${channelId}&part=snippet,id&order=date&maxResults=20`
  );
  const videoData = await videoRes.json();

  const videosDiv = document.getElementById("videos");
  const shortsDiv = document.getElementById("shorts");

  videosDiv.innerHTML = "";
  shortsDiv.innerHTML = "";

  for (let vid of videoData.items) {
    if (!vid.id.videoId) continue;

    const videoId = vid.id.videoId;

    // Get duration
    const detailsRes = await fetch(
      `https://www.googleapis.com/youtube/v3/videos?part=contentDetails&id=${videoId}&key=${API_KEY}`
    );
    const detailsData = await detailsRes.json();

    const duration = detailsData.items[0].contentDetails.duration;

    const isShort = duration.includes("S") && !duration.includes("M");

    const html = `
      <div class="video">
        <a href="https://youtube.com/watch?v=${videoId}" target="_blank">
          <img src="${vid.snippet.thumbnails.medium.url}">
        </a>
        <p>${vid.snippet.title}</p>
      </div>
    `;

    if (isShort) {
      shortsDiv.innerHTML += html;
    } else {
      videosDiv.innerHTML += html;
    }
  }
}
</script>

</body>
</html>
