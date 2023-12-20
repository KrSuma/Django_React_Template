Two main directories, one React and one Django.

On django_react "settings.py", these two settings were added to use React configured files.

- TEMPLATES = ... 'DIRS': [os.path.join(BASE_DIR, 'reactapp/build')]
- STATICFILES_DIRS = [os.path.join(BASE_DIR, 'reactapp/build/static')]

in the "urls.py", TemplateView has been added to use the "index.html" from reactapp/src:

- ...    path('', TemplateView.as_view(template_name='index.html'))
