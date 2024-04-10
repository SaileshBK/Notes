
Useful commands:

1) To search the file and get the preview of the file on the side with syntax highlighting:
~~~ 
fzf --preview 'bat --color=always {}'
~~~

Note: On preview window we can use  Shift + Up and Shift + Down to navigate 

2) To open the file in preview mode and open with Enter, replace  cursor with code if needed:
~~~
fzf --preview 'bat --color=always {}' --bind 'enter:execute(cursor {})'
~~~
