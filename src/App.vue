<script>
export default {
  onLaunch: function () {
    console.log("App Launch");
  },
  onShow: function () {
    console.log("App Show");
  },
  onHide: function () {
    console.log("App Hide");
  },
};
</script>

<style>
/*每个页面公共css */
@import "common/colorui/app.css";
.footer {
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 100%;
  transform: translate(-50%, 0%);
}
</style>
