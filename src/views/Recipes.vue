<template>
  <div id="recipes" class="recipe-container">
    <div class="recipe-info">
      <p class="recipe-title">{{ recipes[accessor].title }}</p>
      <p class="recipe-desc">{{ recipes[accessor].desc }}</p>
      <button @click="recipeModal = !recipeModal">View Recipe</button>
    </div>
    <img :src="recipes[accessor].image" alt="image" />
    <div class="red-box-next">
      <button @click="minusAccessor()">
        <i class="fas fa-chevron-left fa-3x"></i>
      </button>
      <button @click="addAccessor()">
        <i class="fas fa-chevron-right fa-3x"></i>
      </button>
    </div>

    <div class="recipe-modal-container" :v-show="recipeModal">
      <p v-for="(ingredients, index) in recipes[0].ingredients" :key="index">
        {{ ingredients }}
      </p>
      <div v-for="(ingredients, index) in recipes[0].steps" :key="index">
        <p>Step: {{ index + 1 }}</p>
        <p>
          {{ recipes[0].steps }}
        </p>
      </div>
    </div>
  </div>
</template>

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
      accessor: 0,
      recipeModal: false,

      minusAccessor() {
        if (this.accessor > 0) {
          this.accessor -= 1;
        }
        this.accessor;
      },
      addAccessor() {
        if (this.accessor < 9) {
          this.accessor += 1;
        }
        this.accessor;
      },

      recipes: [
        { 
          image: Pie,
          title: "Blueberry Pie",
          desc:
            "This is the best when made with fresh picked blueberries! It is a beautiful sight with a lattice top.",
          ingredients: [
            "¾ cup white sugar",
            "3 tablespoons cornstarch",
            "¼ teaspoon salt",
            " ½ teaspoon ground cinnamon",
            "4 cups fresh blueberries",
            "1 recipe pastry for a 9 inch double crust pie",
            "1 tablespoon butter",
          ],
          steps: [
            "Preheat oven to 375 degrees F (190 degrees C).",
            "Mix sugar, cornstarch, salt, and cinnamon, and sprinkle over blueberries.",
            "Line pie dish with one pie crust. Pour berry mixture into the crust, and dot with butter. Cut remaining pastry into 1/2 - 3/4 inch wide strips, and make lattice top. Crimp and flute edges.",
            "Bake pie on lower shelf of oven for about 50 minutes, or until crust is golden brown.",
          ],
        },
        {
          image: Smoothie,
          title: "Blueberry Smoothie",
          desc: "A delicious way to use up your blueberries!",
          recipe: "hi",
        },
        {
          image: Smoothie,
          title: "Blueberry Smoothie",
          desc: "A delicious way to use up your blueberries!",
          ingredients: [
            "1 cup blueberries (frozen or fresh)",
            "1 (8 ounce) container plain yogurt",
            "¾ cup 2% reduced-fat milk",
            "2 tablespoons white sugar ",
            "½ teaspoon vanilla extract",
            "⅛ teaspoon ground nutmeg",
          ],
          steps: [
            "Blend the blueberries, yogurt, milk, sugar, vanilla, and nutmeg in a blender until frothy, scraping down the sides of the blender with a spatula occasionally. Serve immediately.",
          ],
        },
        {
          image: Pancakes,
          title: "Blueberry Pancakes",
          desc:
            "These pancakes are light and fluffy and golden brown – and take just a few minutes to whip up. You can have 4 Belgian sized pancakes in about 15 minutes! DIG IN!!",
          ingredients: [
            "2 cups all purpose flour",
            "2 tablespoons baking powder",
            "1 teaspoon kosher salt",
            "3 tablespoons light brown sugar",
            "2 eggs",
            "1 teaspoon vanilla",
            "1 1/2 cups milk",
            "5 tablespoons butter, melted",
            "2 cups fresh blueberries",
            "butter for frying",
          ],
          steps: [
            "In a large bowl whisk the flour, baking powder, salt and brown sugar together.",
            "In separate bowl whisk the eggs, vanilla and milk together.",
            "Add the wet ingredients into the dry and mix until just combined. Lastly mix in the melted butter and stir until combined, the batter will be slightly lumpy. Set the batter aside while you heat your griddle to medium-low heat. Melt a small pat of butter on the griddle and then scoop out 1/4 cup of pancake batter onto the hot griddle and top evenly with blueberries, as many or few as you prefer.",
            "Cook until the edges are set and bubbles form on top of the pancake. Flip and cook until browned.",
          ],
        },
        {
          image: Waffles,
          title: "Blueberry Waffles",
          desc:
            "These waffles are light and fluffy and golden brown – and take just a few minutes to whip up. You can have 4 Belgian sized waffles in about 15 minutes! DIG IN!!",
          ingredients: [
            "2 cups all purpose flour",
            "1 tsp salt",
            "1 Tbs baking powder",
            "2 Tbs sugar",
            "2 eggs",
            "6 Tbs butter melted",
            "1 1/2 cups milk",
            "2 tsp vanilla extract",
            "4 oz fresh blueberries",
          ],
          steps: [
            "In a large bowl, whisk together the dry ingredients.",
            "In a smaller bowl, whisk the eggs, melted butter, milk and vanilla until well combined",
            "Add the wet ingredients to the dry, and mix until just combined. Mixture will be lumpy.",
            "Fold in the blueberries.",
            "Spray the waffle iron with baking spray, and cook waffles until light brown and slightly crispy.",
          ],
        },
        {
          image: PieBars,
          title: "Blueberry Pie Bars",
          desc:
            "Blueberry Pie Bars are the perfect easy treat to throw together for the pie lovers in your life. No rolling pin required!",
          ingredients: [
            "3/4 cup (1 ½ sticks) butter, softened",
            "1 1/2 cup granulated sugar",
            "3/4 teaspoon salt",
            "3 eggs",
            "1 teaspoon vanilla",
            "2 1/4 cup flour",
            "1 (21 ounce) can blueberry pie filling",
            "1/2 cup powdered sugar",
            "1/4 teaspoon vanilla",
            "1-2 tablespoons heavy whipping cream or milk",
          ],
          steps: [
            "Preheat oven to 350 degrees F. Grease a 9x13 inch baking pan with cooking spray.",
            "Cream butter, sugar, and salt for about 3 minutes, until light and fluffy.",
            "Mix in one egg at a time until combined. Mix in the vanilla and then the flour.",
            "Reserve 1 heaping cup of the dough and set aside. Place remaining dough evenly in the greased pan.",
            "Spread the pie filling over the dough and then drop spoonfuls of the reserved dough on top.",
            "Bake for 30-35 minutes or until golden. Let cool completely before adding glaze.",
            "Whisk all glaze ingredients together, adding one tablespoon milk at a time until desired consistency. Drizzle over cooled bars. Cut and serve.",
          ],
        },
        {
          image: Icecream,
          title: "Blueberry Icecream",
          desc:
            "The wild blueberries on our property spark recipe ideas. When my daughter and I made this ice cream at a Girl Guide meeting, it was well received. Even today, our 10 children, 19 grandkids and 4 great-grandchildren think it tastes great. —Alma Mosher, Mohannes, New Brunswick",
          ingredients: [
            "4 cups fresh or frozen blueberries",
            "2 cups sugar",
            "2 tablespoons water",
            "4 cups half-and-half cream",
          ],
          steps: [
            " In a large saucepan, combine the blueberries, sugar and water. Bring to a boil. Reduce heat; simmer, uncovered, until sugar is dissolved and berries are softened. Press mixture through a fine-mesh strainer into a bowl; discard pulp. Stir in cream. Cover and refrigerate overnight.",
            "Fill cylinder of ice cream freezer two-thirds full; freeze according to the manufacturer’s directions. (Refrigerate any remaining mixture until ready to freeze.) Transfer ice cream to freezer containers, allowing headspace for expansion. Freeze until firm, 2-4 hours. Repeat with any remaining ice cream mixture.",
          ],
        },
        {
          image: Cookies,
          title: "Blueberry Cookies",
          desc:
            "These cookies are everyone’s favorite, they remind me of a blueberry muffin in cookie form!",
          ingredients: [
            "2 ½ cups all-purpose flour",
            "2 teaspoons baking powder",
            "1 pinch salt",
            "½ cup butter",
            "1 cup white sugar",
            "2 eggs, beaten ",
            "½ teaspoon lemon extract",
            "½ cup milk",
            "1 cup fresh blueberries",
          ],
          steps: [
            "Preheat oven to 375 degrees F (190 degrees C). Grease cookie sheet.",
            "Sift together flour, baking powder and salt.",
            "In a large bowl, cream butter or margarine with sugar. Beat in eggs and lemon flavoring. Mix in milk and flour mixture alternately in three parts, starting with the milk. Gently mix in blueberries.",
            "Drop batter by tablespoons onto prepared sheets 1 1/2 inches apart.",
            "Bake 12 to 15 minutes.",
          ],
        },

        {
          image: Cake,
          title: "Blueberry Cake",
          desc:
            "This is a nice tender cake - one of my Mom's specialties from years ago. It is a great cake to take along to a picnic.",
          ingredients: [
            "½ cup butter",
            "½ cup white sugar",
            "¼ teaspoon salt",
            "1 teaspoon vanilla extract",
            "2 egg yolks ",
            "1 ½ cups all-purpose flour",
            "1 teaspoon baking powder",
            "⅓ cup milk",
            "2 egg whites",
            "¼ cup white sugar",
            "1 ½ cups fresh blueberries",
            "1 tablespoon all-purpose flour",
            "1 tablespoon white sugar",
          ],
          steps: [
            "Preheat oven to 350 degrees F (175 degrees C). Grease and flour an 8 inch square pan.",
            "Cream butter or margarine and 1/2 cup sugar until fluffy. Add salt and vanilla. Separate eggs and reserve the whites. Add egg yolks to the sugar mixture; beat until creamy.",
            "Combine 1 1/2 cups flour and baking powder; add alternately with milk to egg yolk mixture. Coat berries with 1 tablespoon flour and add to batter.",
            "In a separate bowl, beat whites until soft peaks form. Add 1/4 cup of sugar, 1 tablespoon at a time, and beat until stiff peaks form. Fold egg whites into batter. Pour into prepared pan. Sprinkle top with remaining 1 tablespoon sugar.",
            "Bake for 50 minutes, or until cake tests done.",
          ],
        },
        {
          image: Muffin,
          title: "Blueberry Muffin",
          desc:
            "These muffins are extra large and yummy with the sugary-cinnamon crumb topping. I usually double the recipe and fill the muffin cups just to the top edge for a wonderful extra-generously-sized deli style muffin. Add extra blueberries too, if you want!",
          ingredients: [
            "1 ½ cups all-purpose flour",
            "¾ cup white sugar",
            "½ teaspoon salt",
            "2 teaspoons baking powder",
            "⅓ cup vegetable oil",
            "1 egg ",
            "⅓ cup milk, or more as needed",
            "1 cup fresh blueberries",
            "½ cup white sugar",
            "⅓ cup all-purpose flour",
            "¼ cup butter, cubed",
            "1 ½ teaspoons ground cinnamon",
          ],
          steps: [
            "Preheat oven to 400 degrees F (200 degrees C). Grease muffin cups or line with muffin liners.",
            "Combine 1 1/2 cups flour, 3/4 cup sugar, salt and baking powder. Place vegetable oil into a 1 cup measuring cup; add the egg and add enough milk to reach the 1-cup mark. Mix this with flour mixture. Fold in blueberries. Fill muffin cups right to the top, and sprinkle with crumb topping mixture.",
            "To Make Crumb Topping: Mix together 1/2 cup sugar, 1/3 cup flour, 1/4 cup butter, and 1 1/2 teaspoons cinnamon. Mix with fork, and sprinkle over muffins before baking.",
            "Bake for 20 to 25 minutes in the preheated oven, or until done.",
          ],
        },
        {
          image: Cheesecake,
          title: "Blueberry Cheesecake",
          desc:
            "These muffins are extra large and yummy with the sugary-cinnamon crumb topping. I usually double the recipe and fill the muffin cups just to the top edge for a wonderful extra-generously-sized deli style muffin. Add extra blueberries too, if you want!",
          ingredients: [
            "Dough for single-crust pie",
            "4 ounces cream cheese, softened",
            "1/2 cup confectioners' sugar",
            "1/2 cup heavy whipping cream, whipped",
            "2/3 cup sugar",
            "1/4 cup cornstarch",
            "1/2 cup water",
            "1/4 cup lemon juice",
            "3 cups fresh or frozen blueberries",
          ],
          steps: [
            "On a lightly floured surface, roll dough to a 1/8-in.-thick circle; transfer to a 9-in. pie plate. Trim to 1/2 in. beyond rim of plate; flute edge. Refrigerate 30 minutes. Preheat oven to 425°.",
            "Line crust with a double thickness of foil. Fill with pie weights, dried beans or uncooked rice. Bake on a lower oven rack until edge is golden brown, 20-25 minutes. Remove foil and weights; bake until bottom is golden brown, 3-6 minutes longer. Cool on a wire rack.",
            "In a small bowl, beat cream cheese and confectioners' sugar until smooth. Fold in whipped cream. Spread into pie shell.",
            "In a large saucepan, combine sugar, cornstarch, water and lemon juice until smooth; stir in blueberries. Bring to a boil over medium heat; cook and stir 2 minutes or until thickened. Cool. Spread over cream cheese layer. Refrigerate until serving.",
          ],
        },
      ],
    };
  },
};
</script>

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

.recipe-modal-container
  height: 70rem
  width: 130rem
  left: 20vw
  background: rgba(255, 247, 204, .95) !important
  position: absolute
  border-radius: 20px
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
  width: 40vw
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