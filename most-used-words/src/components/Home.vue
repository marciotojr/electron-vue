<template>
  <v-container fluid>
      <v-form>
          <v-file-input 
            v-model="files"
            multiple
            chips 
            counter
            label="Select your subtitles"
            placeholder="Select your subtitles"
            prepend-icon="mdi-paperclip"
            outlined
            :show-size="1000"
            append-outer-icon="mdi-send"
            @click:append-outer="processSubtitles">

          </v-file-input>
      </v-form>
      <div class='pills'>
          <Pill v-for="word in groupedWords" :key="word.name" :name="word.name" :amount="word.amount" />
      </div>
  </v-container>
</template>

<script>
import Pill from './Pill'

export default {
    components: { Pill },
    data: function() {
        return {
            files:[],
            groupedWords: [
                {name: 'I', amount: 1234},
                {name: 'you', amount: 999},
                {name: 'he', amount: 666},
            ]
        }
    },
    methods:{
        processSubtitles(){
            console.log(this.files)
        }
    }
}
</script>

<style>
    .pills{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }
</style>