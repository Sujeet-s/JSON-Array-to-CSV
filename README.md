# JSON-Array-to-CSV
The ipynb file added will help in getting all the columns present in the JSON arrat. In order to get selected rows, there will be a minor change in one snippet (mentioned below):


l=[]
for i in range(len(parsed)):
    flat = flatten_json(parsed[i])
    m=json_normalize(flat)
    idvars_cols = [col for col in m.columns if ('character' not in col.lower() and 'character_2' not in col.lower())]
    l.append(m[idvars_cols])
