<template>
  <div class="benefits-omni-container" id="facts">
    <div class="benefits-container">
      <button class="red-box-left" @click="minusAccessor()">
        <i class="fas fa-chevron-left fa-3x"></i>
      </button>

      <div class="info-container">
        <p class="title">{{ factsT[accessor] }}</p>
        <p class="desc">{{ factsD[accessor] }}</p>
      </div>

      <button class="red-box-right" @click="plusAccessor()">
        <i class="fas fa-chevron-right fa-3x"></i>
      </button>
    </div>

    <div @click="isNutrition = !isNutrition" class="red-nutrition-box">
      <p>Nutrition Facts</p>
      <button>
        <i class="fas fa-chevron-up fa-3x"></i>
      </button>
    </div>
    <div v-if="isNutrition">
      <div class="nutrition-left">
        <p class="nutrition-title">{{ nutritionTitle }}</p>
        <p v-for="(nutritionLeft, index) in nutritionLeft" :key="index">
          {{ nutritionLeft }}
        </p>
      </div>

      <div class="nutrition-right">
        <p class="nutrition-title">{{ nutritionTitle }}</p>
        <p v-for="(nutritionRight, index) in nutritionRight" :key="index">
          {{ nutritionRight }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "facts",
  data() {
    return {
      accessor: 0,
      isNutrition: false,
      nutritionTitle: "Serving Size: 1 Cup",

      minusAccessor() {
        if (this.accessor > 0) {
          this.accessor -= 1;
        }
        null;
      },
      plusAccessor() {
        if (this.accessor < 7) {
          this.accessor += 1;
        }
        null;
      },

      nutritionLeft: [
        "84 calories",
        "0 g of cholesterol",
        "1.1 g of protein",
        "0.49 g of fat",
        "21.45 g of carbohydrate",
        "3.6 g of dietary fiber",
        "14.74 g of total sugars",
      ],

      nutritionRight: [
        "9 milligrams (mg) calcium",
        "0.41 mg of iron",
        "114 mg of potassium",
        "9 mg of magnesium",
        "18 mg of phosphorus",
        "1 mg of sodium",
        "0.24 mg of zinc",
      ],

      factsT: [
        "Maintaining healthy bones",
        "Skin health",
        "  Lowering blood pressure",
        " Managing diabetes",
        " Protecting against heart disease",
        " Preventing cancer",
        "Improving mental health",
        "Healthy digestion, weight loss, and feeling full",
      ],

      factsD: [
        "Blueberries contain iron, phosphorous, calcium, magnesium, manganese, zinc, and vitamin K. Each of these is a component of bone. Adequate intake of these minerals and vitamins contributes to building and maintaining bone structure and strength. Iron and zinc fulfil crucial rolesTrusted Source in maintaining the strength and elasticity of bones and joints. Low intakes of vitamin K have been linked to a higher risk of bone fractureTrusted Source. However, adequate vitamin K intake improves calcium absorption and may reduce calcium loss.",
        "Collagen is the support system of the skin. It relies on vitamin C as an essential nutrient, and works to help prevent skin damage caused by the sun, pollution, and smoke. Vitamin C may also improve collagen’s ability to smooth wrinkles and enhance overall skin texture. One cup of blueberries provides 24 percent of the recommended daily allowance of vitamin C.",
        "Maintaining low sodium levels is essential to keeping blood pressure at a healthful level. Blueberries are free of sodium. They contain potassium, calcium, and magnesium. Some studies have shown that diets low in these minerals are associated with higher blood pressure. Adequate dietary intake of these minerals is thought to help reduce blood pressure. However, other studies have counteracted these findings. For example, a 2015 studyTrusted Source of people with metabolic syndrome found that daily blueberry consumption for 6 weeks did not affect blood pressure levels.",
        "Studies have found that people with type 1 diabetes who consume high-fiber diets have low blood glucose levels, and people with type 2 diabetes who consume the same may have improved blood sugar, lipid, and insulin levels. One cup of blueberries contributes 3.6 grams (g) of fiber. A large 2013 cohort studyTrusted Source published in the BMJ suggested that certain fruits may reduce the risk of type 2 diabetes in adults. Over the course of the study, 6.5 percent of the participants developed diabetes. However, the researchers found that consuming three servings per week of blueberries, grapes, raisins, apples or pears reduced the risk of type 2 diabetes by 7 percent.",
        "Blueberries can help to preserve cardiovascular health. The fiber, potassium, folate, vitamin C, vitamin B6, and phytonutrient content in blueberries supports heart health. The absence of cholesterol from blueberries is also beneficial to the heart. Fiber content helps to reduce the total amount of cholesterol in the blood and decrease the risk of heart disease. Vitamin B6 and folate prevent the buildup of a compound known as homocysteine. Excessive buildup of homocysteine in the body can damage blood vessels and lead to heart problems. According to a study from the Harvard School of Public Health and the University of East Anglia, in the United Kingdom (U.K.) regular consumption of anthocyanins can reduce the risk of heart attack by 32 percent Trusted Sourcein young and middle-aged women. The study found that women who consumed at least three servings of blueberries or strawberries per week showed the best results.",
        "Vitamin C, vitamin A, and the various phytonutrients in blueberries function as powerful antioxidants that may help protect cells against damage from disease-linked free radicals. Research suggests that antioxidants may inhibit tumor growth, decrease inflammation in the body, and help ward off or slow down esophageal, lung, mouth, pharynx, endometrial, pancreatic, prostate, and colon cancers. Blueberries also contain folate, which plays a role in DNA synthesis and repair. This can prevent the formation of cancer cellsTrusted Source due to mutations in the DNA.",
        "Population-based studies have shown that consumption of blueberries is connected to slower cognitive declineTrusted Source in older women. Studies have also found that in addition to reducing the risk of cognitive damage, blueberries can also improve a person’s short-term memoryTrusted Source and motor coordination.",
        "Blueberries help to prevent constipation and maintain regularity for a healthful digestive tract because of their fiber content. Dietary fiber is also commonly recognized as an important factor in weight loss and weight management by functioning as a “bulking agent” in the digestive system. High fiber foods increase satiety, or the feeling of being full, and reduce appetite. Feeling fuller for longer can reduce a person’s overall calorie intake.",
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

.nutrition-left, .nutrition-right
  bottom: 100px
  position: absolute
  p
    margin: .5rem

.nutrition-left
  left: 100px

.nutrition-right
  right: 100px

.title
  font-size: 3rem
  font-weight: black
  text-align: center
.desc

.nutrition-title
  font-family: nunito-bold

.red-box-left, .red-box-right
  height: 10rem
  background: linear-gradient(180deg, rgba(255,63,63,1) 0%, #ff6e6e 50%, rgba(255,63,63,1) 100%)
  width: 10rem
  border: none

.red-box-left
  border-top-left-radius: 10px
  border-bottom-left-radius: 10px
.red-box-right
  border-bottom-right-radius: 10px
  border-top-right-radius: 10px

.red-nutrition-box
  height: 8rem
  background: linear-gradient(180deg, rgba(255,63,63,1) 0%, #ff6e6e 50%, rgba(255,63,63,1) 100%)
  width: 35rem
  position: absolute
  bottom: 0px
  display: flex
  justify-content: center
  align-items: center
  border-top-right-radius: 10px 
  border-top-left-radius: 10px 
  p
    font-size: 2.5rem
    margin-right: 20%
  button
    background: transparent
    border: none
</style>
