# Django Models

## Best Practices

Best Practices for Django models:

### No fieldname 'link' in a CMSPlugin model
If you want to add a link to your model, don't name your field ```link``` because you may receive the error ```Cannot assign "u''": "YourModel.link" must be a "Link" instance.```
* The ```link``` name is reserved for a link to a CMS page.
* Solution: you could name your field ```url```.
