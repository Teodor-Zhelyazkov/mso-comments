# mso-comments
Match all MSO Conditional Comments 

# Regex 
/<!--\[\s*if (\s*(\||\s*)\s*(!|\(|\s*)\s*(!|\s*)(lte|gte|lt|gt|\s*)\s*(mso)\s*(\d+|\s*)\s*(\)|\s*)\s*)+\]>\s*(<!(-)+>|\s*)([\s\S]*?)(<!(-)+|\s*)\s*<!\[endif\]-->/gm

# Match
<!--[if mso]> your code <![endif]-->
<!--[if mso 9]> your code <![endif]-->
<!--[if mso 10]> your code <![endif]-->
<!--[if mso 11]> your code <![endif]-->
<!--[if mso 12]> your code <![endif]-->
<!--[if mso 14]> your code <![endif]-->
<!--[if mso 15]> your code <![endif]-->
<!--[if mso 16]> your code <![endif]-->

<!--[if gt mso 14]> Everything above Outlook 2010 <![endif]-->
<!--[if lt mso 14]> Everything below Outlook 2010 <![endif]-->
<!--[if gte mso 14]> Outlook 2010 and above <![endif]-->
<!--[if lte mso 14]> Outlook 2010 and below <![endif]-->
<!--[if (!mso 12)|(mso 16)]>    Outlook 2007 / 2016 only <![endif]-->
<!--[if (mso 12)|(!mso 16)|(mso 11)|(lte mso 6)]>    Outlook 2007 / 2016 only <![endif]-->
<!--[if (lt mso 12)|(lte mso 16)|(gt mso 11)|(gte mso 6)]>    Outlook 2007 / 2016 onl <![endif]-->
<!--[if !mso]><!--> All Outlooks will ignore this <!--<![endif]-->
<!--[if gte mso 9]> your code <![endif]-->
<!--[if !mso 91]> your code <![endif]-->
<!--[if mso 10 | mso 11 | gte mso 11 | !mso 9 ]> your code <![endif]-->
