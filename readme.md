


# Krippendorff


### Installation

```bash
pip install krippendorff
```


### Example usage

```python
import krippendorff
krippendorff.alpha(reliability_data=...)
```


------------------------------------------------------------------

from nltk import agreement
coder1 = [1,4,1,2,4,1,1,1,5,1]

coder2 = [1,4,1,3,4,1,1,1,4,1]

coder3 = [1,4,1,2,4,1,1,1,5,1]

formatted_codes = [[1,i,coder1[i]] for i in range(len(coder1))] + [[2,i,coder2[i]] for i in range(len(coder2))]  + [[3,i,coder3[i]] for i in range(len(coder3))]
ratingtask = agreement.AnnotationTask(data=formatted_codes)
print('Krippendorff\'s alpha:',ratingtask.alpha())


