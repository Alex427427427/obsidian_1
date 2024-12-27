Category: [[Information Theory]] 
___
Prerequisite:
___
Related: [[What Information Is]] [[Information]]
___
For much of history, information was a vague concept. It was with Claude Shannon in the 1940s that a modern notion of information that was precise and quantifiable was born. 
## What is Information
Information is that which is transported in communication. And communication need not happen if there was no ignorance / uncertainty. That which receives information, undergoes a reduction of uncertainty. The amount of information content of a message corresponds to how much reduction of uncertainty does the message provide. Equivalently, it may be thought of as how surprising is the message, or to what granularity the message stands among the sea of possibilities. 

Information is transported with symbols - an agreed upon pattern of physical change that may or may not be abstracted. 
## Measuring Information Content
Shannon decided that information should be measured in the amount of symbols required to transport it with ideal efficiency. Of course, this amount of information would have different numerical measurements depending on the nature of the symbols. 

Regardless of the specific alphabet or universe of symbols chosen, each symbol ought to reduce uncertainty by a proportion. A sequence of symbols reduces the uncertainty by that proportion, exponentiated. thus the amount of symbols must have a **logarithmic** relationship from the corresponding reduction of uncertainty. 

To understand this concretely, it's best to consider an example. 
##### Coin in a box example
Remember that we wish to measure information by the amount of symbols required to carry it in communication. And communication need not exist if there was no difference of ignorance between the ends of communication. So we construct an example when there is an ignorance asymmetry. 

Person A puts a coin in a closed box. Person B does not know where it is. How could B pinpoint the location of the coin in the box without interacting with it? B must seek communication from A. 

A can only give B information in discrete, because the absolutely precise position of the coin in space has infinitesimal granularity, and would be impossible to convey with finite symbols. Thus A must make a sacrifice - they must divide the box into small regions, and tell B that the coin lies within that region. A may associate each region with a particular message. 

The least granular division is dividing the box by half. Call the left half X and the right half Y. If A tells B either X or Y, then B knows which half of the box the coin must lie. *B's uncertainty about the location of the coin is halved.* And it took A 1 symbol to do so. 

If A instead divides the box into four spaces, the shortest way to associate each space is with two-symbol strings. XX is top left, XY is top right, YX is bottom left, YY is bottom right. *B's uncertainty quartered, and it took A 2 symbols to do so.*

In general, it will take A n symbols to halve B's uncertainty of the coin's location n times. 

We happen to **define one unit of information as one uncertainty-halving symbol**. We call this a "bit", for its binary division of uncertainty. Thus, for an event $x$ (e.g. "coin lies in top left quadrant"), the information content $I$, the number of bits required to communicate that is: 
$$I(E)=\log_{1/2}(Pr(E))$$
$$\boxed{I(E)=-\log_2(Pr(E))}$$
## Units of Information Content
##### Bit
The example given above. A single, uncertainty-halving symbol. Information content formula has base 2. Also known as "Shannon".
##### Nat
Information content formula has base $e$. 
##### Bat
Information content formula has base 10. 
## Entropy
While information content is a property of a specific message, entropy is a property of a universe of symbols, a language, or a collection of possible outcomes of a random event. 

For whatever collection of messages or events, we describe it with a random variable $X$, and use $E$ to denote a possible outcome of the random variable. The Shannon Entropy H is simply the expected information content of such a random event. 
$$\boxed{H=-\sum Pr(E)\log(Pr(E))}$$
Where the base of the logarithm can take any value, depending on the unit of information chosen. 