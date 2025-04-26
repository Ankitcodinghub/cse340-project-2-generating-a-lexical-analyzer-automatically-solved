# cse340-project-2-generating-a-lexical-analyzer-automatically-solved
**TO GET THIS SOLUTION VISIT:** [CSE340 Project 2: Generating a lexical analyzer automatically! Solved](https://www.ankitcodinghub.com/product/cse340-project-2-generating-a-lexical-analyzer-automatically-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;76270&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE340 Project 2: Generating a lexical analyzer automatically! Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
<h1>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Introduction</h1>
I will start with a high-level description of the project in this section. In subsequent sections, I will go into a detailed description of the requirements and how to go about implementing a solution that satisfies them.

The goal of this project is to implement a lexical analyzer automatically for any list of tokens that are specified using regular expressions. The input to your program will have two parts:

<ol>
<li>The first part of the input is a list of tokens separated by commas and terminated with the <sub># </sub>(hash) symbol. Each token in the list consists of a token name and a token description. The token description is a regular expression for the token. The list has the following form:</li>
</ol>
t1_name t1_description , t2_name t2_description , … , tk_name tk_description #

<ol start="2">
<li>The second part of the input is a <em><sub>input string </sub></em>of letters and digits and space characters.</li>
</ol>
Your program will read the list of tokens, represent them internally in appropriate data structures, and then do lexical analysis on the <em><sub>input string </sub></em>to break it down into a sequence of tokens and lexeme pairs from the provided list of tokens. The output of the program will be this sequence of tokens and lexemes. If during the processing of the input string, your program cannot identify a token to match from the list, it outputs ERROR and stops.

If the input to the program has a syntax error, then your program should not do any lexical analysis of the input string and instead it should output a syntax error message and exits.

More details about the input format and the expected output of your program are given in what follows.

The remainder of this document is organized as follows.

<ol>
<li>The second section describes the input format.</li>
<li>The third section describes the expected output.</li>
<li>The fourth section describes the requirements on your solution and the grading criteria.</li>
<li>The fifth and largest section is a detailed explanation how to go about implementing a solution. This section also includes a description of regular expressions.</li>
</ol>
<h1>3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Input Format</h1>
The input of your program is specified by the following context-free grammar:

<table width="648">
<tbody>
<tr>
<td width="165">input</td>
<td width="62">→</td>
<td width="421">tokens sectionINPUT TEXT</td>
</tr>
<tr>
<td width="165">tokens section</td>
<td width="62">→</td>
<td width="421">token listHASH</td>
</tr>
<tr>
<td width="165">token list</td>
<td width="62">→</td>
<td width="421">token</td>
</tr>
<tr>
<td width="165">token list</td>
<td width="62">→</td>
<td width="421">token COMMA token list</td>
</tr>
<tr>
<td width="165">token</td>
<td width="62">→</td>
<td width="421">ID expr</td>
</tr>
<tr>
<td width="165">expr</td>
<td width="62">→</td>
<td width="421">CHAR</td>
</tr>
<tr>
<td width="165">expr</td>
<td width="62">→</td>
<td width="421">LPAREN expr RPAREN DOT LPAREN expr RPAREN</td>
</tr>
<tr>
<td width="165">expr</td>
<td width="62">→</td>
<td width="421">LPAREN expr RPAREN OR LPAREN expr RPAREN</td>
</tr>
<tr>
<td width="165">expr</td>
<td width="62">→</td>
<td width="421">LPAREN expr RPAREN STAR</td>
</tr>
<tr>
<td width="165">expr</td>
<td width="62">→</td>
<td width="421">UNDERSCORE</td>
</tr>
</tbody>
</table>
Where

CHAR&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a | b | … | z | A | B | … | Z | 0 | 1 | … | 9

LETTER&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a | b | … | z | A | B | … | Z

SPACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’ ’ | \n | \t

INPUT_TEXT = ” (CHAR | SPACE)* ”

COMMA&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’,’

LPAREN&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’(’

RPAREN&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’)’

STAR&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’*’

DOT&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’.’

OR&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = ’|’

UNDERSCORE = ’_’

ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = LETTER . CHAR*

Like the first project, you are provided with a lexer to read the input, but you are asked to write the parser. Compared to the first project, writing the parser should be easy.

In the description of regular expressions, UNDERSCORE represents epsilon (more about that later).

<h2>3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Examples</h2>
The following are examples of input.

<ol>
<li>t1 (a)|(b) , t2 (a).((a)*) , t3 (((a)|(b))*).(c) #</li>
</ol>
“a aa bb aab”

This input specifies three tokens <sub>t1</sub>, <sub>t2</sub>, and <sub>t3 </sub>and an INPUT TEXT “a aa bb aab”.

<ol start="2">
<li>t1 (a)|(b) , t2 ((c)*).(b) #</li>
</ol>
“a aa bb aad aa”

This input specifies two tokens <sub>t1</sub>, <sub>t2</sub>, and an INPUT TEXT “a aa bb aad aa”. 3. t1 (a)|(b) , t2 (c).((a)*) , t3 (((a)|(b))*).(((c)|(d))*)#

“aaabbcaaaa”

This input specifies three tokens <sub>t1</sub>, <sub>t2 </sub>and textttt3 and an INPUT TEXT “aaabbcaaaa”.

<ol start="4">
<li>tok (a).((b)|(_)) , toktok (a)|(_), tiktok ((a).(a)).(a) # “aaabbcaaaa”</li>
</ol>
This input specifies three tokens whose names are <sub>tok</sub>, <sub>toktok</sub>, and <sub>tiktok </sub>and an INPUT TEXT “aaabbcaaaa”. Recall that in the description of regular expressions, underscore represents epsilon, so the regular expressions for the token <sub>tok </sub>is equivalent to and the regular expressions for the token <sub>toktok </sub>is equivalent to

<strong>Note 1 </strong>The code we provided breaks down the input to the program into tokens like ID, LPAREN, RPAREN and so on. Like the first project, to read the input, the code we provide has an object called <sub>lexer </sub>and a function <sub>GetToken() </sub>used in reading the input according to the fixed list of tokens for the input to the program. Your program will then have to break down the INPUT TEXT string into a sequence of tokens according to the list of token in the input to the program. In order not to confuse the function that breaks down the INPUT TEXT from the function <sub>GetToken() </sub>in the code we provided, you should call your function something else like <sub>my </sub><sub>GetToken()</sub>

<h1>4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Output Format</h1>
The output will be either SYNTAX ERROR if the input has a syntax error or a message indicating that one or more of the tokens have expressions that are not valid (see below) or a sequence of tokens and their corresponding lexemes according to the list of tokens provided if there are no errors. More specifically, the following are the output requirements.

<ol>
<li>if the input to your program is not in the correct format (not according to the grammar in Section 2), your parser should output SYNTAX ERROR and nothing else, so you should make sure not to print anything before the complete parsing of the input is completed.</li>
<li>if the input to your program is syntactically correct, then there are two cases to consider:
<ul>
<li>If any of the regular expressions of the tokens in the list of tokens in the input to your program can generate the empty string, then your program should output</li>
</ul>
</li>
</ol>
EPSILON IS NOOOOOT A TOKEN !!! tok_1 tok_2 … tok_k

where <sub>tok 1</sub>, <sub>tok 2</sub>, <sub>…</sub>, <sub>tok k </sub>is the list of tokens whose regular expressions can generate the empty string.

<ul>
<li>If there is no syntax error and none of the expressions of the tokens can generate the empty string, your program should do lexical analysis on <sub>INPUT TEXT </sub>and produce a sequence of tokens and lexemes in <sub>INPUT TEXT </sub>according to the list of tokens specified</li>
</ul>
in the input to your program. Each token and lexeme should be printed on a separate line. The output on a given line will be of the form

t , “lexeme”

where t is the name of a token and lexeme is the actual lexeme for the token t. If during lexical analysis of <sub>INPUT TEXT</sub>, a syntax error is encountered then ERROR is printed on a separate line and the program exits.

In doing lexical analysis for <sub>INPUT TEXT</sub>, <sub>SPACE </sub>is treated as a separator and is otherwise ignored.

<strong>Note 2 </strong>The <sub>my </sub><sub>GetToken() </sub>that you will write is a general function that takes a list of token representations and does lexical analysis according to those representations. In later sections, I explain how that can be done, so do not worry about it yet, but keep in mind that you will be writing a general <sub>my GetToken() </sub>function.

<strong>Examples&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>Each of the following examples gives an input and the corresponding expected output.

<ol>
<li>t1 (a)|(b) , t2 ((a)*).(a) , t3 (((a)|(b))*).(((c)*).(c)) #</li>
</ol>
“a aac bbc aabc”

This input specifies three tokens <sub>t1</sub>, <sub>t2</sub>, and <sub>t3 </sub>and an INPUT TEXT “a aac bbc aabc”. Since the input is in the correct format and none of the regular expressions generates epsilon, the output of your program should be the list tokens in the INPUT TEXT:

t1 , “a” t3 , “aac” t3 , “bbc” t3 , “aabc”

<ol start="2">
<li>t1 (a)|(b) , t2 ((a)*).(a) , t3 (((a)|(b))*).(c) #</li>
</ol>
“a aa bbc aad aa”

This input specifies three tokens <sub>t1</sub>, <sub>t2</sub>, and <sub>t3 </sub>and an INPUT TEXT “a aa bbc aad aa”. Since the input is in the correct format and none of the regular expressions generates epsilon, the output of your program should be the list tokens in the INPUT TEXT the output of the program should be

t1 , “a” t2 , “aa” t3 , “bbc” t2 , “aa”

ERROR

Note that doing lexical analysis for INPUT TEXT according to the list of tokens produces ERROR after the second <sub>t2 </sub>token because there is no token that starts with <sub>’d’</sub>.

<ol start="3">
<li>t1a (a)|(b) , t2bc (a).((a)*) , t34 (((a)|(b))*).((c)|(d))# “aaabbcaaaa”</li>
</ol>
This input specifies three tokens whose names are <sub>t1a</sub>, <sub>t2bc</sub>, and <sub>t34 </sub>and an input text “aaabbcaaaa”. Since the input is in the correct format, the output of your program should be the list tokens in the INPUT TEXT:

t34 , “aaabbc” t2bc , “aaaa”

<ol start="4">
<li>t1 (a)|(b) , t2 ((a)*).(a) , t3 (a)*, t4 b , t5 ((a)|(b))* #</li>
</ol>
“a aac bbc aabc”

This input specifies five tokens and an INPUT TEXT “a aac bbc aabc”. Since some of the regular expressions can generate epsilon, the output:

EPSILON IS NOOOOOT A TOKEN !!! t3 t5

<h1>5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Requirements and Grading</h1>
You should write a program to produce the correct output for a given input as described above. You will be provided with a number of test cases. Since this is the second project, the number of test cases provided with the project will be small relative to the number of test cases provided for project 1. <strong>In your solution, you are not allowed to use any built-in or library support for regular expressions in C/C++. This requirement will be enforced by checking your code.</strong>

The grade is broken down as follows

<ol>
<li>Submission compiles and every function has comments and every file has your name: <strong><sub>10 </sub>points</strong></li>
<li>Submission does not compile or some functions have no comments or some submitted file does not have your name: <strong>no credit for the submission</strong>.</li>
<li>Syntax checking: <strong><sub>10 points </sub></strong>(no partial credit for this)</li>
<li>EPSILON IS NOOOOOT A TOKEN !!! error: <strong><sub>15 points </sub></strong>(grade is strictly proportional to the number of test cases that your program successfully passes)</li>
<li>Lexical analysis of <sub>INPUT </sub><sub>TEXT</sub>: <strong><sub>65 points </sub></strong>(grade is strictly proportional to the number of test cases that your program successfully passes)</li>
</ol>
The compiler and environment used is the same as for project 1, so refer to project 1 document for the information.

<strong>Note 3 </strong>If your code does not compile on the submission website, you will not receive any points, not even for documentation.

<h1>6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; How to Implement a Solution</h1>
The main difficulty in coming up with a solution is to transform a given list of token names and their regular expression descriptions into a <sub>my </sub><sub>GetToken() </sub>function for the given list of tokens. This transformation will be done in three high-level steps:

<ol>
<li>Transform regular expressions into REGs. The goal here is to parse a regular expression description and generate a graph that represents the regular expression<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. The generated graph will have a specific format and I will describe below how to generate it. I will call it a <em>regular expression graph</em>, or REG for short.</li>
<li>Write a function <sub>match(r,s,p)</sub>, where <sub>r </sub>is a REG , <sub>s </sub>is a string and <sub>p </sub>is a position in the string <sub>s</sub>. The function match will return the longest possible lexeme starting from position <sub>p </sub>in the string <sub>s </sub>that matches the regular expression of the graph <sub>r</sub>.</li>
<li>Write a class my LexicalAnalyzer(list,s) where list is a list of structures of the form {token name<em>,reg </em><em>pointer</em><sub>} </sub>and s is an input string. my LexicalAnalyzer stores the list of structures and keeps track of the part of the input string that has been processed. The class myLexicalAnalyzer has a method my GetToken(). For every call of my GetToken(), match(r,s,p) is called for every REG <em><sub>r </sub></em>in the list starting from the current position <sub>p </sub>maintained in my LexicalAnalyzer. my GetToken() returns the token with the longest matching prefix together with its lexeme and updates the current position. If the longest matching prefix matches more than one token, the matched token that is listed first in the list of tokens is returned.</li>
</ol>
In what follows I describe how a regular expression description can be transformed into a REG and how to implement the function <sub>match(r,s,p)</sub>. But first, I will give an overview of regular expressions and the sets of strings they represent.

<h2>6.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Set of Strings Represented by Regular Expressions</h2>
A regular expression is a compact representation of a set, possibly infinite, of strings. For a given regular expression, we say that expression can <em><sub>generate </sub></em>a string if the string is in set that is represented by the regular expression. We start with a general description, then we give examples.

<h3>6.1.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; General description</h3>
We start with the simple expressions (the base cases)

<ul>
<li>(<strong><sub>One-character strings</sub></strong>) The regular expression <sub>a </sub>represents the set of strings {<em>a</em><sub>}</sub>, that is the set consisting of only the string <sub>“a”</sub>.</li>
<li>(<strong><sub>Epsilon</sub></strong>) The regular expression represents the set of strings {<sub>}</sub>, that is the set consisting of only the string <em><sub>&nbsp;</sub></em>(which is the empty string).</li>
</ul>
For the inductive step (recursion of your parser), there are four cases:

<ul>
<li>(<strong><sub>Parentheses</sub></strong>) If <sub>R </sub>is a regular expression, the regular expression <sub>(R) </sub>represents the same set of strings that <sub>R </sub> The parentheses are used for grouping and to facilitate parsing and do not have a meaning otherwise.</li>
<li>(<strong><sub>Concatenation</sub></strong>) If <sub>R1 </sub>and <sub>R2 </sub>are regular expressions that represents sets of strings <sub>S1 </sub>and <sub>S2 </sub>respectively, then <sub>(R1).(R2) </sub>represents a new set of strings that can be obtained by concatenating one string from <sub>S1 </sub>with one string from <sub>S2 </sub>(order matters).</li>
<li>(<strong><sub>Union</sub></strong>) If <sub>R1 </sub>and <sub>R2 </sub>are regular expressions that represents sets of strings <sub>S1 </sub>and <sub>S2 </sub>respectively, then <sub>(R1)|(R2) </sub>represents the union of the two sets of strings <sub>S1 </sub>and <sub>S2</sub>. • (<strong><sub>Kleene star</sub></strong>) The last case is the most interesting because it allows us unlimited number of repetition. If <sub>R </sub>is a regular expression that represents the set of strings <sub>S</sub>, then <sub>(R)* </sub>represents the set of strings that can be obtained by concatenating any number of strings from <sub>S</sub>, including zero strings (which gives us epsilon).</li>
</ul>
<h3>6.1.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Examples</h3>
<ol>
<li>The set of strings represented by <sub>a </sub>is</li>
</ol>
{<em>a</em>}

<ol start="2">
<li>The set of strings represented by <sub>b </sub>is</li>
</ol>
{<em>b</em>}

<ol start="3">
<li>The set of strings represented by <sub>(a)|(b) </sub>is</li>
</ol>
{<em>a, b</em>}

<ol start="4">
<li>The set of strings represented by <sub>((a)|(b)).(c) </sub>is</li>
</ol>
{<em>ac, bc</em>}

<ol start="5">
<li>The set of strings represented by ((a)|(b)).((c)|(d)) is</li>
</ol>
{<em>ac, ad, bc, bd</em>}

<ol start="6">
<li>The set of strings represented by ((c)|(d)).((a)|(b)) is</li>
</ol>
{<em>ca, cb, da, db</em>}

<ol start="7">
<li>The set of strings represented by <sub>(a)* </sub>is</li>
</ol>
{<em>, a, aa, aaa, aaaa, …</em>}

<ol start="8">
<li>The set of strings represented by <sub>(b)* </sub>is</li>
</ol>
{<em>, b, bb, bbb, bbbb, …</em>}

Figure 1: Regular expressions graphs for the base cases

Figure 2: Regular expression graph for the an expression obtained using the dot operator

<ol start="9">
<li>The set of strings represented by <sub>(a)|((b)*) </sub>is</li>
</ol>
{<em>a, , b, bb, bbb, bbbb, …</em>}

<ol start="10">
<li>The set of strings represented by <sub>((a)*)|((b)*) </sub>is</li>
</ol>
{<em>,a,b,aa,bb,aaa,bbb,aaaa,bbbb,…</em>}

<ol start="11">
<li>The set of strings represented by <sub>((a)|(b))* </sub>is</li>
</ol>
{<em>, a, b, aa, ab, ba, bb, aaa, aab, aba, abb, baa, bab, bba, bbb, …</em>}

<h2>6.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Constructing REGs</h2>
The construction of REGs is done recursively. The construction we use is called Thompson’s construction. Each REG has a one <sub>start </sub>node and one <sub>accept </sub>node. For the base cases of epsilon and <sub>a</sub>, where <sub>a </sub>is a character of the alphabet, the REGs are shown in Figure 1. For the recursive cases, the constructions are shown in Figures 2, 3, and 4. An example REG for the regular expression <sub>((a)*).((b)*) </sub>is shown in Figure 5.

Figure 3: Regular expression graph for the an expression obtained using the or operator

Figure 4: Regular expression graph for the an expression obtained using the star operator

<h3>6.2.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Data Structures and Code for REGs</h3>
In the construction of REGs, every node has at most two outgoing arrows. This will allow us to use a simple representation of a REG node.

Figure 5: Regular expression graph for the an expression obtained using concatenation and star operators

struct REG_node { struct REG_node * first_neighbor; char first_label; struct REG_node * second_neighbor; char second_label;

}

In the representation, first neighbor is the first node pointed to by a node and second neighbor is the second node pointed to by a node. <sub>first label </sub>and <sub>second label </sub>are the labels of the arrows from the node to its neighbors. If a node has only one neighbor, then <sub>second neighbor </sub>will be NULL. If a node has no neighbors, then both first neighbor and second neighbor will be NULL.

Figure 6: Data structure representation for the REG of <sub>((a)*).((b*))</sub>

struct REG { struct REG_node * start; struct REG_node * accept;

}

In the your parser, you should write a function <sub>parse expr() </sub>that parses the regular expressions returns the REG of the regular expression that is parsed. The construction of REGs is done recursively. An outline of the process is shown on the next page.

struct REG * parse_expr() {

// if expression is UNDERSCORE or a CHAR, say ’a’ for example

// create a REG for the expression and return a pointer to it

// (see Figure 1, for how the REG looks like)

// if expression is (R1).(R2)

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; the program will call parse_expr() twice, once

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; to parse R1 and once to parse R2

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Each of the two calls will return a REG, say they are

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; r1 and r2

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; construct a new REG r for (R1).(R2) using the

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; two REGs r1 and r2

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (see Figure 2 for how the two REGs are combined)

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; return r

//

// the cases for (R1)|(R2) and (R)* are similar and

// are omitted from the description

}

<h3>6.2.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Detailed Examples for REG Construction</h3>
I consider the regular expression <sub>((a)*).((b)*) </sub>and explain step by step how its REG is constructed (Figure 5).

When parsing <sub>((a)*).((b)*)</sub>, the first expression to be fully parsed and its REG is constructed is <sub>a </sub>(Figure 1). In Figure 5, the nodes for the REG of the regular expression <sub>a </sub>have numbers 1 and 2 to indicate that they are the first two nodes to be created.

The second expression to be fully parsed and its REG constructed when parsing <sub>((a)*).((b)*) </sub>is <sub>(a)*</sub>. The REG for <sub>(a)* </sub>is obtained from the REG for the regular expression <sub>a </sub>by adding two more nodes (3 and 4) and adding the appropriate arrows as described in the general case in Figure 4.

The starting node for the REG of <sub>(a)* </sub>is the newly created node 3 and the accepting node is the newly created node 4.

The third regular expression to be fully parsed while parsing <sub>((a)*).((b)*) </sub>is the regular expression <sub>b</sub>. The REG for regular expression <sub>b </sub>is constructed as shown in Figure 1. The nodes for this REG are numbered 5 and 6.

The fourth regular expression to be fully parsed while parsing <sub>((a)*).((b)*) </sub>is <sub>(b)*</sub>. The REG for <sub>(b)* </sub>is obtained from the REG for the regular expression <sub>b </sub>by adding two more nodes (7 and 8) and adding the appropriate arrows as described in the general case in Figure 4. The starting node for the REG of <sub>(b)* </sub>is the newly created node 7 and the accepting node is the newly created node 8.

Finally, the last regular expression to be fully parsed is the regular expression <sub>((a)*).((b)*)</sub>.

The REG of <sub>((a)*).((b)*) </sub>is obtained from the REGs of <sub>(a)* </sub>and <sub>(b)* </sub>by creating a new REG whose initial node is node 3 and whose accepting node is node 8 and adding an arrow from node 4 (the accepting node of the REG of <sub>(a)*</sub>) to node 7 (the initial node for the REG of <sub>(b)*</sub>).

Another example for the REG of <sub>(((a)*).((b).(b)))|((a)*) </sub>is shown in Figures 8 and 9. In the next section, I will use REG of (((a)*).((b).(b)))|((a)*) to illustrate how match(r,s,p) can be implemented.

<h2>6.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Implementing match(r,s,p)</h2>
Given an REG <sub>r</sub>, a string <sub>s </sub>and a position <sub>p </sub>in the string <sub>s</sub>, we would like to determine the longest possible lexeme that matches the regular expression for <sub>r</sub>.

As you will see in CSE355, a string <sub>w </sub>is in L(<sub>R</sub>) for a regular expression <sub>R </sub>with REG <sub>r </sub>if and only if there is a path from the starting node of <sub>r </sub>to the accepting node of <sub>r </sub>such that <sub>w </sub>is equal to the concatenation of all labels of the edges along the path. I will not go into the details of the equivalence in this document. I will describe how to find the longest possible substring <sub>w </sub>of <sub>s </sub>starting at position <sub>p </sub>such that there is a path from the starting node of <sub>r </sub>to the accepting node of <sub>r </sub>that can be labeled with <sub>w</sub>.

To implement <sub>match(r,s,p)</sub>, we need to be able to determine for a given input character <sub>a </sub>and a set of nodes <sub>S </sub>the set of nodes that can be reached from nodes in <sub>S </sub>by <em><sub>consuming </sub></em><sub>a</sub>. To consume <sub>a </sub>we can traverse any number of edges labeled ’ ’, traverse one edge labeled <sub>a</sub>, then traverse any number of edges labeled ’ ’. To match one character, you will implement a function called <sub>Match </sub><sub>One Char() </sub>shown in Figure 7. For a given character <sub>c </sub>and a given set of nodes

Match_One_Char(set_of_nodes S, char c) returns set_of_nodes

{

// 1. find all nodes that can be reached from S by consuming c

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S’ = empty set

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; for every node n in S

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if ( (there is an edge from n to m labeled with c) &amp;&amp;

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ( m is not in S’) ) {

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; add m to S’

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (S’ is empty)

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; return empty set

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; At this point, S’ is not empty and it contains the nodes that

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; can be reached from S by consuming the character c directly

//

// 2. find all nodes that can be reached from the resulting

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; set S’ by consuming no input

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; changed = true

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S’’ = empty set

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; while (changed) {

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; changed = false

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; for every node n in S’ {

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; add n to S’’

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; for ever neighbor m of n {

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if ( (the edge from n to m labeled with ’_’) &amp;&amp;

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ( m is not in S’’) )

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; add m to S’’

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (S’ not equal to S’’) {

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; changed = true;

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S’ = S’’

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S’’ = empty set

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at this point the set S’ contains all nodes that can be reached

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; from S by first consuming C, then traversing 0 or more epsilon

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; edges

//

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; return S’

}

Figure 7: Pseudocode for matching one character

.

Figure 8: Regular expression graph ((a)*).((b).(b))

S, <sub>Match </sub><sub>One Char() </sub>will find all the nodes that can be reached from <sub>S </sub>by consuming the single character <sub>c</sub>.

In order to match a whole string, we need to match the characters of the strings one after another. At each step, the solution will keep track of the set of nodes <sub>S </sub>that can be reached by consuming the prefix of the input string that has been processed so far.

To implement <sub>match(r,s,p)</sub>, we start with the set of nodes that can be reached from the starting node of <sub>r </sub>by consuming no input. Then we repeatedly call <sub>Match One </sub><sub>Char() </sub>for successive characters of the string <sub>s </sub>starting from position <sub>p </sub>until the returned set of nodes <sub>S </sub>is empty or we run out of input. If at any point during the repeated calls to <sub>Match </sub><sub>One Char() </sub>the set <sub>S </sub>of nodes contains the accepting node, we note the fact that the prefix of string <sub>s </sub>starting from position <sub>p </sub>up to the current position is matching. At the end of the calls to <sub>Match One </sub><sub>Char() </sub>when <sub>S </sub>is empty or the end of input is reached, the last matched prefix is the one returned by <sub>match(r,s,p)</sub>. If none of the prefixes are matched, then there is no match for <sub>r </sub>in <sub>s </sub>starting at <sub>p</sub>.

<strong>Note 4</strong>

<ul>
<li>The algorithms given above are not the most efficient, but they are probably the simplest to implement the matching functions.</li>
<li>The algorithm uses sets, so you need to have a representation for a set of nodes and to do operations on sets of nodes.</li>
</ul>
<h2>6.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Detailed Example for Implementing match(r,s,p)</h2>
In this section, I illustrate the steps of an execution of <sub>match(r,s,p) </sub>on the REG of

(((a)*).((b).(b)))|((a)*) shown in Figure 9. The input string we will consider is the string <sub>s = “</sub><sub>a</sub><sub>a</sub><sub>ba” </sub>and the initial position is <sub>p = 0</sub>.

Figure 9: Regular expression graph <sub>(((a)*).((b).(b)))|((a)*)</sub>

<ol>
<li>Initially, the set of states that can reached by consuming no input starting from node 17 is</li>
</ol>
<em>S</em><sub>0 </sub>= <sub>{</sub>17<em>,</em>3<em>,</em>1<em>,</em>4<em>,</em>9<em>,</em>15<em>,</em>13<em>,</em>16<em>,</em><strong>18</strong><sub>}</sub>

Note that <em><sub>S</sub></em><sub>0 </sub>contains node <strong><sub>18 </sub></strong>which means that the empty string is a matching prefix. This means that this expression should result in a “<sub>EPSILON IS NOOOOOT A TOKEN !!!</sub>” error if it is used in a token specification.

<ol start="2">
<li>Consuming <sub>a</sub>.</li>
</ol>
The set of states that can be reached by consuming <sub>a </sub>starting from <em><sub>S</sub></em><sub>0 </sub>is

<em>S</em><sub>1 </sub>= <sub>{</sub>2<em>,</em>14}

The set of states that can be reached by consuming no input starting from <em><sub>S</sub></em><sub>1 </sub>is

<em>S</em><sub>1 </sub>&nbsp;= <sub>{</sub>2<em>,</em>1<em>,</em>4<em>,</em>9<em>,</em>14<em>,</em>13<em>,</em>16<em>,</em><strong>18</strong><sub>}</sub>

Note that <em><sub>S</sub></em><sub>1 </sub>&nbsp;contains node <strong><sub>18</sub></strong>, which means that the prefix <sub>“</sub><sub>a</sub><sub>” </sub>is a matching prefix.

<ol start="3">
<li>Consuming <sub>a</sub></li>
</ol>
The set of states that can be reached by consuming <sub>a </sub>starting from <em><sub>S</sub></em><sub>1 </sub>&nbsp;is

<em>S</em><sub>2 </sub>= <sub>{</sub>2<em>,</em>14}

The set of states that can be reached by consuming no input starting from <em><sub>S</sub></em><sub>2 </sub>is

<em>S</em><sub>2 </sub>&nbsp;= <sub>{</sub>2<em>,</em>1<em>,</em>4<em>,</em>9<em>,</em>14<em>,</em>13<em>,</em>16<em>,</em><strong>18</strong><sub>}</sub>

Note that <em><sub>S</sub></em><sub>2 </sub>&nbsp;contains node <strong><sub>18</sub></strong>, which means that the prefix <sub>“</sub><sub>a</sub><sub>a</sub><sub>” </sub>is a matching prefix.

<ol start="4">
<li>Consuming <sub>b</sub></li>
</ol>
The set of states that can be reached by consuming <sub>b </sub>starting from <em><sub>S</sub></em><sub>2 </sub>&nbsp;is

<em>S</em><sub>3 </sub>= <sub>{</sub>10}

The set of states that can be reached by consuming no input starting from <em><sub>S</sub></em><sub>3 </sub>is

<em>S</em><sub>3 </sub>&nbsp;= <sub>{</sub>10<em>,</em>11}

Note that <em><sub>S</sub></em><sub>3 </sub>does not contain node <strong><sub>18 </sub></strong>which means that <sub>“</sub><sub>a</sub><sub>a</sub><sub>b” </sub>is not a matching prefix, but is still a viable prefix, which means that there is hope we can read more characters that will turn it into a matching prefix.

<ol start="5">
<li>Consuming <sub>a</sub></li>
</ol>
The set of states that can be reached by consuming <sub>a </sub>starting from <em><sub>S</sub></em><sub>3 </sub>&nbsp;is

<em>S</em>4 = {}

Since <em><sub>S</sub></em><sub>4 </sub>is empty, <sub>“</sub><sub>a</sub><sub>a</sub><sub>ba” </sub>is not viable and we stop.

The longest matching prefix is <sub>a</sub><sub>a</sub>. This is the lexeme that is returned. Note that the second call to <sub>match(r,s,p) </sub>starting after <sub>“</sub><sub>a</sub><sub>a</sub><sub>” </sub>will return ERROR.

<a href="#_ftnref1" name="_ftn1">[1]</a> The graph is a representation of a non-deterministic finite state automaton
