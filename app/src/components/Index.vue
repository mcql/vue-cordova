<template>
  <div class="index">
    <div @click="show_mobile_version">获取当前应用的版本号</div>
  </div>
</template>

<script>
export default {
  methods: {
    show_mobile_version() {
        cordova.getAppVersion.getVersionNumber().then(function (version) {
            alert(version)
        })
    }
  }
}
</script>

<style scoped>
.index {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
</style>
