<template>
  <button :class="type">
    <slot></slot>
    <span v-if="dropable" class="dropdown-arrow">
      <img src="../assets/img/dropdown.png" alt="">
    </span>
  </button>
</template>

<script>
export default {
  props: {
    type: { type: String, default: 'default' },
    dropable: { type: Boolean, default: false }
  },
}
</script>

<style scoped lang="less">
  button {
    border-radius: 100px;
    padding: 18px 20px;
    font-size: var(--default-font-size);
    cursor: pointer;
    margin: 0 5px;
    text-align: center;
    &.default {
      background-color: rgba(0,0,0,0);
      border: 1px solid var(--border-color);
      color: var(--main-font-color);
      &:hover { background-color: var(--main-font-color); color: #fff }
    }
    &.primary {
      background: linear-gradient(180deg, #55BCFC 0%, #3D75F1 100%);
      color: #fff;
      border: none;
      &:hover { background: linear-gradient(180deg, #15eCFC 0%, #1D75F1 100%); }
    }
    .dropdown-arrow{
      margin-left: 12px;
    }
  }
</style>