# 🐾 Patinhas & Cia | Login and Sign-up

A **login and sign-up page** for a fictional pet shop, built with **HTML and CSS**, using only a tiny bit of JavaScript.

> An orange panel slides from side to side to switch between the two forms.

🔗 **Demo:** [vitoriacdev.github.io/pagelogin_petshop](https://vitoriacdev.github.io/pagelogin_petshop/)

## Features

| Feature | How it works |
|---|---|
| Switching between login and sign-up | Hidden checkbox + `:checked` selector (no JavaScript) |
| Sliding panel | `transform: translateX()` with `transition` |
| Visual validation | `:valid`, `:invalid` and `:placeholder-shown` pseudo-classes |
| Pet type selector | Styled `radio` inputs |
| Terms of use modal | `:target` selector, with a custom checkbox shared by the form and the modal (kept in sync with a few lines of JavaScript) |
| Responsive | Media query: on mobile, the forms swap and the panel is hidden |
| Accessibility | A `label` on every field, visible focus and `prefers-reduced-motion` |

## Built with

- HTML5
- CSS3 (variables, Grid, Flexbox, transitions)
- JavaScript (only to sync the terms checkboxes)
- Google Fonts: Baloo 2 and Nunito

##  Getting started

1. Download or clone the repository
2. Open `login-petshop.html` in your browser (keep `style.css` in the same folder)

No installation needed.

## Project structure

```
.
├── index.html   # page structure (HTML)
├── style.css            # styles (CSS)
└── README.md
```

## Customization

The colors are defined in `:root`, at the top of `style.css`:

```css
:root {
  --laranja:  #ff8a3d;  /* orange */
  --manteiga: #ffe9a8;  /* butter yellow */
  --azul:     #cfeaf7;  /* light blue */
  --marrom:   #4a2c17;  /* brown */
}
```

To change the theme, update these values and the form texts.

## How the switch works without JavaScript

```html
<input type="checkbox" id="modo-cadastro" class="toggle">
<label for="modo-cadastro">Create account</label>
```

```css
.toggle:checked ~ .card .painel { transform: translateX(-100%); }
```

Clicking the `label` checks the checkbox. CSS reads that state with `:checked` and moves the panel.

## Next steps

- Password strength meter
- Dark mode
- Show/hide password button
- Connect to a back end

Developed by [vitoriacdev] as part of my web development studies.
