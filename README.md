# iris_project


### rs.iris_researchers(keyword)




#### Parameters:
**keyword**: _str_

    keyword to search in the iris database,e.g('housing', 'urban planning')
    
**onlyiriscodes**: _boolean_
    
    Return the list of the iris alias of the relevant authors based on the input keyword. Will default on false returning
    the abstracts
    
#### Return:

**authorlist**: _list_

    Returned if onlyriscodes=True. List of the identified authors' iris codes.
    
    
    
    
#### Examples: 

```python
housing_related_authors = rs.iris_researchers('housing')
```
--------------------------------------------------------------------------------------------------------------

### rs.fetch_publications(listofauthors)




#### Parameters:
**listofauthors**: _list_

    List of iris code names of authors.
    
    
#### Return:

**abstracts**: _dict_

    Returned if onlyriscodes=True. List of the identified authors.
    
**detailed_data_frame**: _pd.DataFrame_

    Overview data frame with details for the authors that were fetched. 
    

    
    
#### Examples: 

```python

housing_related_authors = rs.iris_researchers('housing',onlyiriscodes=True)

abstracts,test_dataframe = rs.fetch_publications(housing_related_authors)

```


```python

housing_related_authors = ['ABCSF']

abstracts,test_dataframe = rs.fetch_publications(housing_related_authors)

```




