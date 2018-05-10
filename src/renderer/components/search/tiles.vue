<template>
  <div>
    <section class="hero is-info is-bold">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            1.890 families found
          </h1>
          <h2 class="subtitle">
            hackSERA is developed and maintained by your fellow examiners Borja Rojano and Stephan Heising
          </h2>
        </div>
      </div>
    </section>

    <div class="tile is-ancestor preview-row" v-for='row in rows'>
      <div class="tile is-parent patent">
        <div class="tile is-child box">
          <p class="title is-size-4 patent-title">{{row[0].title}}</p>
          <figure class="image image is-2by3">
            <img v-bind:src="row[0].image">
          </figure>
        </div>
      </div>
      <div class="tile is-parent patent">
        <div class="tile is-child box">
          <p class="title title is-size-4 patent-title">{{row[1].title}}</p>
          <figure class="image image is-2by3">
            <img src="https://patentimages.storage.googleapis.com/pages/US5455008-1.png">
          </figure>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    patents: {
      type: Array,
      required: true
    }
  },
  computed:{
    rows: function() {
      // We take the patents and pair them in twos for the rows, so there is one row per every two patents
      let rows = []
      for (var i = 0; i < this.patents.length; i += 2) {
          let newRow = []
          newRow.push(this.patents[i])
          newRow.push(this.patents[i+1])
          rows.push(newRow)
      }
      return rows
    }
  },

  data(){
    return {

    }
  }
}
</script>

<style scoped>

.hero {
  margin-top: 20px
}

.preview-row{
  margin-top: 20px;
}

.patent{
  padding-top: 0;
  padding-bottom: 0;
}

.patent-title {
  margin-bottom: 0
}
</style>
