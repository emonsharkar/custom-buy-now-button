<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>Custom Buy Now Button – README</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root { --ink:#111; --ink-2:#333; --muted:#666; --accent:#96588a; --bg:#fff; }
    body{font:16px/1.6 system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,Helvetica,Arial,sans-serif;color:var(--ink);background:#fafafa;margin:0;padding:32px}
    h1,h2,h3{line-height:1.2}
    h1{font-size:2rem;margin:.2rem 0 1rem}
    h2{font-size:1.4rem;margin:1.6rem 0 .6rem}
    h3{font-size:1.1rem;margin:1.2rem 0 .4rem}
    p{margin:.6rem 0}
    code,kbd,pre{font-family:ui-monospace,SFMono-Regular,Consolas,Menlo,monospace}
    pre{background:#121212; color:#eaeaea; padding:16px; border-radius:8px; overflow:auto}
    .small{color:var(--muted); font-size:.92rem}
    .badge{display:inline-block;padding:.15rem .5rem;border-radius:.5rem;background:#eee;color:#222;font-weight:600;margin-right:.35rem}
    .grid{display:grid; gap:10px}
    .two{grid-template-columns:repeat(auto-fit,minmax(260px,1fr))}
    ul{margin:.4rem 0 .8rem}
    li{margin:.25rem 0}
    table{border-collapse:collapse;width:100%;background:#fff}
    th,td{border:1px solid #e6e6e6;padding:8px 10px;text-align:left;vertical-align:top}
    th{background:#f6f6f6}
    .muted{color:#777}
    a{color:var(--accent);text-decoration:none}
    a:hover{text-decoration:underline}
    .callout{border-left:4px solid var(--accent); background:#fff; padding:12px 14px; border-radius:6px}
  </style>
</head>
<body>

  <h1>Custom Buy Now Button</h1>
  <p class="small">
    <span class="badge">WooCommerce</span>
    <span class="badge">Elementor</span>
    <span class="badge">Gutenberg Block</span>
    <span class="badge">Shortcode</span>
  </p>

  <p><strong>Custom Buy Now Button</strong> adds a fast-checkout button you can place anywhere. Clicking it
  adds the selected product to the cart and immediately redirects the shopper to the
  <em>Checkout</em> page. The plugin ships with a Gutenberg block, an Elementor widget, and a shortcode, plus
  multiple visual variants, sizes, hover animations, and a selectable icon.</p>

  <h2>Plugin Metadata</h2>
  <table>
    <tr><th>Plugin Name</th><td>Custom Buy Now Button</td></tr>
    <tr><th>Description</th><td>Customizes Buy Now Button as you wish. Adds a Gutenberg block, Elementor widget and shortcode to place a “Buy Now” button that adds a product to the cart and takes the customer directly to Checkout.</td></tr>
    <tr><th>Version (header)</th><td><strong>1.5</strong></td></tr>
    <tr><th>Text Domain</th><td><code>custom-buy-now</code></td></tr>
    <tr><th>Author</th><td>MD EMON SHARKAR — <a href="https://github.com/emonsharkar">github.com/emonsharkar</a></td></tr>
    <tr><th>Requires</th><td>WordPress 5.8+, WooCommerce, PHP 7.4+</td></tr>
    <tr><th>Optional</th><td>Elementor (for the native Elementor widget)</td></tr>
  </table>
  <p class="muted"><strong>Note:</strong> Ensure the internal constant <code>CBN_PLUGIN_VERSION</code> matches the header version.</p>

  <h2>Installation</h2>
  <ol>
    <li>Upload the plugin folder or ZIP via <em>Plugins → Add New → Upload Plugin</em>.</li>
    <li>Activate the plugin and verify <strong>WooCommerce</strong> (and <strong>Elementor</strong> if you use it) are active.</li>
    <li>Go to a page/post/product and insert the button using:
      <ul>
        <li><strong>Elementor</strong> → search “<em>Custom Buy Now</em>” (categories: <em>Custom Buy Now</em>, <em>WooCommerce Elements</em>, or <em>General</em>),</li>
        <li><strong>Gutenberg</strong> → add the block “<em>Custom Buy Now</em>” (WooCommerce category),</li>
        <li>or place the <strong>shortcode</strong> shown below.</li>
      </ul>
    </li>
  </ol>

  <h2>Usage</h2>

  <h3>Elementor Widget</h3>
  <div class="grid two">
    <div>
      <h4>Content Controls</h4>
      <ul>
        <li><strong>Product ID</strong> (required)</li>
        <li><strong>Quantity</strong></li>
        <li><strong>Button Text</strong> (e.g., <em>ক্রয় করুন</em>)</li>
        <li><strong>Variant</strong>: outline (default), solid, primary, ghost, link</li>
        <li><strong>Size</strong>: sm, md, lg; <strong>Full width</strong> toggle</li>
        <li><strong>Icon</strong>: show/hide; position left/right</li>
        <li><strong>Icon source</strong>:
          <ul>
            <li><em>Built-in SVG set</em> (cart, bag, bolt, flash, credit, arrow, check, star, tag)</li>
            <li><em>Elementor Icon Library</em> (Font Awesome, etc.)</li>
          </ul>
        </li>
        <li><strong>Hover Animation</strong>: lift, pulse, wiggle (icon), none</li>
      </ul>
    </div>
    <div>
      <h4>Style Controls</h4>
      <ul>
        <li>Alignment</li>
        <li>Typography</li>
        <li>Text / Background / Border colors</li>
        <li>Padding &amp; Border Radius</li>
      </ul>
    </div>
  </div>

  <h3>Gutenberg Block</h3>
  <p>Insert the block “<strong>Custom Buy Now</strong>” and set the same attributes in the sidebar:
  Product ID, Quantity, Text, Variant, Size, Icon (name &amp; position), Full width, and Animation.</p>

  <h3>Shortcode</h3>
  <pre>[custom_buy_now
  product_id="123"
  quantity="1"
  text="ক্রয় করুন"
  variant="outline"      ; outline | solid | primary | ghost | link
  size="md"              ; sm | md | lg
  fullwidth="no"         ; yes | no
  icon="yes"             ; yes | no
  icon_name="cart"       ; cart | bag | bolt | flash | credit | arrow | check | star | tag
  icon_pos="left"        ; left | right
  animation="lift"       ; lift | pulse | wiggle | none
]</pre>

  <h2>Attributes Reference</h2>
  <table>
    <thead>
      <tr><th>Attribute</th><th>Type</th><th>Default</th><th>Description</th></tr>
    </thead>
    <tbody>
      <tr><td><code>product_id</code> *</td><td>int</td><td>—</td><td>WooCommerce product ID to purchase.</td></tr>
      <tr><td><code>quantity</code></td><td>int</td><td>1</td><td>Quantity to add.</td></tr>
      <tr><td><code>text</code></td><td>string</td><td><code>Buy Now</code></td><td>Button label (supports any language).</td></tr>
      <tr><td><code>variant</code></td><td>enum</td><td><code>outline</code></td><td>Visual style: outline / solid / primary / ghost / link.</td></tr>
      <tr><td><code>size</code></td><td>enum</td><td><code>md</code></td><td>Button size: sm / md / lg.</td></tr>
      <tr><td><code>fullwidth</code></td><td>yes/no</td><td><code>no</code></td><td>Makes the button span 100% width.</td></tr>
      <tr><td><code>icon</code></td><td>yes/no</td><td><code>yes</code></td><td>Toggle the icon.</td></tr>
      <tr><td><code>icon_name</code></td><td>enum</td><td><code>cart</code></td><td>Built-in icon name (cart, bag, bolt, flash, credit, arrow, check, star, tag).</td></tr>
      <tr><td><code>icon_pos</code></td><td>enum</td><td><code>left</code></td><td>Icon position relative to text: left / right.</td></tr>
      <tr><td><code>animation</code></td><td>enum</td><td><code>lift</code></td><td>Hover animation: lift / pulse / wiggle / none.</td></tr>
      <tr><td><code>class</code></td><td>string</td><td>—</td><td>Extra CSS classes to add.</td></tr>
    </tbody>
  </table>
  <p class="small">* Required</p>

  <h2>Behavior</h2>
  <ul>
    <li>Button click hits a lightweight handler via query vars: <code>?custom-buy-now=PRODUCT_ID&amp;qty=QTY</code>.</li>
    <li>The product is added to cart, then the user is redirected to <strong>Checkout</strong>.</li>
    <li>If the product isn’t purchasable/in stock, WooCommerce shows a notice and redirects to the cart.</li>
  </ul>

  <h2>Styling &amp; Classes</h2>
  <p>The button outputs utility classes you can target in your theme:</p>
  <pre>cbn-btn custom-buy-now-button cbn-variant-<em>{outline|solid|primary|ghost|link}</em> cbn-size-<em>{sm|md|lg}</em> cbn-anim-<em>{lift|pulse|wiggle|none}</em>
cbn-w-full (optional), cbn-icon-right (optional)</pre>

  <h2>Localization</h2>
  <p>All strings are translation-ready. Example localized label in Bengali: <code>text="ক্রয় করুন"</code>.</p>

  <h2>Troubleshooting</h2>
  <ul>
    <li><strong>Button not visible in Elementor:</strong> confirm Elementor is active; reload the editor; clear caches; check user role/capabilities.</li>
    <li><strong>Redirect not happening:</strong> check for caching/optimization plugins that alter query vars; exclude the page from aggressive caching.</li>
    <li><strong>Variable products:</strong> this button adds a specific product ID. For variations, use a concrete variation ID or extend the UI with attribute pickers.</li>
  </ul>

  <h2>Changelog</h2>
  <ul>
    <li><strong>1.5</strong> – README refresh; icon picker &amp; hover animations documented; Elementor direct-icon rendering.</li>
    <li><strong>1.2</strong> – Added hover animations (lift, pulse, wiggle), built-in icon set + Elementor Icon Library support.</li>
    <li><strong>1.1</strong> – Default outline style like screenshot; style variants (outline/solid/primary/ghost/link); sizes; full-width.</li>
    <li><strong>1.0</strong> – Initial release with Gutenberg block, shortcode, add-to-cart + checkout redirect.</li>
  </ul>

  <h2>License</h2>
  <p>GPL-2.0+ – You are free to use, modify, and redistribute under the GPL terms.</p>

  <h2>Credits</h2>
  <p>© <a href="https://github.com/emonsharkar">MD EMON SHARKAR</a>. Thanks to the WooCommerce and Elementor teams for their excellent developer APIs.</p>

  <div class="callout">
    <strong>Pro tip:</strong> Want a custom funnel (e.g., skip cart + send to a one-page checkout, or attach coupons)? Add a filter on the generated URL or extend the shortcode to accept a <code>redirect</code> parameter.
  </div>

</body>
</html>
