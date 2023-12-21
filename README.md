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

### Header

#### Header content

- Add an `<h1></h1>` heading tag, and a `<p></p>` paragraph tag inside the `<header></header>` container.

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

#### Header styles

- Add the basic selector `header` to the `main.css` file.

```css
* {...
}

html {...
}

header {... 👈🏽
}
```

![Header](https://i.imgur.com/lSQjImF.png)

- Let's add the CSS declaration `display: flex;`, which transform the `header` element as a container and its childs `h1`, `p` as a flex items.

```css

...

header {
    display: flex; 👈🏽
}
```

![Header - display: flex](https://i.imgur.com/nxFYzp8.png)

- Now, let's define the `flex-direction` property as `column`.

```css

...

header {
    display: flex;
    flex-direction: column; 👈🏽
}
```

![Header - flex-direction: column](https://i.imgur.com/uJhnUKJ.png)

- Define the `height` property of the `container`.

```css

...

header {
    display: flex;
    flex-direction: column;
    height: 320px; 👈🏽
}
```

![Header - height](https://i.imgur.com/KxijYiB.png)

- Align items around the center using the CSS declaration `justify-content: center;`.

```css

...

header {
    display: flex;
    flex-direction: column;
    height: 320px;
    justify-content: center; 👈🏽
}
```

![Header - justify-content: center](https://i.imgur.com/Ao72mzA.png)

- Set the `position` property as `relative`, and align the text to the center using the CSS declaration `text-align: center;`.

```css

...

header {
    display: flex;
    flex-direction: column;
    height: 320px;
    justify-content: center;
    position: relative; 👈🏽
    text-align: center; 👈🏽
}
```

![Header . position & text-align](https://i.imgur.com/Oh0X2C9.png)

- As last step with the container styles let's define the `background` and the text `color` using hexadecimal values.

```css

...

header {
    background: #1abc9c; 👈🏽
    color: #ffffff; 👈🏽
    display: flex;
    flex-direction: column;
    height: 320px;
    justify-content: center;
    position: relative;
    text-align: center;
}
```

![Header - background & color](https://i.imgur.com/maDuo8d.png)

- By setting the `font-size` as `62.5%` for the `html`, allow us to set specific element `font-size` and `line-height` in `rem` units easily.

```css

...

header {...
}

header h1 {
    font-size: 3.2rem; 👈🏽
    line-height: 3.4rem; 👈🏽
}

header p {
    font-size: 1.8rem; 👈🏽
    line-height: 2.2rem; 👈🏽
}

```

![Header - font-size & line-height](https://i.imgur.com/YkGfPz1.png)

### Link CSS with the `media` attribute

- Add a new `desktop.css` file inside the `styles` folder.

```css
header h1 {
    font-size: 4.8rem;
    line-height: 5rem;
}

header p {
    font-size: 3.4rem;
    line-height: 3.8rem;
}

```

- Link the `desktop.css` file to the `index.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    ...
👉🏽  <link rel="stylesheet" href="./styles/desktop.css">
</head>
<body>...
</body>
</html>
```

- Add the `media` attribute to the `link` tag.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    ...
    <link rel="stylesheet" href="./styles/desktop.css" media="screen and (min-width: 768px)">
</head>
<body>...
</body>
</html>
```

- By setting the values `screen` and `min-width: 768px` means the styles inside the `desktop.css` file will apply only if the screen width is equal or bigger than `768 pixels`.

![Header - Desktop: font-size](https://i.imgur.com/gvy50FE.png)

### CSS custom properties

- Define custom properties at the top of the `main.css` file using the `:root` pseudo-class.

```css
:root {
    /* Colors */
    --mountain-meadow: #1abc9c;
    --white: #ffffff;
}

...
```

- Then replace the direct use of the hexadecimal values in both the `background` and `color` properties at the `header` selector by using the custom properties defined above.

```css
...

header {
    background: #1abc9c; ❌
    color: #ffffff; ❌
    background: var(--mountain-meadow); 👈🏽
    color: var(--white); 👈🏽
    ...
}

...
```
