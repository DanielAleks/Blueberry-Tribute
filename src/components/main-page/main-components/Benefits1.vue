<template>
  <div class="benefits-omni-container" id="facts">
    <div class="benefits-container">
      <div class="red-box">left</div>
      <div class="info-container">
        <p class="title">{{ facts[accessor].title }}</p>
        <p class="desc">{{ facts[accessor].desc }}</p>
      </div>
      <div class="red-box">right</div>
    </div>

    <div class="red-nutrition-box">
      <p>Nutrition Facts</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "facts",
  data() {
    return {
      accessor: 0,

      facts: [
        {
          title: "Maintaining healthy bones",
          desc:
            "Blueberries contain iron, phosphorous, calcium, magnesium, manganese, zinc, and vitamin K. Each of these is a component of bone. Adequate intake of these minerals and vitamins contributes to building and maintaining bone structure and strength. Iron and zinc fulfil crucial rolesTrusted Source in maintaining the strength and elasticity of bones and joints. Low intakes of vitamin K have been linked to a higher risk of bone fractureTrusted Source. However, adequate vitamin K intake improves calcium absorption and may reduce calcium loss.",
        },
      ],
    };
  },
};
</script>

<style lang="sass">
.benefits-omni-container
  height: 80vh
  width: 100%
  display: flex
  justify-content: center
  position: relative


.benefits-container
  display: flex
  justify-content: center
  align-items: center

.info-container
  border: 1px solid black
  border-bottom: none
  border-top: none
  padding: 5rem
  width: 50rem

.title
  font-size: 3rem
  font-weight: black
  text-align: center
.desc

.red-box
  height: 10rem
  background: red
  width: 10rem

.red-nutrition-box
  height: 10rem
  background: red
  width: 40rem
  position: absolute
  bottom: 0px
</style>
