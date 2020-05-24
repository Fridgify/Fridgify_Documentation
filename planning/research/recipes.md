# Recipes

This document is going to showcase some options we have regarding recipes in **Fridgify**.

## Option 1: [spoontacular API](https://spoonacular.com/food-api)
### Benefits
*spoontacular* provides us with everything we need. We have the opportunity to filter recipes based on ingredients and even nutrients. Additionally we would have a lot of room to play around filtering options (importance of fridge content for recipes, etc.). We can even filter after a diet type.

### Pricing
*spoontacular* has the following pricing:
| Category | Price | Rate Limit |
| - | - | - |
| Free | 0$/mo | 150 pts/day <sup>1</sup>
| Cook | 29$/mo | 1500 pts/day (then 0,005$/pt)
| Academic Access<sup>2</sup> | 10$/mo | up to 5000 requests/day

[Pricing - spoontacular](https://spoonacular.com/food-api/pricing)

1 - Calling the endpoint requires 1 point, every returned recipe costs 0.01 point<br/>
2- If there is any intention to commercialize the app, we would have to reconsider this option

## Option 2: [edamam](https://developer.edamam.com/edamam-docs-recipe-api)
### Benefits
*edamam* provides an API, which is able to return recipes based on ingredients. We can even state which type diet type (balanced, high-protein, etc.) or meal type (lunch, dinner, breakfast, snack) it shall have.

### Pricing
*edamam* has the following pricing:
| Category | Price | Rate Limit | Extra
| - | - | - | - |
| Free | 0 | 5000/month, 5/min | no dish type, cuisine filters, basic nutrition, up to 100 results per call
| Startup | Free | 20000/month, 15/min | 30+ diet, health, allergy filters, up to 100 results per call, dish type, cuisine filter

[Pricing - edamam](https://developer.edamam.com/edamam-recipe-api)

This API requires attribution.
