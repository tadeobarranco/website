# Website

## How to make a website from scratch?

### Dealing with files

- Homepage content file: `index.html`
- Media folder: `images`
- CSS folder: `styles`
- JavaScript folder: `scripts`

### Layout Draft

- `header`
- `nav`
- `aside`
- `main`
- `footer`

### Link CSS

- Add a new `main.css` file inside the `styles` folder.

```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    font-size: 62.5%;
    font-family: Arial, Helvetica, sans-serif;
}

```

- Link the `main.css` file to the `index.html` file.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    ...
👉🏽  <link rel="stylesheet" href="./styles/main.css">
</head>
<body>...</body>
</html>
```

- Header content: add an `<h1></h1>` heading tag, and a `<p></p>` paragraph tag inside the `<header></header>` container.

```html
<!DOCTYPE html>
<html lang="en">
<head>...
</head>
<body>
❌ <header></header>
    <header>
👉🏽      <h1>Website</h1>
👉🏽      <p>How to make a Website</p>
    </header>
    ...
</body>
</html>
```
