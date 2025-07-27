# retrieve.md

from bookshelf.models import Book
book = Book.objects.get(title="1984")
print(book.title)         # Output: 1984
print(book.author)        # Output: George Orwell
print(book.published_date)  # Output: 1949-06-08
# update.md

from bookshelf.models import Book
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()
print(book.title)  # Output: Nineteen Eighty-Four
# delete.md

from bookshelf.models import Book
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()  # Output: (1, {'bookshelf.Book': 1})

# Confirm deletion
Book.objects.all()  # Output: <QuerySet []>
