#[Overheard at Breakfast](https://tryhackme.com/room/hh-overheardatbreakfast-6f01793c)
This is part of the Hacker Holidays series. 
It is a short OSINT challenge that asks to analyze a conversation, extract its identifying details, locate a hidden account, and retrieve the flag.

Analyze the provided conversation for identifying details
Conversation: <img width="1175" height="781" alt="conversation" src="https://github.com/user-attachments/assets/3d298e0d-1b51-4ecc-8d1c-22d3f26a1315" />
 
Extract the relevant clues:
First we have lambo email: lambobytelotushotel@gmail.com, and a platform to upload users names and provide other accounts, it starts with G.
 
Locate the hidden account
With a simple online search i found that the web was [gravatar](https://es.gravatar.com/) Then i looked up the mail and it led me to this [page](https://es.gravatar.com/cheerfullysongf28e3c3716) where he had this info: <img width="645" height="445" alt="image" src="https://github.com/user-attachments/assets/a7db8310-50ec-404c-bf67-a299b0b6bd7c" />

This is an alphanumeric hash: VEhNe1MzY3JlVF9QcjBmaWwzX0g0c19iMzNuX0lkZW50MWZpM2R9
I went to CyberChef and dehashed it from Base64.
Submit the flag: THM{S3creT_Pr0fil3_H4s_b33n_Ident1fi3d}
📸 @0xMia's STORY
 
@0xMia
· posted 40 min after room unlock
"the breakfast crowd really said the quiet part out loud this morning 😭 y'all need to actually READ what they said, not just skim it #HackerHolidays"

And with that i passed the room.
