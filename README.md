# cerebuswrapper
A thin convenience wrapper around CereLink's cerebus.cbpy.

## Installation

Requirements:

[Cerelink](https://github.com/dashesy/CereLink) python module `cerebus` must be installed.

Then...

* Download this repository, change to this directory, then `pip install .`.
* Alternatively, `pip install git+https://github.com/SachsLab/cerebuswrapper.git`

## Usage

```Python
from cerebuswrapper import CbSdkConnection
cbsdk_conn = CbSdkConnection()
cbsdk_conn.connect()
cbsdk_conn.cbsdk_config = {'reset': True, 'get_continuous': True}
result, data = cbsdk_conn.get_continuous_data()
cbsdk_conn.disconnect()  # Will also disconnect when being deleted.
```