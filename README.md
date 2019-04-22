
# Bayes' Theorem

## Introduction

Bayes theorem is an indispensable law of probability, allowing you to deductively quantify unknown probabilities. The theory rests upon conditional probability. Let's take a look in practice.

## Objectives

You will be able to:

* Define Bayes' Theorem
* Provide examples of Bayes' Theorem

## Bayes' Formula

# $P(A|B) = \frac{P(B|A)P(A)}{P(B)}$

## Breaking the Formula Apart

Bayes' theorem is quite intuitive, decomposing the conditional probability of 'A given B' in terms of the probability that both events are true divided by the probability that B is true. Bayes theorem takes this natural idea a step further, expressing the probability that both events are true as a conditional probability multiplied by the condition itself.

To recap, 

Bayes' Theorem takes the definition of the conditional likelihood:

### $P(A|B) = \frac{P(A \cap B)}{P(B)}$

and rewrites the $P(A \cap B)$ as $P(B|A)P(A)$, which makes perfect sense; the probability of B given A is true, multiplied by the probability that A is true, gives us the probability that both are true.

Making this substitution, you have Bayes' Theorem:

### $P(A|B) = \frac{P(B|A)P(A)}{P(B)}$


## A Silly Example

Let's take a simple theoretical example to demonstrate. Imagine there are two fish tanks at the local pet store. The small tank holds 10 Betta fish.  The large tank has 200 goldfish and 35 Betta fish. Given that a fish is a Betta fish, what's the probability it comes from the small tank? 

On the one hand, it seems that if you were to select a fish from the large tank, you'd probably end up with a goldfish. However, because these tanks are of such vastly different sizes, the probability that the fish came from the larger tank is actually more probable. 

Using Bayes' Theorem, you are looking to find the probability that the fish came from the small tank, given that it is a Betta fish:

$P(small\_tank | Betta\_fish) = \frac{P(Beta\_fish | small\_tank)P(small\_tank)}{P(Beta\_fish)}$  

Furthermore, you know:  
$P(Beta\_fish | small\_tank) = 1$  
$P(small\_tank) = \frac{number of fish in small tank}{number of all fish} = \frac{10}{245}$  
$P(Beta\_fish) = \frac{45}{245}$

Giving you:

$P(small\_tank | Betta\_fish) = \frac{1 \bullet \frac{10}{245}}{\frac{45}{245}}$  

$ P(small\_tank | Betta\_fish) = \frac{10}{45}$  

While concrete, this example fails to demonstrate the full power of Bayes' theorem since you had all of the underlying information, so you don't even need to use Bayes' theorem. You could have simply looked at the number of Betta fish in the small tank versus the number of Betta fish overall:   

$\frac{10}{45}$  

giving you exactly the same result.

## A NLP Example

With one silly example out of the way, let's examine a more practical example from natural language processing. In fact, this is an example you'll further flesh out later this section.

A common introductory example to natural language processing or classification is spam. While you may enjoy spam in a can, you probably don't enjoy getting spam in your inbox. 
