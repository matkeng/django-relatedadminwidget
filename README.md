django-relatedadminwidget
=========================

Widget for displaying edit and delete links alongside foreign key admin widgets

![Flowers](https://github.com/benjaoming/django-relatedadminwidget/raw/master/screenshot.png)

Installation:

1. Install:
    pip install django-relatedadminwidget
2. Put relatedwidget folder in your project folder.
3. Add "relatedwidget" to settings.INSTALLED_APPS
4. In your other application's admin.py, let the model admins inherit from RelatedWidgetWrapperBase like in this example:

    from relatedwidget import RelatedWidgetWrapperBase

    class MyModelAdmin(RelatedWidgetWrapperBase, admin.ModelAdmin):
        pass
    
    admin.site.register(MyModel, MyModelAdmin)

It also works with TabularInline and StackedInline! Remember the order of inheritence, always put RelatedWidgetWrapperBase first!

