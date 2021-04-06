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

    <div class="Mfreeze-info">
      <div style="display: flex; width: 400%; transform: translateX(60vw)">
        <div
          v-for="(freezeStep, index) in freezeSteps"
          :key="index"
          :style="{ transform: `translate(${x}%)` }"
          class="title-desc-container"
        >
          <p class="title">{{ freezeStep.title }}</p>
          <p @click="imgHandler(index)" class="desc">{{ freezeStep.desc }}</p>
        </div>
      </div>

      <div class="freeze-img-container">
        <img
          v-for="(freezeStep, index) in freezeSteps"
          :key="index"
          :src="freezeStep.image"
          alt="image"
          @click="imgHandler(index)"
          :style="
            accessor === index
              ? 'filter: brightness(100%)'
              : 'filter: brightness(40%)'
          "
        />
      </div>
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
      x: -105,
      imgHandler(index) {
        this.accessor = index;
        if (index === 0) {
          this.x = -100;
        } else if (index === 1) {
          this.x = -200;
        } else if (index === 2) {
          this.x = -300;
        }
      },
      freezeSteps: [
        {
          image: Pan,
          accessor: 0,
          title: "Sorting",
          desc:
            "Sort the blueberries: Spread the blueberries on a rimmed baking sheet in an even layer. Remove any stems and any shriveled or moldy blueberries. You can skip washing because the blueberries have a coat that keeps them fresh.",
        },
        {
          image: Ziplock,
          accessor: 1,
          title: "Freezing",
          desc:
            "Freeze: Freeze the blueberries on the baking sheet until solid, about 4 hours. Bag and label: Transfer the blueberries from the baking sheet to a zip-top freezer bag. Label the bag with the date and return to the freezer.",
        },
        {
          image: Wash,
          accessor: 2,
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
.Mfreeze-info
  display: none
@media (max-width: 900px)
  .freezing-container
  .Mfreeze-info
    display: block
    width: 40rem
    margin-right: 5vw
    margin-left: 5vw
    font-family: Nunito-regular
  .desc
    width: 80%
    margin-left: 10%
    margin-right: 10%
  .title-desc-container
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    transition: transform 1s
    margin-left: -50px
    width: 70%

  .freeze-img-container
    display: flex
    justify-content: center
    margin-left: -10%
    margin-top: 10rem
    width: 120%
    img
      @media (max-width: 900px)
        transition: filter 1s
        margin: 1.5rem
        height: 20rem
        width: 50%
        border-radius: 10px
        object-fit: cover
        cursor: pointer
      @media (max-width: 800px)
        margin: .4rem
      @media (max-width: 700px)
        width: 40%
      @media (max-width: 600px)
        width: 33%

.freeze-info
  width: 40rem
  height: 20rem
  margin-right: 5vw
  margin-left: 5vw
  margin-bottom: 25vh
  font-family: Nunito-regular
  @media (max-width: 900px)
    display: none
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
</style>