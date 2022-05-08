# E-commerce Back End Starter Code

Step 1. define columns in models
13.1.6

Be sure to import proper models into the routes

13.4.4 Make sure this PUT route is defined before the /:id PUT route, though. Otherwise, Express.js will think the word "upvote" is a valid parameter for /:id.

use force: true to drop tables and recrete them.

13.4.5 using `through: Vote`

13.4.6
When setting up a many-to-many association between Sequelize models, what association method do we use with both models?

`.belongsToMany()`
.hasMany()

Yes, when setting up a many-to-many relationship, we indicate that both models belong to one another but through a third-party model.

13.5.3 through table vote
