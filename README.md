Veggio - Case Study

Veggio (vego, Australian slang for vegetarian, crossed with -gio, the Italian first-person singular: I eat vegetables.)

The problem
Most people who want to eat more vegetables are not short of motivation. They are short of ideas. When someone opens their fridge and sees courgette, chickpeas and a tired bunch of parsley, they reach for their phone and order something. Not because they do not care, but because nothing obvious comes to mind.
Most recipe sites work backwards from popularity rather than forwards from what you have. They surface the dishes everyone already knows, using the ingredients that photograph well. They do not start from your fridge, your mood, or the thing you absolutely cannot stand eating.

What I built
Veggio is an AI-powered vegetable recipe tool with three modes of input and a personalisation layer that builds over time.
The user can tell Veggio what is in their fridge, describe a cuisine or mood, or hit Surprise me and let it pick. In every case it returns three recipe options, each from a different cuisine and cooking method, with a full ingredient list, step by step instructions and a nutritional estimate per serving. If none of the three land, the user can generate again.
Logged-in users can save favourite recipes, complete an onboarding flow that personalises future generations, and confirm which recipes they actually cooked.
Live at veggio.lovable.app

Who it is for
People who want to eat more vegetables but find their repertoire too narrow and too repetitive. The target user is curious and open to trying something new, but not willing to spend an afternoon sourcing unfamiliar ingredients. They are not tracking every macro and they are not already fluent in the kitchen. They just want something good to cook tonight that happens to be vegetable-led.

Key product decisions
Three modes, not one
The core insight was that "what do I cook tonight" is not always the same question. Sometimes the constraint is what is already in the fridge. Sometimes it is a craving or a mood. Sometimes the user just wants to be surprised. Building three distinct input modes rather than a single search field respects that. It also means the tool is useful on different days for different reasons, which matters for retention.
Onboarding as personalisation, not friction
Most recipe tools treat the user as anonymous. Veggio asks five questions on first use: current vegetable intake, motivation, goal, ingredients to always avoid, and cooking confidence. That data changes what gets generated. A user who wants quick and simple gets different recipes than one who is happy to try something more involved. The onboarding is optional and skippable, but users who complete it get a meaningfully better experience.
Cooking confirmation and data integrity
One of the more interesting product decisions was how to track what users actually cook. The obvious approach would be to assume that saving a recipe means cooking it. That would have been wrong. Saving is curiosity, not commitment. Cooking is the real signal.
The solution was a simple explicit prompt: "Did you make this?" shown when a user expands a full recipe and again on saved recipes that have not yet been confirmed. No assumptions, no automation. Just an honest question. This keeps the data meaningful when analytics are added in a later version.
Descoping supplements
An early version of the brief included supplement recommendations for users with nutritional gaps. This was cut deliberately. Advice about supplementation requires clinical expertise that the product cannot claim and the AI cannot reliably provide. Getting it wrong could cause harm. The cut was not about scope, it was about responsibility.
What I cut
Recipe images were considered and parked. The product works without them and adding AI-generated food photography before the core experience is validated would have been decoration over substance.
Salads were scoped and cut. Expanding from vegetable-led meals to salads would have broadened the audience but diluted the positioning. "Vegetables the headline" is a clear brief. Salads are a different product.
A fridge photo upload feature was an interesting idea that added significant technical complexity for uncertain gain. Parked for v2.
Calorie targets, macro tracking and dietary restriction modes were considered and cut. They would have shifted the product toward a different user entirely: someone actively managing their diet rather than simply trying to eat better. That is a different product with a different brief.
Meal planning was scoped and removed. Generating a week of meals is a compelling idea but requires a significantly more complex interface and a different relationship with the user. It belongs in a later version when the single-session experience has been validated.
Shopping list generation was cut for the same reason. Without meal planning, a shopping list has nothing meaningful to draw from.
Analytics, including counts of vegetables eaten, nutritional trends and cooking streaks, require reliable cooking confirmation data to be meaningful. Building the analytics layer before the data layer was solid would have produced misleading outputs. Sequenced for v2.

What I learned
Shipping is a decision. Veggio generated more feature ideas per session than my two previous projects combined. The product kept growing in ambition faster than it was being built. At some point the right move was to draw a line, call the core experience complete, and publish. That decision is as deliberate as any feature choice and deserves to be treated as one.
The prompt is still the product. As with Focal, the quality of the recipe output depends almost entirely on how the model is instructed. Onboarding data only improves results if it is passed into the prompt correctly and the model is told what to do with it. Prompt design is a product decision, not a technical one.
Personalisation changes the value proposition. A recipe generator and a personalised recipe generator are different products. The onboarding flow is what separates Veggio from just asking ChatGPT the same question.

What is next

Staples: a saved list of ingredients the user always has, reducing the typing burden on repeat visits
Number of servings: scaling recipes up or down based on how many people are eating
AI-generated recipe images to make the output more visually compelling
Cooking confirmation dashboard: a simple view of what the user has actually cooked over time
Nutritional analytics: tracking vegetable and macro intake across confirmed meals
Fridge photo upload: photograph your fridge instead of typing the contents
Meal planning and shopping list generation
