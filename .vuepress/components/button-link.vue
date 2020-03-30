<template>
  <div>
    <button class="button-link">Email confirmation.pdf</button>
    <button class="button-link disabled">Email confirmation.pdf</button>
    <div class="button-link-group">
      <button class="button-link">
        <span class="icon icon-add" />
        <span class="text">Add new item</span>
      </button>
      <button class="button-link">
        <span class="icon icon-delete" />
        <span class="text">Delete item</span>
      </button>
      <button class="button-link" disabled>
        <span class="icon icon-delete" />
        <span class="text">I'm disabled</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
$color-button-link: #1a0dab;
$color-button-link-hover: #660099;
$color-text: #404040;

.button-link {
  display: inline-block;
  background: none;
  border: 0;
  outline: 0;
  cursor: pointer;
  color: $color-button-link;
  font-size: 14px;
  text-decoration: underline;

  &:hover {
    color: $color-button-link-hover;
  }

  &[disabled],
  &.disabled {
    opacity: .6;
    cursor: not-allowed;
    color: inherit;
  }

  &-group {
    display: inline-block;
    margin-left: 15px;;

    .button-link {
      text-decoration: none;
    }

    .text {
      text-decoration: none;
      border-bottom: 1px dashed $color-text;
      font-size: 16px;
      color: $color-text;
      font-weight: bold;

      &:hover {
        color: #3c4858;
      }
    }

    .icon {
      width: 16px;
      height: 16px;
      display: inline-block;
      background-size: cover;
      background-repeat: no-repeat;
      vertical-align: sub;
    }

    .icon-add {
      //background-image: url('../assets/images/icon-circle-add.svg');
    }

    .icon-delete {
      //background-image: url('../assets/images/icon-basket.svg');
    }
  }
}

</style>