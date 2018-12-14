# vue-interview
This is a starter kit for interviews.

## Setup
```
npm i -g @vue/cli
npm install
```

## Develop
```
npm run serve
```

# Requirements
## Internship
- Only screen resolution what will be tested is 360x640. (mobile)

**Must**
- The text within the menubar should say `To Do List` instead of `menu`.
- The text `menu` should be vertically centered within the menu bar.
- The menu bar should stay at the top, even if the user scrolls down.
- The menubar should have a drop shaddow.
- The the input field should have a blue drop shaddow if it's focussed.
- The `Add` button should be green.


**Should**
- If you click `Add`, there will be a item appended to the list with the content of the input.
- Disable the `Add` button if the input is empty.
- If you press `Enter` while the input is focussed. The same behaviour will be executed as the `Add` button.
- There should be a `Remove` button in every `Item` (on the right).
- The `Remove` button should be red.
- If you click `Remove`, the corresponding item should disappear from the list.


**Could**
- Works in IE11 with only possible visual bugs.
- Move the `div` with the class `item-creator` to a seperate component called `ItemCreator`. The functionality should still work, while the `Item` components are still a direct child of the `App` component.
- Use `SASS` or `LESS` for the styles in stead of `CSS`.
- The input field should as wide as the remaining width next to the button.
- Every second `Item` element should have a darken background color `#e0e0e0`.

**Would**
- Works in IE11 without bugs.
- If you refresh the page, the content is still the same. **Including the items you added!**