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
- The input field should have a blue drop shadow if it's focussed.
- The `Add` button should be green.


**Should**
- If you click `Add`, there will be a item appended to the list with the content of the input.
- Disable the `Add` button if the input is empty.
- If you press `Enter` while the input is focussed, the same behaviour will be executed as the `Add` button.
- There should be a `Remove` button in every `Item` (on the right).
- The `Remove` button should be red.
- If you click `Remove`, the corresponding item should disappear from the list.
- The footer should have a minimal height of `10rem`.
- The footer should contain a copyright symbol. 

**Could**
- Works in IE11 with only possible visual bugs.
- Move the `div` with the class `item-creator` to a seperate component called `ItemCreator`. The functionality should still work, while the `Item` components are still a direct child of the `App` component.
- Use `SASS` or `LESS` for the styles in stead of `CSS`.
- The input field should as wide as the remaining width next to the button.
- Every second `Item` element should have a darken background color `#e0e0e0`.

**Would**
- Works in IE11 without bugs.
- If you refresh the page, the content is still the same. **Including the items you added!**
- The footer should stick to the bottom if the content is smaller then the viewport.

**Extra mile**
- If you `Add` a new to do list `Item`. The content must be encrypted using the `sha-256` algorithm.
- If you click a to do list `Item`. Show a popup with the decrypted content.