# Vi and Vim editor:


## Vim:

Open terminal and input: <b>pwd</b>

Output: <b>/home/rashik</b>

We are in the <b>home/rashik</b> directory.

Now enter <b>ls</b> command to see files and directories.

Input: <b>ls</b>
<pre>
<b>
Output: Desktop                                 Music          Templates
discord.deb                             Pictures       Videos
Documents                               Public         WhiteSur-gtk-theme
Downloads                               Python-3.12.0
google-chrome-stable_current_amd64.deb  snap
</b>
</pre>

Then using <b>cd</b> command go to the "/Desktop/command line practice" directory.

Now create and open a file using <b>vim</b>:

Input: <b>vim file1.txt</b>

<pre>
Output:

~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
"file1.txt" [New]                                             0,0-1         All

</pre>

now press "i" to insert or write something.

<pre>
Hello world
this is a text file
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
-- INSERT --                                                  2,21          All
</pre>

to save the changes and exit from the file:
press <b>"esc"</b> and the "<b>:wq"</b>

Now we have a new text file.

To read the file: 
Input: <b>cat file1.txt</b>

Output:
<pre>
Hello world
this is a text file 
</pre>

If we write something wrong and we don't want to save that the

press <b>"esc"</b> and then <b>":q!"</b> 

## Now we will see what operations we can operate with vim one by one.

open the <b>"file1.txt"</b> file

Input: <b>vim file1.txt</b>

<pre>
Hello world
this is a text file
The towels had been hanging from the rod for years. They were stained and worn, and quite frankly, just plain ugly. Debra didn't want to touch them but she really didn't have a choice. It was important for her to see what was living within them.
The trail to the left had a "Danger! Do Not Pass" sign telling people to take the trail to the right. This wasn't the way Zeke approached his hiking. Rather than a warning, Zeke read the sign as an invitation to explore an area that would be adventurous and exciting. As the others in the group all shited to the right, Zeke slipped past the danger sign to begin an adventure he would later regret.
It had been a late night. To be more correct, it had been an early morning. It was now 3:00 AM and George was just getting home. He wasn't sure if it had been worth it. He was supposed to have been finished by 10:00 PM, but his boss had implored him to stay and help when it was clear they weren't going to meet the 10:00 PM target time. So, he had stayed an extra 5 hours and lost a good night's sleep for something he didn't really believe in, but he did anyway because he was afraid if he refused he might lose his job.
"Begin today!" That's all the note said. There was no indication from where it came or who may have written it. Had it been meant for someone else? Meghan looked around the room, but nobody made eye contact back. For a brief moment, she thought it might be a message for her to follow her dreams, but ultimately decided it was easier to ignore it as she crumpled it up and threw it away.
She didn't understand how changed worked. When she looked at today compared to yesterday, there was nothing that she could see that was different. Yet, when she looked at today compared to last year, she couldn't see how anything was ever the same.
Dave watched as the forest burned up on the hill, only a few miles from her house. The car had been hastily packed and Marta was inside trying to round up the last of the pets. Dave went through his mental list of the most important papers and documents that they couldn't leave behind. He scolded himself for not having prepared these better in advance and hoped that he had remembered everything that was needed. He continued to wait for Marta to appear with the pets, but she still was nowhere to be seen.
Do you think you're living an ordinary life? You are so mistaken it's difficult to even explain. The mere fact that you exist makes you extraordinary. The odds of you existing are less than winning the lottery, but here you are. Are you going to let this extraordinary opportunity pass?
He was after the truth. At least, that's what he told himself. He believed it, but any rational person on the outside could see he was lying to himself. It was apparent he was really only after his own truth that he'd already decided and was after this truth because the facts didn't line up with the truth he wanted. So he continued to tell everyone he was after the truth oblivious to the real truth sitting right in front of him.
It went through such rapid contortions that the little bear was forced to change his hold on it so many times he became confused in the darkness, and could not, for the life of him, tell whether he held the sheep right side up, or upside down. But that point was decided for him a moment later by the animal itself, who, with a sudden twist, jabbed its horns so hard into his lowest ribs that he gave a grunt of anger and disgust.
They had no proof. He knew that they knew he had done it but they didn't have any proof. It was a huge distinction and it was the difference between him keeping his freedom or being locked away for decades. They continued to question him, probing him for information that they could use against him or find the proof they needed to put him away. He smiled and continued to block their every inquiry by feigning his innocence for a crime they all knew he committed.
After hunting for several hours, we finally saw a large seal sunning itself on a flat rock. I took one of the wooden clubs while Larry took the longer one. We slowly snuck up behind the seal until we were close enough to club it over its head. The seal slumped over and died. This seal would help us survive. We could eat the meat and fat. The fat could be burned in a shell for light and the fur could be used to make a blanket. We declared our first day of hunting a great success.
There wasn't a whole lot more that could be done. It had become a wait-and-see situation with the final results no longer in her control. That didn't stop her from trying to control the situation. She demanded that things be done as she desperately tried to control what couldn't be.
He wandered down the stairs and into the basement. The damp, musty smell of unuse hung in the air. A single, small window let in a glimmer of light, but this simply made the shadows in the basement deeper. He inhaled deeply and looked around at a mess that had been accumulating for over 25 years. He was positive that this was the place he wanted to live.
Trees. It was something about the trees. The way they swayed with the wind in unison. The way they shaded the area around them. The sounds of their leaves in the wind and the creaks from the branches as they sway, The trees were making a statement that I just couldn't understand.   GNU nano 6.2                        file1.txt                                 
Hello world this is a text fileThe towels had been hanging from the rod for years. They were stained and worn,>
The trail to the left had a "Danger! Do Not Pass" sign telling people to take t>
It had been a late night. To be more correct, it had been an early morning. It >
"Begin today!" That's all the note said. There was no indication from where it >
She didn't understand how changed worked. When she looked at today compared to >
Dave watched as the forest burned up on the hill, only a few miles from her hou>
Do you think you're living an ordinary life? You are so mistaken it's difficult>
He was after the truth. At least, that's what he told himself. He believed it, >
It went through such rapid contortions that the little bear was forced to chang>
They had no proof. He knew that they knew he had done it but they didn't have a>
After hunting for several hours, we finally saw a large seal sunning itself on >
There wasn't a whole lot more that could be done. It had become a wait-and-see >
He wandered down the stairs and into the basement. The damp, musty smell of unu>
Trees. It was something about the trees. The way they swayed with the wind in u>

~                                                                               
~                                                                               
"file1.txt" 31L, 6615B                                        30,72         Bot

</pre>

+To jump to the next line: <b>Shift + G</b>

+To jump to the top of the line: <b>Shift + gg</b>

+ To search any word(Top to Bottom): <b>press Esc</b> then <b>/word</b>
    + For next occurance of the searched word: <b>press "n"</b>

+ To search any word (Bottom to Top): <b>press Esc</b> then <b>?word</b>

+ To globally replace a word: <b>%s/word1/word2/g</b>
    + word1= the word that will be changed
    + word2= Changed word or new word

+ Undo= <b>u</b>
+ To undo all the changes in one time: <b>:e!</b>
+ Redo= <b>ctrl + r</b>

+ To start editing from the begeining of the line: <b>Shift + I</b>
+ To start editing from the end of the line: <b>Shift + O</b>

+ To delete a character where cursor is present: <b>x</b>

+ To replace a single character where cursor is present: <b>r</b>

+ To delete a line where cursor is present: <b>dd(twice d)</b>
