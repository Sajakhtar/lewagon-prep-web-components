# Le Wagon Web Components

[Reference Repo](https://github.com/Papillard/UI-sprint)

5 to 10 components will cater to 90% of the design of your app.

We'll build a library of reusable commponents.

[See Live]()

## Index.html

The HTML file has

- Bootstrap
- Font Awesome
- JQuery
- Bootstrap JavaScript Component
- Components
  - Avatar
  - [Button](https://getbootstrap.com/docs/5.0/components/buttons/) - using Bootstrap button component
  - [Dropdown](https://getbootstrap.com/docs/4.0/components/dropdowns/) - using Bootstrap JS
  - [Card](https://getbootstrap.com/docs/4.0/components/card/) - using Bootstrap rows
  - [Badge](https://getbootstrap.com/docs/5.0/components/badge/) - using Bootstrap badge component
  - Banner - using Flexbox
  - Tabs - using Flexbox
  - Product List
    - using Bootstrap `list-inline`, `img-rounded`, `text-center`
    - Flexbox for each product list item

## Organizing CSS component files

```
├── css
│ ├── components
│ │ ├── avatar.css
│ │ ├── banner.css
│ │ └── button.css
│ └── style.css
└── index.html
```

```css
/* Importing all components file */
@import url("components/avatar.css");
@import url("components/banner.css");
@import url("components/button.css");
```

```html
<head>
  <link rel="stylesheet" href="css/style.css" />
</head>
```

Overwrite Bootstrap CSS by using `!important` next to your own CSS.

### Relative / Absolute

An element with `position: relative`; is positioned relative to its normal position.

The relative/absolute CSS pattern is important when you need to position stuff in a specific place inside a component (e.g. a card).

- Putting the card as position: relative is a way to pin it and be able to position the things inside it precisely.
- Then you can make the inner elements `position: absolute` and place them wherever you want in the card thanks to the top/bottom/left/right properties.

### Flexbox

Flexboxes are awesome. It’s a layout mode intended to accommodate different screen sizes and different display devices. To turn a div into a flexbox is super easy: just add display: flex on your div. Then:

- That div is the flexbox
- All of its children elements are called flex items and can be distributed vertically and horizontally within the flexbox.

[CSS Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

[Flexbox Froggy game](http://flexboxfroggy.com/)

**Main Flexbox Flex Container properties**

- `justify-content` distributes flex items horizontally (either with space-around the items or space-between the items).
- `align-items: center` allows use to vertically align the items (very useful).

You can also make a **flex item** grow and take all available space:

- `flex-grow: 1` will make a flex item grow and push its neighbours on the left and on the right.
