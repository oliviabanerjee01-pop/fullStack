# Flexbox Notes

## Properties on the container
- `justify-content` → moves items left/right (main axis)
- `align-items` → moves items up/down (cross axis)
- `flex-direction` → changes which way the row runs
- `flex-wrap` → allows items to spill onto next row
- `flex-flow` → shortcut for direction + wrap
- `align-content` → moves multiple rows up/down as a group

## Properties on individual items
- `order` → changes position of one item in the row
- `align-self` → overrides align-items for one item

## Key rule
When flex-direction is column, justify and align swap axes.