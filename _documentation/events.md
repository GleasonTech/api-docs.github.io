---
title: Events
position: 2
---

When configuring a webhook, you can choose which events you would like to receive payloads for. You can even opt-in to all current and future events. Only subscribing to the specific events you plan on handling is useful for limiting the number of HTTP requests to your server. You can change the list of subscribed events through the API or UI anytime. By default, webhooks are only subscribed to the push event.

Each event corresponds to a certain set of actions that can happen to your organization and/or report. For example, if you subscribe to the update event you'll receive detailed payloads every time a report is updated.

The available events are:


| Name            | Description                      |
|-----------------|----------------------------------|
| *               | Any time any event is triggered  |
| report-create   | Any time a report is created     |
| report-update   | Any time a report is updated     |
| report-delete   | any time a report is deleted     |

#### Wildcard Event

We also support a wildcard (*) that will match all supported events. When you add the wildcard event, we'll replace any existing events you have configured with the wildcard event and send you payloads for all supported events. You'll also automatically get any new events we might add in the future.
