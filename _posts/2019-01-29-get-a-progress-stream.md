---
category: 'Progress'
apipath: '/progress/stream'
title: 'Get a Progress Stream'
type: 'GET'
---

This endpoint allows getting a event stream for a progress key. **This should be done after calling the** [`/translate`](#/translate) **endpoint.**

### Parameters

#### Required

- `progressKey`: The progress key to get the event stream for.

### Response

The response is an event stream (text/event-stream).

#### Example
```
...

data: Loading phrases...
data: Loading synonyms...
data: Interpreting...

...
```
