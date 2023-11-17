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
    font-size: 2.4rem; 👈🏽
    line-height: 2.6rem; 👈🏽
}

header p {
    font-size: 1.4rem; 👈🏽
    line-height: 1.8rem; 👈🏽
}

```

![Header - font-size & line-height](https://i.imgur.com/YkGfPz1.png)
