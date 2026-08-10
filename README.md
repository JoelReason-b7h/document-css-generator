# Glyph

Bondsmith's statement branding tool. Customise how your brand appears on the statements and ISA
transfer forms we generate for your customers: set your colours, type and table styling, check
them against a sample document, then download the stylesheet to send us.

Open `index.html` in any browser. Nothing is uploaded, and nothing leaves your machine.

## How to use it

1. Pick the layout closest to what you want under **Start from**, then work through the
   **Colour**, **Type**, **Table** and **Layout** tabs. Trying another layout does not lose your
   work — it is kept under **Your changes**, at the top of the same list.
2. Anything marked **Auto** follows your brand colour. Click the pill to set it yourself; click
   again to go back to following the brand.
3. Every colour shows its contrast against whatever sits behind it. Green passes; amber is below
   4.5:1, the point where text starts to be hard to read on paper. One weak pair often lights up
   several controls, because they all resolve to the same two colours.
4. Set **Sample**, above the preview, to the statement your customers get. It changes the sample
   document only, never the stylesheet, but the four arrangements list different transactions and
   the longest description is what decides how wide your columns need to be.
5. Watch the notices above the preview. They flag choices that will not survive the move to PDF.
6. Download the stylesheet and send it to your Bondsmith contact along with your logo.

Your settings are kept in the browser, so closing the tab and coming back does not lose them.

The stylesheet also covers the ISA transfer authority form, which has no preview here. The
**ISA form rules and headings** colour on the **Colour** tab is what sets its title underline,
section borders and headings.

**Copy shareable link** puts your settings in the URL, which is the easiest way to show someone else
what you are proposing — open the link and the controls come back exactly as you left them.

Ask us for a sample document before we switch the branding on for your customers.

## Two things worth knowing

**Fonts have to be embedded.** The PDF renderer only has the handful of fonts built into every
PDF reader. Naming any other font silently falls back to Helvetica — the statement will not use
your brand typeface. To use your own, send us the `.ttf` file, and we will host it and give you a
URL to paste into the tool.

**Your logo is not part of the stylesheet.** We store it separately, so send it alongside. The
logo box in the tool is only there so the preview looks right.

## Why some things are not adjustable

Statements are rendered to PDF by an engine that supports a subset of CSS, so a stylesheet that
looks right in a browser can lose half its styling on the way to the page. Every option in the
tool was tested against the real renderer, and only the ones that genuinely survive are offered.

Deliberately absent, because the renderer discards them:

- letter spacing and word spacing
- transparency — both `opacity` and `rgba()` colours
- drop shadows and gradients
- CSS variables

The two groups fail differently and both fail quietly. `opacity`, `rgba()`, gradients and
variables are rejected outright, and the renderer throws away the whole declaration when that
happens — an `rgba()` background is not a faded colour, it is no background at all. Letter
spacing and borders on table rows are worse: they are accepted without complaint and then simply
never drawn.

That is why the tool will not let you paste a stylesheet in. Everything it produces is written by
the tool itself, so it can guarantee that what you see in the preview is what your customers get.

## Questions

Talk to your Bondsmith contact — they can get you a sample statement with your branding applied
before anything goes live.
