Question.objects.all()
Question.objects.filter(id=1)
Question.objects.filter(question_text__startswith='What')
Question.objects.get(pub_date__year=current_year)
Question.objects.get(pk=1)

q.save()
q.choice_set.all()
q.choice_set.create(choice_text='Not much', votes=0)


Generating admin sites for your staff or clients to add, change, and delete content is tedious work that doesn’t require much creativity. For that reason, Django entirely automates creation of admin interfaces for models.

Django was written in a newsroom environment, with a very clear separation between “content publishers” and the “public” site. Site managers use the system to add news stories, events, sports scores, etc., and that content is displayed on the public site. Django solves the problem of creating a unified interface for site administrators to edit content.

