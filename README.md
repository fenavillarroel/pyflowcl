PyFlowCL
============
Cliente API para operaciones con el servicio de pagos Flow.cl  [FlowAPI-3.0.1](https://www.flow.cl/docs/api.html)  
Frunciona como wrapper sobre cliente [OpenAPI3] (https://github.com/Dorthu/openapi3)  

[![pyflowcl-tests](https://github.com/mariofix/pyflowcl/actions/workflows/pyflowcl.yml/badge.svg?branch=dev)](https://github.com/mariofix/pyflowcl/actions/workflows/pyflowcl.yml)
[![PyPI version](https://badge.fury.io/py/pyflowcl.svg)](https://badge.fury.io/py/pyflowcl)
---

## Instalación
Este proyecto está desarrollado para Python 3.7 y superior.  
Este proyecto es administrado por Poetry.  


```bash
# con Poetry
$ poetry add pyflowcl
# con PIP
$ pip install pyflowcl
```


## Uso
APIKey y SecretKey pueden ser configurados de dos maneras

### Usando el constructor
```python
from pyflowcl import FlowAPI

flow = FlowAPI(flow_key="key", flow_secret="secret")
```

### Usando variables de entorno

```bash
export PYFLOWCL_KEY="key"
export PYFLOWCL_SECRET="SECRET"
python cliente_flow.py
```


### Cliente Antiguo

```python
from pyflowcl import Payment
from pyflowcl.Clients import ApiClient

API_URL = "https://www.flow.cl/api"
API_KEY = "your_key"
API_SECRET = "your_secret"
FLOW_TOKEN = "your_payment_token"
api = ApiClient(API_URL, API_KEY, API_SECRET)

call = Payment.getStatus(api, FLOW_TOKEN)
print(call)
```

---

## Licencia
>Puedes revisar el texto completo de la licencia [aqui](https://github.com/mariofix/pyflowcl/blob/stable-v3/LICENSE)

Este proyecto está licenciado bajo los términos de la licencia **MIT**.  
FlowAPI está licenciado bajo los términos de la licencia **Apache 2.0**.