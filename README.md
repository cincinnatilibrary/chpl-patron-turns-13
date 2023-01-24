# CHPL Patron Turns 13

This script utilizes the Sierra REST API endpoint, `put /v6/patrons/{id}` to modify patron records, changing any child-only card to a teen-only card after they have turned 13 years old.

This script will query for:

* patrons who have turned 13 years old on the last `script_run_date`
* patrons that are one of the following ptypes : 
    ```python
        (
            1
        )
    ```

The content of the body sent in the PUT request (`/v6/patrons/{id}`) will look like the following:

```python
{
  "patronType": 2
}
```
