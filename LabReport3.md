# Lab Report 3: 

## Command Examples: ##

Chosen Command: grep

First Command Line Option:

**grep -B (num)**

Command:

          grep -B 5 papyrus HistoryEgypt.txt
          
Output:
    
          T he fertile Nile Valley has supported human life for over
          8,000 years. Stone Age settlers developed from hunters to farmers,
          growing barley and wheat crops that originated in Mesopotamia.
          Mesopotamian script was also copied, but it developed into the first
          Egyptian written language. From the earliest days Egyptians recorded
          their activities on papyrus paper, helping us to piece together the
          
This command prints 6 lines, including the line containing the word "papyrus", and the 5 lines before it. The number of lines printed before the target line depends on the argument passed to grep -B.
          

Command:

          grep -B 1 Mediterranean HistoryFrance.txt
          
Output:
    
        Franche-Comté, Alsace, and Bur­gundy. At the same time, migrants from
        the Mediterranean countries were trickling into the south.
        
This command prints 2 lines, including the line containing the word "Mediterranean", and the 1 line before it. The number of lines printed before the target line depends on the argument passed to grep -B.
          
          
          
          
