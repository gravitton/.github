<div align="center" width="100%">

<a href="https://github.com/gravitton">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gravitton/.github/refs/heads/main/profile/logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gravitton/.github/refs/heads/main/profile/logo-light.svg">
  <img alt="Gravitton" src="https://raw.githubusercontent.com/gravitton/.github/refs/heads/main/profile/logo-light.svg" width="300">
</picture>
</a>

[![Stars][ico-stars]][link-repositories]
[![Go Dev Reference][ico-go-dev-reference]][link-go-dev-reference]
[![Go Version][ico-go-version]][link-go]
[![Software License][ico-license]][link-license]
[![Blog][ico-blog]][link-blog]

Go libraries for game development

<hr>

</div>

Generic, allocation-conscious and tested to 100% coverage, with results that stay bit-identical
across amd64 and arm64.

## Libraries

One map of walls, rough ground, a scout and a goal, drawn by each library in turn: as shapes,
as hexes, and as grids of every layout. Each library builds on the one before it.

### [geometry][link-geometry]

Immutable 2D geometry: points, vectors and shapes with their tests, casts and constructions.

<p align="center">
<a href="https://github.com/gravitton/geometry">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gravitton/geometry/refs/heads/main/docs/images/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gravitton/geometry/refs/heads/main/docs/images/hero-light.svg">
  <img alt="The map drawn with geometry: the scout's view cast by rays that stop at the walls, with one ray reflected until it reaches the goal, the scout swept toward the goal until it hits a wall, and a Bezier route to the goal, checked against the wall edges" src="https://raw.githubusercontent.com/gravitton/geometry/refs/heads/main/docs/images/hero-light.svg">
</picture>
</a>
</p>

### [hexagon][link-hexagon]

Hexagonal grid math: coordinates, rings, lines, line of sight and field of view.

<p align="center">
<a href="https://github.com/gravitton/hexagon">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gravitton/hexagon/refs/heads/main/docs/images/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gravitton/hexagon/refs/heads/main/docs/images/hero-light.svg">
  <img alt="The map in hexes: the scout's field of view, its line to the goal, hidden behind a wall, and its field of view in a sector toward the goal" src="https://raw.githubusercontent.com/gravitton/hexagon/refs/heads/main/docs/images/hero-light.svg">
</picture>
</a>
</p>

### [grid][link-grid]

2D grids with rectangular, isometric and hexagonal layouts, range and sight queries, and
pathfinding, on geometry, hexagon and container.

<p align="center">
<a href="https://github.com/gravitton/grid">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gravitton/grid/refs/heads/main/docs/images/hero-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gravitton/grid/refs/heads/main/docs/images/hero-light.svg">
  <img alt="The map on a rectangular, an isometric and a pointy-top grid: on each the scout's field of view and its cheapest path to the goal around the rough ground" src="https://raw.githubusercontent.com/gravitton/grid/refs/heads/main/docs/images/hero-light.svg">
</picture>
</a>
</p>

### Supporting libraries

- [container][link-container]: generic containers, a table of values per index and an
  immutable sorted set, on geometry.
- [spatial][link-spatial]: broad-phase spatial indexes, a spatial hash with box, point and cast
  queries and touching pairs, on geometry.
- [assert][link-assert]: lightweight test assertions.
- [errors][link-errors]: a drop-in superset of `errors` with fields, stack traces and
  multi-errors.

## Writing

Each post on the [blog][link-blog] takes one decision from these libraries and shows the code and
the numbers behind it.

- [Go libraries for 2D games: geometry, hexagon and grid][link-post-libraries] (2026-11-06): the
  three libraries on one map.

## Contributing

Bug reports and proposals are welcome in each library's issues. Please see
[Contributing][link-contributing] before opening a pull request, and [Security][link-security]
to report a vulnerability.

## License

Every library is released under the MIT License, in the `LICENSE.md` of its repository.


[ico-stars]:                https://img.shields.io/github/stars/gravitton?style=flat-square&color=e8883a
[ico-go-version]:           https://img.shields.io/github/go-mod/go-version/gravitton/geometry?style=flat-square&color=007d9c
[ico-go-dev-reference]:     https://img.shields.io/badge/go.dev-reference-007d9c?style=flat-square
[ico-license]:              https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square
[ico-blog]:                 https://img.shields.io/badge/blog-posts-e8883a?style=flat-square

[link-repositories]:        https://github.com/orgs/gravitton/repositories
[link-go]:                  https://go.dev/doc/devel/release
[link-go-dev-reference]:    https://pkg.go.dev/search?limit=25&m=package&q=github.com%2Fgravitton
[link-license]:             https://github.com/gravitton/geometry/blob/main/LICENSE.md
[link-contributing]:        https://github.com/gravitton/.github/blob/main/CONTRIBUTING.md
[link-security]:            https://github.com/gravitton/.github/blob/main/SECURITY.md
[link-geometry]:            https://github.com/gravitton/geometry
[link-hexagon]:             https://github.com/gravitton/hexagon
[link-grid]:                https://github.com/gravitton/grid
[link-container]:           https://github.com/gravitton/container
[link-spatial]:             https://github.com/gravitton/spatial
[link-assert]:              https://github.com/gravitton/assert
[link-errors]:              https://github.com/gravitton/errors
[link-blog]:                https://gravitton.github.io/blog/
[link-post-libraries]:      https://gravitton.github.io/blog/posts/gravitton-libraries/
