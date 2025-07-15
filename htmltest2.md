<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Test Page</title>
  <style>
    .container { padding: 20px; background: #f0f0f0; }
    .header, .footer { background: #ccc; padding: 10px; }
    .content { display: flex; gap: 20px; }
    .sidebar { width: 200px; background: #ddd; }
    .main { flex: 1; background: #fff; padding: 10px; }
    .card { margin-bottom: 15px; border: 1px solid #aaa; padding: 10px; }
    .title { font-weight: bold; }
    .button { padding: 5px 10px; background: blue; color: white; border: none; }
  </style>
</head>
<body>
  <div class="container">
    <div class="header">
      <div class="nav">
        <div class="nav-item">Home</div>
        <div class="nav-item">About</div>
        <div class="nav-item">Contact</div>
      </div>
    </div>
    <div class="content">
      <div class="sidebar">
        <div class="menu">
          <div class="menu-item">Dashboard</div>
          <div class="menu-item">Settings</div>
          <div class="menu-item">Profile</div>
        </div>
      </div>
      <div class="main">
        <div class="card">
          <div class="title">Card Title 1</div>
          <div class="description">This is the description for card 1.</div>
          <button class="button">Click Me</button>
        </div>
        <div class="card">
          <div class="title">Card Title 2</div>
          <div class="description">Another description here.</div>
          <div class="actions">
            <button class="button">OK</button>
            <button class="button">Cancel</button>
          </div>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="footer-content">© 2025 My Website</div>
    </div>
  </div>
</body>
</html>
