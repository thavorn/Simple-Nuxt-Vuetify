<template>
  <h1>{{finalParamsRequest}}</h1>
</template>

<script>
export default {
  head() {
    let tempParams = this.$route.params.id;

    return {
      title: tempParams,
      meta: [
        {
          hid: tempParams,
          name: tempParams,
          content: tempParams
        }
      ]
    };
  },
  data() {
    finalParamsRequest: " ";
  },
  created() {
    let tempParams = this.$route.params.id;
    this.splitRequestStringWithDash(tempParams);
  },

  methods: {
    splitRequestStringWithDash: function(tempParams) {
      let afterSplit = " ";
      let tempArray = tempParams.split("-");
      tempArray.forEach(function(val) {
        afterSplit += " ";
        afterSplit += val;
      });
      this.finalParamsRequest = afterSplit;
    }
  }
};
</script>

