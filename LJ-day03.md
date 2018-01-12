12jan2018
So, I figured out my little dilema.
In a scenario where you ask one question, say "What is the temperature difference between the return and supply air?"
depending on the numerical range, you may need a different alert().

For example, if the answer is less than 25 and greater than 15 
15<answer<25
You should get the alert
('That is really good!)

If, however, your answer is greater than 25  
answer>25
You should get a different message
alert('That is really high!')

But, if the answer is less than 15
answer<15
The alert should read aler('wow, that is really low')

I had made the mistake of attempting to use a differential expression in my first "if"
if (15<answer<25)
and my code would just run straigth to my last line of code.

Instead, I decided to make my adecuate temperature range ...15<answer<25...
my default, making my code look like this:


        if(answer>=25) {
            alert('.....);
             //Display message for HIGH temp. difference//
        }else if (answer<12) {
            alert('.......');
            //Display message for LOW temp difference//
        }else
            {alert('.......');
            //Display message for GOOD temperature difference. The 15-20 degree split is the DEFAULT//
        }
       