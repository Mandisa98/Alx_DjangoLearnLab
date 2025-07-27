# retrieve.md

from bookshelf.models import Book
book = Book.objects.get(title="1984")
print(book.title)         # Output: 1984
print(book.author)        # Output: George Orwell
print(book.published_date)  # Output: 1949-06-08
