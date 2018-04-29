# Hash Vs. Trie, Pros and Cons when storing a word
Hash uses more space than Trie, in certain cases. With a hash table, when hashing a word, it will require twice the amount of space relative to the total number of words you will be storing.
A hash table needs to have extra filler space to avoid collisions which can result in a O(n) when there are many collisions during the hashing phase. With a trie, each character is mapped and will be fully utilized. Only scenario that a Trie may take more space than a hash table, is when you add words with low length, then add one word with a high length value.
The Trie will then create multiple hash tables within each trie node that only have one character stored in it. This creates a lot of useless space.

Another thing to note, the run-time of hashing a word is N(length of the word). Also by hashing then retrieving the value, you are not guaranteed that the value matches the word that you hashed. There is a chance that by hashing two different words, it will create the same hash. That means, you must check the word retrieved with the word you are searching for.

# Memoization vs Dynamic programming
Some people believe these concepts are the same, but they are different. 

First, memoization is about caching previously computed results, then when it comes time to compute the same result again, check in the cache if it was previously computed already, if so, return that. Dynamic programming is very similar, it uses previously computed values in some stored space. However, dynamic programming is instead attempting to use previously calculated values to create a brand new calculation. So you can think of dynamic programming as a bottom up approach to solving problems. Mainly, sub-answers of sub-problems, when summed together, we can the next sub-answer to the next sub-problem, on and on.