---
id: monetization-event-asset-scale
title: MonetizationEvent.assetScale
sidebar_label: MonetizationEvent.assetScale
---

import Specifications from '@site/src/components/Specifications';
import BrowserCompat from '@site/src/components/BrowserCompat';

The **`assetScale`** property of the [MonetizationEvent](monetization-event.md) interface returns the scale of the successfully streamed amount.

## Value

An integer. Represents the scale of the amount of money received according to the last receipt.

## Examples

```html
<link rel="monetization" href="https://example.com/pay" />
<script>
  const link = document.querySelector('link[rel="monetization"]')
  link.addEventListener('monetization', (event) => {
    // See how much your received and in what currency
    const { amount, assetCode, assetScale } = event
    console.log(`Browser sent ${assetCode}${amount / (10 * assetScale)}.`)
  })
</script>
```

## Specifications

<Specifications link="assetscale-attribute">Web Monetization API</Specifications>

## Browser compatibility

<BrowserCompat data="assetScale.json">Web Monetization API</BrowserCompat>