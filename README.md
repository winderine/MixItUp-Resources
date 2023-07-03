# Publicly Released MixItUp Commands

## ![Photo of several dice used in tabletop role playing games, with a 20 sided die in the center of the shot. The dice are a pearlescent blue with yellow numbers and the background is light pink.](assets/images/Dice-Thumbnail.png) [Dice](https://mixitupapp.com/community/command/45c6cd17-384b-4039-b874-6b581824f3de) 

Simple dice roller that adds the dice (Now with Safety Precautions™)

use !d (dice) (sides):

!d 10 6
> You rolled 10 dice of 6 sides (⚄-2-3-5-3-2-5-3-4-2-1-⚄), which adds up to 30.

You could extend this by setting a "Counter" or Global "Special Identifier" to store the dice's last output for other interactions.

## ![Graphic of the words "Rina's Dynamic Dictionary" in yellow text on an orange, beveled square with trimmed corners. There are orange dotted lines at the top and bottom with squares at the ends, and the background is a darker red-orange.](/assets/images/Dynamic-Dictionary-Thumbnail.png) [Dynamic Dictionary](https://mixitupapp.com/community/command/b3953d70-a866-455d-98ca-ce337914a8dd) 

A pretty robust dictionary command that uses Wiktionary via the Free Dictionary API (https://dictionaryapi.dev/). It can load multiple definitions for multiple parts of speech, and because of some curious behavior on the part of the API there is also support for a second "word", although this second word only supports two parts of speech. 

Test the script with words like "well" and "fast" to see how spammy it can get.

Please note that this script relies on an initializer JSON file that is hosted on my github. If something happens to that file, there is no guarantee I will remember to come update this command. I've shown the location of the initializer file in the screenshot, I recommend setting up a github or other web host and cloning or copying that file to your own host just in case.

## ![Graphic of the letter "P" in yellow text on an orange, beveled square with cut-out corners. The background is a darker red-orange.](/assets/images/Pronouns-Thumbnail.png) Pronouns And Auxiliary Verbs 

Two parts: 
- [Set Pronouns](https://mixitupapp.com/community/command/5dae9acf-6102-4cce-8e7e-45b04ef7257c)
- [Pronouns And Auxiliary Verbs Example](https://mixitupapp.com/community/command/79f1d101-9907-424c-8b21-967340f67f46)

The first is a complete script to grab the pronouns from Alejo Pronouns for Twitch; you will need to create the Currency/Rank that it stores to in order for it to work properly. If the user does not have pronouns set, it prompts them to do so with a link.

Based on the Pronouns command by TicketsTom

Once this command is set up (see below) and run, you can refer to people's pronouns in other commands using $targetuserpronouns (numerical value) and $targetuserpronounsrank (pronouns category), which is used in the "Pronouns and Auxiliary Verbs" command

⚠ Because it stores pronouns to ranks for integration with other commands, you will need to create this "ranking" system as shown in the screenshot with these values:
``` Unset 0
Ae/Aer 1
Any 2
E/Em 3
Fae/Faer 4
He/Him 5
He/She 6
He/They 7
It/Its 8
Other 9
Per/Per 10
She/Her 11
She/They 12
They/Them 13
Ve/Ver 14
Xe/Xem 15
Zie/Hir 16 
```

The second is an example/Usage Guide specifically for integration with my "Set Pronouns From Alejo" command. This command does not work on it's own. 

Usage: copy the included Web Request into any command that requires dynamic pronouns, such as the example shown. Write any chat output using "They/Them" pronouns as a model, then insert $ character immediately before any word that would be gendered. If there are any words that I've missed, please report it as an issue on my Github.

This command uses a JSON stored on my Github. If something happens to that file, I will likely not remember to come and update this command. I recommend cloning or otherwise duplicating that JSON to your own github account or other web host in order to prevent unexpected loss of function. 