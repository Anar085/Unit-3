# Quiz 048

## Python Code 
```.py
class Book:
    def __init__(self,title,author,isbn):
        self.title=title
        self.author=author
        self.isbn=isbn
    def display_info(self):
        print(f"Title:{self.title},Author:{self.author},ISBN:{self.isbn}")

class Library:
    def __init__(self):
        self.books=[]
    def add_book(self, book):
        self.books.append(book)
        print(f"Added book: {book.title}")
    def show_books(self):
        if not self.books:
            print("No books in the library.")
        else:
            for book in self.books:
                book.display_info()
m=Library()
ex_book=Book("To Kill a Mockingbird", "Harper Lee", "9780446310789")
m.add_book(ex_book)
m.show_books()
```


## Proof of work

![image](https://github.com/user-attachments/assets/6c570038-45aa-41ef-a7a5-2e95221f0e5e)



