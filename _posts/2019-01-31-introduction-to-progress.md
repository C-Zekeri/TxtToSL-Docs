---
title: 'Introduction to Progress'
category: 'Progress'
---

Progress Keys are how the API / Server / Backend keep track of the progress of each request. How to use them:

1. Get a progress key via the [`/progress/key`](#/get-a-progress-key) endpoint
2. Provide progress key to [`/translate`](#/translate) endpoint
3. Provide progress key to [`/progress/stream`](#/get-a-progress-stream) endpoint
4. Get progress / events returned by the event stream, gotten from the [`/progress/stream`](#/get-a-progress-stream) endpoint above
