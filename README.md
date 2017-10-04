# eu-energy-label

A (vanilla) Web Component to show an EU Energy Label.

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/elvomka/eu-energy-label)

## Demo

Example how to create a "Directive 2010/30/EU" energy label (colors need adjustment, see next demo):
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-loader.js"></script>
    <link rel="import" href="eu-energy-label.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<div style="width:300px">
  <eu-energy-label efficiency-classes="A+++,A++,A+,A,B,C,D"
                   selected-class="A++">
  </eu-energy-label>
</div>
```

Example of of arbitrary label content and using the CSS custom properties:
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-loader.js"></script>
    <link rel="import" href="eu-energy-label.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<div style="width:300px">
  <style type="text/css" scoped>
    eu-energy-label {
      --efficiency-class-background-1: linear-gradient(#9aff9a, #0f0);
      --efficiency-class-background-2: linear-gradient(#ffff9a, #ff0);
      --efficiency-class-background-3: linear-gradient(#d6485b, #f00);
    }
  </style>
  <eu-energy-label efficiency-classes="green,yellow,red"
                   selected-class="green">
  </eu-energy-label>
</div>
```
## Usage

In order to use the `eu-energy-label`, you need to configure two parameters:

* efficiency classes: The available energy efficiency classes to display
* selected class: The selected (active) energy efficiency class to highlight

These parameters can either be set via attribute- or property-value on the `eu-energy-label` instance.


### Attributes and properties

To configure the available 'efficiency classes', use either the `efficiency-classes` attribute or the `efficiencyClasses` property and pass it a comma-separated list of labels for the efficiency classes you want to display. The order of the items in the comma-separated list will go from the top to the bottom of the efficiency scale.

To configure the 'selected class' that will be highlighted, use the `selected-class` attribute or the `selectedClass` property and pass it a value that also exists in the 'efficiency classes' list.

### CSS custom properties

The webcomponent exposes a number of CSS custom properties (variables) which allow to customize the look of the rendered energy efficiency label. For details, please have a look at the top of the file `eu-energy-label.html`.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

MIT License
