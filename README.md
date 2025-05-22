# geography-site
<li>
  📄 <strong>New Topic Title</strong> — 
  <a href="docs/New_Document_Name.pdf" download>Download PDF</a>
</li>
<li>
  📄 <strong>Population Growth</strong> — 
  <a href="docs/Population_Growth.pdf" download>Download PDF</a>
</li>
<h3>Unit 2: Human Geography</h3>
<ul>
  <li>
    📄 <strong>Population Growth</strong> —
    <a href="docs/Population_Growth.pdf" download>Download PDF</a>
  </li>
  <li>
    📄 <strong>Migration Patterns</strong> —
    <a href="docs/Migration_Patterns.pdf" download>Download PDF</a>
  </li>
</ul>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Content Uploader (Offline Tool)</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 2rem;
      background: #f0f0f0;
    }

    h1 {
      color: #2c3e50;
    }

    label {
      display: block;
      margin: 1rem 0 0.3rem;
    }

    input, textarea, button {
      padding: 0.5rem;
      width: 100%;
      max-width: 500px;
      margin-bottom: 1rem;
    }

    #output {
      background: #fff;
      border: 1px solid #ccc;
      padding: 1rem;
      white-space: pre-wrap;
      font-family: monospace;
      max-width: 600px;
    }
  </style>
</head>
<body>
  <h1>Content Uploader Tool</h1>
  <p>This tool helps you generate HTML code to add documents to your website.</p>

  <label for="title">Document Title:</label>
  <input type="text" id="title" placeholder="e.g., Deforestation Trends">

  <label for="file">Choose Document:</label>
  <input type="file" id="file">

  <button onclick="generate()">Generate Code</button>

  <h3>HTML Snippet:</h3>
  <div id="output">(Your code will appear here)</div>

  <script>
    function generate() {
      const title = document.getElementById('title').value.trim();
      const fileInput = document.getElementById('file');
      const file = fileInput.files[0];

      if (!title || !file) {
        alert("Please enter a title and select a file.");
        return;
      }

      const filename = file.name;
      const html = `
<li>
  📄 <strong>${title}</strong> —
  <a href="docs/${filename}" download>Download PDF</a>
</li>`.trim();

      document.getElementById('output').textContent = html;
    }
  </script>
</body>
</html>
