# Dinner Time

A fully responsive application for a recipe finder
[By Andrea Longhitano](https://www.linkedin.com/in/andrealonghitano/)

https://dinner-time-fe.fly.dev

## Built With

- React
- Ruby on Rails
- Postgres
- Fly.io

## Code repositories

I like to split my FE and BE in two repositories, as I prefer the separation of concerns, especially when working with other people. I have added all relevant users to the private repos, please let me know if someone is unable to access them.

### Frontend

[Github repo](https://github.com/andlon10/dinner-time-fe)

### Backend

[Github repo](https://github.com/andlon10/dinner-time)

## Task description

This is my technical task for my application at Pennylane.

### Main Challenges

When I started working on this I was not very familiar with Ruby and Rails, while I did work with them years ago it has been quite a long time so I spent a day going through the relevant docs.

The very first issue I encountered was with the provided dataset. I believe the data was scraped using a script which resulted in a quite incoherent set, where certain fields are not representing the correct information.

For example, what should be a simple "egg" ingredient comes in tens of variations based on the ingredient amount, such as "egg yolk, egg yolks, egg lightly beaten, large egg, eggs lightly beaten" and so on. This poses several challenges, especially in term of searching for ingredient names (from the client) and displaying relevant ingredients. I did a little data transformation but due to the limited time I figured it would make sense to focus on the implemenation of the taks, since in an ideal scenario the data would be well structured.
Note: In order to fix this duplicate issue, some ingredient/recipes will be provided in the **Easy to find recipes** section to allow for easy searching of recipes among the many duplicate ingredients.

Another slightly time consuming process was learning to use Fly.io. Now I find it quite fun to use, but initially I had to spend some time reading their forum to solve some problems I was facing.

Lastly, another challenge I faced was the time constraint. I was given roughly a week to complete this so I didn't spend too much time focusing on the small bits, I mostly made sure the end to end flow was complete and worked well.

## User stories already implemented

- As a first time user, I want to be able to find recipes with minimal instructions, so that I can enjoy them straight away.
- As a busy user, I want to select ingredients that I already have at home, so I can avoid unnecessary shopping.
- As a user, I want recipe URLs to reflect my ingredient selection, so I can share or revisit recipes easily.

## Ideal future user stories

- As a user, I want to be able to see the the recipe instructions, so that I can easily know how to prepare them (difficult with the current dataset).
- As a user, I want to be able to exclude certain types of recipes or ingredients, so that I can follow my dietary preferences, such as being vegan or vegetarian.
- As a user, I want to be able to exclude ingredients i'm allergic to, so that I can safely prepare meals.
- As a user, I want to be able to save my favourite recipes so that I can easily find them.

## Easy to find recipes

As I mentioned earlier, due to the incosistent ingredient values in the seed file, the list of ingredients is quite confusing and has many duplicates. To speed up the review of the functionalities, I am attaching a list of ingredients you can **copy and paste** into the search field to find matching recipes quickly.
Note: **match the exact string so that you can avoid the duplicates**

- Pretzel Buns - [Link](https://dinner-time-fe.fly.dev/?ingredient_ids%5B%5D=6728&ingredient_ids%5B%5D=6601&ingredient_ids%5B%5D=6691):

  - ½ teaspoons active dry yeast
  - teaspoon white sugar
  - ½ cup warm water

- Honey Whole Wheat Bread - [Link](https://dinner-time-fe.fly.dev/?ingredient_ids%5B%5D=6663&ingredient_ids%5B%5D=6726&ingredient_ids%5B%5D=6727)

  - tablespoons vegetable oil
  - tablespoons honey
  - ⅓ teaspoon salt

- Awesome Carrot Muffins - [Link](https://dinner-time-fe.fly.dev/?ingredient_ids%5B%5D=6776&ingredient_ids%5B%5D=6801&ingredient_ids%5B%5D=6661)
  - cup raisins
  - teaspoons baking soda
  - cups warm water

## Final thoughts

### Suggestions for a more developer friendly task

Although I enjoyed this taks, I struggled a bit with working with the dataset provided. I think that for a non data science role this file is a little difficult to work with and requires time consuming work to be sanitised in a good way, which unfortunately I had little of. While I think the main features of the prototype are well designed, some ugly UX elements could be fixed with a more structured file.

### Use of AI tools

I am generally in favour of using AI tools such as Copilot, Cursor, etc. during development, to speed up things when dealing with boilerplate code or repetetive tasks. In this project I limited the scope of their use to the following actions, to prevent building something I'm not 100% familiar with:

- Transforming the dataset (I used a mix of migrations and SQL commands to try to sanitise the ingredients)
- Generate the rails seed for the JSON file
- Troubleshooting Fly.io errors, mostly related to figuring out why my database was not being seeded correctly and some issues I had with the deployment phase.
