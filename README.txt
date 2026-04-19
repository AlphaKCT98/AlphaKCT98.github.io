<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Self-assessment quiz about web servers and HTTP.">
  <title>Web Servers and HTTP | Quiz</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body id="top">
<!-- I kept the skip link near the top because I think it makes the page easier to use for keyboard navigation. -->
  <a class="skip-link" href="#main-content">Skip to main content</a>
  <!-- This header stays the same on every page so the site feels connected and easier to move through. -->
  <header class="site-header">
    <div class="header-inner">
      <div class="branding">
        <a id="site-title" href="index.html">Web Servers and HTTP</a>
        <p>Intro to Web Development class project</p>
      </div>
	  <!-- Main navigation stays consistent on every page -->
      <nav class="site-nav" aria-label="Main navigation">
        <ul>
          <li><a href="index.html">Home</a></li>
          <li><a href="how-it-works.html">How It Works</a></li>
          <li><a href="http-evolution.html">HTTP Evolution</a></li>
          <li><a href="web-servers.html">Web Servers</a></li>
          <li><a href="key-concepts.html">Key Concepts</a></li>
          <li><a href="quiz.html" class="active">Quiz</a></li>
          <li><a href="references.html">References</a></li>
          <li><a href="about.html">About</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- The quiz form lives in the main area, and the results section stays hidden until JavaScript fills it in after submission. -->
  <main id="main-content" class="page-shell">
    <section class="hero">
      <p class="eyebrow">Self-assessment page</p>
      <h1>Self-Assessment Quiz</h1>
      <p class="subhead">Use this quiz to check how well you understand the main ideas from the site. It includes a fill-in-the-blank question, single-answer multiple-choice questions, and one multi-selection question.</p>
    </section>

    <section class="page-section two-column quiz-layout">
      <article class="content-card">
        <div class="section-heading">
          <h2>Before you start</h2>
          <p>This page is meant to work like a study check, not a trick test.</p>
        </div>
        <ul>
          <li>Read each question carefully before answering.</li>
          <li>Questions 2 through 5 use radio buttons because only one answer is correct.</li>
          <li>Question 6 uses checkboxes because more than one answer is correct.</li>
          <li>Your results will appear on the same page right after you submit the quiz.</li>
        </ul>
      </article>

      <article class="content-card">
        <div class="section-heading">
          <h2>Quick study guide</h2>
          <p>Review these pages if you want a refresher first.</p>
        </div>
        <div class="study-grid">
          <div class="study-card">
            <h3>Need the request cycle?</h3>
            <p><a href="how-it-works.html">Read How It Works</a></p>
          </div>
          <div class="study-card">
            <h3>Need version history?</h3>
            <p><a href="http-evolution.html">Read HTTP Evolution</a></p>
          </div>
          <div class="study-card">
            <h3>Need server roles?</h3>
            <p><a href="web-servers.html">Read Web Servers</a></p>
          </div>
          <div class="study-card">
            <h3>Need definitions?</h3>
            <p><a href="key-concepts.html">Read Key Concepts</a></p>
          </div>
        </div>
      </article>
    </section>
	<!-- Quiz form starts here -->
    <!-- The form uses fieldsets to group questions, which I think makes the quiz feel cleaner and easier to follow. -->

    <form id="quiz-form" class="quiz-form" novalidate>
      <fieldset class="quiz-fieldset">
        <legend>Question 1</legend>
        <label for="q1"><strong>Fill in the blank:</strong> The system that translates domain names into server addresses is called <span class="pill">_____</span>.</label>
        <input type="text" id="q1" name="q1" class="text-answer" placeholder="Type your answer here">
      </fieldset>

      <fieldset class="quiz-fieldset">
        <legend>Question 2</legend>
        <p><strong>Which HTTP version introduced persistent connections?</strong></p>
        <div class="choice-list">
          <label><input type="radio" name="q2" value="HTTP/0.9"> HTTP/0.9</label>
          <label><input type="radio" name="q2" value="HTTP/1.0"> HTTP/1.0</label>
          <label><input type="radio" name="q2" value="HTTP/1.1"> HTTP/1.1</label>
          <label><input type="radio" name="q2" value="HTTP/3"> HTTP/3</label>
        </div>
      </fieldset>

      <fieldset class="quiz-fieldset">
        <legend>Question 3</legend>
        <p><strong>Which version of HTTP is known for multiplexing and a binary format?</strong></p>
        <div class="choice-list">
          <label><input type="radio" name="q3" value="HTTP/1.0"> HTTP/1.0</label>
          <label><input type="radio" name="q3" value="HTTP/1.1"> HTTP/1.1</label>
          <label><input type="radio" name="q3" value="HTTP/2"> HTTP/2</label>
          <label><input type="radio" name="q3" value="HTTP/3"> HTTP/3</label>
        </div>
      </fieldset>

      <fieldset class="quiz-fieldset">
        <legend>Question 4</legend>
        <p><strong>What does a 404 status code usually mean?</strong></p>
        <div class="choice-list">
          <label><input type="radio" name="q4" value="The request was successful"> The request was successful</label>
          <label><input type="radio" name="q4" value="The browser is being redirected permanently"> The browser is being redirected permanently</label>
          <label><input type="radio" name="q4" value="The requested resource could not be found"> The requested resource could not be found</label>
          <label><input type="radio" name="q4" value="The server is using HTTPS"> The server is using HTTPS</label>
        </div>
      </fieldset>

      <fieldset class="quiz-fieldset">
        <legend>Question 5</legend>
        <p><strong>Which web server software is especially known for speed, scalability, and an event-driven design?</strong></p>
        <div class="choice-list">
          <label><input type="radio" name="q5" value="Apache"> Apache</label>
          <label><input type="radio" name="q5" value="Nginx"> Nginx</label>
          <label><input type="radio" name="q5" value="IIS"> IIS</label>
          <label><input type="radio" name="q5" value="DNS"> DNS</label>
        </div>
      </fieldset>

      <fieldset class="quiz-fieldset">
        <legend>Question 6</legend>
        <p><strong>Select every task that modern web servers commonly handle.</strong></p>
        <div class="choice-list">
          <label><input type="checkbox" name="q6" value="Serve HTML, CSS, images, and other files"> Serve HTML, CSS, images, and other files</label>
          <label><input type="checkbox" name="q6" value="Manage encrypted HTTPS connections"> Manage encrypted HTTPS connections</label>
          <label><input type="checkbox" name="q6" value="Work with back end systems such as APIs and databases"> Work with back end systems such as APIs and databases</label>
          <label><input type="checkbox" name="q6" value="Translate spoken language into sign language"> Translate spoken language into sign language</label>
          <label><input type="checkbox" name="q6" value="Physically repair broken computer screens"> Physically repair broken computer screens</label>
        </div>
      </fieldset>

      <div class="quiz-actions">
        <button type="submit" class="button-primary">Submit Quiz</button>
        <button type="button" id="reset-quiz" class="button-secondary">Retake / Reset Quiz</button>
      </div>
    </form>
<!-- Results are filled in by JavaScript after submission -->
    <!-- This results block starts hidden on purpose, then the script reveals it after the quiz is graded. -->
	
    <section id="quiz-results" class="quiz-results" aria-live="polite" hidden>
      <div id="result-summary" class="result-summary"></div>
      <div id="result-details" class="result-details"></div>
    </section>
  </main>

 <!-- The footer repeats key links and the class project note so that info stays easy to find on every page. -->
  <footer class="page-footer">
    <div class="footer-inner">
      <p><strong>Web Servers and HTTP</strong> class project site.</p>
      <div class="footer-links">
          <a href="index.html">Home</a>
          <a href="quiz.html">Quiz</a>
          <a href="references.html">References</a>
          <a href="about.html">About</a>
          <a href="#top">Back to top</a>
      </div>
      <div id="project-note">
        This website was created as a class project for Intro to Web Development. Visit the course website here:
        <a href="https://ksuweb.github.io/IT3203/" target="_blank" rel="noopener noreferrer">IT 3203 class site</a>.
      </div>
    </div>
  </footer>
  <script src="quiz.js"></script>
</body>
</html>