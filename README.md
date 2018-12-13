# IG REST trading API client

Small Python library to connect to [IG](https://www.ig.com/) REST trading API (more information and API reference is available on [IG Labs](https://labs.ig.com/) website).

## Installation

```bash
pip install git+https://github.com/wjszlachta/ig-rest-client.git
```

## Usage

For demo account:

```python
from ig_rest_client import IgRestSession

api_key = '...'
account_id = '...'
username = '...'
password = '...'

session = IgRestSession(api_key, account_id, username, password)

print(session.session_details())
```

For live account:

```python
from ig_rest_client import IgRestSession, IG_REST_TRADING_API_LIVE_URL

api_key = '...'
account_id = '...'
username = '...'
password = '...'

session = IgRestSession(api_key, account_id, username, password, api_url=IG_REST_TRADING_API_LIVE_URL)

print(session.session_details())
```
