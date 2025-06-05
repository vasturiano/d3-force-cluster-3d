### ⚠️ Note: This module is now deprecated! Please use [d3-force-clustering](https://github.com/vasturiano/d3-force-clustering) instead. ⚠️

d3-force-cluster-3d
===================

[![NPM package][npm-img]][npm-url]
[![Build Size][build-size-img]][build-size-url]
[![NPM Downloads][npm-downloads-img]][npm-downloads-url]

This is a 3D port of [d3-force-cluster](https://github.com/ericsoco/d3-force-cluster), a force type that attracts nodes toward a set of cluster centers.

This force plugin is compatible with [d3-force-3d](https://github.com/vasturiano/d3-force-3d) and can function in a one, two or three dimensional space.

## Quick start

```js
import d3ForceCluster from 'd3-force-cluster-3d';
```
or using a *script* tag
```html
<script src="//cdn.jsdelivr.net/npm/d3-force-cluster-3d"></script>
```
then
```js
d3.forceSimulation()
    .nodes(<myNodes>)
    .force('cluster', d3.forceCluster()
        .centers(node => clusters[node.cluster])
    );
```

## API reference

| Method | Description | Default |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- | ------------- |
| <b>centers</b>([<i>fn</i>]) | Getter/setter for the accessor function (`fn(node)`) to define each node's cluster center. All cluster centers should be defined as a radius and set of coordinates `{ radius, x, y, z }`, according to the number of spatial dimensions in the simulation. | `node => ({ x: 0, y: 0, z: 0 })` |
| <b>strength</b>([<i>num</i>]) | Getter/setter for the force strength. The value must be within the [0,1] range. This parameter determines the attraction strength of each node to the specified cluster center. | 0.1 |
| <b>centerInertia</b>([<i>num</i>]) | Getter/setter for the inertia of cluster center nodes. The value must be within the [0,1] range. Lower values (close to 0) result in cluster center nodes with lower inertia: they are easily pulled around by other nodes in the cluster. Higher values (close to 1) result in cluster center nodes that are moved very little by other nodes in the cluster. | 0 |

[npm-img]: https://img.shields.io/npm/v/d3-force-cluster-3d
[npm-url]: https://npmjs.org/package/d3-force-cluster-3d
[build-size-img]: https://img.shields.io/bundlephobia/minzip/d3-force-cluster-3d
[build-size-url]: https://bundlephobia.com/result?p=d3-force-cluster-3d
[npm-downloads-img]: https://img.shields.io/npm/dt/d3-force-cluster-3d
[npm-downloads-url]: https://www.npmtrends.com/d3-force-cluster-3d
