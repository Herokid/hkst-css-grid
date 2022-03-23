# BEM CSS GRID
Flexbox grid system with BEM notation.

## Basic markup structure with auto width columns
If you don't use columns modifier classnames the columns has auto width.
In this example the grid system have 12 columns and each .g-col element in this markup use 3 columns space(3*4=12)
```scss
<div class="g-wrap">
    <div class="g-row">
        <div class="g-col">
            <!-- Your content -->
        </div>
        <div class="g-col">
            <!-- Your content -->
        </div>
        <div class="g-col">
            <!-- Your content -->
        </div>
        <div class="g-col">
            <!-- Your content -->
        </div>
    </div>
</div>
```

## Basic markup structure with columns width by breakpoint
*(Very similar html markup than bootstrap grid)*
```scss
<div class="g-wrap">
    <div class="g-row">
        <div class="g-col--xs-6">
            <!-- Your 6 columns content in all  breakpoints -->
        </div>
        <div class="g-col--xs-6">
            <!-- Your 6 columns content in all  breakpoints -->
        </div>
        <div class="g-col--sm-6 g-col--md-4">
            <!-- Your 6 columns content since 'small' breakpoint -->
            <!-- Your 4 columns content since 'medium' breakpoint -->
        </div>
        <div class="g-col--sm-6 g-col--md-4">
            <!-- Your 6 columns content since 'small' breakpoint -->
            <!-- Your 4 columns content since 'medium' breakpoint -->
        </div>
        <div class="g-col--lg-4">
            <!-- Your 4 columns content since 'large' breakpoint -->
        </div>
    </div>
</div>
```

## Customization
You can custom this sass variables:

### Grid width
```scss
$grid-width: 100% !default;
```
### Grid columns
```scss
$grid-columns: 12 !default;
```
### Grid main gutter
```scss
$grid-gutter: 14px !default;
```
### Grid breakpoints for .g-col--[BREAKPOINT]-[COLUMNS] *modifier*
```scss
$grid-breakpoints: ( "xs" : 0px, "sm" : 768px, "md" : 992px, "lg" : 1200px) !default;
```
### Grid gutter *modifiers* for .g-row *block*
```scss
$grid-gutter-modifiers: ( "xs" : 0.25, "sm" : 0.75, "md" : 1.5, "lg" : 1.75) !default;
```