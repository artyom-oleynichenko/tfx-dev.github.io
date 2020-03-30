<template>
  <div>
    <button class="button">Button default</button>
    <button class="button" disabled>Button disabled</button>

    <button class="button button-white">Button white</button>
    <button class="button button-white" disabled>Button disabled</button>
    <br><br>
    <button class="button button-small">Button small</button>
    <button class="button button-white button-small">Button white and small</button>

    <button class="button button-extra-small">Update</button>
    <button class="button button-white button-extra-small">Save</button>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "./styles/beyonce-styles";

$color-button: #2586ea;
$color-button-hover: #1a6dbd;
$color-button-disabled: #6ac6ff;
$color-white: #fff;

.button {
  position: relative;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  vertical-align: top;
  padding: 8px 12px;
  min-width: 93px;
  min-height: 42px;
  border-radius: 4px;
  font-family: 'PT Sans', sans-serif;
  font-size: 14px;
  font-weight: 700;
  overflow: hidden;
  outline: none;
  line-height: 1.7;
  text-align: center;
  text-overflow: ellipsis;
  text-decoration: none;
  white-space: nowrap;
  user-select: none;
  transition: all .3s ease;
  color: $color-white;
  border: 1px solid transparent;
  background: $color-button;
  cursor: pointer;

  &.disabled,
  &[disabled] {
    background: #6ac6ff;
    cursor: not-allowed;

    &:hover {
      background: #6ac6ff;
    }
  }

  &:hover {
    background: $color-button-hover;
  }

  + .button {
    margin-left: 5px;
  }

  &-small {
    max-height: 36px;
    min-height: 36px;
    padding: 0 12px;
  }

  &-extra-small {
    min-width: 70px;
    max-height: 27px;
    min-height: 27px;
    padding: 0 10px;
  }
}

.button-white {
  background: $color-white;
  color: $color-button;
  border: 1px solid $color-button;
  font-weight: normal;

  &:hover {
    color: $color-white;
    background: $color-button;
  }

  &.disabled,
  &[disabled] {
    background: $color-white;
    opacity: .6;
    cursor: not-allowed;

    &:hover {
      background: $color-white;
      color: $color-button;
    }
  }
}
</style>