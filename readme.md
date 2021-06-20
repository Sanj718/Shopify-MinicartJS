# Shopify MiniCart JS

![](https://raw.githubusercontent.com/Sanj718/Shopify-MinicartJS/main/logo.svg)


## Features 🚀
- Slide-out min-cart
- Total quantity indicator
- Easy deployment & customizable
- Custom cart endpoint support
- Global usage through `window.mini_cart`

## Integration ⚙️
1. Copy files to corresponding directories into your theme
2. Modify `theme.liquid` file (follow the sample in layouts folder)

## Usage ✅

1. Add `data-minicart-open` data attribute to trigger open mini cart.
2. Add `data-minicart-totalCount` to show cart total items quantity.

*Sample:*
```html
<button data-minicart-open type="button">MINICART - <span data-minicart-totalCount>{{ cart.item_count }}</span></button>
```

**Add `window.mini_cart.updateCart()` after add to cart script.**

*Sample:*
```javascript
 _addItemToCart: function(data) {
      var params = {
        url: '/cart/add.js',
        data: $(data).serialize(),
        dataType: 'json'
      };
      $.post(params)
        .done(
          function(item) {
            window.mini_cart.updateCart()
          }.bind(this)
        )
        .fail(
          function(response) {
            console.error(response)
          }.bind(this)
        );
    }
```

------------


##### TODO ⏳
- Support of Compare at price

🌟 Feel free to Star and PR.
<<<<<<< HEAD
[https://sanjar.dev](sanjar.dev "sanjar.dev")
=======
[sanjar.dev](https://sanjar.dev)
>>>>>>> bab821b464accd7a28b7d02df6f6efa86798247b

