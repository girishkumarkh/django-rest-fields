# django-rest-fields
List of all Serializable fields in Django Rest Framework

#### ArrayField
```
class ArrayField(serializers.Field):

    def from_native(self, data):
        if isinstance(data, list):
            return Arrays(data)
        else:
            msg = self.error_messages['invalid']
            raise ValidationError(msg)

    def to_native(self, obj):
        return obj.arrays
        
```
