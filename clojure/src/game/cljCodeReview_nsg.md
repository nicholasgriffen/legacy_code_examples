## from @nicholasgriffen 
## to @author 
## RE:legacy_code_examples/clojure/src/

### Winning with DRY

#### X Writing Over O Spots 
Perhaps this is cheating, but try:   
`lein run`  
`0`  
`4`  
`8`  
I get: `Game over` and sweet victory.  
Generally I group this with some similar experiences under **Unhandled Illegal User Input**

Non-numbers, duplicates, empty string all crash the program.  

Speaking of **early exits**, this is less a nit than a wishlist item:    
 `As a player I want the option to continue after Game over so I can play games faster.`   

#### Not Winning  
Ultimately the spec does call for an unbeatable opponent, and I did not _not_ win 100% of the time. A tough problem, but one you are on a path to solving.

### Mutable State
In the larger category of [clojure style guide](https://github.com/bbatsov/clojure-style-guide) considerations, I am frankly not super well versed in this, but I have read that swap! is preferred to reset!. 

### Dependency Injection 
I would consider injecting variables as dependencies for more deterministic outcomes.  

### Testing and Documentation
For me, the two are inseprable. Describe's and it's, a little mocha here, a little css reset there, and boom my tests can turn into some nice docs. That's 
for me, for all the future you's and me's typing code.

#### How to play 
I showed the code and game to someone for a few minutes and they asked me: "What game is this supposed to be?" Sure the old X's and O's is widely played in some cultures, but I wonder about people who this game would be inaccessible to, or difficult to play because of how quickly the board changes, similarity of O and 0, things like that.

#### Test cases 
I am easily dizzied by nested branching logic and find that approaching the problem from the ground up with some test cases leads me to more straightforward solutions.   
Something I tried on a hunch: 
##### Line 35: (let [container []])
I removed the container and the conj that builds it and the game ran just the same for me. Artifacts maybe of another strategy, or an idea not yet at fruition?   