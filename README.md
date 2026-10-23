# AED 1 Second Pizza: Kiosk Prototype

A clickable, high-fidelity prototype of a portrait self-ordering kiosk for the offer
**"Buy 1 medium or large pizza, get your 2nd pizza for AED 1"**.

> All products, prices and options are illustrative sample data.

## Run locally

Requires Node.js 18 or later. There are no dependencies to install.

```bash
npm start
```

Then open:

- http://localhost:3000: the kiosk prototype
- http://localhost:3000/docs.html: the UX documentation (flow, approaches, pricing model, edge cases, components)

Set a different port with `PORT=8080 npm start`.

You can also double-click `public/index.html` to open it without a server.

## Journey

1. Attract screen with the offer banner
2. Home, where the banner changes to "AED 1 pizza waiting" once pizza 1 is in the cart
3. Choose the first pizza (eligible medium and large only)
4. Customize pizza 1, with the price updating as options change
5. Offer unlocked: choose the AED 1 pizza on the same screen, with no pop-up
6. Customize the AED 1 pizza, with paid extras shown separately
7. Cart with savings, plus edit, swap and remove on each line
8. Checkout, card payment and order confirmation

Edge cases such as skip, exit, removing pizza 1, swapping, a third pizza, small sizes and items already in the cart are handled by the offer engine in `public/index.html`.

## Structure

```
public/
  index.html   kiosk prototype (self-contained HTML/CSS/JS)
  docs.html    UX documentation and the prototype with config panel
server.js      zero-dependency static server
package.json
```
