# Tool reference

All tools are read-only (`readOnlyHint`) and need no authentication.

## search_recipes
`{ "q": string }` – full-text search over titles, ingredients and instructions.

## recipes_list
`{ "page"?: integer >=1, "limit"?: integer 1-100 }` – title, slug, servings, image and page URLs.

## recipes_get
`{ "id_or_slug": string }` – ingredients, method, categories, image and page URL.

## ingredients_search_recipes
`{ "ingredient": string }` – recipes whose ingredient list contains the text.

## categories_list
`{}` – category tree with published recipe counts.

## categories_recipes
`{ "slug": string, "sort"?: "title" | "newest" | "views" | "views30" }` – recipes in a category, including child categories.
