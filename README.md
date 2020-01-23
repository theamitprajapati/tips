# Tips for write code

## Don’t be too DRY
DRY stands for Don’t Repeat Yourself. 
That is probably the easiest rule to follow. 
As soon as you see duplicated lines of code, you make an abstraction. 
It can be a base class, a helper method, whatever.

`Poor readability is not a good trade for code repetitions.`



What happens then? The next person comes and the common code needs to change to cover more cases. She or he adds parameters and if statements to cope with the emerging complexities. Soon, the 5 initial and simple lines become 30 lines and it’s difficult to figure out what is happening. 

Poor readability is not a good trade for code repetitions.

It would have been better to keep the duplicated lines. You could then change each instance at will.

The next time you reach for “abstraction over repetition”, ask yourself: how many times did you see someone go back from an abstraction? Like removing a base class and putting the common code back to the inheriting classes. I bet the answer is never.

The reason is abstractions and design patterns in general are cool and sophisticated. And if one exists then “there must be a good reason”. So once you introduce the abstraction, there is a good chance it will stay there forever.

Does this mean you should never use abstractions? No. User abstractions when they fit requirements. Things like:

`“We want to log every call to this method with inputs outputs”
“We want to log every HTTP requests with data a, b, c”
“Every time a user is created we need to do this and that`

These are good candidates for abstraction and there are many more examples, but notice how the requirements are more technical than business related (logging, security, analytics, etc.). It is rare that abstraction friendly requirements are part of your business domain.

Why? Because the business domain is close to the real world. And that we can’t control. Assumptions made at the beginning of a project often fall short pretty soon. Don’t over engineer code just to avoid repetition.

Lego analogy : None. There is no DRY concept in Lego bricks.

## Takeaways
Working smart is not about better code. It is about figuring out what needs to be done, and safely progressing toward the goal.

Large and challenging development tasks will carry unknowns. Embrace it. Learn to work with it.

You will be more productive if you keep things simple and align expectations for the outcome with your team, boss, customer, ideally everybody.

Thanks for reading!
