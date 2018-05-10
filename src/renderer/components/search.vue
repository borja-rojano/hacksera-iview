<template>
  <div class="container is-fluid" id="mainSearch">
  <div class="columns">
<!-- Search column -->
      <div class="column is-3">

        <div class="field" id='query-top'>
          <label class="label">Concept 1:</label>
          <div class="control">
            <textarea
            class="textarea"type="text"
            placeholder="Enter a PQL query"
            v-model.lazy.trim='concepts[0]'
            ></textarea>
          </div>
        </div>

        <div class="field" id='query-top'>
          <label class="label">AND Concept 2:</label>
          <div class="control">
            <textarea
            class="textarea"type="text"
            placeholder="Enter a PQL query"
            v-model.lazy.trim='concepts[1]'
            ></textarea>
          </div>
        </div>

        <div class="field" id='query-top'>
          <label class="label">AND Concept 3:</label>
          <div class="control">
            <textarea
            class="textarea"type="text"
            placeholder="Enter a PQL query"
            v-model.lazy.trim='concepts[2]'
            ></textarea>
          </div>
        </div>

        <div class="field" id='query-top'>
          <label class="label">AND Concept 4:</label>
          <div class="control">
            <textarea
            class="textarea"type="text"
            placeholder="Enter a PQL query"
            v-model.lazy.trim='concepts[3]'
            ></textarea>
          </div>
        </div>

        <p>{{newQuery}}</p>

      </div>

<!-- Preview column -->
      <div class="column is-9" id="preview">
<!-- Results Hero -->
      <tiles
        :patents='patents'
      >
      </tiles>
    </div>
      <!-- End of the preview column -->
  </div>
  </div>
</template>

<script>
import tiles from './search/tiles'

export default {

  components: { tiles },

  data (){
    return {
      patents: [
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
        {
          title: 'Apparatus for robotically performing sanger dideoxynucleotide DNA sequencing reactions using controlled pipet',
          abstract: 'A robotic system for performing nucleic acid sequencing reactions in microtiter plate format. The robot has a robot arm and its controller, robot hands with which it can manipulate microtiter plates with lids and microtiter plates without lids and with which it can perform pipetting in the 5 to 200 microliter range, cooled storage chambers with electronically controllable doors for storage of microtiter plates, cooled storage with an electronically controllable cover for storage of nucleic acid sequencing reagents, heating blocks to incubate the reactions at appropriate temperatures above ambient temperature, storage for boxes of micropipet tips, storage for microtiter plates in which sequence reactions will be performed and software for controlling the operation of the robot during pipetting.',
          image:'https://patentimages.storage.googleapis.com/pages/US5455008-2.png'
        },
        {
          title: 'Heat and pH measurement for sequencing of DNA',
          abstract: 'The present method involves sequencing by synthesis in which a template strand having an attached primer is immobilized in a small volume reaction mixture. In one embodiment, the reaction mixture is in contact with a sensitive heat sensor, which detects the heat of reaction from incorporation of a complementary base (dNTP) in the presence of appropriate reagents (DNA polymerase, and polymerase reaction buffer). Alternatively, or in addition, a change in pH resulting from the incorporation of nucleotides in the DNA polymerase reaction is measured. A device is provided having delivery channels for appropriate reagents, including dNTPs, which may be delivered sequentially or in a mixture. Preferably, the dNTPs are added in a predetermined sequence, and the dNTP is incorporated or not depending on the template sequence.',
          image:'https://patentimages.storage.googleapis.com/US7932034B2/US07932034-20110426-D00001.png'
        },
      ],

      queryHistory:[],
      concepts: ['','','',''],
    }
  },

  computed:{
    newQuery: function() {
      //We take the fisrt concept and then add all the others with an AND combination
      let query = this.concepts[0]
      for (var i = 1; i < this.concepts.length; i++) {
        if (this.concepts[i]!== '') {
          query= query + ' and ' + this.concepts[i]
        }
      }
    }
  },

  methods: {

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

</style>
