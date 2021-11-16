# JSON-Array-to-CSV
The ipynb file added will help in getting all the columns present in the JSON arrat. In order to get selected rows, there will be a minor change in one snippet (mentioned below):


#### _l=[]_
#### _for i in range(len(parsed)):_
####    _flat = flatten_json(parsed[i])_
####    _m=json_normalize(flat)_
####    _idvars_cols = [col for col in m.columns if ('character' not in col.lower() and 'character_2' not in col.lower())]_
####    _l.append(m[idvars_cols])_
