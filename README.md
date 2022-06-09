# K-TCD for a Reverse Repo transaction
Data was imported from a json file and shown as follows:
```bash
with open('data.json') as json_data:
    firedata = json.load(json_data)
    print(type(firedata))
    print(type(firedata['data']))
    print(json.dumps(firedata, indent=2, sort_keys=False))
```
The data was named as firedata.

The important information was accessed as follows:

```bash
for item in firedata['data']:
    sft_leg = item['id']
    start_date = item['start_date']
    end_date = item['end_date']
    trade_date = item['trade_date']
    rc = firedata['data'][0].get('balance')
    asset = item.get('mtm_dirty')
    issuer_type = item.get('issuer', {}).get('type')
    counterparty_type = item['customer']['type']
    print(item)
```
