# Roadmap

An overview of what the core Polymer team is looking to work on over the next few months.

As a caveat - this is a living doc, and will evolve as priorities grow and shift. The Polymer project will always be adapting to new use-cases and evolutions in the platform - this roadmap is more of a "North Star" of what we're looking to work on than a strict timeline.

Please feel free to file issues on this repository if you have questions, concerns, or suggestions.

### Core Library

**Improve ergonomics**

The Polymer library is essentially an ergonomic layer over Web Components. We're always looking to make the library more intuitive, make it do "what you expect", and make you successful-by-default when building with it.

* Explore improving the way object observation works in the data-binding system, specifically around notifying any changes when observing something like `object.*`.
* Fix and make the usage of `undefined` consistent throughout the library.
* Explore creating either a layer, or additional documentation and guidance, around supporting "action-at-a-distance"-style data-binding.
* Look into creating something along the lines of `array-selector` but for objects.

**Improve styling system**

* Close p1 issues - get solid baseline for styling.
* Explore interaction between forthcoming native CSS properties and the current styling system, making sure Polymer is ready to take advantage of native CSS properties when they land cross-browser.
* Support dynamism in applying styling system when using `Polymer.dom`.
* Support method/tool for loading external stylesheets.

**Improve code hygiene**

* Explore refactoring annotations & effects.
* Explore refactoring `polymer-micro` and `polymer-mini` layering.

### Performance

* Create tool for measuring an element's "cost" - its creation time weight.
* Explore enhancing performance of `iron-list` and `dom-repeat`, to more ergonomically support long lists of items.
* Improve basic element instantiation performance - make creating a basic Polymer element 10% faster.
* Make `paper-button` 2x as fast to create.

### Elements

We keep element roadmaps on each element product line's meta-repo:

* [Paper Elements](https://github.com/polymerelements/paper-elements)
* [Iron Elements](https://github.com/polymerelements/iron-elements)
* [Gold Elements](https://github.com/polymerelements/gold-elements)
* [Platinum Elements](https://github.com/polymerelements/platinum-elements)
* [Neon Elements](https://github.com/polymerelements/neon-elements)

### Application Rails

The Polymer library is specifically focused on making it easy to create encapsulated elements. This has always been and will continue to be the scope of the library itself.

But the project overall wants to help with much more than that - to make it easy for anyone to build high-quality experiences on the web. We do this by providing elements built using the library as well as tools to make development and productionization easier.

With a solid foundation with the library and element product lines, we're looking to move up the stack and provide better guidance around how to build entire applications out of elements, without the need for a single overarching "framework." Instead, we're looking to provide app-structure features in the form of elements, so you can use exactly what you need to build applications in an ergonomic and idiomatic way. These elements are tentatively named the `Carbon` elements.

* Prototype an idiomatic "router" element.
* Prototype a lazy-loading solution to be able to dynamically load new markup from a server when it is needed.
* Explore a l10n solution for translating strings.
* Explore RTL support for all elements.
* Prototype a set of layout elements that make structuring responsive applications more straightforward.

It is important to note that these are not additions to the core Polymer library - the scope of the library itself will be unchanged. We'll enable these with new elements built with the library, that you only use if you'd like to.

### Tooling

* Build a solution for sharded vulcanization, to be able to dynamically load only parts of an application as-needed.
* Release a tool to lint Polymer code.
* Prototype a development-time Polygit tool, to be able to develop an application out of elements without needing any package manager.
* Prototype a vulcanize tool to work with Polygit, so that you can build and deploy your application entirely without needing client-side package management.


### Operations

As the Polymer project grows we're working on building out our own tool support to enable greater productivity within the team and community.

* Have consistent labels across all repos
* Institute clear requirements for filing issues - asking for a repro or test codebase
* Institute clear requirements for adding a PR - asking for tests with every change
* Shift CI to Travis for all repos
* CI should fail on jscompiler failures
* CI should fail on linter errors
