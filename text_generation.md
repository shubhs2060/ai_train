Text genereation

For doing Text genereation there are 2 main techniques

Deterministic
The determinitics one will always provide same output whenver you run for the same input
These are not being used currently with LLMs
Example
One example is the Greedy Approach
The greedy approach as the name suggests will always take the token with the highest probabilty so will always return the same output



Schoistic
This will generate a different output always for the input that is provided

Some examples of this approach are

Top K Approach
The top k approaach works like it will always take the top k tokens and from that select the one with highest probabilty
here k is a hyper parameter that can be configured

Top P Approach
This is the approach that is being used by most of the LLMS
Here P is the hyperparameter that can be set. The P denotes the total value percentage
Suppose each token would have a value . And if we set the P value as 0.85 and the first token itself has the value of 0.85 then it will take that token only as the next token
Another example if the P value is set to 0.85 and combining the minimal 3 token that we get 0.85 then those 3 tokens would be taken as the next token for text generation

Advantage:
Top-P adapts dynamically — sometimes few tokens are enough (for confident predictions), and sometimes more are needed (for uncertainty).

The above approaches are the Pre training for Base model
The Base model is not capable of producing accurate results so we need to do some Post training steps on top of it