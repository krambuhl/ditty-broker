# Herodotus Explorer

Provides an API for querying ngwenya data.

## Goals

Get personnel for a song/release:

```js
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

```

Get songs for a specific person:

```js
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
