# Lab Report 3: 

## Command Examples: ##

**Chosen Command**: `grep`

### ::First Command Line Option:: ###

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

I found this command using `man grep` in the terminal

Second Command Line Option:

**grep -c**

Command:

          grep -c is ch1.txt 
          
Output:
    
          135
          
This command counts the number of times the pattern, "is", occurs in the file ch1.txt of the *Berk* directory.
          

Command:

          grep -c Morowitz ./Kauffman/ch7.txt
          
Output:
    
          4
        
This command counts the number of times the pattern, "Morowitz", occurs in the file ch7.txt of the *Kauffman* directory.

I found this command using `man grep` in the terminal

Third Command Line Option:

**grep -o**

Command:

          grep -o Compaq ./Abernathy/ch14.txt
          
Output:
    
          Compaq
          Compaq
          Compaq
          Compaq
          Compaq
          Compaq
          Compaq
          Compaq
          
This command only prints the part of a line that matches the pattern passed to the grep command. In other words, it returns the pattern only. Hence, it can also be used to count the number of occurences like the -c command. The pattern "Compaq" appears 8 times in this file.
          

Command:

         grep -o issues ./Abernathy/ch14.txt
          
Output:
    
        issues
        issues
        
This command prints 2 lines, which means the pattern "issues" appears 2 times in this file as well.

I found this command using `man grep` in the terminal

Fourth Command Line Option:

**grep -r**

Command:

          grep -r Hello
          
Output:
    
          ./non-fiction/OUP/Berk/CH4.txt:Children’s earliest efforts at make-believe also reveal how challenging they ﬁnd the task of detaching thought from reality. Initially, object substitutions are closely tied to the real things they represent. Toddlers between ages 1 1/2 and 2 generally use only realistic-looking objects while pretending—a toy telephone to talk into or a cup to drink from.9 Once, I handed a 21-month-old a small wooden block, put another to my ear, and called her on the phone: “Ring! Ring! Hello, Lynnay!” She responded by throwing down the block and turning to another activity. Yet when given a plastic replica of a push-button phone, Lynnay readily put the receiver to her ear and pretended to converse.
          ./non-fiction/OUP/Berk/CH4.txt:As children engage in play talk, they not only build their vocabularies but correct one another’s errors, either directly or by demonstrating the acceptable way to speak. In one instance, a kindergartner enacting a telephone conversation said, “Hello, come to my house, please.” Her play partner quickly countered with appropriate telephone greeting behavior: “No, ﬁrst you’ve got to say ‘How are you? What are you doing?’”28
          ./travel_guides/berlitz1/WhereToFrance.txt:        Saint-Wandrille, Le Bec-Hellouin, and Caen, culminating in their
          
This command recursively traverses through all files in the written_2 directory to print lines that have a matching pattern. In this case, the pattern "Hello" is found in 3 files. 
          

Command:

          grep -r Morowitz
          
Output:
    
          ./non-fiction/OUP/Kauffman/ch7.txt:I close this chapter with a surprising calculation and conjecture by Harold Morowitz, a biophysicist at George Mason University. Morowitz considers the atoms that form organic molecules, C, H, N, O, P, S: carbon, hydrogen, nitrogen, oxygen, phosphorus, and sulphur. He then considers molecules of these elements and the kinds of bonds that can form between the elements. There are two kinds of bonds, chain-terminating bonds, like a terminal hydroxyl group, -OH, and chain-extending bonds, like C=C. Chain-extending bonds will tend to make a molecular system with many kinds of molecules even more diverse. Chain-terminating bonds will tend to limit the diversity of molecular species that can form.
          ./non-fiction/OUP/Kauffman/ch7.txt:Morowitz then considers the equilibrium ratio of chain-extending bonds to all bonds, chain-extending plus chain-terminating, that would occur as a function of temperature, or equivalently, the energy per unit volume of the system. At very high temperatures, the system is a plasma, and chain-terminating bonds are vastly more predominant at equilibrium than chain-extending bonds. At very low temperatures, chain-terminating bonds predominate overwhelmingly.
          ./non-fiction/OUP/Kauffman/ch7.txt:If one plots the equilibrium ratio of chain-extending bonds to all bonds as a function of temperature, or energy per unit volume, the curve goes up, reaches a single peak, then trends downward. Thus, there is an optimal temperature, or energy per unit volume, where the equilibrium ratio of bonds maximizes the ratio of chain-extending chemical bonds to all bonds. Morowitz’s remarkable conclusion is that the maximum of this curve, where chain-extending bonds are as abundant as possible at equilibrium, corresponds quite closely to the average energy per unit volume of the biosphere of the Earth!
          ./non-fiction/OUP/Kauffman/ch7.txt:Morowitz’s calculation should be taken cautiously. My conclusions based on his almost back-of-the-envelope calculation should be taken even more cautiously. The arguments are cogent but unestablished. On the other hand, the biosphere has exploded in molecular diversity, the workspace of the biosphere has expanded, the adjacent possible of the biosphere has expanded. It is certainly interesting if the energy per unit volume of the biosphere is roughly that which makes this expansion as energetically inexpensive as possible for the autonomous agents coevolving with one another, exapting to new forms of making a living playing natural games, as we coconstruct our biosphere.
        
This command once again recursively traverses through all files in the written_2 directory and prints out a few lines of the files that have the matching pattern. In this case, 4 files contain the pattern "Morowitz"

I found this command using `man grep` in the terminal
          
          
          
          

          
          
          
          

          
          
          
          

          
          
          
          
