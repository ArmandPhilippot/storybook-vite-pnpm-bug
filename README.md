# Storybook Vite Pnpm Bug

## Requirements

* `pnpm`

## To Reproduce

1. Clone this repo
2. `pnpm i`
3. `pnpm storybook`

## Error messages

### Before adding `@mdx-js/mdx`

With Firefox:
* `error loading dynamically imported module`

With Chromium, the error message is more detailed:
* `Failed to fetch dynamically imported module: http://localhost:6006/src/stories/Introduction.stories.mdx?import`


### After adding `@mdx-js/mdx`

With Firefox:
* `import not found: mdx`

Once again, with Chromium, the error message is clearer:
* `The requested module '/node_modules/.vite-storybook/deps/@mdx-js_react.js?v=497b04c7' does not provide an export named 'mdx'`

### Finally

Adding `@mdx-js/react` changes nothing. I also tried `@storybook/mdx2-csf` but without improving things. It is always the same error.
