# aliaelmeligy.GitHub.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Information Representation & Processing</title>

<style>
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: "Poppins", sans-serif; }

  body {
    background: #fff1f7;
    color: #222;
    transition: background 0.3s, color 0.3s;
  }

  .dark-mode {
    background: #1a0b12;
    color: #fce7f3;
  }

  a { text-decoration: none; }

  /* HEADER */
  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 26px;
    background: linear-gradient(135deg, #ec4899, #f472b6);
    color: white;
    box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  }

  header h1 {
    font-size: 28px;
    font-weight: 700;
  }

  #modeToggle {
    padding: 10px 16px;
    background: white;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    font-weight: 600;
    color: #db2777;
    transition: 0.3s;
  }

  #modeToggle:hover { transform: scale(1.05); }

  /* HERO */
  .hero {
    max-width: 1200px;
    margin: 40px auto;
    padding: 24px;
    display: flex;
    gap: 30px;
    align-items: center;
  }

  .hero img {
    width: 340px;
    border-radius: 16px;
    box-shadow: 0 6px 20px rgba(0,0,0,0.15);
  }

  .hero-text h2 {
    font-size: 32px;
    margin-bottom: 12px;
    color: #be185d;
  }

  .hero-buttons { margin-top: 18px; display: flex; gap: 10px; }

  .btn {
    background: #ec4899;
    padding: 10px 18px;
    color: white;
    border-radius: 8px;
    font-weight: 600;
    transition: 0.3s;
  }

  .btn:hover { transform: translateY(-4px); }

  /* GRID */
  .grid {
    max-width: 1200px;
    margin: 26px auto;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
    padding: 20px;
  }

  .card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    transition: 0.3s;
  }

  .card:hover { transform: translateY(-6px); }

  .card img {
    width: 100%;
    height: 160px;
    object-fit: cover;
  }

  .card .content {
    padding: 16px;
  }

  .content h3 {
    font-size: 20px;
    margin-bottom: 8px;
    color: #be185d;
  }

  .content p { opacity: 0.85; }

  .content .links {
    margin-top: 14px;
    display: flex;
    gap: 10px;
  }

  /* SECTIONS */
  section {
    max-width: 1100px;
    margin: 40px auto;
    padding: 20px;
    background: white;
    border-radius: 12px;
    border-left: 6px solid #ec4899;
    box-shadow: 0 6px 20px rgba(0,0,0,0.06);
  }

  section h2 {
    font-size: 26px;
    margin-bottom: 10px;
    color: #be185d;
  }

  section ul { margin-top: 10px; padding-left: 20px; }

  /* FOOTER */
  footer {
    text-align: center;
    margin: 40px 0 20px;
    font-size: 14px;
    opacity: 0.7;
  }

	audio{
		align-items: center;
	}
</style>
</head>

<body>

<header>
  <h1>Information Representation & Processing</h1>
  <button id="modeToggle">Dark Mode</button>
</header>

<div class="hero">
  <div class="hero-text">
    <h2>Welcome to IRP Homepage</h2>
    <p>
      Explore how computers represent audio, images, and video through sampling,
      bit depth, pixels, digital conversion, and compression.
    </p>

    <div class="hero-buttons">
      <a href="#audio" class="btn">Audio</a>
      <a href="#visual" class="btn">Visual</a>
      <a href="#video" class="btn">Video</a>
    </div>
  </div>

  <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?w=900&q=80" />
</div>

<div class="grid">
  <div class="card">
    <img src="https://images.unsplash.com/photo-1502920917128-1aa500764b6b?w=1200&q=80" />
    <div class="content">
      <h3>Audio Representation</h3>
      <p>Sampling, ADC, bit depth, frequency & digital audio systems.</p>
      <div class="links">
        <a href="#audio" class="btn">Read</a>
        <a href="https://en.wikipedia.org/wiki/Sampling_(signal_processing)" target="_blank" class="btn" style="background:#f472b6;">Wiki</a>
      </div>
    </div>
  </div>
	
  <div class="card">
    <img src="https://images.unsplash.com/photo-1504198453319-5ce911bafcde?w=1200&q=80" />
    <div class="content">
      <h3>Image Representation</h3>
      <p>Pixels, color depth, raster graphics & compression.</p>
      <div class="links">
        <a href="#visual" class="btn">Read</a>
        <a href="https://en.wikipedia.org/wiki/Raster_graphics" target="_blank" class="btn" style="background:#f472b6;">Wiki</a>
      </div>
    </div>
  </div>

  <div class="card">
    <img src="https://images.unsplash.com/photo-1581091215367-6b3a9d39b5b9?w=1200&q=80" />
    <div class="content">
      <h3>Video Representation</h3>
      <p>Frames, resolution, codecs, and digital video encoding.</p>
      <div class="links">
        <a href="#video" class="btn">Read</a>
        <a href="https://en.wikipedia.org/wiki/Video_compression" target="_blank" class="btn" style="background:#f472b6;">Wiki</a>
      </div>
    </div>
  </div>
</div>

<section id="audio">
  <h2>Audio Representation</h2>
  <ul>
    <li>Sound is a continuous wave → must be digitized.</li>
    <li>ADC samples the wave at regular intervals.</li>
    <li>Sampling rate: samples per second (e.g., 44.1 kHz).</li>
    <li>Bit depth: bits per sample (8-bit, 16-bit, 24-bit).</li>
    <li>Higher rate/depth → higher quality + larger file size.</li>
  </ul>
</section>
	
	<audio controls autoplay muted>
  <source src="audio.mp3" type="audio/ogg">
  Your browser does not support the audio element.
</audio>

<section id="visual">
  <h2>Image Representation</h2>
  <ul>
    <li>Images consist of small squares called pixels.</li>
    <li>Color depth determines how many colors the image can show.</li>
    <li>JPEG uses lossy compression; PNG uses lossless.</li>
    <li>Resolution = height × width (e.g., 1080×1920).</li>
  </ul>
</section>

<section id="video">
  <h2>Video Representation</h2>
  <ul>
    <li>Video = sequence of frames shown quickly.</li>
    <li>Frame rate: 24fps, 30fps, 60fps.</li>
    <li>Codecs reduce file size (H.264, VP9, HEVC).</li>
    <li>Resolutions: 720p, 1080p, 4K.</li>
  </ul>
</section>
	
	<video width="450" controls>
  <source src="video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<footer>
  © 2025 IRP Homepage — Pink Edition for Alia 💗  
</footer>

<script>
  const toggle = document.getElementById("modeToggle");

  toggle.addEventListener("click", () => {
    document.body.classList.toggle("dark-mode");

    toggle.textContent = 
      document.body.classList.contains("dark-mode")
      ? "Light Mode"
      : "Dark Mode";
  });
</script>

</body>
</html>
