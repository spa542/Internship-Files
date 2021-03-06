# BusinessCardParser Program Documentation
# Entegra Systems Coding Challenge
# Author: Ryan Rosiak
# Date: 12/25/2019
<br /> <br />
## Description:
This program allows the user to input a basic string that represents a business card that was parsed
from an app. This string will then parse necessary information so a Contact can be created and be 
filled with basic information. The program is simple using two classes, be it the BusinessCardParser and
ContactInfo. Only one instance of each is needed to run the program in a main function as a library.
BusinessCardParser will parse the name, phone number, and email address from a user entered string and then 
return a new instance of ContactInfo with the parsed info assigned to it. After this, the ContactInfo
instance is left up to the user or other programs to do with the information as they see fit.
<br /> <br />
## How to Run:
Within the ParseBusinessCard Folder you will find another ParseBusinessCard folder and a .sln file. 
Follow Directory path ParseBusinessCard->obj->Debug->ParseBusinessCard.exe To run the command line
for the program. If application causes issues, refer to .sln file in microsoft visual studio or
email creator at ryan11291129@gmail.com
<br /> <br />
## Libraries that are used:
* Regex C# engine
<br /> <br />
## Program files:
* Program.cs, BusinessCardParser.cs, and ContactInfo.cs - Written code
* sample.txt - Used to test regular expressions
<br /> <br />
## Specifications:
1. The input string must me one long continuous entry that has all of the "scanned" information 
	of the business card
2. The parsed names that match the regular expression used will be displayed to the user to choose
	which of the matches is a correct human name to disambiguate between company names and 
	addresses etc.
<br /> <br />
## Highlights of the Program:
1. The user can run the program on platforms that do not have a common method of displaying text like Console.WriteLine
because none of the classes use features that have the possibility of being unsupported
2. The program is open to future extensions and further additions that will allow for more accurate and 
well-rounded usage
<br /> <br />
## Minor Bug:
Currently, There is a bug with the parsing of the name from the input string. Using regular expressions,
there is no concurrent way to match and separate a person's name, a company name, and job name.
The regular expression used will sometimes pull information from other criteria e.x.(The match contains
both the company name and person's name within it) and will be displayed to the user. Some of this is fixed
by the program allowing the user to choose what correctly matches a persons name from the business card, but 
unwanted information can still slip in to the assigned name field of ContactInfo.
<br /> <br />
## Potential Fixes:
A fix to this bug could be using pattern matching or a libray that contains a list of common names for people. 
The list of common people would be helpful because the computer would then be able to recognize a person's name by
matching the parsed matches from the input string to a list of commonly used names. Pattern matching would be useful
because a computer would scan inputs from enough business cards to eventually determine where a name can be placed in the
string in comparison to other things like the company name or the job name. Also, the computer could learn to disambiguate
between a common human name and a company name.
<br /> <br />
## Things to add:
* An extension allowing a list of common human names to be used as a reference for the computer when parsing the name from the 
business card string
* Further function of the ContactInfo class, at the moment it is just a class with private members and no member methods
