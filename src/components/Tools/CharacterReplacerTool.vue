<template>
  <div class="character-replacer-tool">
    
    <h2>Character replacer tool</h2>
    
    Characters: {{ textareaText.length }} Words: {{ textareaText ? textareaText.split(' ').length: 0 }}
    
    <br/>
    <br/>
    
    <textarea v-model="textareaText" cols="50" rows="10"></textarea>
    
    <br/>
    <br/>
    
    Replace: <input v-model="textToReplace" type="text"/> With: <input v-model="replaceTextWith" type="text">
    
    <br/>
    <br/>

    <a @click="replaceCharacters" href="#">Replace all</a>
  
  </div>
</template>

<script>
  export default {
    name: 'CharacterReplacerTool',
    data(){
      return {
        textareaText: '',
        textToReplace: '',
        replaceTextWith:''
      }
    },
    methods: {
      replaceCharacters: replaceCharacters
    }
  }

  function replaceCharacters() {
    this.textareaText = this.textareaText.split(this.textToReplace).join(this.replaceTextWith);
  }
</script>
