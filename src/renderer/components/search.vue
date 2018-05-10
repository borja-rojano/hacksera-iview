<template>
  <div class="container is-fluid" id="mainSearch">
  <div class="columns">
<!-- Search column -->
      <div class="column is-3">

        <div class="field" id='query-top'>
          <label class="label">Query 1/1</label>
          <div class="control">
            <textarea class="textarea" type="text" placeholder="Enter a PQL query. Remember that car, (motor d vehicle?) is equal to car OR (motor d vehicle?)"></textarea>
          </div>
        </div>

        <div class="field">
          <label class="label">and</label>
          <div class="control">
            <textarea class="textarea" type="text" placeholder="The contents of each box will be combined with AND.
It is useful to separate the query in different concepts."></textarea>
          </div>
        </div>

        <div class="field">
          <label class="label">and</label>
          <div class="control">
            <textarea class="textarea" type="text" placeholder="Remember that hackSERA runs the ANSERA search engine, this is a FULLTEXT search"></textarea>
          </div>
        </div>

        <div class="field">
          <label class="label">and</label>
          <div class="control">
            <textarea class="textarea" type="text" placeholder="Click on single publications to select them for sending to the viewer"></textarea>
          </div>
        </div>

      </div>

<!-- Preview column -->
      <div class="column is-9" id="preview">
        <div class="tile is-ancestor preview-row" v-for='row in rows'>
          <div class="tile is-parent patent">
            <div class="tile is-child box">
              <p class="title is-size-4 patent-title">Method of identifying chicken variety by DNA strip shape coding</p>
              <!-- <p>The invention discloses a method to appraise chicken species with DNA encoding strip in molecular biology technical domain, which comprises the following steps: utilizing DNA test-sequence technology; checking gene sequence of the chicken group and standard control sample mitochondria cell coloring matter C oxidase I(cytochrome C oxidase I COI); proceeding chicken specie checking according to point of discontinuity of COI sequence, haploid type, haploid type multiple degree (Hd), nucleic acid multiple degree (Pi), genetic distance of double parametric model among species, nucleic acid branch degree among species, specific site of each specie and DNA classified image. This invention can reflect the difference among species compared to the other methods, which result can be scientific proof to appraise genuine-fake of chicken species.</p> -->
              <figure class="image image is-2by3">
                <img src="https://patentimages.storage.googleapis.com/pages/US5455008-1.png">
              </figure>
            </div>
          </div>
          <div class="tile is-parent patent">
            <div class="tile is-child box">
              <p class="title title is-size-4 patent-title">Method of identifying chicken variety by DNA strip shape coding</p>
              <!-- <p>The invention discloses a method to appraise chicken species with DNA encoding strip in molecular biology technical domain, which comprises the following steps: utilizing DNA test-sequence technology; checking gene sequence of the chicken group and standard control sample mitochondria cell coloring matter C oxidase I(cytochrome C oxidase I COI); proceeding chicken specie checking according to point of discontinuity of COI sequence, haploid type, haploid type multiple degree (Hd), nucleic acid multiple degree (Pi), genetic distance of double parametric model among species, nucleic acid branch degree among species, specific site of each specie and DNA classified image. This invention can reflect the difference among species compared to the other methods, which result can be scientific proof to appraise genuine-fake of chicken species.</p> -->
              <figure class="image image is-2by3">
                <img src="https://patentimages.storage.googleapis.com/pages/US5455008-1.png">
              </figure>
            </div>
          </div>
        </div>
      </div>
  </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      rows: [0,0,0,0]
    }
  }
}
</script>

<style scoped>
  #mainSearch {
    margin-left: 15px;
    margin-right: 15px;
  }



  .field{
    margin-top: 10px
  }

  #preview {
    /* This is how you make the other column not scroll */
    height: 100vh;
    overflow: auto;
  }

  #query-top, .preview-row{
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
