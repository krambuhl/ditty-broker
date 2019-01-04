# Herodotus Explorer

Provides an API for querying ngwenya data.

## Goals

```js
// get personnel for a song/release
const likeAStonePersonnel = await herodotus.getPersonnel({
  title: 'Like a Stone',
  artist: 'Audioslave'
})

/*
[{
  id: '12349532',
  name: 'Chris Cornell',
  role: 'vocals'
}, {
  name: 'Tim Commerford',
  role: 'bass'
}, {
  name: 'Brad Wilk',
  role: 'drums'
}, {
  name: 'Tom Morello',
  role: 'guitars'
}, {
  name: 'Rick Rubin',
  role: 'producer'
}, {
  name: 'Rich Costey',
  role: 'mixer'
}, {
  name: 'David Schiffman',
  role: 'engineer'
}]
*/

// get songs for a specific personnel
const chrisCornellSongs = await herodotus.getSongs({
  id: '12349532'
  name: 'Chris Cornell'
})

/*
[{
  id,
  title: 'Like a Stone',
  artist: 'Audioslave',
  album: 'Audioslave'
}, {
  title: 'Nearly Forgot My Broken Heart',
  artist: 'Chris Cornell',
  album: 'Higher Truth'
}, {
  title: 'Spoonman',
  artist: 'Soundgarden',
  album: 'Superunknown'
}]
*/
```
