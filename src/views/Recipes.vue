<template>
  <div id="recipes" class="recipe-container">
    <div class="recipe-info">
      <p class="recipe-title">{{ recipes[0].title }}</p>
      <p class="recipe-desc">{{ recipes[0].desc }}</p>
      <button>View Recipe</button>
    </div>
    <img :src="recipes[0].image" alt="image" />
    <div class="red-box-next">
      <button>
        <i class="fas fa-chevron-left fa-5x"></i>
      </button>
      <button>
        <i class="fas fa-chevron-right fa-5x"></i>
      </button>
    </div>
  </div>
</template>

<style lang="sass">
.recipe-container
  height: 100vh
  width: 100%
  position: absolute
  display: flex
  align-items: center
  img
    height: 80rem
    width: 120rem
    background-position: 50% 50%
    object-fit: cover
    position: absolute
    right: 0px
    bottom: 0px
.recipe-info
  button
    height: 7rem
    width: 15rem
    background: red
    border: none
    border-radius: 10px
    font-size: 2rem
    font-family: nunito-bold
.recipe-title
  font-family: Rubik
  font-weight: 900
  font-size: 10rem
.recipe-desc
  width: 50rem
.red-box-next
  height: 8rem
  width: 20rem
  background: red
  position: absolute
  right: 55vw
  bottom: 0px
  button
    background: none
    height: 100%
    width: 50%
    border: none

</style>

<script>
import Pie from "../assets/images/recipes/pie.jpeg";
import Smoothie from "../assets/images/recipes/smoothie.jpeg";
import Pancakes from "../assets/images/recipes/pancakes.jpeg";
import Waffles from "../assets/images/recipes/waffles.jpeg";
import PieBars from "../assets/images/recipes/piebars.jpg";
import Icecream from "../assets/images/recipes/icecream.jpg";
import Cookies from "../assets/images/recipes/cookies.jpg";
import Cake from "../assets/images/recipes/cake.jpeg";
import Muffin from "../assets/images/recipes/muffin.jpg";
import Cheesecake from "../assets/images/recipes/cheesecake.jpg";

export default {
  name: "recipes",
  data() {
    return {
      recipes: [
        {
          image: Pie,
          title: "Blueberry Pie",
          desc:
            "This is the best when made with fresh picked blueberries! It is a beautiful sight with a lattice top.",
          recipe: "hi",
        },
        {
          image: Smoothie,
          title: "Blueberry Smoothie",
          desc: "A delicious way to use up your blueberries!",
          recipe: "hi",
        },
        {
          image: Pancakes,
          title: "Blueberry Smoothie",
          desc:
            "Blueberry Pancakes are light and fluffy, loaded with delicious blueberries and made from scratch! A guaranteed weekend favorite!",
          recipe: "hi",
        },
        {
          image: Waffles,
          title: "Blueberry Waffles",
          desc:
            "These waffles are light and fluffy and golden brown – and take just a few minutes to whip up. You can have 4 Belgian sized waffles in about 15 minutes! DIG IN!!",
          recipe: "hi",
        },
        {
          image: PieBars,
          title: "Blueberry Pie Bars",
          desc:
            "Blueberry Pie Bars are the perfect easy treat to throw together for the pie lovers in your life. No rolling pin required!",
          recipe: "hi",
        },
        {
          image: Icecream,
          title: "Blueberry Icecream",
          desc:
            "The wild blueberries on our property spark recipe ideas. When my daughter and I made this ice cream at a Girl Guide meeting, it was well received. Even today, our 10 children, 19 grandkids and 4 great-grandchildren think it tastes great. —Alma Mosher, Mohannes, New Brunswick",
          recipe: "hi",
        },
        {
          image: Cookies,
          title: "Blueberry Cookies",
          desc:
            "These cookies are everyone’s favorite, they remind me of a blueberry muffin in cookie form!",
          recipe: "hi",
        },

        {
          image: Cake,
          title: "Blueberry Cake",
          desc:
            "This is a nice tender cake - one of my Mom's specialties from years ago. It is a great cake to take along to a picnic.",
          recipe: "hi",
        },
        {
          image: Muffin,
          title: "Blueberry Muffin",
          desc:
            "These muffins are extra large and yummy with the sugary-cinnamon crumb topping. I usually double the recipe and fill the muffin cups just to the top edge for a wonderful extra-generously-sized deli style muffin. Add extra blueberries too, if you want!",
          recipe: "hi",
        },
        {
          image: Cheesecake,
          title: "Blueberry Cheesecake",
          desc:
            "These muffins are extra large and yummy with the sugary-cinnamon crumb topping. I usually double the recipe and fill the muffin cups just to the top edge for a wonderful extra-generously-sized deli style muffin. Add extra blueberries too, if you want!",
          recipe: "hi",
        },
      ],
    };
  },
};
</script>