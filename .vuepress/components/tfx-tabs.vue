<template>
  <div :class="['tfx-tabs', customClass]">
    <a class="tab tab-link tab-active">
      <span class="tab-inner">
        Status/Notes
      </span>
    </a>
    <a class="tab tab-link">
      <span class="tab-inner">
        Info
      </span>
    </a>
  </div>
</template>

<script>
export default {
  props: ['customClass']
}
</script>

<style lang="scss" scoped>
@import "./styles/beyonce-styles";
html {
  font-size: 10px !important;
}
.tfx-tabs {
  font-size: 10px !important;
  border-bottom: .1rem solid $bd-color-grey-silver;
  margin-bottom: 1.5rem;
  padding-bottom: 1.1rem;
  width: 100%;
  user-select: none;

  &:nth-of-type(2) {
    margin-bottom: 1.5rem;
  }

  .tab {
    color: $bd-color-black;
    cursor: pointer;
    display: inline-block;
    font-size: $base-font-size;
    margin-right: 3.8rem;
    position: relative;
    text-decoration: none !important;

    &::after {
      border-top-left-radius: $small-border-radius;
      border-top-right-radius: $small-border-radius;
      bottom: -1.2rem;
      content: '';
      height: .4rem;
      background: transparent;
      left: 0;
      position: absolute;
      width: 100%;

      @include transition(all, ease-in-out, .1s);
    }

    &-active {
      cursor: default;
      pointer-events: none;

      &::after {
        height: .4rem;
      }
    }

    &:hover::after {
      height: .4rem;
    }

    &_counter {
      $measurments: 2.4rem;

      align-items: center;
      background-image: linear-gradient(157deg, $bd-color-blue-light, $bd-color-blue-darken);
      border-radius: 50%;
      color: $bd-color-white;
      display: flex;
      font-size: $base-font-size;
      font-weight: bold;
      height: $measurments;
      justify-content: center;
      min-width: $measurments;
      padding: .4rem;
      position: absolute;
      right: -2.8rem;
      top: -.5rem;

      &.big {
        right: -3.5rem;
      }
    }
  }

  &-blue {
    .tab {
      &-active {
        color: $bd-color-blue-dark;

        &::after {
          background-image: linear-gradient(166deg, $bd-color-blue-light, $bd-color-blue-darken);
        }
      }
    }
  }

  &-sky {
    .tab {
      color: $bd-color-grey-darkest;

      &::after {
        background: transparent;
      }

      &-active {
        color: $bd-color-blue-sky;

        &::after {
          background: $bd-color-blue-sky;
        }
      }
    }
  }

  &-simple {
    background: $bd-color-grey-platinum;
    border: 0;
    border-radius: 4px;
    padding: .8rem;

    .tab {
      margin-right: 1.9rem;
      opacity: .6;
      padding: 1rem 1.5rem .9rem 1.3rem;

      @include transition(all, ease-in-out, .1s);

      &::after {
        display: none;
      }

      &-active {
        background: $bd-color-white;
        border-radius: $base-border-radius;
        opacity: 1;

        @include transition(all, ease-in-out, .1s);
      }

      &.on-hover {
        background: $bd-color-white;
        opacity: 1;

        @include transition(all, ease-in-out, .1s);
      }
    }

    .notification__small {
      .icon-check-mark,
      .icon-attention {
        height: 1.7rem;
        margin-right: .5rem;
        width: 1.7rem;
      }
    }
  }

  &-small {
    align-items: center;
    background-color: #fff;
    border-radius: 1.6rem;
    box-shadow: .3rem .4rem .7rem -.1rem rgba(0, 33, 55, .13);
    display: flex;
    display: inline-flex;
    height: 3.2rem;
    overflow: hidden;
    padding: 0 .5rem;
    user-select: none;
    width: auto;

    &:not(.with-nav) {
      .nav {
        display: none;
      }

      .wrapper {
        width: 100%;
      }

      .scrollable .tab:last-child {
        margin-right: 0;
      }
    }

    &.with-nav {
      .scrollable {
        padding-right: 2rem;
      }
    }

    .container {
      align-items: center;
      display: flex;
      flex-wrap: nowrap;
      height: 100%;
      overflow: visible;
      width: 100%;
      border-radius: 1.6rem;
      margin: 0 auto;
    }

    .tab {
      display: flex;
      align-items: center;
      flex-wrap: nowrap;
      justify-content: center;
      margin-right: 1.3rem;
      text-decoration: none;
      font-weight: bold;
      border-radius: 1.6rem;
      padding: .5rem .7rem;
      color: #3c4858;
      transition: all .3s ease;

      &:last-child {
        margin-right: 0;
      }

      &:not(.tab-active):hover {
        background: rgba(217, 217, 217, .6);
      }

      &-active {
        color: white;
        background: #2586ea;
      }

      &-important {
        color: $bd-color-pizzas;
        .tab-name {
          color: $bd-color-pizzas;
        }
      }

      .icon {
        width: 1.4rem;
        height: 1.4rem;
        margin-right: .2rem;
        border-radius: 50%;

        &-lock {
          width: .6rem;
          height: .7rem;
          margin-right: 0;
        }
      }

      &-name {
        font-size: 1.4rem;
        word-break: keep-all;
        padding-top: .2rem;
      }
    }

    .nav {
      border-radius: 50%;
      cursor: pointer;
      height: 2rem;
      padding: .3rem;
      width: 2rem;

      &:hover {
        .icon {
          box-shadow: 0 0 0 .5rem #d2dfe2;
        }
      }

      .icon {
        width: 100%;
        height: 100%;
        background-color: #2586ea;
        border-radius: 50%;
        transition: all .3s ease;
      }

      svg {
        fill: white;
      }

      &-left {
        svg {
          transform: rotate(90deg) translateY(.1rem);
        }
      }

      &-right {
        svg {
          transform: rotate(-90deg) translateY(.1rem);
        }
      }

      &.disabled {
        &:hover {
          .icon {
            box-shadow: none;
          }
        }

        .icon {
          background-color: rgb(121, 121, 121);
          cursor: not-allowed;
        }
      }
    }

    .delete-tab {
      transform: translateX(-8px);

      .icon-delete {
        width: 12px;
        height: 12px;

        background: none;
      }
    }
  }

  &-flat {
    display: flex;
    border-bottom: 0;
    margin-bottom: 0;
    padding: 0;
    overflow: hidden;
    border-bottom: .3rem solid $bd-color-white;

    .tab {
      padding: 1rem 2rem;
      position: relative;
      margin: 0 .2rem 0 0;
      background-color: $bd-color-seashell;
      border: 0;
      color: $bd-color-slate-darker;
      border-radius: .4rem;
      font-weight: normal !important;
      white-space: nowrap;

      &-inner {
        position: relative;

        &_state {
          position: absolute;
          top: -.3rem;
          right: -.7rem;
          width: .9rem;
          height: .9rem;
          border-radius: 100%;
          background-color: #2586ea;
        }
      }


      @include transition(all, ease-in-out, .1s);

      &-active {
        opacity: 1;
        background-color: $bd-color-blue-flat-tabs;
        color: $bd-color-slate-darker;

        @include transition(all, ease-in-out, .1s);
      }

      &.on-hover {
        background: $bd-color-blue-flat-tabs;
        opacity: 1;

        @include transition(all, ease-in-out, .1s);
      }
    }
  }

  &-pure {
    border-bottom: 0;
    margin-bottom: 0;
    padding: 0;
    overflow: hidden;

    .tab {
      padding: 1rem 1.5rem;
      height: 3rem;
      position: relative;
      margin: 0;

      &::before {
        content: '|';
        position: absolute;
        left: -.3rem;
        color: $bd-color-grey;
        font-weight: normal;
      }

      @include transition(all, ease-in-out, .1s);

      &::after {
        display: none;
      }

      &:first-of-type::before {
        display: none;
      }

      &-active {
        background: #fff;
        border-top-left-radius: 1rem;
        border-top-right-radius: 1rem;
        box-shadow: .3rem .4rem .7rem -.1rem rgba(0, 33, 55, .26);
        opacity: 1;
        color: $bd-color-prm-btn;

        + .tab {
          &::before {
            display: none;
          }
        }

        &::before,
        &::after {
          display: block;
          content: "";
          position: absolute;
          height: 1rem;
          width: 2rem;
          bottom: 0;
        }

        &::after {
          left: auto;
          right: -2rem;
          border-radius: 0 0 0 1rem;
          box-shadow: -1rem 0 0 0 #fff;
        }

        &::before {
          right: auto;
          left: -2rem;
          border-radius: 0 0 1rem 0;
          box-shadow: 1rem 0 0 0 #fff;
        }

        @include transition(all, ease-in-out, .1s);
      }

      &.on-hover {
        background: $bd-color-white;
        opacity: 1;

        @include transition(all, ease-in-out, .1s);
      }
    }
  }

  // Page styles
  &-content {
    display: none;
    width: 100%;

    &-active {
      display: flex;
      flex-flow: row wrap;

      &.as-block {
        display: block;
      }
    }
  }
}

// Rules for wrapper
.with-blue-tabs {
  .tab {
    .tabs-component-tab-a {
      color: $bd-color-grey-darkest;
      cursor: pointer;
      display: inline-block;
      font-size: $base-font-size;
      position: relative;
      text-decoration: none;

      &::after {
        background: linear-gradient(166deg, $bd-color-blue-light, $bd-color-blue-darken);
        border-top-left-radius: $small-border-radius;
        border-top-right-radius: $small-border-radius;
        bottom: -1.2rem;
        content: '';
        height: 0;
        left: 0;
        position: absolute;
        width: 100%;

        @include transition(all, ease-in-out, .1s);
      }
    }

    &.tab-active {
      .tabs-component-tab-a {
        color: $bd-color-blue-dark;
        font-weight: bold;

        &::after {
          height: .4rem;
        }
      }
    }
  }
}

.with-grey-tabs {
  .tfx-tabs {
    background: $bd-color-grey-platinum;
    border: 0;
    border-radius: .4rem;
    margin-bottom: 3.1rem;
    padding: .8rem;
    width: 100%;
  }

  .tab {
    cursor: pointer;
    display: inline-block;
    margin-right: 1.9rem;
    padding: 1rem 1.5rem .9rem 1.3rem;
    position: relative;

    @include transition(all, ease-in-out, .1s);

    &.tab-active {
      background: $bd-color-white;
      border-radius: .4rem;
    }

    .notification__small {
      color: $bd-color-slate-darker;
      font-size: $big-font-size;
      font-weight: bold;
      position: relative;
      text-decoration: none;

      .icon-attention,
      .icon-check-mark {
        height: 1.7rem;
        margin-right: .5rem;
        width: 1.7rem;
      }
    }
  }
}

.with-white-bg .tfx-tabs {
  background: $bd-color-white;
  border-radius: .4rem;
  padding: 1.2rem 2rem;
}

</style>