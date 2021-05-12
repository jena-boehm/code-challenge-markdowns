CC12: `Regex`
===

Use the built-in jest testing in CRA to TDD the following functions. Create one set of files: one called `code-challenge-13.js` and one file called `code-challenge-13.test.js`. 

View the [Jest Docs for `expect` style of assertion](https://jestjs.io/docs/using-matchers)

---

Basic test file looks like:
```js
describe('Testing challenge 1', () => {
  test('It should sort the characters by number of children', () => {
    expect(sortByChildren(characters)[0].name).toStrictEqual('Euron');
    expect(sortByChildren(characters)[0].children.length).toStrictEqual(0);
  });
});
```

Use `npm test` to start your test runner locally.

---
## CHALLENGE 1 - Review
`Please use the above example test for your first exercise.`

Use the characters data below for challenge 1:

```js
let characters = [
  {
    name: 'Eddard',
    spouse: 'Catelyn',
    children: ['Robb', 'Sansa', 'Arya', 'Bran', 'Rickon'],
    house: 'Stark'
  },
  {
    name: 'Jon A.',
    spouse: 'Lysa',
    children: ['Robin'],
    house: 'Arryn'
  },
  {
    name: 'Cersei',
    spouse: 'Robert',
    children: ['Joffrey', 'Myrcella', 'Tommen'],
    house: 'Lannister'
  },
  {
    name: 'Daenarys',
    spouse: 'Khal Drogo',
    children: ['Drogon', 'Rhaegal', 'Viserion'],
    house: 'Targaryen'
  },
  {
    name: 'Mace',
    spouse: 'Alerie',
    children: ['Margaery', 'Loras'],
    house: 'Tyrell'
  },
  {
    name: 'Euron',
    spouse: null,
    children: [],
    house: 'Greyjoy'
  },
  {
    name: 'Jon S.',
    spouse: null,
    children: [],
    house: 'Snow'
  }
];
```

Write a function named sortByChildren that sorts the characters below by the number of children in each house (fewest to most). If a house has the same number of children, sort alphabetically by house name.

```js
const sortByChildren = (charArray) => {
 
};
```
---
## CHALLENGE 2
Write a function named containsW that takes in a string. This function should use a regular expression pattern to return true if the string contains the letter 'w' in lower case or false if it does not. 

```js
const containsW = (str) => {

};
```

In | Out
---|---
'hello world' | true
'Hello World' | false
'hello everyone' | false

---
## CHALLENGE 3
Write a function named isNum that takes in a string or number of any length. This function should use a regular expression pattern to return true if the input contains a number, and false if the input does not contain a number.

```js
const isNum = (input) => {
  
};
```

In | Out
---|---
1234567890 | true
'12345' | true
'h3llo w0rld' | true
'hello world' | false
'' | false

---

## CHALLENGE 4
Write a function named containsWorld that takes in a string or number of any length. This function should use a regular expression pattern to return true if the input contains the word 'world' all in lower-case letters, and false if the input does not.

```js
const containsWorld = (input) => {

};
```

In | Out
---|---
'hello world' | true
'Hello World' | false
'hello everyone' | false

---

## CHALLENGE 5
Write a function named isCapitalized that takes in a string. This function should use a regular expression pattern to match all words that begin with a capital letter. It should only match words, not punctuation.

Return an array containing all the matches.

```js
const isCapitalized = (str) => {

};
```

In | Out
---|---
'We only want to Return the Words that begin With a capital Letter' | [ 'We', 'Return', 'Words', 'With', 'Letter' ]
'Given by our hand in the meadow that is called Runnymede, between Windsor and Staines, on the fifteenth day of June in the seventeenth year of our reign (i.e. 1215: the new regnal year began on 28 May).' | ['Given', 'Runnymede', 'Windsor', 'Staines', 'June', 'May']
'these words are all failures' | []

---

## CHALLENGE 6
Write a function named citiesAtoJ that takes in an array of city names and uses a regular expression pattern to return a new array containing any cities that begin with the letters A through J, inclusive.

```js
const citiesAtoJ = (arr) => {

};
```

In | Out
---|---
['Cleveland', 'San Diego', 'Birmingham', 'Seattle', 'Miami', 'New York City', 'Omaha', 'Portland', 'Austin', 'Boston', 'Newport Beach', 'Hoboken'] | 'Cleveland', 'Birmingham', 'Austin', 'Boston', 'Hoboken'
['Albuquerque', 'Chicago', 'Philadelphia', 'Newark', 'Sacramento', 'Eugene'] | ['Albuquerque', 'Chicago', 'Eugene']
[] | []

---

## CHALLENGE 7 - Stretch Goal
You have created a game application and begin by asking users an easy question: In which month is Halloween?

Write a function named matchMonth which uses a regular expression pattern to match any of these inputs: October, Oct, october, oct

If the user enters any of these four inputs, return true. For any other input, return false.

Do not use the vertical bar (pipe) in your pattern.

```js
const matchMonth = (input) => {

};
```

In | Out
---|---
'Oct' | true
'oct' | true
'October' | true
'october' | true
'November' | false
'nov' | false
123 | false
'octob' | false
'OCTOBER' | false
'notOctober' | false

---

## CHALLENGE 8 - Stretch Goal
Write a function named noPunctuation that contains a regular expression pattern to find all of the words that contain a space immediately at the end of the word. Return an array of all such words, still containing the space at the end.

For example, if given the string "Hello, and have a wonderful day!", the word "Hello, " would not be returned because it is immediately followed by a comma. The word "day!" would not be returned because it is immediately followed by an exclamation point.

The expected output of "Hello, and have a wonderful day!" is ["and ", "have ", "a ", "wonderful "].


```js
const noPunctuation = str => {

};
```

In | Out
---|---
'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras lacinia vel massa sed egestas. Nunc faucibus iaculis elit, a scelerisque enim condimentum sed. Aenean ac scelerisque sem, et pharetra diam.' | ['Lorem ', 'ipsum ', 'dolor ', 'sit ', 'consectetur ', 'adipiscing ', 'Cras ', 'lacinia ', 'vel ', 'massa ', 'sed ', 'Nunc ', 'faucibus ', 'iaculis ', 'a ', 'scelerisque ', 'enim ', 'condimentum ', 'Aenean ', 'ac ', 'scelerisque ', 'et ', 'pharetra ']
'Given by our hand in the meadow that is called Runnymede, between Windsor and Staines, on the fifteenth day of June in the seventeenth year of our reign (i.e. 1215: the new regnal year began on 28 May).' | ['Given ', 'by ', 'our ', 'hand ', 'in ', 'the ', 'meadow ', 'that ', 'is ', 'called ', 'between ', 'Windsor ', 'and ', 'on ', 'the ', 'fifteenth ', 'day ', 'of ', 'June ', 'in ', 'the ', 'seventeenth ', 'year ', 'of ', 'our ', 'reign ', 'the ', 'new ', 'regnal ', 'year ', 'began ', 'on ', '28 ']

---

## CHALLENGE 9 - Stretch Goal
You want to teach a friend how to play hangman and want to show them using a partially complete puzzle.

Write a function named hangman which uses the replace method to remove all of the vowels (a, e, i, o, u) from the hangman string, regardless of capitalization, and replace them with an underscore.

The function should return a string containing the consonants in their original positions and underscores where the vowels were previously located.

For example, 'Welcome to Code 301!' will return 'W_lc_m_ t_ C_d_ 301!'.

```js
let hangman = (str) => {

};
```

In | Out
---|---
'This is a regex challenge. We are trying to create a hangman phrase where all of the vowels are missing!' | `Th_s _s _ r_g_x ch_ll_ng_. W_ _r_ try_ng t_ cr__t_ _ h_ngm_n phr_s_ wh_r_ _ll _f th_ v_w_ls _r_ m_ss_ng!`
'I wAnt them all tO bE removed and replaced with Underscores.' | `_ w_nt th_m _ll t_ b_ r_m_v_d _nd r_pl_c_d w_th _nd_rsc_r_s.`

---

## CHALLENGE 10 - Stretch Goal
Write a function named findShells that takes in the string below and uses a regular expression pattern to find all instances of the following words: "sells", "shells", "seashells".

Do not use the vertical bar (pipe) character.

Hint: All of these words end with the letters "ells".

```js
const seashells = `She sells seashells by the seashore. The shells she sells are surely seashells. So if she sells shells on the seashore, I'm sure she sells seashore shells.`;

const findShells = (str) => {

};
```

In | Out
---|---
`seashells` | ['sells', 'seashells', 'shells', 'sells', 'seashells', 'sells', 'shells', 'sells', 'shells']
