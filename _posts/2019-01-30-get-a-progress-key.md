---
category: 'Progress'
apipath: '/progress/key'
title: 'Get a Progress Key'
type: 'GET'
---

This endpoint allows getting a progress key. **Progress keys are not required to be gotten this way, you can specify your own, but it is the recommended and best way.**

### Parameters

#### Optional

- `prefix`: Allows specifying a prefix to the progress key returned. The prefix has to be characters within the regex pattern: `/[a-zA-Z0-9]/g` (English letters and numbers), anything that does not match that pattern will be removed. If no prefix is provided, it will be set to `''` (blank / nothing).

### Response

The response is in plain text (text/plain).

#### Format

```
{prefix}-{id}
```

- `prefix`: The prefix parameter provided, explained above.
- `id`: The randomly generated ID, a random 128 bit hexadecimal string.

#### Example
```
APIDocs-70b23c8b4cb2ef30ac186f75fed61d9d5b25c39...
```
