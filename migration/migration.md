Migration
---

---
<img src="https://img.shields.io/badge/v-3.0-blue?style=for-the-badge" alt="">
---

Чтобы переименовать модель, сначала необходимо создать пустую миграцию:

    manage.py makemigrations <app_name> --empty

Затем вам нужно отредактировать код миграции следующим образом:

    from django.db import models, migrations

        class Migration(migrations.Migration):

        dependencies = [
            ('yourapp', 'XXXX_your_previous_migration'),
        ]

        operations = [
            migrations.RenameField(
                model_name='Foo',
                old_name='name',
                new_name='full_name'
            ),
            migrations.RenameField(
                model_name='Foo',
                old_name='rel',
                new_name='odd_relation'
            ),
        ]

И после этого вам нужно бежать:

    manage.py migrate <app_name>

---