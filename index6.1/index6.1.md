<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assignment 6.1 | CSS Box Model Inspection</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header class="site-header">
    <div class="container">
      <p class="eyebrow">ASSIGNMENT 6.1 · CSS FUNDAMENTALS</p>
      <h1>Box Model <span>Inspection Lab</span></h1>
      <p class="intro">Explore how content, padding, border, and margin affect an element's size and spacing.</p>
    </div>
  </header>

  <main class="container">
    <section class="controls-panel" aria-labelledby="controls-title">
      <div>
        <p class="eyebrow">INTERACTIVE EXPERIMENT</p>
        <h2 id="controls-title">Compare box sizing</h2>
        <p>Choose a sizing mode to see how the same declared width behaves.</p>
      </div>
      <div class="toggle-group" role="group" aria-label="Box sizing mode">
        <button class="mode-button active" type="button" data-mode="content-box">content-box</button>
        <button class="mode-button" type="button" data-mode="border-box">border-box</button>
      </div>
      <p class="mode-note" id="mode-note" aria-live="polite">content-box: padding and border are added outside the declared width.</p>
    </section>

    <section class="cards-grid" aria-label="Three box model examples">
      <article class="demo-card card-one">
        <span class="card-number">BOX 01</span>
        <h2>Content First</h2>
        <p>This box uses small padding, a thin border, and a generous outer margin. Notice the breathing room around the text.</p>
        <div class="measure">Width: 260px · Padding: 12px · Border: 2px</div>
      </article>
      <article class="demo-card card-two">
        <span class="card-number">BOX 02</span>
        <h2>Balanced Space</h2>
        <p>This box has more internal padding and a thicker border. The text sits farther from the edge.</p>
        <div class="measure">Width: 260px · Padding: 24px · Border: 5px</div>
      </article>
      <article class="demo-card card-three">
        <span class="card-number">BOX 03</span>
        <h2>Room to Breathe</h2>
        <p>This box has the largest padding and a distinct border. Compare its overall size with the other boxes.</p>
        <div class="measure">Width: 260px · Padding: 32px · Border: 8px</div>
      </article>
    </section>

    <section class="explain-grid">
      <article class="explain-card">
        <h2>CSS Box Model</h2>
        <p>Every element is represented by four nested layers. From the inside out: content, padding, border, then margin.</p>
        <div class="box-model" role="img" aria-label="Diagram of margin surrounding border, border surrounding padding, and padding surrounding content">
          <div class="layer margin-layer"><span class="layer-label">MARGIN</span>
            <div class="layer border-layer"><span class="layer-label">BORDER</span>
              <div class="layer padding-layer"><span class="layer-label">PADDING</span>
                <div class="layer content-layer">CONTENT</div>
              </div>
            </div>
          </div>
        </div>
        <ul class="legend">
          <li><span class="swatch content-swatch"></span><strong>Content:</strong> text, image, or other actual content.</li>
          <li><span class="swatch padding-swatch"></span><strong>Padding:</strong> space between content and border.</li>
          <li><span class="swatch border-swatch"></span><strong>Border:</strong> line around padding and content.</li>
          <li><span class="swatch margin-swatch"></span><strong>Margin:</strong> outside space separating elements.</li>
        </ul>
      </article>
      <article class="explain-card sizing-card">
        <h2>What changes?</h2>
        <div class="sizing-example">
          <p class="eyebrow">DECLARED WIDTH = 260PX</p>
          <div class="sizing-row"><span>content-box</span><div class="bar bar-content"></div><strong>Width grows</strong></div>
          <div class="sizing-row"><span>border-box</span><div class="bar bar-border"></div><strong>Width stays 260px</strong></div>
        </div>
        <p><code>content-box</code> applies the declared width to the content only. Padding and border are added to the total.</p>
        <p><code>border-box</code> includes content, padding, and border inside the declared width, making layouts easier to control.</p>
        <pre><code>* {
  box-sizing: border-box;
}</code></pre>
      </article>
    </section>

    <section class="devtools-note">
      <div class="devtools-icon">⌕</div>
      <div><h2>Inspect it in Chrome DevTools</h2>
        <ol>
          <li>Right-click any demo card and choose <strong>Inspect</strong>.</li>
          <li>In the <strong>Elements</strong> panel, select the card element.</li>
          <li>Open the <strong>Computed</strong> panel and find the Box Model diagram.</li>
          <li>Hover over content, padding, border, and margin in the diagram to highlight each region.</li>
          <li>Take a screenshot of the diagram and label each part for submission.</li>
        </ol>
      </div>
    </section>
  </main>

  <footer><div class="container">Assignment 6.1 · Box Model Inspection · HTML + External CSS</div></footer>
  <script src="js/script.js"></script>
</body>
</html>
