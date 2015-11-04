# dummyjs
JS library for generating dummy text for web developer. Lorem Ipsum....etc

# How To use dummyjs

Import dummyjs inside your html file
    
     <script src="path/to/dummy.js" ></script> 
    
  * Note: Import jquery before importing dummyjs

You can use dummyjs in three way
    
    1. Generating dummy words
    
    2. Generating dummy Sentences
    
    3. Generating dummy paragraphs 
    
    
## 1.Generating Dummy Words
  inside your html code add new attribute data-dummy with values "nw" where n is numeric value and w is type word
  example
    
    <div data-dummy="4w"> </div>
    
    then inside div tag 4 dummy words will be generated.
    
## 2.Generating Dummy Sentences
  inside your html code add new attribute data-dummy with values "ns" where n is numeric value and s is type sentence
  example
    
    <div data-dummy="4s"> </div>
    
    then inside div tag 4 dummy sentences will be generated.
    
    
## 3.Generating Dummy Paragraphs
  inside your html code add new attribute data-dummy with values "np" where n is numeric value and p is type paragraph
  example
    
    <div data-dummy="4p"> </div>
    
    then inside div tag 4 dummy paragraphs will be generated.
    
If you want to generate words, sentences, paragraph of random size then use minimum and maximum values as the value of data-dummy with it's type
example

    <div data-dummy="2-6w"> </div>
    this will generate words between 2 to 6

    <div data-dummy="2-6s"> </div>
    this will generate sentences between 2 to 6

    <div data-dummy="2-6p"> </div>
    this will generate paragraphs between 2 to 6
    
Enjoy...Cheers!!
