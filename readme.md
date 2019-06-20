# Nuz Klassifir

Classifying news into categories. Calculating the interest of each user in each of the categories as well.

### Training Dataset
News Dataset used from:
https://www.kaggle.com/antcorpus/antcorpus

Dataset has these categories:

```
'culture', 'diverse', 'economy', 'internationalNews', 'localNews', 'politic', 'society', 'sport', 'technology'
```

Dataset is in XML format, so text is extracted from `<TITLE><\TITLE>, <ABSTRACT><\ABSTRACT>, <TEXT><\TEXT>` tags.

### Testing Dataset
provided from an API, in JSON format, 2000 users, 50 article per user.

```
{
  "0": [
        [
          "عنوان",
          "محتوي"
        ]
 }
 ```

### Data preprocessing
 - lowercase and linebreak removal
 - URL, special characters and digits removal
 - stemming
 - stop-word removal

### Interests
For a user, interest per category is the ratio between the number of articles that the user reads in that category and the total number of articles he reads.
```
User 0: internationalNews 12.0%, technology 22.0%, localNews 8.0%, diverse 20.0%, sport 22.0%, culture 6.0%, politic 6.0%, economy 6.0%
```

### Model

Niave Bayes classifier, achieving around 78% accuracy.
