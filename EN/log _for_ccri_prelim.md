## Fixing an ugly page - part 1
March 5, 2002

## In the beginning
1. On the minus side
- CCRI_prelim.md looks junky. Tons of information and sections all crammed into one page. <br/>
2. On the plus side
- Sandra had created a table of contents at the top of the page to make this massive page more navigable (via html links to ## level 2 headers) 
- \## - level 2 headers display nice horizontal lines on the line just below providing good section demarcators.  
<!-- the backslash before ## in the line above let's you to sneak in text that Markdown knows as a format tag -->
3. Some prep:
- Shannon installed Atom and the markdown preview package
- We commented out test change info for tracking, e.g., \<!-- Susan TO SHANNON, abc changed to xyz, keep change? -->    
We will delete most of these comments as soon as we have a good handle on what we are doing.<br/>
4. We looked at ways of: 
- Improving spacing (like more white space);
- Improving flow (clearer hierarchy and progression, keeping explanations short and presentation more consistent). 
5. We want clearer and consistent line breaks between sections, proportionate to the hierarchy of the sections. 

## Solutions so far
### 1. Spacing
1.1 A good idea is standardizing numbers of line breaks between sections - probably to a maximum of four line breaks before ## headers.  
1.2 We want to better control line breaks.  
#### Method
- The page now controls line breaks with two spaces at the end of the line above.  
- This reflects best practises A, B and C.  

A) ONE line break    
First line with two spaces after.     
And the next line.
<!-- One line break -->
 
B) TWO line breaks  
Line with two spaces after. 

And the next line.  
<!-- Two line breaks -  the two spaces in the first line may be optional in this case, but not sure -->
C) THREE line breaks  
Line with two spaces after <br/> \<br/> 

And the next line. 
<!-- Three line breaks - needs the two spaces in the first line -->

D) FOUR LINE BREAKS.   
Line with two spaces after<br/>\<br/><br/>\<br/>


And the next line. 
<!-- Four line breaks - needs the two spaces in the first line. In this example, I didn't put two spaces after the first line -->

### 2. More consistent formatting 
1. Added sub-header numbers to unnumbered sub-headers.  We probably won't number the sections above CCRI Data Sources: 1 Selected published data tables be numbered.  This would create numbering like 2.2.3.1.1.
2. Any sections that look weird probably need to be formatted like the others

### 3. It's too much!
1. So much is crammed into **2. Microdata**.  
2. Solution: a detailed table of contents for the cluttered **CCRI Data Sources** section.

#### Method

Part 1. 

I used a Markdown table for table of contents because it gives more better with alternating shaded rows for this great big blob of content links.
Just a small related point, I also got rid of text centering for everything under the header row by taking off the colons, so that the line 
| :----: | :----: | :----: |
became:
| ---- | ---- | ---- |

Part 2.

Used workarounds for table (of contents):
1. Superscript format **\<sup>1-2\<sup/>** for a small font.  Otherwise the massive table of contents looks horrible and cumbersom to read.    
I don't think offset superscript text is a biggie.  
2. Got rid of any periods in the section numbering, so 1.2 became **1-2**.   
This one change lets you create internal page links to the CCRI data sources section headers.    
3. Fiddling with header names at the pointer end so table of contents can link to target page headers
- using the current URL <https://github.com/SusanMowers/reCens_doc/blob/main/EN/ccri-prelim.md>
- the link for **\### 1-2 Map summary data** header becomes:  
\[\<sup>Map summary data\</sup>](https://github.com/SusanMowers/reCens_doc/blob/main/EN/ccri-prelim.md#1-2-Map-summary-data)  
- Markdown reoads page and jumps to actual header **\### 1-2 Map summary data** as per the URL extension: **\#** followed by **1-2-Map-summary-data**  
4. Added a leading space before the section number in column 1 for any section numbers having more than one character
- **1-2** becomes **\&nbsp; 1-2**, or more accurately, **\<sup>\&nbsp; 1-2**
6. Haven't finished step 3 (internal page links).
