<script>
import axios from "axios";
export default {
  name: "FetchData",
  props: ['url'],
  data() {
    return {
      response: null,
      loading: true
    }
  },
  created() {
    console.log("created");
    axios.get(this.url)
      .then(response => {
        this.response = response.data;
        this.loading = false;
      })
      .catch(error => {
        alert('[ERROR] fetching the data', error);
        console.log(error);
      });
  },
  render() {
    /**
     * Note:
     * $scopedSlots: 등록한 하위 컴포넌트에 노출
     */
    console.log("render");
    return this.$slots.default({
      response: this.response,
      loading: this.loading,
    });
  },
}
</script>