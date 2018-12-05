---
title: Component Specification

# Navigation config
nav_display: true
nav_label: Components
nav_order: 15
---

# {{page.title}}

Origami components are repositories containing front end code which can be used as part of a web page. Components are intended to be reusable UI patterns or functions; examples of good use-cases for components are:

  - A sortable table
  - A cookie notice
  - A consistent top navigation
  - Functions to track user behaviour


## Origami.json manifest

All Origami components _must_ contain an `origami.json` file at the top of the repository's directory structure. The [`origami.json` manifest specification](/spec/v1/manifest/) covers the contents of this file. In addition to the rules outlined in the manifest specification, Origami components _must_ set the `type` property in the JSON to `"module"`.

<aside>
	The <code>type</code> of <code>"module"</code> is a hangover from when client-side Origami components were named "modules". It's likely to change in a later version of the spec.
</aside>


## Naming conventions

Components _must_ be named using a short descriptive term (hyphenated if necessary) and _should_ be prefixed with `o-` (for Origami). The name _must_ only contain lower-case letters and hyphens. This name _must_ be used as the repository name, the `name` property in `origami.json`, and as a prefix for any default CSS class names.

<aside>
	Examples of good component names include <code>o-colors</code>, <code>o-grid</code>, <code>o-cookie-message</code>.
</aside>

If a component is not maintained by the Origami team, then it _may_ be prefixed with a different letter than `o-`, E.g. `n-button`, `g-audio`. This practice is discouraged, it's preferred that authors specify a support contact other than Origami in the component manifest.


## Folder structure

_This section is non-normative._

A component's folder structure _may_ be organised as follows. The following is what the Origami team use for all of their supported components, but it's not a requirement.

<aside class="no-padding">
<p><a href="https://github.com/Financial-Times/origami-build-tools" class="o-typography-link--external" target="_blank">Origami Build Tools</a> provides a useful command to generate a component boilerplate in this style for you:</p>
<pre style="white-space: normal; word-break: keep-all;"><code class="o-syntax-highlight--bash">npx origami-build-tools init o-example-component</code>
</pre>
</aside>

<pre><code class="o-syntax-highlight--bash">.
├── demos
│   └── src (containing Mustache files)
├── src
│   ├── js (containing JavaScript files)
│   └── scss (containing SCSS files)
├── test (containing JavaScript and Sass tests)
├── bower.json
├── README.md
├── main.js
├── main.scss
├── origami.json
└── package.json</code>
</pre>


## Requirements

TODO this should possibly be multiple headings.

[Current documentation](https://origami.ft.com/docs/component-spec/modules/#requirements) seems to use this as a bucket list of stuff that doesn't fit elsewhere?