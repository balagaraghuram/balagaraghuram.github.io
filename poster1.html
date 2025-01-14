<?php
session_start();

/**********************************************
 * Initialize the session storage for comments
 **********************************************/
if (!isset($_SESSION['comments'])) {
    $_SESSION['comments'] = [];
}

// This flag will be used to trigger the “New Year Poster” display in JavaScript.
$showPoster = false;

/****************************************************
 * Handle Form Submission (via POST)
 ****************************************************/
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $comment = trim($_POST['comment'] ?? '');
    if (!empty($comment)) {
        // Store comment in session
        $_SESSION['comments'][] = $comment;
        // Set flag so JS shows the poster for 1 minute
        $showPoster = true;
    }
}
?>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>view the poster and share your comments!</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      background-color: #f4f4f9;
    }
    h1 {
      margin-bottom: 20px;
    }
    /* PDF Poster Styles (smaller viewer) */
    .poster-container {
      margin-bottom: 20px;
    }
    .poster-container embed {
      display: block;
      width: 100%;
      height: 500px; /* Adjust this height for a smaller/bigger PDF view */
      border: none;
      border-radius: 8px;
    }
    #pdf-fallback {
      display: none;
      text-align: center;
      margin-top: 10px;
    }

    /* Comments Section Styles */
    .comments-section {
      margin-top: 20px;
      max-width: 600px;
    }
    .comments-section h2 {
      margin-bottom: 10px;
    }
    .comments-list {
      list-style: none;
      padding: 0;
      border: 1px solid #ddd;
      border-radius: 8px;
      margin-bottom: 10px;
    }
    .comments-list li {
      background: #f9f9f9;
      margin: 10px;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ddd;
    }

    /* Comment Form */
    .comment-form {
      display: flex;
      flex-direction: column;
      margin-bottom: 10px;
    }
    textarea {
      width: 100%;
      height: 80px;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ddd;
      resize: none;
      font-size: 14px;
      margin-bottom: 10px;
    }
    button {
      width: 120px;
      padding: 8px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      background: #007bff;
      color: #fff;
      font-size: 14px;
    }
    button:disabled {
      background: #ccc;
      cursor: not-allowed;
    }
    .note {
      font-size: 13px;
      color: #555;
    }
    .confirmation {
      margin-top: 15px;
      font-weight: bold;
      color: green;
    }

    /* Happy New Year Poster Styles */
    #new-year-poster {
      display: none; /* Will be displayed dynamically with JS */
      margin-top: 20px;
      text-align: center;
    }
    #new-year-poster img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
    }
  </style>
</head>
<body>
  <!-- Page Title -->
  <h1>view the poster and share your comments!</h1>

  <!-- Poster (PDF) Below the Title -->
  <div class="poster-container">
    <embed 
      src="https://github.com/balagaraghuram/balagaraghuram.github.io/blob/main/hospital%20admission%20and%20weather%20activity%20dashboard.pdf?raw=true" 
      type="application/pdf"
      onerror="document.getElementById('pdf-fallback').style.display='block'">
    <!-- Fallback if PDF doesn't load -->
    <p id="pdf-fallback">
      Your browser does not support displaying PDFs. 
      <a href="https://github.com/balagaraghuram/balagaraghuram.github.io/blob/main/hospital%20admission%20and%20weather%20activity%20dashboard.pdf?raw=true" target="_blank">
        Click here to download the poster.
      </a>
    </p>
  </div>

  <!-- Accessible Comments Section -->
  <div class="comments-section">
    <h2>Accessible Comments</h2>
    
    <!-- Display existing comments -->
    <ul class="comments-list">
      <?php if (!empty($_SESSION['comments'])): ?>
        <?php foreach ($_SESSION['comments'] as $cmt): ?>
          <li><?= htmlspecialchars($cmt) ?></li>
        <?php endforeach; ?>
      <?php else: ?>
        <li style="background: #fff; border: none; margin: 10px;">
          No comments yet.
        </li>
      <?php endif; ?>
    </ul>

    <!-- Comment Form -->
    <!-- For testing, the form is always enabled. 
         To disable after first comment, 
         you can check if comments already exist and hide/disable accordingly. -->
    <form method="POST" class="comment-form">
      <textarea name="comment" placeholder="Enter your comment..."></textarea>
      <button type="submit">Submit Comment</button>
    </form>

    <div class="note">
      The comments will be converted in the accessible format for visually challenged as per W3C guidelines
    </div>

    <!-- Confirmation Message -->
    <div id="confirmation" class="confirmation" style="display:none;">
      Thank you for the comments and Happy New Year 2025
    </div>
  </div>

  <!-- Happy New Year Poster (displayed on submit for 1 minute) -->
  <div id="new-year-poster">
    <img 
      src="https://github.com/balagaraghuram/balagaraghuram.github.io/blob/main/happy%20new%20year1.png?raw=true" 
      alt="Happy New Year 2025 Poster"
    />
  </div>

  <script>
    // In PHP, we set $showPoster = true if a new comment was just submitted.
    var showPoster = <?php echo ($showPoster ? 'true' : 'false'); ?>;

    if (showPoster) {
      // 1) Display confirmation message
      document.getElementById('confirmation').style.display = 'block';
      // 2) Display the poster for 1 minute
      var newYearPoster = document.getElementById('new-year-poster');
      newYearPoster.style.display = 'block';
      setTimeout(function() {
        newYearPoster.style.display = 'none';
      }, 60000); // 1 minute = 60,000 ms
    }
  </script>
</body>
</html>
