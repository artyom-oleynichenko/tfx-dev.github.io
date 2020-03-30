<template>
  <div class="tfx-table-wrapper">
    <table class="tfx-table">
      <thead>
        <tr>
          <th width="15%">Name</th>
          <th width="30%">Email</th>
          <th width="9%">Country</th>
          <th width="7%">Phone</th>
          <th width="12%">Last Login</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>
            Mr. Willette Willette Rowe
          </td>
          <td>
            test@taxesforexpats.com (login)<br>
            test@clients.tfx.life
          </td>
          <td>
            Ukraine
          </td>
          <td>
            +79631257200
          </td>
          <td>
            Nov-11-2019
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
// vuepress reset
tr {
  border-top: 0;
}
th, td {
  border: 0;
  padding: 0;
}
// end vuepress reset

.tfx-table-wrapper {
  position: relative;
  background-color: #fff;
  border-radius: .4rem;
  padding: .1rem .1rem 0;
  margin-bottom: .2rem;

  table {
    border-collapse: collapse;
    border-spacing: 0;
    width: 100%;
    background-color: #fff;
    box-shadow: 0 0.2rem 0 0 rgba(0,20,29,.07);
    margin: 0;

    thead {
      tr {
        width: 100%;
        height: 4.2rem;
        background-color: #eeedf3;
        border-radius: .4rem;
      }

      th:first-child {
        border-top-left-radius: .4rem;
      }

      th:last-child {
        border-top-right-radius: .4rem;
      }
    }

    th, td {
      padding: .8rem 1.2rem;

      &:not(:last-child) {
        border-right: .1rem solid #d8d8d8;
      }
    }
  }
}
</style>