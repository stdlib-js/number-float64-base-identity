<!--

@license Apache-2.0

Copyright (c) 2020 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Identity Function

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Evaluate the [identity function][identity-function] of a double-precision floating-point number.

<section class="intro">

The [identity-function][identity-function] is defined as

<!-- <equation class="equation" label="eq:identity_function" align="center" raw="f(x) = x" alt="Identity function"> -->

```math
f(x) = x
```

<!-- <div class="equation" align="center" data-raw-text="f(x) = x" data-equation="eq:identity_function">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@ad7afa5d7ec1b1596f8a4828153d8c2e87a90161/lib/node_modules/@stdlib/number/float64/base/identity/docs/img/equation_identity_function.svg" alt="Identity function">
    <br>
</div> -->

<!-- </equation> -->

for all `x`.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/number-float64-base-identity
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var identity = require( '@stdlib/number-float64-base-identity' );
```

#### identity( x )

Evaluates the [identity function][identity-function] for a double-precision floating-point number.

```javascript
var v = identity( -1.0 );
// returns -1.0

v = identity( 2.0 );
// returns 2.0

v = identity( 0.0 );
// returns 0.0

v = identity( -0.0 );
// returns -0.0

v = identity( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var identity = require( '@stdlib/number-float64-base-identity' );

var rand;
var i;

for ( i = 0; i < 100; i++ ) {
    rand = round( randu() * 100.0 ) - 50.0;
    console.log( 'identity(%d) = %d', rand, identity( rand ) );
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/number/float64/base/identity.h"
```

#### stdlib_base_float64_identity( x )

Evaluates the identity function for a double-precision floating-point number.

```c
double y = stdlib_base_float64_identity( 2.0 );
// returns 2.0
```

The function accepts the following arguments:

-   **x**: `[in] double` input value.

```c
double stdlib_base_float64_identity( const double x );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/number/float64/base/identity.h"
#include <stdio.h>

int main( void ) {
    const double x[] = { 3.14, -3.14, 0.0, 0.0/0.0 };

    double y;
    int i;
    for ( i = 0; i < 4; i++ ) {
        y = stdlib_base_float64_identity( x[ i ] );
        printf( "f(%lf) = %lf\n", x[ i ], y );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/number-float32/base/identity`][@stdlib/number/float32/base/identity]</span><span class="delimiter">: </span><span class="description">evaluate the identity function for a single-precision floating-point number.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/number-float64-base-identity.svg
[npm-url]: https://npmjs.org/package/@stdlib/number-float64-base-identity

[test-image]: https://github.com/stdlib-js/number-float64-base-identity/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/number-float64-base-identity/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/number-float64-base-identity/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/number-float64-base-identity?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/number-float64-base-identity.svg
[dependencies-url]: https://david-dm.org/stdlib-js/number-float64-base-identity/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/number-float64-base-identity/tree/deno
[deno-readme]: https://github.com/stdlib-js/number-float64-base-identity/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/number-float64-base-identity/tree/umd
[umd-readme]: https://github.com/stdlib-js/number-float64-base-identity/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/number-float64-base-identity/tree/esm
[esm-readme]: https://github.com/stdlib-js/number-float64-base-identity/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/number-float64-base-identity/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/number-float64-base-identity/main/LICENSE

[identity-function]: https://en.wikipedia.org/wiki/Identity_function

<!-- <related-links> -->

[@stdlib/number/float32/base/identity]: https://github.com/stdlib-js/number-float32-base-identity

<!-- </related-links> -->

</section>

<!-- /.links -->
