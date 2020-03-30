<template>
  <div>
    <a class="link" href="">Ссылка для перехода на другую страницу</a>
    <a class="link dashed" href="">Ссылка для открытия модальных окон</a>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.link {
  color: #2586ea;
  border-bottom: 1px solid #2586ea;
  text-decoration: none;
  margin-right: 10px;
  transition: all .3s ease;

  &:hover {
    border-bottom: 1px solid #004486;
    color: #004486;
    text-decoration: none !important;
  }

  &.dashed {
    border-bottom: 1px dashed #2586ea;

    &:hover {
      border-bottom: 1px dashed #004486;
    }
  }
}
</style>