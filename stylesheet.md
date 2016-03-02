# Aloha Code Guide

> Code Guide Stylesheets
> 
> This code guide is based on [MDO][1] CSS and [Idiomatic CSS][2]
> If in doubt, use one of these, giving priority to the MDO

> "Arguments over style are pointless. There should be a style   guide, and you should follow it"
 _Rebecca Murphey_

## Syntax

- Use soft tabs with two spaces
- Grouping selector, keep individual selectors in a single line
- DON'T use braces, semicolon or colon (this is stylus, plis)
- One Declaration per line
- Include a space when separate comma, except on functions
- DON'T use leadings zero
- Lowercase hex values
- Use shorthand hex values when available
- SINGLE QUOTES!
- Avoid specify units for zero
- Use only 2 levels of nesting (not including pseudo-class like `:hover`)

## Comments

Describe your component if this isn't obvious
```stylus
// Your Component
// ----------------------------------------------------------------------------|
// 
// Describe your component, if necessary use html makrup to explain
// @todo Somothing to do later
```

## Declaration Order

1. Placeholders
2. Mixins
3. Function
4. Positions
5. Box Model
6. Typography
7. Visual

```stylus
.awesome-component
	@extend $placeholder
    $mixin($param, $param)
    /** Positions */
    position relative
    /** Box Model */
    display block
	/** Typography */
    font-size 1.6rem
    /** Visual */
    background-color $component-background
```

## Imports

Import all files in `assets/stylus/_app.styl`. Don't worry gulp is look for this file.

## Class Names

Class names is based [rscss][3] with some changes conventions based in components and Elements

- Use class ever is possible
- Avoid tag selectors

### Components

- Like Button `.like-button`
- Search Form `.search-form`
- News Article Card `.article-card`

### Elements

We don't use `>` selector

```stylus
.article-card
	.title 
	.author       
```

### Variants
For variants uses another class

```stylus
.article-card
	&.main
    
    .title
    .author
    .author.small
```

[1]: http://mdo.github.io/code-guide/#css "MDO Code Guide"
[2]: https://github.com/necolas/idiomatic-css/tree/master/translations/pt-BR "Idiomatic CSS"
[3]: http://rscss.io/ "Rscss"
