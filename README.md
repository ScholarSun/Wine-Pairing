# Wine-Pairing
## Table of Contents
1. [Introduction](#introduction)
2. [Phase 1: Scraping and Parsing](#paragraph1)
3. [Phase 2: Modeling and Predictions](#paragraph2)
4. [Phase 3: Web Application](#p3)

## Introduction <a name="introduction"></a>
Can a machine learn to pair food and wine?
The main idea: we scrape a bunch of recipes with well known wine pairings and see if a machine can detect a patterns or form abstractions between the two. I expect to see group key ingredients that go well with wines together or perhaps certain wines and cooking methods pair well together. 

## Phase 1: Scraping and Parsing <a name="paragraph1"></a>
This mainly concerns the recipescraping folder.
We first scraped the website allrecipe.com with a list of about 420 full recipies with 17 different types of wine pairings using beautifulsoup. I parsed all the information accordingly and broke down the recipe into a JSON. Heres is an exmample of a parsed recipie: 

```javascript
{
   "id":"20858",
   "name":"Best Ever Jalapeno Poppers",
   "ingredients":[
      {
         "descriptions":[
            "softened"
         ],
         "amount":12,
         "unit":"ounces",
         "ingredient":"cream cheese",
         "labels":[
            "fat and vitamins",
            "dairy"
         ]
      },
      {
         "descriptions":[
            "8 ounce",
            "shredded"
         ],
         "amount":1,
         "unit":"packages",
         "ingredient":"Cheddar cheese",
         "labels":[
            "cheese",
            "dairy"
         ]
      },
      {
         "descriptions":[

         ],
         "amount":1,
         "unit":"tablespoons",
         "ingredient":"bacon bits",
         "labels":[
            "meat"
         ]
      },
      {
         "descriptions":[
            "seeded",
            "halved"
         ],
         "amount":12,
         "unit":"ounces",
         "ingredient":"jalapeno peppers",
         "labels":[
            "spicy",
            "vegetable"
         ]
      },
      {
         "descriptions":[

         ],
         "amount":1,
         "unit":"cups",
         "ingredient":"milk",
         "labels":[
            "fat and vitamins",
            "dairy"
         ]
      },
      {
         "descriptions":[

         ],
         "amount":1,
         "unit":"cups",
         "ingredient":"all purpose flour",
         "labels":[
            "baking ingredient"
         ]
      },
      {
         "descriptions":[
            "dry",
            "crumbs"
         ],
         "amount":1,
         "unit":"cups",
         "ingredient":"bread",
         "labels":[
            "grain"
         ]
      },
      {
         "descriptions":[
            "for frying"
         ],
         "amount":2,
         "unit":"quarts",
         "ingredient":"oil",
         "labels":[
            "cooking liquid"
         ]
      }
   ],
   "directions":[
      {
         "step":0,
         "direction":"In a medium bowl, mix the cream cheese, Cheddar cheese and bacon bits."
      },
      {
         "step":1,
         "direction":"Spoon this mixture into the jalapeno pepper halves."
      },
      {
         "step":2,
         "direction":"Put the milk and flour into two separate small bowls."
      },
      {
         "step":3,
         "direction":"Dip the stuffed jalapenos first into the milk then into the flour, making sure they are well coated with each."
      },
      {
         "step":4,
         "direction":"Allow the coated jalapenos to dry for about 10 minutes."
      },
      {
         "step":5,
         "direction":"Dip the jalapenos in milk again and roll them through the breadcrumbs."
      },
      {
         "step":6,
         "direction":"Allow them to dry, then repeat to ensure  the entire surface of the jalapeno is coated."
      },
      {
         "step":7,
         "direction":"In a medium skillet, heat the oil to 365 degrees F ( 180 degrees C)."
      },
      {
         "step":8,
         "direction":"Deep fry the coated jalapenos 2 to 3 minutes each, until golden brown."
      },
      {
         "step":9,
         "direction":"Remove and let drain on a paper towel."
      }
   ],
   "footnotes":[
      "Editor's Note",
      "We have determined the nutritional value of oil for frying based on a retention value of 10% after cooking. The exact amount may vary depending on cook time and temperature, ingredient density, and the specific type of oil used.",
      "Tip",
      "Aluminum foil can be used to keep food moist, cook it evenly, and make clean-up easier."
   ],
   "labels":[
      "spicy",
      "vegetable"
   ],
   "category":"Appetizers and Snacks",
   "subcategory":"Vegetable",
   "servings":32,
   "calories":149,
   "wine":"Albarino and Alvarinho"
}
```

The base framework scrape was done by @kbrohkahn on github. I adjusted it to my specific requirements. Natural language toolkit library was used to parse each recipe step into sentences. Hardcoded arrays were used to label the ingredients. I traversed the website through beautifulsoup to get the corresponding wine pairings. 

I then manually cleaned up the data to check for mis-labelling and unlabbeled items. I parse this into a csv and then a load it to a pandas dataframe. 

## Phase 2: Modeling and Predictions <a name="paragraph2"></a>


## Phase 3: Web Application <a name="p3"></a>



