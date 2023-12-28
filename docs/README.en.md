# EXAMPLE-OF-EVENT-PRODUCT-NODE

<!-- DOCS-IGNORE:start -->
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->

[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->
<!-- DOCS-IGNORE:end -->

Change language from README to [![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/FelCer/vtex-event-example-node/blob/main/docs/README.md)

## Catalog Broadcast 

VTEX IO app designed to listen to and send events.

This event will query all the product information with the product id.
<br>

## Implementation

1. Importar `{{vendor}}.events-example` en el archivo `manifest.json` del tema de IO.

```
  "dependencies": {
    // Validar la versión que se encuentra la aplicación.
    "{{vendor}}.events-example": "0.x",
  }
```

## example use

This app handles events sent by the app `vtex.orders-broadcast`, as you can see by looking at `node/service.json`.

```
{
  "memory": 128,
  "ttl": 10,
  "timeout": 2,
  "minReplicas": 2,
  "maxReplicas": 10,
  "workers": 4,
  "events": {
    "example": {
      "sender": "vtex.events-example",
      "keys": [
        "send-event"
      ]
    },
    "skuChange": {
      "keys": [
        "broadcaster.notification"
      ]
    }
  },
  "routes": {
    "hcheck": {
      "path": "/_v/app/events-example/hcheck",
      "public": true
    }
  }
}
```


<!-- DOCS-IGNORE:start -->

## Contributors ✨

Thanks goes to these wonderful people: ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<table>
  <tr>
    <td align="center"><img src="https://avatars.githubusercontent.com/u/22477264?v=4" width="100px;" alt=""/><br /><sub><b>Luis Felipe Cerero Garcia</b></sub></a><br /><a href="https://github.com/FelCer/vtex-event-example-node/commits?author=felcer" title="Documentation">📖</td>
  </tr>
</table>

<!-- DOCS-IGNORE:end -->
