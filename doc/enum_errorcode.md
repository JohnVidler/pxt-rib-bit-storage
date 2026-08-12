---
layout: layouts/catalog-page
title: Error Code Enum
---

## Enum `ErrorCode`

Operation result codes used by SDCard APIs.

- `OK = 0`: Operation succeeded.
- `TIMEOUT = 1`: Timeout while waiting for card response.
- `CRC_ERROR = 2`: CRC validation failed.
- `WRITE_ERROR = 3`: Write operation failed.
- `INIT_FAILED = 4`: Card or filesystem init failed.
- `NOT_INITIALIZED = 5`: SDCard not initialized.
- `INVALID_PARAM = 6`: Invalid argument value.
- `FILE_NOT_FOUND = 7`: File does not exist.
- `NO_FILE_OPEN = 8`: No file is currently open.
- `DISK_FULL = 9`: No remaining write space.
- `INVALID_FS = 10`: Unsupported or invalid filesystem.
- `END_OF_FILE = 11`: End of file reached.
