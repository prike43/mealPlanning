# Troop Campout Meal Planner

`index.html` is a standalone meal-planning page for preparing a patrol campout menu. It collects trip details, meals, ingredient quantities and costs, cooking notes, and produces a consolidated shopping list and printable plan. It runs in a modern browser without a build step or external dependencies.

## Open the Planner

Open `index.html` in a browser. Use the reference link below the title for the troop's food-planning guidance. Planner entries stay in the current page and are not saved automatically, so export or print the plan before closing or reloading the page.

## Plan a Menu

1. Enter the campout, patrol, Scout responsible, and number of people.
2. For each meal, choose a time slot, enter the dish name, choose a heat source, and enter calories per person.
3. Add an ingredient row for each ingredient. Enter its name, MyPlate food group, quantity for the whole patrol, unit, and unit price. Add or remove rows as needed.
4. Enter cooking methods, equipment and utensils, and any preparation, food-safety, or serving notes.
5. Review meal costs, the consolidated shopping list, and the plan totals. Add or remove meals as needed.
6. Select **Export / Print to PDF** and use the browser's print dialog to print or save a PDF.

The planner starts with one meal and one ingredient row. It always keeps at least one of each. Available meal slots are Friday dinner and dessert, Saturday breakfast, lunch, snack, dinner and dessert, and Sunday breakfast.

## Fields and Calculations

- **Trip information:** campout, patrol, Scout responsible, and number of people. The number of people is used to calculate per-person cost.
- **Meal details:** meal time, dish name, heat source, and calories per person. Meal calorie values are summed into the plan's Calories per person total.
- **Ingredients:** quantity is for the whole patrol, not per person. Each line cost is quantity multiplied by unit price; the meal cost is the sum of its ingredient line costs.
- **Food groups:** each ingredient can be assigned one group: Vegetables, Fruits, Protein, Grains, or Dairy.
- **Cooking notes:** cooking methods, equipment and utensils, and meal notes are included in the plan.
- **Shopping list:** matching ingredient names and units are combined across meals. Quantities and estimated costs are added together.
- **Plan totals:** total estimated cost sums the meal costs; cost per person divides that total by the number of people.

## Validation Rules

Validation runs when **Export / Print to PDF** is selected. If any meal fails a check, the planner lists the problem on that meal and does not open the print dialog. After the first attempt, validation messages update as the plan is edited.

- **Food groups:** every meal, including snacks and desserts, must have a named ingredient assigned to each of the five food groups.
- **Meal budgets:** breakfast and lunch may cost no more than $3 per person; dinner may cost no more than $4 per person. The planner compares each meal's patrol total with the applicable per-person limit multiplied by the number of people. Snack and dessert slots do not have a meal-budget limit.
- **Numeric input settings:** calories, quantities, and unit prices have a configured minimum of zero; number of people has a configured minimum of one. These fields, as well as trip details, dish names, units, and notes, are not separately required by the planner's print validation.

The budget rules are estimates for planning. Review the completed menu for dietary restrictions, food safety, nutrition, and troop approval before purchasing food.