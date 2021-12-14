
![image](https://user-images.githubusercontent.com/11935062/146062732-3d2aad7a-f2d6-44e5-8d4e-cfb55c024119.png)
Smells de Complejidad cognitiva
![image](https://user-images.githubusercontent.com/11935062/146062896-52d04eeb-c3a7-4621-b64d-9af18748e199.png)
![image](https://user-images.githubusercontent.com/11935062/146062846-3d360c8b-69f2-40f8-bc5c-eb15be29ef33.png)
![image](https://user-images.githubusercontent.com/11935062/146063026-fab6ccd5-a32e-45c1-85e8-1d853ff00b6d.png)

Falsos Positivos 
![image](https://user-images.githubusercontent.com/11935062/146062985-d4f841a9-63e3-4c1a-9ff2-7f0a7fffbe0b.png)
![image](https://user-images.githubusercontent.com/11935062/146063089-fa8409de-c176-4fdc-8dcc-32c001e28943.png)


# [react-hn](https://insin.github.io/react-hn)

A [React](http://facebook.github.io/react) &
[react-router](https://github.com/rackt/react-router)-powered implementation of
[Hacker News](https://news.ycombinator.com) using its
[Firebase API](https://github.com/HackerNews/API).

[![react-hn screenshot](https://github.com/insin/react-hn/raw/master/screenshot.png "New comment highlighting in react-hn")](https://insin.github.io/react-hn)

Live version: https://insin.github.io/react-hn

## Features

* Supports display of all item types:
  [stories](https://insin.github.io/react-hn/#/story/8863),
  [jobs](https://insin.github.io/react-hn/#/job/8426937),
  [polls](https://insin.github.io/react-hn/#/poll/126809) and
  [comments](https://insin.github.io/react-hn/#/comment/8054455)
* Basic [user profiles](https://insin.github.io/react-hn/#/user/patio11)
* Collapsible comment threads, with child counts
* "Realtime" updates (free via Firebase!)
* Last visit details for stories are cached in `localStorage`
* New comments are highlighted:
  * Comments since your last visit to an item
  * New comments which load while you're reading an item
  * New comments in collapsed threads
* Automatic or manual collapsing of comment threads which don't contain any new
  comments
* Manual highlighting of the X most recent comments to catch up on threads you were reading elsewhere
* Stories with new comments are marked on list pages
* Stories can be marked as read to remove highighting from new comments
* "comments" sections driven by the Changed Items API
* Story listing pages are cached in `sessionStorage` for quick back button usage
  and pagination in the same session
* Configurable settings:
  * auto collapse - automatically collapse comment threads without new comments
    on page load
  * show reply links - show "reply" links to Hacker News
  * show dead - show items flagged as dead
  * show deleted - show comments flagged as deleted in threads
* Delayed comment detection - so tense! Who will it be? What will they say?

[Feature requests are welcome!](https://github.com/insin/react-hn/issues/new)

## Building

Install dependencies:

```
npm install
```

### npm scripts

* `npm start` - start development server
* `npm run build` - build into the `dist/` directory
* `npm run lint` - lint `src/`
* `npm run lint:fix` - lint `src/` and auto-fix issues where possible

## MIT Licensed
