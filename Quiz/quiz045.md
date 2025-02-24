# Quiz 045

## Python Code 
```.py


class WordCounter:
    def __init__(self,text:str):
        self.text=text
    def word_count(self):
        text=self.text
        text=text.lower()
        text=text.split()
        new_word_list=[]
        for word in text:
            new_word=""
            for letter in word:
                if letter.isalpha():
                    new_word+=letter
            new_word_list.append(new_word)
        words_dict={}
        for word in new_word_list:
            if not word in words_dict.keys():
                words_dict[word]=new_word_list.count(word)

        return words_dict

m=WordCounter("This is what it is.")
print(m.word_count())

```


## Proof of work

![image](https://github.com/user-attachments/assets/0aa1ab01-6abe-4cae-9a75-7ee5d1a798bb)

## UML diagram 
![image](https://github.com/user-attachments/assets/910d5ca1-c8e7-445e-8afd-3ce5f1a34df6)


