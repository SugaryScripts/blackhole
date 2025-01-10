

#### Unsupported post request. Object with ID '371105279409151' does not exist, cannot be loaded due to missing permissions, or does not support this operation. Please read the Graph API documentation at

Solved by
Use token temp only that expired within 24 hours

##### Error Log
```json
request body: {'object': 'whatsapp_business_account', 'entry': [{'id': '284820308058955', 'changes': [{'value': {'messaging_product': 'whatsapp', 'metadata': {'display_phone_number': '6282112221208', 'phone_number_id': '371105279409151'}, 'contacts': [{'profile': {'name': '🔒'}, 'wa_id': '628973201171'}], 'messages': [{'from': '628973201171', 'id': 'wamid.HBgMNjI4OTczMjAxMTcxFQIAEhggQUUyNkQyQkU0MkZDQzM3N0I0QURFQzM4MUExRjFBMzcA', 'timestamp': '1718319822', 'text': {'body': 'how about chatgpt'}, 'type': 'text'}]}, 'field': 'messages'}]}]}

openai response: Squeeeeee! New friends! Let's unravel some mysteries together!

whatsapp message response: {'error': {'message': "Unsupported post request. Object with ID '371105279409151' does not exist, cannot be loaded due to missing permissions, or does not support this operation. Please read the Graph API documentation at https://developers.facebook.com/docs/graph-api", 'type': 'GraphMethodException', 'code': 100, 'error_subcode': 33, 'fbtrace_id': 'AALrQCK-Q2WZsEOd6qz1Nhi'}}

unknown error: 400 Client Error: Bad Request for url: https://graph.facebook.com/v19.0/371105279409151/messages
```


