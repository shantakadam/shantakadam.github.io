# shantakadam.github.io

Personal academic website of Shanta Kadam, live at **https://shantakadam.github.io**.

It is plain HTML and CSS. There are no frameworks and no build step: you edit a file on GitHub, click **Commit changes**, and the site updates within 1–2 minutes.

## What is in this repository

| File / folder        | What it is                                              |
|----------------------|---------------------------------------------------------|
| `index.html`         | Home page (banner, photo, bio, contact links)           |
| `research.html`      | Research page (papers)                                  |
| `teaching.html`      | Teaching page                                           |
| `others.html`        | Others page (media engagement)                          |
| `style.css`          | All colours, fonts and layout for every page            |
| `images/profile.jpg` | Profile photo shown on the Home page                    |
| `images/background.jpg` | Campus photo used as the Home page banner            |

## How to edit text

1. On GitHub, open the repository and click the file you want to change, e.g. `index.html`.
2. Click the **pencil icon** (Edit this file) at the top right of the file.
3. Change only the words **between** the tags. For example, in
   `<p>My current work spans migration, climate change, and innovation.</p>`
   change only the sentence and leave `<p>` and `</p>` alone.
4. Scroll down (or top right) and click **Commit changes…**, then **Commit changes** again.
5. Wait 1–2 minutes and refresh the website. If you don't see the change, press `Ctrl + F5` (Windows) or `Cmd + Shift + R` (Mac).

Useful patterns:

- A link: `<a href="https://the-address.com">Text people see</a>`
- A new paragraph: `<p>Your text here.</p>`
- A new list item (e.g. on the Teaching page): `<li>Course name (dates)</li>`
- Special characters: write `&amp;` for `&` inside a link address.

**The navigation bar and footer appear on every page.** If you change them, for example to update the CV link, make the same change in all four `.html` files.

### Updating the CV link

The CV link currently points to Dropbox. To change it, search each `.html` file for `dropbox.com` (press `Ctrl + F` in the GitHub editor) and replace the whole address in **both** places on the Home page and the one place in the menu of every other page.

You can also host the CV on the site itself. Upload `CV.pdf` to the main folder of the repository (**Add file → Upload files**), then use `href="CV.pdf"` as the link.

## How to add a new paper

1. Open `research.html` and click the pencil icon.
2. Find the block that starts with `<!-- ===== PAPER START` and ends with `<!-- ===== PAPER END ===== -->`.
3. Copy that entire block and paste it directly **above** the existing one, so the newest paper comes first.
4. In the copy, change:
   - the title inside `<h3> ... </h3>`
   - the co-authors: add `<p class="authors">with Name One and Name Two</p>` under the title
   - the paper link inside `href="..."`
   - the abstract text inside `<p> ... </p>` within `<details>`. Visitors click "Abstract" to open it.
   - remove the `Coverage:` and `Podcast:` lines if the new paper doesn't have them
5. For a new section, such as "Work in Progress" or "Publications", add a heading above the papers:
   `<h2>Work in Progress</h2>`
6. **To link to your own PDF:** upload it with **Add file → Upload files** (for example, into a folder called `papers`), then use `href="papers/my-paper.pdf"`.
7. Commit changes.

## How to change the background image

1. Choose a photo you are allowed to reuse, for example from [Wikimedia Commons](https://commons.wikimedia.org) with a CC BY or CC BY-SA licence. Landscape photos work best.
2. Compress it to under about 1 MB. Go to <https://squoosh.app>, drop the image in, set **Resize** width to `2400`, choose **MozJPEG** with quality around `75–80`, and download it.
3. Rename the file to `background.jpg`.
4. On GitHub, open the `images` folder → **Add file → Upload files** → drag in the new `background.jpg` → **Commit changes**. It replaces the old one.
5. **Update the attribution** in the footer of all four `.html` files. Search for `Background photo:` and change the title, author, licence and links.
6. Optional: to make the banner darker or lighter, open `style.css`, find `--banner-overlay` near the top, and change the three numbers `0.10`, `0.35` and `0.75` (top, middle, bottom). Higher numbers make it darker. `--banner-position` just below it moves the photo up or down.

To use a different file name, change `url("images/background.jpg")` in `style.css`.

## How to change the profile photo

Upload a new square-ish photo named `profile.jpg` into the `images` folder. It will replace the old one. Keep it under about 300 KB; at Squoosh, a width of `600` is plenty.

## Changing colours

At the top of `style.css`, under `:root`, `--accent` is the link colour (currently maroon `#7a1c2e`). Change it to any colour code, for example `#1f4e79` for navy.

## Image credit

Background photo: "Great Hall seen in line with the clock tower" by Tom Axford, CC BY-SA 4.0, via Wikimedia Commons:
https://commons.wikimedia.org/wiki/File:Great_Hall_seen_in_line_with_the_clock_tower.jpg
