# [Letter Room](https://tryhackme.com/room/letter)

It's just another Monday morning on your mail delivery route when an unusual letter catches your eye. The envelope is battered, riddled with holes as if it's been through a storm. 
The address is barely legible, and your coworkers at the post office wave it off as a lost cause.

Task Files:  
<img width="1448" height="1086" alt="letter" src="https://github.com/user-attachments/assets/247a7df1-35b4-4c49-b894-bf7c8ca8a5d0" />  
<img width="1021" height="397" alt="Newspaper_clipping" src="https://github.com/user-attachments/assets/18dc0874-9757-4815-9023-3fe402d84e12" />

Note.txt content:  
"Mon cher Édouard,

Aujourd'hui, en rangeant le grenier chez mes grands-parents, je suis tombée sur cette vieille coupure de journal. Ton arrière-grand-père n'avait même pas l'âge de passer le permis quand il s'est distingué ce jour-là. Le benjamin de l'équipe, et certainement pas le moins courageux.

Il serait si fier de te voir sur l'eau à ton tour.

Avec toute mon affection,  
Audette"

What is the postal code of the delivery address on the envelope?
Answer format: *****

We need to decode the barcode from letter.png.  
How? The envelope is from La Poste, so we need a postal code from France coded into bars and then reverse-engineer it to our own barcode.  
Or find a [web](https://www.dcode.fr/french-postal-barcode) page that does that for you, or do it by hand using the table provided on the website.  
The result is 29760.

What is the flag?

First, we need to read the instructions to see what we are looking for.  
Flag format: THM{Name_Surname_age}, only the first letter of the name and surname should be capitalised.  
Example: THM{Pierre-Henry_Lagaffe_23}

We are looking for a name. We translate the French note: it talks about a great-grandpa (the one we are looking for), he is young, not enough age to drive, and something about the water.  
Now we look into the newspaper: a few titles to translate vaguely, first something urgent, then Finistère (as common knowledge it's a gulf, so water-related), the North Pole, and Morocco. I'll check Finistère first because it's the most distressed, as if someone had done it on purpose.

We have some dates to keep track of the timeline because L'Ouest-Éclair was only published between 1899 and 1944, so 45 years to check. 
I just searched *L'Ouest-Éclair une catastrophe sur du Finistère*, so we have the date from the first [link](https://kbcpenmarch.franceserv.com/la-catastrophe-du-23-mai-1925-selon-la-presse-locale.html) and the complete article.

I did a search of the number 15 because that's the youngest age I could think of for someone going to the sea, and I found Gourlaouen Yves Marie, 15 years old, and I tried him, that's the flag.

Flag: TryHackMe{Yves-Marie_Gourlaouen_15}
