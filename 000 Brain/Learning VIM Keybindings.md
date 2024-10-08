---
Created On: 2023-10-12, 12:33
Unique ID: 202310121233
---
**Status:** #review 

**Tags:** #VimCards

# Learning VIM Keybindings


#### How Do you move halfway down or up the page?
?
CNTL-D and CNTL-U
<!--SR:!2025-10-31,448,250-->


#### How do operators work?
?
`{operator}{count}{motion}` || `{count}{operator}{motion}`
<!--SR:!2025-06-10,441,290-->


#### In Vim, what is the delete operator? 
?
`d`
`dd` - delete line
`D` - delete until end of line
<!--SR:!2025-02-13,370,309-->


#### In Vim, what is the find-in-line operator? 
?
`f`
<!--SR:!2025-01-27,353,309-->


#### In Vim, what is the find unTil operator? 
?
`t`
<!--SR:!2025-03-01,340,270-->

#### In Vim, what is the change operator? 
?
`c`
`cc` - change entire line
`C` - change until end of line
<!--SR:!2026-02-21,618,270-->

#### In Vim, what is the copy (yank) operator? 
?
`y`
`yy` - yank entire line
<!--SR:!2024-11-20,285,270-->

#### In Vim, what is the paste operator? 
?
`p` - paste
`P` - paste before cursor
<!--SR:!2024-11-18,283,269-->

#### In Vim, what is the lowercase operator? 
?
`gu`
<!--SR:!2024-11-21,240,250-->

#### In Vim, what is the uppercase operator? 
?
`gU`
<!--SR:!2024-11-16,235,250-->

#### In Vim, what is the delete character under the cursor operator? 
?
`x`
<!--SR:!2025-01-05,331,289-->


#### In Vim, what is the operator to indent or dedent?
?
`> | <`
<!--SR:!2025-03-16,276,269-->

#### In Vim, how do you move backward or forward words?
?
`w` - word
`b` - back
`e` - end of word
`ge` - end of word backwards
<!--SR:!2025-02-28,339,270-->


#### In Vim, how do you navigate around lines?
?
`hjkl` - left, down, up, right
`0` - start of line
`^` - start of line after whitespace
`$` - end of line
<!--SR:!2026-04-08,664,290-->


#### What are VIM Text Objects?
?
w-word
s-sentence
p-paragraph
"-quotes - Which are also forward seeking - which is so cool. Quotes are " ' `
<!--SR:!2024-08-13,28,209-->

#### What are the different ways to enter insert mode?
?
i - insert
a - append
I - insert at the start of line
A- Append to end of line
o-next line
O-previous line
<!--SR:!2024-11-19,284,270-->


#### What can you do in Visual Block Mode? How do you enter visual block mode? How do you perform operations in Visual Block Mode?
?
CNTL-V to enter it. 
This allows you to do multi cursor actions.
Capital `I` or `A` to insert after that.
<!--SR:!2024-10-02,54,210-->


---
# References
