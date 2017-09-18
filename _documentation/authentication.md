---
title: Payloads
position: 3
right_code: |
  ~~~
  POST /payload HTTP/1.1

  Host: localhost:4567
  X-RiskLimiter-Delivery: 72d3162e-cc78-11e3-81ab-4c9367dc0958
  User-Agent: GitHub-Hookshot/044aadd
  Content-Type: application/json
  Content-Length: 6615
  X-RiskLimiter-Event: report-create

  {
    "action": "created",
    "report-payload": {

    },
    "report": {

    },
    "sender": {

    }
  }
  ~~~
  {: title="Example Payload" }
---

Each event type has a specific payload format with the relevant event information. All event payloads mirror the payloads for the Event types, with the exception of the original create event, which has a more detailed webhook payload.

In addition to the fields documented for each event, webhook payloads include the user who performed the event (sender) as well as the organization (organization) and/or report which the event occurred on.


#### Delivery Headers

| Name                    | Description                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|
| X-RiskLimiter-Event     | Name of the event that triggered this delivery.                                         |
| X-RiskLimiter-Signature | HMAC hex digest of the payload, using the hook's secret as the key (if configured).     |
| X-RiskLimiter-Delivery  | Unique ID for this delivery.                                                            |

Also, the User-Agent for the requests will have the prefix RiskLimiter-Hookshot/.
