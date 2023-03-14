# Lab Report 5: 

## Command Examples: ##

**Chosen Command**: `find `

### First Command Line Option: ###

---

**find -name**

Command:

          find . -name chP.txt
          
Output:
    
         ./non-fiction/OUP/Castro/chP.txt
          
This command recursively searches the current directory and its children for a file with the name "chP.txt" and outputs its relative path

Command:

          find . -name non-fiction 
          
Output:
    
        ./non-fiction
        
This command outputs the path of the "non-fiction" directory.

I found this command on the internet

---

### Second Command Line Option: ###

---

**grep -c**

Command:

           find . -size -1000c 
          
Output:
    
              .
        ./non-fiction
        ./non-fiction/OUP
        ./non-fiction/OUP/Berk
        ./non-fiction/OUP/Abernathy
        ./non-fiction/OUP/Rybczynski
        ./non-fiction/OUP/Kauffman
        ./non-fiction/OUP/Fletcher
        ./non-fiction/OUP/Castro
        ./travel_guides
        ./travel_guides/berlitz1/HandRIstanbul.txt
        ./travel_guides/berlitz1/HandRIbiza.txt
        
          
This command outputs the paths of all the files and directories that take up less than 1000 bytes of space
          

Command:

          find . -size -500c 
          
Output:
    
          .
          ./non-fiction
          ./non-fiction/OUP
          ./non-fiction/OUP/Berk
          ./non-fiction/OUP/Abernathy
          ./non-fiction/OUP/Rybczynski
          ./non-fiction/OUP/Kauffman
          ./non-fiction/OUP/Fletcher
          ./travel_guides

This command outputs the paths of all the files and directories that take up less than 500 bytes of space
          


I found this command on the internet
 
 ---

### Third Command Line Option: ###

---

**find -s**

Command:

          find -s non-fiction   
          
Output:
    
        non-fiction
        non-fiction/OUP
        non-fiction/OUP/Abernathy
        non-fiction/OUP/Abernathy/ch1.txt
        non-fiction/OUP/Abernathy/ch14.txt
        non-fiction/OUP/Abernathy/ch15.txt
        non-fiction/OUP/Abernathy/ch2.txt
        non-fiction/OUP/Abernathy/ch3.txt
        non-fiction/OUP/Abernathy/ch6.txt
        non-fiction/OUP/Abernathy/ch7.txt
        non-fiction/OUP/Abernathy/ch8.txt
        non-fiction/OUP/Abernathy/ch9.txt
        non-fiction/OUP/Berk
        non-fiction/OUP/Berk/CH4.txt
        non-fiction/OUP/Berk/ch1.txt
        non-fiction/OUP/Berk/ch2.txt
        non-fiction/OUP/Berk/ch7.txt
        non-fiction/OUP/Castro
        non-fiction/OUP/Castro/chA.txt
        non-fiction/OUP/Castro/chB.txt
        non-fiction/OUP/Castro/chC.txt
        non-fiction/OUP/Castro/chL.txt
        non-fiction/OUP/Castro/chM.txt
        non-fiction/OUP/Castro/chN.txt
        non-fiction/OUP/Castro/chO.txt
        non-fiction/OUP/Castro/chP.txt
        non-fiction/OUP/Castro/chQ.txt
        non-fiction/OUP/Castro/chR.txt
        non-fiction/OUP/Castro/chV.txt
        non-fiction/OUP/Castro/chW.txt
        non-fiction/OUP/Castro/chY.txt
        non-fiction/OUP/Castro/chZ.txt
        non-fiction/OUP/Fletcher
        non-fiction/OUP/Fletcher/ch1.txt
        non-fiction/OUP/Fletcher/ch10.txt
        non-fiction/OUP/Fletcher/ch2.txt
        non-fiction/OUP/Fletcher/ch5.txt
        non-fiction/OUP/Fletcher/ch6.txt
        non-fiction/OUP/Fletcher/ch9.txt
        non-fiction/OUP/Kauffman
        non-fiction/OUP/Kauffman/ch1.txt
        non-fiction/OUP/Kauffman/ch10.txt
        non-fiction/OUP/Kauffman/ch3.txt
        non-fiction/OUP/Kauffman/ch4.txt
        non-fiction/OUP/Kauffman/ch5.txt
        non-fiction/OUP/Kauffman/ch6.txt
        non-fiction/OUP/Kauffman/ch7.txt
        non-fiction/OUP/Kauffman/ch8.txt
        non-fiction/OUP/Kauffman/ch9.txt
        non-fiction/OUP/Rybczynski
        non-fiction/OUP/Rybczynski/ch1.txt
        non-fiction/OUP/Rybczynski/ch2.txt
        non-fiction/OUP/Rybczynski/ch3.txt
          
This command traverses the directories reversely.

Command:
  
      find -s non-fiction/OUP

Output:
      
      non-fiction/OUP
      non-fiction/OUP/Abernathy
      non-fiction/OUP/Abernathy/ch1.txt
      non-fiction/OUP/Abernathy/ch14.txt
      non-fiction/OUP/Abernathy/ch15.txt
      non-fiction/OUP/Abernathy/ch2.txt
      non-fiction/OUP/Abernathy/ch3.txt
      non-fiction/OUP/Abernathy/ch6.txt
      non-fiction/OUP/Abernathy/ch7.txt
      non-fiction/OUP/Abernathy/ch8.txt
      non-fiction/OUP/Abernathy/ch9.txt
      non-fiction/OUP/Berk
      non-fiction/OUP/Berk/CH4.txt
      non-fiction/OUP/Berk/ch1.txt
      non-fiction/OUP/Berk/ch2.txt
      non-fiction/OUP/Berk/ch7.txt
      non-fiction/OUP/Castro
      non-fiction/OUP/Castro/chA.txt
      non-fiction/OUP/Castro/chB.txt
      non-fiction/OUP/Castro/chC.txt
      non-fiction/OUP/Castro/chL.txt
      non-fiction/OUP/Castro/chM.txt
      non-fiction/OUP/Castro/chN.txt
      non-fiction/OUP/Castro/chO.txt
      non-fiction/OUP/Castro/chP.txt
      non-fiction/OUP/Castro/chQ.txt
      non-fiction/OUP/Castro/chR.txt
      non-fiction/OUP/Castro/chV.txt
      non-fiction/OUP/Castro/chW.txt
      non-fiction/OUP/Castro/chY.txt
      non-fiction/OUP/Castro/chZ.txt
      non-fiction/OUP/Fletcher
      non-fiction/OUP/Fletcher/ch1.txt
      non-fiction/OUP/Fletcher/ch10.txt
      non-fiction/OUP/Fletcher/ch2.txt
      non-fiction/OUP/Fletcher/ch5.txt
      non-fiction/OUP/Fletcher/ch6.txt
      non-fiction/OUP/Fletcher/ch9.txt
      non-fiction/OUP/Kauffman
      non-fiction/OUP/Kauffman/ch1.txt
      non-fiction/OUP/Kauffman/ch10.txt
      non-fiction/OUP/Kauffman/ch3.txt
      non-fiction/OUP/Kauffman/ch4.txt
      non-fiction/OUP/Kauffman/ch5.txt
      non-fiction/OUP/Kauffman/ch6.txt
      non-fiction/OUP/Kauffman/ch7.txt
      non-fiction/OUP/Kauffman/ch8.txt
      non-fiction/OUP/Kauffman/ch9.txt
      non-fiction/OUP/Rybczynski
      non-fiction/OUP/Rybczynski/ch1.txt
      non-fiction/OUP/Rybczynski/ch2.txt
      non-fiction/OUP/Rybczynski/ch3.txt


I found this command using `man find` in the terminal

          
          
          
          

          
          
          
          

          
          
          
          

          
          
          
          
