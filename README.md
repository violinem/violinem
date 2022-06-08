# K-TCD for a Reverse Repo transaction
Data was imported from a json file as follows:
```bash
with open('data.json') as json_data:
    firedata = json.load(json_data)
    print(type(firedata))
    print(type(firedata['data']))
    print(json.dumps(firedata, indent=2, sort_keys=False))
```
