---
layout: post
title: The Unique Challenges and Practical Lessons of Simple Predictive Modeling
subtitle: Making fundamental decisions and testing our models
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [ data science]
---

Predicting the listing price of used cars on Craigslist is almost a standard textbook problem.  We use features like model, manufacturer, and year to come up with a rough estimate of what the user listing price of a specific car might look like.  Our features inform the target we're trying to estimate not just because I say so but also because we intuit that idea automatically - two of the same model car may go for different prices if they're from different years or are separate specific makes.

The challenges and lessons for my project came then not from the context of the project but from the simplicity itself.  Tackling a straightforward problem like this allowed me to dive deeper into the minutiae of model design and dataset wrangling.  At the end of it, I gathered valuable intuitions.  Questions with simple answers become opportunities to cement my fundamental and basic understanding of a dense, complex topic.

Often one of the choices that can most meaningfully affect the models we design is choosing whether to estimate values for missing training data or not.  Another important factor is the size of our dataset and how much of it is complete data.  In this particular case, I decided to do some early model testing by trying a dropna() method version of my model, and a version that used SimpleImputer.  In practice, I suspect that estimating missing training data can result in weighter, tighter relationships being formed by your model on the training data - possibly resulting in overfitting.  This ended up being the case for my model once I found metrics (results) for my model versus model testing.  Another theory I have is that observations with missing values may be likely to be missing even more data than just one feature - making the option of dropping these sparsely populated observations much more valuable.
