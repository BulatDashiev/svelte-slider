# svelte-slider

Simple svelte range slider component

## Install

Install with npm or yarn:

```bash
TODO
```

Then import `Slider` component to your Svelte app.

```js
TODO
```

## Usage

### Simple usage
```html
<Slider bind:value >
```

### Range input
```html
<Slider bind:value range />
```

### Min, max and step
```html
<Slider min="-50" max="50" step="10" bind:value range />
```

You can `bind`  to min, max and value, slider will change according to props change

### Slots

Default slot
```html
<Slider bind:value>
  <span style="font-size: 20px;">&#128079;</span>
</Slider>
```

Left, right slots
```html
<Slider bind:value range>
  <span slot="left" style="font-size: 20px;">&#128078;</span>
  <span slot="right" style="font-size: 20px;">&#128077;</span>
</Slider>
```

## Props

|Name|Type|Default|Description|
|---|---|---|---|
|value|Array [number, number]|`[min, max]`||
|min|number|`0`||
|max|number|`100`||
|step|number|`1`||
|name|Array [string, string]|empty array|Provide names to inputs if you want use slider in form input|
|range|boolean|`false`|Set to `true` to use range input|
|order|boolean|`false`|Set to `true` if you want value[0] always be greater then value[1]|

## Slots

- `default` - customizes both thumbs if `left` or `right` slots isn't provided
- `left` - provide to customize left thumb
- `right` - provide to customize right thumb


## Events

- `input` - event fires when the value changes within thumb drag

## Style

```css
:root {
  --track-bg: #ebebeb;
  --progress-bg: #8abdff;
  --thumb-bg: #5784fd;
}
```

set `--thumb-bg` to `transparent` if you use custom thumb
```css
:root {
  --thumb-bg: transparent;
}
```

## License

MIT &copy; BulatDashiev