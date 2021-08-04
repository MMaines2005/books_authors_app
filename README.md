# books_authors_app
Readme only

<QuerySet [<Author: Author object (1)>, <Author: Author object (2)>, <Author: Author object (3)>, <Author: Author object (4)>, <Author: Author object (5)>]>


<QuerySet [<Book: Book object (1)>, <Book: Book object (2)>, <Book: Book 
object (3)>, <Book: Book object (4)>, <Book: Book object (5)>]>

{'_state': <django.db.models.base.ModelState object at 0x000001F7D0129F28>, 'id': 1, 'title': 'C#', 'description': 'Learning C Sharp', 
'created_at': datetime.datetime(2021, 7, 29, 1, 37, 5, 658373, tzinfo=<UTC>), 'updated_at': datetime.datetime(2021, 7, 29, 2, 37, 21, 162108, tzinfo=<UTC>)}


>>> c=Author.objects.get(id=4)
>>> print(c.first_name) Lau
>>> Author.objects.get(id=4).__dict__
{'_state': <django.db.models.base.ModelState object at 0x000001F7D0142438>, 'id': 4, 'first_name': 'Bill', 'last_name': 'Tzu', 'notes': '', 'created_at': datetime.datetime(2021, 7, 29, 1, 45, 49, 214800, tzinfo=<UTC>), 
'updated_at': datetime.datetime(2021, 7, 29, 2, 44, 51, 372503, tzinfo=<UTC>)}


>>> William.book.all()
<QuerySet [<Book: C#>, <Book: PHP>]>

>>> Jane.book.add(C)
>>> Jane.book.add(PHP)
>>> Jane.book.add(Java)
>>> Jane.book.all()
<QuerySet [<Book: C#>, <Book: PHP>, <Book: Java>]>

>>> Emily.book.add(C)
>>> Emily.book.add(PHP)
>>> Emily.book.add(Java)
>>> Emily.book.add(Python)
>>> Emily.book.all()
<QuerySet [<Book: C#>, <Book: PHP>, <Book: Java>, <Book: Python>]>


>>> Bill.book.add(C)
>>> Bill.book.add(PHP)
>>> Bill.book.add(Java)
>>> Bill.book.add(Python)
>>> Bill.book.add(Ruby)
>>> Bill.book.all()
<QuerySet [<Book: C#>, <Book: PHP>, <Book: Java>, <Book: Python>, <Book: Ruby>]>

>>> Java.authors.all()
<QuerySet [<Author: Jane>, <Author: Emily>, <Author: Bill>]>
>>> Book.objects.all()
<QuerySet [<Book: C#>, <Book: PHP>, <Book: Java>, <Book: Python>, <Book: Ruby>]>

>>> Java.authors.remove(Jane)
>>> Java.authors.all()
<QuerySet [<Author: Emily>, <Author: Bill>]>

>>> Fyodor.book.add(PHP)
>>> PHP.authors.all()
<QuerySet [<Author: William>, <Author: Jane>, 
<Author: Emily>, <Author: Bill>, <Author: Fyodor>]>

>>> Emily.book.all()
<QuerySet [<Book: C#>, <Book: PHP>, <Book: Java>, <Book: Python>]>

>>> Ruby.authors.all()
<QuerySet [<Author: Bill>]>
