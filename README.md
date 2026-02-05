<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>HireReady | Job Portal</title>

<style>
:root {
  --primary: #2563eb;
  --primary-dark: #1e40af;
  --bg: #f5f7fb;
  --card: #ffffff;
  --text: #1f2937;
  --muted: #6b7280;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Segoe UI", Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

/* Layout */
.container {
  width: 90%;
  max-width: 1100px;
  margin: auto;
}

.section {
  padding: 64px 0;
}

/* Navbar */
.navbar {
  background: #ffffff;
  border-bottom: 1px solid #e5e7eb;
  position: sticky;
  top: 0;
  z-index: 10;
}

.nav-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 14px 0;
}

nav a {
  margin-left: 18px;
  text-decoration: none;
  color: var(--text);
  font-size: 14px;
}

nav a:hover {
  color: var(--primary);
}

/* Buttons */
.btn {
  padding: 10px 18px;
  border-radius: 6px;
  text-decoration: none;
  font-size: 14px;
  display: inline-block;
}

.btn-primary {
  background: var(--primary);
  color: #fff;
}

.btn-primary:hover {
  background: var(--primary-dark);
}

/* Cards */
.card {
  background: var(--card);
  padding: 18px;
  border-radius: 10px;
  margin-top: 14px;
  border: 1px solid #e5e7eb;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.card:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.06);
}

/* Badges */
.badge {
  display: inline-block;
  background: #e0e7ff;
  color: #1e3a8a;
  padding: 4px 10px;
  border-radius: 999px;
  font-size: 12px;
  margin-right: 6px;
}

/* Grid helpers */
.grid-4 {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 18px;
}

.grid-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

/* Hero */
.hero {
  background: linear-gradient(135deg, #2563eb, #60a5fa);
  color: #ffffff;
  position: relative;
  overflow: hidden;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  align-items: center;
  min-height: 420px;
}

.hero h1 {
  font-size: 38px;
  margin-bottom: 12px;
}

.hero p {
  color: #e5edff;
  margin-bottom: 22px;
  max-width: 420px;
}

/* Hero art */
.circle {
  width: 260px;
  height: 260px;
  background: rgba(255,255,255,0.18);
  border-radius: 50%;
  position: absolute;
  right: 8%;
  top: 18%;
}

.mini-card {
  width: 200px;
  position: relative;
  background: #ffffff;
  color: var(--text);
}

/* Jobs layout */
.jobs-layout {
  display: grid;
  grid-template-columns: 1fr 3fr;
  gap: 24px;
}

/* Auth */
.auth-box {
  max-width: 420px;
  margin: auto;
}

input {
  width: 100%;
  padding: 10px 12px;
  margin: 10px 0;
  border-radius: 6px;
  border: 1px solid #d1d5db;
}

/* Footer */
.footer {
  background: #ffffff;
  border-top: 1px solid #e5e7eb;
  text-align: center;
  padding: 24px;
  font-size: 14px;
  color: var(--muted);
}

/* Responsive */
@media (max-width: 768px) {
  .hero-grid,
  .grid-4,
  .grid-3,
  .jobs-layout {
    grid-template-columns: 1fr;
  }

  .hero h1 {
    font-size: 30px;
  }
}
</style>
</head>

<body>

<!-- NAVBAR -->
<header class="navbar">
  <div class="container nav-flex">
    <strong>HireReady</strong>
    <nav>
      <a href="#home">Home</a>
      <a href="#jobs">Jobs</a>
      <a href="#company">Companies</a>
      <a href="#login" class="btn btn-primary">Sign In</a>
    </nav>
  </div>
</header>

<!-- HERO -->
<section class="hero" id="home">
  <div class="container hero-grid">
    <div>
      <h1>Build your career with the right opportunity</h1>
      <p>
        HireReady helps professionals discover roles that match their skills,
        experience, and career goals.
      </p>
      <a class="btn btn-primary">Explore Jobs</a>
    </div>

    <div>
      <div class="circle"></div>
      <div class="card mini-card">
        Frontend Developer<br />
        <small class="badge">₹8–12 LPA</small>
      </div>
      <div class="card mini-card">
        Backend Engineer<br />
        <small class="badge">₹10–15 LPA</small>
      </div>
    </div>
  </div>
</section>

<!-- FEATURED COMPANIES -->
<section class="section container">
  <h3>Featured companies hiring on HireReady</h3>
  <div class="grid-4">
    <div class="card">Google</div>
    <div class="card">Amazon</div>
    <div class="card">Microsoft</div>
    <div class="card">Netflix</div>
  </div>
</section>

<!-- JOBS -->
<section class="section container" id="jobs">
  <h3>Latest job openings</h3>

  <div class="jobs-layout">
    <aside class="card">
      <strong>Filters</strong>
      <p style="color:#6b7280; font-size:14px; margin-top:8px;">
        Location, experience, salary range
      </p>
    </aside>

    <div>
      <div class="card">
        <h4>Frontend Developer</h4>
        <p style="color:#6b7280;">Bangalore · Full-time</p>
        <p><strong>₹8–12 LPA</strong></p>
        <span class="badge">HTML</span>
        <span class="badge">CSS</span>
        <span class="badge">Responsive UI</span>
      </div>

      <div class="card">
        <h4>Backend Developer</h4>
        <p style="color:#6b7280;">Hyderabad · Full-time</p>
        <p><strong>₹10–15 LPA</strong></p>
        <span class="badge">Java</span>
        <span class="badge">SQL</span>
        <span class="badge">APIs</span>
      </div>
    </div>
  </div>
</section>

<!-- LOGIN -->
<section class="section container" id="login">
  <div class="auth-box card">
    <h3>Sign in to your account</h3>
    <input type="email" placeholder="Email address" />
    <input type="password" placeholder="Password" />
    <label style="font-size:14px;">
      <input type="checkbox" /> Remember me
    </label><br /><br />
    <button class="btn btn-primary">Sign In</button>
  </div>
</section>

<!-- COMPANY -->
<section class="section container" id="company">
  <h3>Company profile</h3>
  <div class="card">
    <h4>Google</h4>
    <p style="color:#6b7280;">
      Technology company focused on search, cloud, and AI solutions.
    </p>
    <p><strong>Industry:</strong> Information Technology</p>
    <p><strong>Founded:</strong> 1998</p>
    <p><strong>Employees:</strong> 100,000+</p>

    <h5 style="margin-top:16px;">Open positions</h5>
    <div class="card">Frontend Developer</div>
  </div>
</section>

<footer class="footer">
  © 2026 HireReady · Designed for academic project use
</footer>

</body>
</html>
