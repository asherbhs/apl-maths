- [ ] Trying out some formats
    - [x] preliminary definitions
    - [x] nested array representation
    - [x] depth vector
    - [x] path matrix
        - [ ] construction from depth vector
        - [ ] distances between nodes?
        - [x] oh no it's O(nd)
    - [x] parent vector
    - [x] challenge:
        - on paper, draw a simple tree and write down the nested representation, depth vector, path matrix, and parent vector for the tree
        - use an interpreter to check your answers
- [x] parent vector representation
    - [x] this is super great
    - [x] basic operations
        - [x] find children:    `⍸p∊i`
        - [x] find leaves:      `p~⍨⍳≢p`
        - [x] find roots:       `I⍣≡⍨p`
            - note forests are possible
        - [x] select sub-trees: `I@{...}⍣≡⍨p`
        - [x] snip:             `i@i⊢p`
    - [x] ordering
        - [x] don't need to maintain dfpt order
        - [x] need to maintain sibling order if it matters for your operation
        - [x] invert
- [x] relationship to depth vector
    - [x] construction from depth vector
    - [x] finding depths
    - [x] imposing dfpt order
- [x] forests
    - [x] join multiple into a forest
        - join adjacently
        - just concatenate extra data
    - [x] split multiple into individual (deforest)
    - [x] exercise: join all trees in a forest under 1 root: `{0,(⍵≠⍳≢⍵)×1+⍵}`
- [x] deletion
- [ ] bottom-up acculumation
    - [ ] Lisp
        - using key
        - without using key
        - using a fold
    - [ ] go back and look at `_pp_`
    - [ ] challenges
        - [ ] sum each tree in a forest
            - sanity check: sum of trees should equal sum of all values
            - bonus: find `(I⍣≡⍨p)+/⍤⊢⌸v`
        - [ ] find height of every node in a tree
- [ ] top-down construction
    - [ ] Nary
        - [ ] challenge: find Mary
    - [ ] Collatz
    - [ ] Leet as an example
- [ ] manipulating json with matrix import ⎕json
    - grouping astronauts example
    - mention that ⎕xml uses a similar format
- [ ] small calculator as a larger example
    - point to co-dfns for more
- [ ] translations
- [ ] leetcode problems
    - [x] [invert](https://leetcode.com/problems/invert-binary-tree/)
    - [ ] [height balanced](https://leetcode.com/problems/balanced-binary-tree/)
    - [ ] [leaf similar](https://leetcode.com/problems/leaf-similar-trees/)
