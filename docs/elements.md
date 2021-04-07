# Functions and constants
cmd | inputs | out/effect
---|---|---
| ƛ |   |  * lambda map: ƛ...; |
| ¬ | (a: any)                            |  not a |
| ∧ | (a: any, b: any)                    |  a and b |
| ⟑ | (a: any, b: any)                    |  b and a |
| ∨ | (a: any, b: any)                    |  a or b |
| ⟇ | (a: any, b: any)                    |  b or a |
| ÷ | (a: any)                            |  stack += iterable(a) |
| « |   |  * base-255 compressed string: «...« |
| \<newline> |   |  * NOP |
| » |   |  * base-255 compressed number: »...» |
| ° |   |  * function reference: °defined_function_name; |
| • | (a: number, b: number)              |  log_a(b) |
|  | (a: number, b: string)              |  [char * a for char in b] |
|  | (a: string, b: number)              |  [char * b for char in a] |
|  | (a: string, b: string)              |  a.with_capitalisation_of(b) |
|  | (a: list, b: list)                  |  a molded to the shape of b |
|  | (otherwise)                         |  vectorised |
| ‘ |   |  * one-byte dictionary |
| † | (a: function)                       |  * call function reference |
|  | (a: non-function)                   |  exec(a) |
| € | (a: any, b: any)                    |  a.split_on(b) |
| ½ | (a: number)                         |  a / 2 |
|  | (a: string)                         |  a split into two strings of equal lengths (as close as possible) |
|  | (otherwise)                         |  vectorised |
| ∆ |   |  * mathematic digraphs |
| ø |   |  * string digraphs |
| ↔ | (a: any, b: number)                 |  ations_with_replacement(a, length=b) |
|  | (a: any, b: non-number)             |  remove elements in a that are not in b |
|  | (a: function, b: any)               |  apply a on b until the result doesn't change. Collects intermittent values |
| Ø |   |  infinite list of odd numbers |
| ⌐ | (a: number)                         |  1 - a |
|  | (a: string)                         |  a.split(",") |
|  | (otherwise)                         |  vectorised |
| æ | (a: number)                         |  is_prime(a) |
|  | (a: string)                         |  case_of(a) |
|  | (otherwise)                         |  vectorised |
| ʀ | (a: number)                         |  range(0, a + 1) |
|  | (a: otherwise)                      |  str(a) == "0" |
| ʁ | (a: number)                         |  range(0, a) |
|  | (a: otherwise)                      |  str(a) == "0" # that's because of the way this is implemented - it's literally just 0ar |
| ɾ | (a: number)                         |  range(1, a + 1) |
|  | (a: otherwise)                      |  str(a) == "1" |
| ɽ | (a: number)                         |  range(1, a) |
|  | (a: otherwise)                      |  str(a) == "1" |
| Þ |   |  * list digraphs |
| ƈ | (a: number, b: number)              |  a choose b (n choose r, ncr, n c r) |
|  | (a: number, b: string)              |  [random.choice(b) for _ in range(a)] |
|  | (a: string, b: number)              |  [random.choice(a) for _ in range(b)] |
|  | (a: string, b: string)              |  set(a) == set(b) |
|  | (otherwise)                         |  vectorised |
| ∞ |   |  list of all positive integers, starting at 0 |
| ¨ |   |  * other digraphs |
| \<space> |   |  * NOP |
| ! |   |  length(stack) |
| " | (a: any, b: any)                    |  [a, b] # pair |
| $ | (a: any, b: any)                    |  b, a |
| % | (a: number, b: number)              |  a % b # modulo, modulus |
|  | (a: number, b: string)              |  (b split into a equal pieces)[-1] |
|  | (a: string, b: number)              |  (a split into b equal pieces)[-1] |
|  | (a: string, b: string)              |  a.format(b) |
|  | (a: string, b: list)                |  a.format(b) |
|  | (otherwise)                         |  vectorised |
| & |   |  * apply next element to register: &<element> |
| ' |   |  * lambda filter: '...; |
| ( |   |  * open for loop: (variable|...) |
| ) |   |  * close for loop |
| \* | (a: number, b: number)              |  a * b |
|  | (a: number, b: string)              |  b repeated a times |
|  | (a: string, b: number)              |  a repeated b times |
|  | (a: string, b: string)              |  [char + b for char in a] |
|  | (otherwise)                         |  vectorised |
| + | (a: number, b: number)              |  a + b |
|  | (a: number, b: string)              |  concat(a, b) |
|  | (a: string, b: number)              |  concat(a, b) |
|  | (a: string, b: string)              |  concat(a, b) |
|  | (otherwise)                         |  vectorised |
| , | (a: any)                            |  print(a) |
| - | (a: number, b: number)              |  a - b |
|  | (a: number, string)                 |  ("-" * a) + b |
|  | (a: string, b: number)              |  a + ("-" * b) |
|  | (a: string, b: string)              |  a.remove(b) |
|  | (otherwise)                         |  vectorised |
| . |   |  * decimal seperator |
| / | (a: number, b: number)              |  a / b |
|  | (a: number, b: string)              |  b split into a even length pieces. There may be an extra part if the string is too long. |
|  | (a: string, b: number)              |  a split into b even length pieces. There may be an extra part if the string is too long. |
|  | (a: string, b: string)              |  a.split(b) |
|  | (otherwise)                         |  vectorised |
| 0 |   |  * numeric literal |
| 1 |   |  * numeric literal |
| 2 |   |  * numeric literal |
| 3 |   |  * numeric literal |
| 4 |   |  * numeric literal |
| 5 |   |  * numeric literal |
| 6 |   |  * numeric literal |
| 7 |   |  * numeric literal |
| 8 |   |  * numeric literal |
| 9 |   |  * numeric literal |
| : | (a: any)                            |  a, a  # duplicate |
| ; |   |  * closes a structure |
| \< | (a: non-list, b: non-list)          |  a < b # (numbers converted to strings) |
|  | (a: list, b: any)                   |  vectorised |
| = | (a: non-list, b: non-list)          |  a == b |
|  | (a: list, b: any)                   |  a == b # vectorising equals |
| \> | (a: non-list, b: non-list)          |  a > b # (numbers converted to strings) |
|  | (a: list, b: any)                   |  vectorised |
| ? |   |  input() |
| @ |   |  * define a function: @name:parameters|...; |
|  |   |  * call a function: @name; |
| A | (a: any)                            |  all(a) # all, all truthy |
| B | (a: non-list)                       |  int(a, 2) # convert from binary, binary to ten, 2 to 10 |
|  | (a: list)                           |  int(a, 2) # treats the items in the list as digits |
| C | (a: number)                         |  chr(a) # codepoint to character |
|  | (a: string)                         |  ord(a) if len(a) == 1 else [ord(char) for char in a] |
|  | (otherwise)                         |  vectorised |
| D | (a: any)                            |  a, a, a # triplicate, three copies |
| E | (a: number)                         |  2 ** a # 2 power, two power |
|  | (a: string)                         |  eval(a) |
|  | (otherwise)                         |  vectorised |
| F | (a: any, b: function)               |  filter(b, a) # filter, keep, python filter |
|  | (a: any, b: any)                    |  remove elements of a that are in b |
| G | (a: any)                            |  max(a) # monadic maximum, maximum iterable |
| H | (a: non-list)                       |  int(a, 16) # convert from hexadecimal, hexadecimal to ten, 16 to 10 |
|  | (a: list)                           |  int(a, 16) # treats the items in the list as digits |
| I | (a: number)                         |  int(a) |
|  | (a: string)                         |  int(a) |
|  | (a: list)                           |  int(a) # treats the items in the list as digits |
| J | (a: list, b: non-list)              |  a.append(b) |
|  | (a: non-list, b: list)              |  b.prepend(a) |
|  | (a: list, b: list)                  |  merged(a, b) |
|  | (a: non-list, b: non-list)          |  concatenated(a, b) |
| K | (a: number)                         |  divisors(a) |
|  | (a: string)                         |  prefixes(a) |
|  | (otherwise)                         |  vectorised |
| L | (a: any)                            |  len(a)  # length |
| M | (a: any, b: function)               |  map(b, a) # map, apply to each |
|  | (a: any, b: any)                    |  [[a, item] for item in b] |
| N | (a: number)                         |  -a # negate, * -1 |
|  | (a: string)                         |  swap_case(a) |
|  | (otherwise)                         |  vectorised |
| O | (a: any, b: any)                    |  a.count(b) # non-vectorising count |
| P | (a: any, b: any)                    |  a.strip(b) |
| Q |   |  exit() # quit, halt, stop |
| R | (a: any, b: function)               |  reduce a by b # reduction, reduce |
|  | (a: any, b: any)                    |  a, vectorised_reverse(b) |
| S | (a: any)                            |  str(a) # string, to string, stringify |
| T | (a: any)                            |  [item for item in a if bool(item)] # truthy elements only |
| U | (a: any)                            |  uniquifed(a) # uniquify, unique items |
| V | (a: any, b: any, c: any)            |  a.replace(needle=b, replacement=c) # replace |
| W |   |  [stack] # wrap stack |
| X |   |  * context level down |
| Y | (a: any, b: any)                    |  interleave(a, b) |
| Z | (a: any, b: any)                    |  zip(a, b) |
| [ |   |  * open if statement: [truthy|falsey] |
| \\ |   |  * one character literal: \<letter> |
| ] |   |  * close if statement |
| ` |   |  * string: `...` |
| a | (a: any)                            |  any(a)  # irony. |
| b | (a: number)                         |  bin(a) # binary representation, base 10 to 2 |
|  | (a: string)                         |  [bin(ord(char)) for char in a] |
|  | (otherwise)                         |  vectorised |
| c | (a: any, b: any)                    |  a in b # non-vectorising contains |
| d | (a: number)                         |  a * 2 # double |
|  | (a: string)                         |  a * 2 # double |
|  | (otherwise)                         |  vectorised |
| e | (a: number, b: number)              |  a ** b # exponent, exponentiation |
|  | (a: number, b: string)              |  every ath letter of b |
|  | (a: string, b: number)              |  every bth letter of a |
|  | (a: string, b: string)              |  regex.match(pattern=a, string=b).span() |
|  | (otherwise)                         |  vectorised |
| f | (a: any)                            |  flattened(a) # flatten, deep flatten |
| g | (a: any)                            |  min(a) # monadic minimum, minimum iterable |
| h | (a: any)                            |  a[0] # head, first item |
| i | (a: any, b: number)                 |  a[b] # index |
|  | (a: any, b: [x, y])                 |  a[x:y] # index |
|  | (a: any, b: [x, y, m])              |  a[x:y:m] # index |
| j | (a: any, b: any)                    |  a.join(b) # join |
| k |   |  * constant digraphs |
| l | (a: any, b: number)                 |  n-wise_group(a, b) |
|  | (a: any, b: non-number)             |  length(a) == length(b) |
| m | (a: any)                            |  a + reversed(a) # mirror, mirrored, palindromised |
| n |   |  * context variable |
| o | (a: any, b: any)                    |  a.replace(b, "") # equivalent to b``V |
| p | (a: any, b: any)                    |  a.startswith(b) # has prefix, starts with |
| q | (a: any)                            |  "`" + a + "`" # uneval, quotify |
| r | (a: number, b: number)              |  range(a, b) |
|  | (otherwise)                         |  regex.has_match(pattern=a, string=b) # regex match |
| s | (a: any)                            |  sorted(a) # min → max, sort |
| t | (a: any)                            |  a[-1] # tail, last item |
| u |   |  -1 |
| v |   |  * vectorise next element: v<element> |
| w | (a: any)                            |  [a] # single wrap |
| x |   |  * context level up |
| y | (a: any)                            |  uninterleave(a) |
| z | (a: any, b: function)               |  zip(a, map(b, a)) #zipmap, map and zip |
|  | (a: any, b: any)                    |  a, zip(b, b) |
| { |   |  * open while loop: {condition|...} |
| \| |   |  * branch in structure (syntax) |
| } |   |  * close while loop |
| ~ |   |  * filter by element (monad) |
|  |   |  * execute element without popping (dyad) |
| ß | (a: any)                            |  * execute element if a is truthy: ß<element> |
| ↑ | (a: any)                            |  max(a, key=lambda x: x[-1]) |
| ↓ | (a: any)                            |  min(a, key=lambda x: x[-1]) |
| ∴ | (a: any, b: any)                    |  max(a, b) |
| ∵ | (a: any, b: any)                    |  min(a, b) |
| › | (a: number)                         |  a + 1 # increment |
|  | (a: string)                         |  concat(a, "1") |
|  | (otherwise)                         |  vectorised |
| ‹ | (a: number)                         |  a - 1 # decrement |
|  | (a: string)                         |  a + "-" |
|  | (otherwise)                         |  vectorised |
| ∷ | (a: number)                         |  a % 2 # parity, bit |
|  | (a: string)                         |  [a / 2][-1] |
|  | (otherwise)                         |  vectorised |
| ¤ |   |  "" # empty string |
| ð |   |  " " # space string |
| → | (a: any)                            |  * variable set (= a): →name |
| ← |   |  * variable get: ←name |
| β | (a: any, b: number)                 |  a to base 10 from arbitrary base b |
|  | (a: string, b: string)              |  a to base 10 from custom base b |
| τ | (a: number, b: number)              |  a from base 10 to arbitrary base b |
|  | (a: number, b: string)              |  a from base 10 to custom base b |
|  | (a: number, b: list)                |  a from base 10 to custom base b |
| ȧ | (a: number)                         |  abs(a) |
|  | (a: string)                         |  lowercase(a) |
|  | (otherwise)                         |  vectorised |
| ḃ | (a: any)                            |  bool(a) |
| ċ | (a: any)                            |  a != 1 # falsey |
| ḋ | (a: number, b: number)              |  [a / b, a % b]  # divmod, div mod, [div, mod] |
|  | (a: string, b: number)              |  combinations of a with length b |
|  | (a: list, b: number)                |  combinations of a with length b |
|  | (a: string, b: string)              |  a.trim(b) |
| ė | (a: any)                            |  enumerate(a) |
| ḟ | (a: any, b: any)                    |  a.find(b) |
|  | (a: any, b: function)               |  truthy_indexes(map(b, a)) |
| ġ | (a: list)                           |  gcd(a)  # greatest common denominator |
|  | (a: number, b: number)              |  gcd(a, b) # greatest common denominator |
|  | (a: string, b: any)                 |  longest common suffix(a, str(b)) |
| ḣ | (a: any)                            |  a[0], a[1:] # head extract |
| ḭ | (a: number, b: number)              |  a // b  # integer divison |
| ŀ | (a: any, b: any, c: number)         |  a.find(b, start=c) |
| ṁ | (a: any)                            |  arithmetic_mean(a)  # average |
| ṅ | (a: function)                       |  first integer where a(x) is truthy |
|  | (otherwise)                         |  "".join(a) |
| ȯ | (a: function, b: number)            |  first n integers where a(x) is truthy |
|  | (a: any, b: number)                 |  a[b:] |
| ṗ | (a: any)                            |  powerset(a) |
| ṙ | (a: number)                         |  round(a) |
| ṡ | (a: any, b: function)               |  sorted(a, key=b) |
|  | (a: number, b: number)              |  range(a, b + 1)  # inclusive range |
|  | (a: string, b: any)                 |  regex.split(string=a, pattern=str(b)) # split on regex match |
|  | (a: any, b: string)                 |  regex.split(string=str(a), pattern=b) # split on regex match |
| ṫ | (a: any)                            |  a[:-1], a[-1] # tail extract |
| ẇ | (a: any, b: number)                 |  a wrapped in chunks of length b |
|  | (a: any, b: function)               |  apply b to every second item of a |
|  | (a: function, b: any)               |  apply a to every second item of b |
| ẋ | (a: any, b: number)                 |  repeat(a, times=b) |
|  | (a: function, b: function, c: any)  |  collect_until_false(predicate=f, modifying_function=g, inital=a) # Collect the results of apply g on a while f(a) is truthy |
| ẏ | (a: any)                            |  range(0, len(a)) |
| ż | (a: any)                            |  range(1, len(a) + 1) |
| √ | (a: number)                         |  sqrt(a)  # square root |
|  | (a: string)                         |  every second character of a |
|  | (otherwise)                         |  vectorised |
| ⟨ |   |  * open a list: ⟨...⟩ |
| ⟩ |   |  * close a list |
| ‛ |   |  * two char string: ‛.. |
| ₀ |   |  10 |
| ₁ |   |  100 |
| ₂ | (a: number)                         |  a % 2 == 0 |
|  | (a: string)                         |  len(a) % 2 == 0 |
| ₃ | (a: number)                         |  a % 3 == 0 |
|  | (a: string)                         |  len(a) == 1 |
| ₄ |   |  26 |
| ₅ | (a: number)                         |  a % 5 == 0 |
|  | (a: string)                         |  a, len(a) |
| ₆ |   |  64 |
| ₇ |   |  128 |
| ₈ |   |  256 |
| ¶ |   |  "\n" # newline |
| ⁋ | (a: any)                            |  "\n".join(a) # join on newlines |
| § | (a: any)                            |  vertical_join(a) # vertical join |
| ε | (a: any, b: string)                 |  vertical_join(a, padding=b)  # vertical join |
|  | (a: number, b: number)              |  abs(a - b) |
| ¡ | (a: number)                         |  factorial(a) |
|  | (a: string)                         |  sentence_case(a) |
|  | (otherwise)                         |  vectorised |
| ∑ | (a: any)                            |  sum(a) |
| ¦ | (a: any)                            |  cumulative_sum(a)  # cumulative sum |
| ≈ | (a: any)                            |  are all elements the same? |
| µ |   |  * lambda sort: µ...;. The same as λ...;ṡ |
| Ȧ | (a: list, b: number, c: any)        |  a[b] = c |
| Ḃ | (a: any)                            |  a, reversed(a) # bifurcate |
| Ċ | (a: any)                            |  counts_of_items(a) |
| Ḋ | (a: number, b: number)              |  a % b == 0 |
| Ė | (a: string)                         |  Vyxal_exec(a) |
|  | (a: number)                         |  1 / a  # reciprocal |
|  | (otherwise)                         |  vectorise |
| Ḟ | (a: function, b: any)               |  push Generator of function f with initial vector a |
|  | (a: function, b: any, c: number)    |  push Generator of function f with intial vector a, limited to b items (if present) |
| Ġ | (a: any)                            |  group_consecutive(a) |
| Ḣ | (a: any)                            |  a[1:] |
| İ | (a: any, b: list)                   |  [a[item] for item in b]  # indexed into |
| Ŀ | (a: any, b: any, c: any)            |  transliterate(a, b, c) |
|  | (a: function, b: function, c: any)  |  repeat_until_false(predicate=a, modifying_function=b, inital=c) # equivalent to ẋt |
| Ṁ | (a: list, b: number, c: any)        |  a.insert(b, c) |
|  | (a: list, b: number, c: function)   |  c mapped over every bth item of a |
| Ṅ | (a: number)                         |  integer_paritions(a) |
|  | (otherwise)                         |  " ".join(a) |
| Ȯ |   |  stack[-2] |
| Ṗ | (a: any)                            |  permutations(a) |
| Ṙ | (a: any)                            |  reversed(a) |
| Ṡ |   |  sum(stack) |
| Ṫ | (a: any)                            |  a[:-1] |
| Ẇ | (a: any, b: any)                    |  a.split_and_keep_delimiter(b) |
| Ẋ | (a: any, b: any)                    |  cartesian_product(a, b) |
|  | (a: function, b: any)               |  repeatedly apply a on b until b doesn't change |
| Ẏ | (a: any, b: number)                 |  a[0:b] |
| Ż | (a: any, b: number)                 |  a[1:b] |
| ₌ |   |  * parallel apply next two elements: ₌<element><element> |
| ₍ |   |  * parallel apply next two elements and put into list: ₍<element><element>. Equivalent to ₌..≬ |
| ⁰ |   |  first item from input history |
| ¹ |   |  second item from input history |
| ² | (a: number)                         |  a ** 2 # squared |
|  | (a: string)                         |  a formatted as a square |
|  | (otherwise)                         |  vectorised |
| ∇ | (a: any, b: any, c: any)            |  c, a, b |
| ⌈ | (a: number)                         |  ceiling(a) |
| ⌊ | (a: number)                         |  floor(a) |
| ⁾ | (a: number)                         |  10 ** a |
| ¯ | (a: any)                            |  deltas(a) |
| ± | (a: number)                         |  sign_of(a) # negative = -1, 0 = 0, positive = 1 |
|  | (a: string)                         |  a |
|  | (otherwise)                         |  vectorised |
| ₴ | (a: any)                            |  print(a, end="") |
| … |   |  print(stack[-1]) |
| □ |   |  all inputs wrapped in a list |
| ↳ | (a: number, b: number)              |  a >> b |
|  | (a: string, b: number)              |  a.rjust(b) # right justify |
|  | (a: number, b: string)              |  b.rjust(a) # right justify |
|  | (a: string, b: string)              |  a.rjust(len(b) - len(a)) |
|  | (otherwise)                         |  vectorised |
| ↲ | (a: number, b: number)              |  a << b |
|  | (a: string, b: number)              |  a.ljust(b) # left justify |
|  | (a: number, b: string)              |  b.ljust(a) # left justify |
|  | (a: string, b: string)              |  a.ljust(len(b) - len(a)) |
|  | (otherwise)                         |  vectorised |
| ⋏ | (a: number, b: number)              |  a and b (bitwise) # a & b |
|  | (a: string, b: number)              |  a.center(b) # center |
|  | (a: number, b: string)              |  b.center(a) # center |
|  | (a: string, b: string)              |  a.center(len(b) - len(a)) |
|  | (otherwise)                         |  vectorised |
| ⋎ | (a: number, b: number)              |  a or b (bitwise) # a | b |
|  | (a: string, b: number)              |  remove bth character of a |
|  | (a: number, b: string)              |  remove ath character of b |
|  | (a: string, b: string)              |  a and b joined on longest common prefix and suffix # `abc``cabc`⋎ -> `abcabc` |
|  | (otherwise)                         |  vectorised |
| ꘍ | (a: number, b: number)              |  a xor b (bitwise) |
|  | (a: string, b: number)              |  every bth character of a |
|  | (a: number, b: string)              |  every ath character of b |
|  | (a: string, b: string)              |  levenshtein_distance(a, b) |
|  | (otherwise)                         |  vectorised |
| ꜝ | (a: number)                         |  not a (bitwise) # ~a |
|  | (a: string)                         |  are any letters in a uppercase? |
|  | (a: list)                           |  infinitely cycle list |
| ℅ | (a: any)                            |  random.choice(a) |
| ≤ | (a: any, b: any)                    |  a <= b |
| ≥ | (a: any, b: any)                    |  a >= b |
| ≠ | (a: any, b: any)                    |  a != b (non-vectorising) |
| ⁼ | (a: any, b: any)                    |  a == b (non-vectorising) |
| ƒ | (a: number)                         |  fractionify(a) # returns a two-item list of [numerator, denominator] |
|  | (a: string)                         |  can a be evaluated as a float? |
| ɖ | (a: list)                           |  decimalify(a) # opposite of ƒ, reduce by division |
| × |   |  "*" |
| ∪ | (a: any, b: any)                    |  set union |
| ∩ | (a: any, b: any)                    |  set intersection |
| ⊍ | (a: any, b: any)                    |  set(a) ^ set(b) |
| £ |   |  set register without emptying |
| ¥ |   |  push register without emptying |
| ⇧ | (a: list)                           |  graded_up(a) |
|  | (a: string)                         |  a.upper() |
|  | (a: number)                         |  a + 2 |
| ⇩ | (a: list)                           |  graded_down(a) # equivalent to ⇧Ṙ |
|  | (a: string)                         |  a.lower() |
|  | (a: number)                         |  a - 2 |
| Ǎ | (a: string)                         |  remove all non-letters of a |
|  | (a: number)                         |  2 ** a |
|  | (otherwise)                         |  vectorised |
| ǎ | (a: number)                         |  push ath prime |
|  | (a: string)                         |  substrings(a) |
|  | (otherwise)                         |  vectorised |
| Ǐ | (a: number)                         |  prime factorisation of a |
|  | (a: string)                         |  a + a[0] # enclosed a |
|  | (otherwise)                         |  vectorised |
| ǐ | (a: number)                         |  all prime factors of a (includes duplicates) |
|  | (a: string)                         |  a.titlecase() |
|  | (otherwise)                         |  vectorised |
| Ǒ | (a: number, b: number)              |  how many times does b divide a?  # order |
|  | (a: string, b: string)              |  remove b from a until a doesn't change |
| ǒ | (a: number)                         |  a % 3 |
|  | (a: string)                         |  is string empty? |
|  | (otherwise)                         |  vectorised |
| Ǔ | (a: any, b: number)                 |  rotate a b units to the left |
|  | (a: any, b: any)                    |  a, b rotated to the left once |
| ǔ | (a: any, b: number)                 |  rotate a b units to the right |
|  | (a: any, b: any)                    |  a, b rotated to the right once |
| ⁽ |   |  * one-byte lambda: ⁽<element> |
| ‡ |   |  * two-byte lambda: ‡<element><element> |
| ≬ |   |  * three-byte lambda: ≬<element><element><element> |
| ∂ |   |  * two-byte dyad: ∂<element><element> |
| ⁺ |   |  * index of next character in codepage + 101: ⁺<character> |
| ¢ | (a: string, b: string, c: string)   |  replace b in a with c until a doesn't change |
| ↵ | (a: string)                         |  a.split("\n") |
|  | (a: number)                         |  is a an integer? |
|  | (otherwise)                         |  vectorised |
| ⅛ | (a: any)                            |  push a to global array |
| ¼ |   |  pop from global array and push to stack |
| ¾ |   |  push global array |
| Π | (a: any)                            |  product(a) # reduce by multiplication |
| „ |   |  * rotate stack left |
| ‟ |   |  * rotate stack right |
| kA |   |  "ABCDEFGHIJKLMNOPQRSTUVWXYZ" (uppercase alphabet) |
| ke |   |  2.718281828459045            (math.e) |
| kf |   |  "Fizz" |
| kb |   |  "Buzz" |
| kF |   |  "FizzBuzz" |
| kH |   |  "Hello, World!" |
| kh |   |  "Hello World" |
| k1 |   |  1000 |
| k2 |   |  10000 |
| k3 |   |  100000 |
| k4 |   |  1000000 |
| ka |   |  "abcdefghijklmnopqrstuvwxyz" |
| kL |   |  "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ" |
| kd |   |  "0123456789" |
| k6 |   |  "0123456789abcdef" |
| k^ |   |  "0123456789ABCDEF" |
| ko |   |  "01234567" |
| kp |   |  "!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~" |
| kP |   |  "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~ 	" |
| kw |   |  All ASCII whitespace |
| kr |   |  "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ" |
| kB |   |  "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz" |
| kZ |   |  "ZYXWVUTSRQPONMLKJIHGFEDCBA" |
| kz |   |  "zyxwvutsrqponmlkjihgfedcba" |
| kl |   |  "ZYXWVUTSRQPONMLKJIHGFEDCBAzyxwvutsrqponmlkjihgfedcba" |
| ki |   |  3.141592653589793 |
| kn |   |  math.nan |
| kD |   |  * Today's date, in the format YYYY-MM-DD |
| kN |   |  * Today's time, as a list of ⟨hh|mm|ss⟩ |
| kḋ |   |  * Today's date, in the format DD/MM/YYYY |
| kḊ |   |  * Today's date, in the format MM/DD/YYYY |
| kð |   |  * Today's date, in the format ⟨DD|MM|YYYY⟩ |
| kβ |   |  "{}[]<>()" |
| kḂ |   |  "()[]{}" |
| kß |   |  "()[]" |
| kḃ |   |  "([{" |
| k≥ |   |  ")]}" |
| k≤ |   |  "([{<" |
| kΠ |   |  ")]}>" |
| kv |   |  "aeiou" |
| kV |   |  "AEIOU" |
| k∨ |   |  "aeiouAEIOU" |
| k⟇ |   |  * Yields the Vyxal codepage |
| k½ |   |  [1, 2], |
| kḭ |   |  2 ** 32, |
| k+ |   |  [1, -1], |
| k- |   |  [-1, 1], |
| k≈ |   |  [0, 1], |
| k/ |   |  '/\\', |
| kR |   |  360, |
| kW |   |  'https://', |
| k℅ |   |  'http://', |
| k↳ |   |  'https://www.', |
| k² |   |  'http://www., |
| k" |   |  16, |
| k∴ |   |  32, |
| k… |   |  64, |
| k¶ |   |  512, |
| k⁋ |   |  1024, |
| k¦ |   |  2048, |
| kṄ |   |  4096, |
| kṅ |   |  8192, |
| k¡ |   |  16384, |
| kε |   |  32768, |
| k₴ |   |  65536, |
| k× |   |  2147483648, |
| k⁰ |   |  'bcfghjklmnpqrstvwxyz', |
| k¹ |   |  'bcfghjklmnpqrstvwxz', |
| k□ |   |  string.printable, |
| k• |   |  ['qwertyuiop', 'asdfghjkl', 'zxcvbnm'], |
| kṠ |   |  dt.now().second, |
| kṀ |   |  dt.now().minute, |
| kḢ |   |  dt.now().hour, |
| kτ |   |  int(dt.now().strftime('%j')) |
| ∆c |   |  math.cos(a) |
| ∆C |   |  math.arccos(a) |
| ∆q |   |  roots of quadratic ax^2 + bx = 0 |
| ∆Q |   |  roots of quadratic x^2 + ax + b = 0 |
| ∆s |   |  math.sin(a) |
| ∆S |   |  math.arcsin(a) |
| ∆t |   |  math.tan(a) |
| ∆T |   |  math.arctan(a) |
| ∆P |   |  roots of polynomial with coefficients in a: [2, 5, 1, 3] -> 2x^3 + 5x^2 + x + 3 = 0 |
| ∆ƈ |   |  n pick r (npr) |
| ∆± |   |  math.copysign(a, b) |
| ∆K |   |  sum(proper_divisors(a)) |
| ∆² |   |  is_perfect_square(a) |
| ∆e |   |  e ** a |
| ∆E |   |  (e ** a) - 1 # uses python's math.expm1() |
| ∆L |   |  ln(a) |
| ∆l |   |  log_2(a) |
| ∆τ |   |  log_10(a) |
| ∆d |   |  euclidian_distance(a, b) # Straight line distance |
| ∆D |   |  math.degrees(a) |
| ∆R |   |  math.radians(a) |
| øo |   |  a.remove_until_no_change(b) |
| øV |   |  a.replace_until_no_change(b, c) |
| øc |   |  base_255_string_compressed(a) |
| øC |   |  base_255_number_compressed(a) |
| øl |   |  a.lower() |
| øU |   |  a.upper() |
| øt |   |  a.titlecase() |
| ø$ |   |  a.swapcase() |
| øĊ |   |  centre(a) |
| øe |   |  run_length_encoded(a) |
| ød |   |  run_length_decoded(a) |
| Þ… |   |  b evenly distributed over the elements of a |
| Þ↓ |   |  * minimum of a by function f |
| Þ↑ |   |  * maximum of a by function f |
| Þ× |   |  all_combinations(a) # This is all lengths |
| ÞF |   |  * every fibonacci number |
| Þ! |   |  * every factorial |
