<template>
  <div id="freezing" class="freezing-container">
    <div
      v-for="(freezeStep, index) in freezeSteps"
      :key="index"
      class="freeze-info"
    >
      <img :src="freezeStep.image" alt="image" />
      <p class="title">{{ freezeStep.title }}</p>
      <p class="desc">{{ freezeStep.desc }}</p>
    </div>
  </div>
</template>

 <script>
import Pan from "../assets/images/freeze/pan.jpg";
import Ziplock from "../assets/images/freeze/ziplocked.jpg";
import Wash from "../assets/images/freeze/washed.jpg";

export default {
  name: "freezing",
  data() {
    return {
      accessor: 0,

      freezeSteps: [
        {
          image: Pan,
          title: "Sorting",
          desc:
            "Sort the blueberries: Spread the blueberries on a rimmed baking sheet in an even layer. Remove any stems and any shriveled or moldy blueberries. You can skip washing because the blueberries have a coat that keeps them fresh.",
        },
        {
          image: Ziplock,
          title: "Freezing",
          desc:
            "Freeze: Freeze the blueberries on the baking sheet until solid, about 4 hours. Bag and label: Transfer the blueberries from the baking sheet to a zip-top freezer bag. Label the bag with the date and return to the freezer.",
        },
        {
          image: Wash,
          title: "Preparing",
          desc:
            "Rinse and thaw: Rinse frozen blueberries before using. Frozen blueberries can be sprinkled directly on yogurt or in oatmeal, or even baked in muffins. Frozen berries can be thawed quickly in a bowl of room temperature water.",
        },
      ],
    };
  },
};
</script>

<style lang="sass">
.freezing-container
  display: flex
  justify-content: center
  align-items: center
  height: 100vh
  width: 100%
.freeze-info
  width: 40rem
  height: 20rem
  margin-right: 5vw
  margin-left: 5vw
  margin-bottom: 25vh
  font-family: Nunito-regular
  img
    height: 100%
    width: 100%
    border-radius: 10px
    object-fit: cover

@media (max-width: 1500px)
  .freeze-info
    margin-right: 2vw
    margin-left: 2vw
@media (max-width: 1250px)
  .freeze-info
    margin-right: 3vw
    margin-left: 3vw
    width: 30rem

@media (max-width: 800px)
  .h
</style>