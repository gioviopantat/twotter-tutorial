<template>
    <div class="root">
        <!-- <img class="background" ref="background" src="../../static/bg.jpg"/>
        <img class="foreground" ref="foreground" src='../../static/car2.png'/> -->
      <kinesis-container>
        Here, you can put
        <kinesis-element :strength="10">
          whatever
        </kinesis-element>
        <kinesis-element :strength="20">
          content!
        </kinesis-element>
      </kinesis-container>
        
    </div>
</template>

<script>
export default {

name: 'parallax',
data: () => ({

       
    })
}
</script>

<style scoped>
  .background {
    /* Positioning */
    position: absolute;
    top: 0;
    left: 0;
    /* Fill background */
    min-height: 100%;
    min-width: 1024px;
    
    /* Scale proportionately */
    width: 100%;
    height: auto;
    z-index: 1;
  }
  .foreground {
    position: absolute;
    top: 200px;
    right: 0px;
    max-width: 70%;
    max-height: 70%;
    z-index: 2;
  }
</style>