---
attachments: [Clipboard_2022-03-12-15-05-54.png, Clipboard_2022-03-12-15-06-19.png]
tags: [Notebooks/Programming Basics/Object Oriented Programming]
title: Object Oriented Programming
created: '2022-03-12T08:38:56.369Z'
modified: '2022-03-12T10:00:00.848Z'
---

# Object Oriented Programming

- Dunder functions 
  - _ init _  : will run that dunder function when creating an object
  - _ run _  :  will run the dunder function when we do classname.run()
  - _ repr _ : It is a method od representing data in specific format
  ![](@attachment/Clipboard_2022-03-12-15-06-19.png)
  - To create a method without using self we can use the keyword @classmethod
    - Eg :
    
          class test:

            def __init__(self):
              print('hello')
            
            @classmethod
            def new_function(cls) #cls is a variable like self. 
              print('Hello world')
          
          obj=test()
          obj.new_function() # This will work even without using self as parameter

- Inheritance
  - Using super functions
  
