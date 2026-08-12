---
layout: layouts/catalog-page
title: SD Card Namespace
---

## Namespace `SDCard`

Provides SD card initialization, FAT filesystem access, and file-level read/write calls.

## Primary calls

### `initialize()`

- **Parameters:** None
- **Returns:** `boolean`
- **Description:** Initializes card and filesystem.

### `openFile(filename, mode)`

- **Parameters:**
  - `filename`: File to open.
  - `mode`: Access mode from [FileMode](../enum_filemode/).
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Opens a file for reading, writing, or appending.

### `closeFile()`

- **Parameters:** None
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Closes the current file.

### `writeString(text)`

- **Parameters:**
  - `text`: String data.
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Writes string data.

### `writeBuffer(data)`

- **Parameters:**
  - `data`: Buffer to write.
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Writes raw buffer data.

### `writeLine(text)`

- **Parameters:**
  - `text`: Text line to write.
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Writes a line and line ending.

### `readBytes(length)`

- **Parameters:**
  - `length`: Number of bytes.
- **Returns:** `Buffer`
- **Description:** Reads raw bytes.

### `readString(length)`

- **Parameters:**
  - `length`: Number of characters/bytes requested.
- **Returns:** `string`
- **Description:** Reads string data.

### `readLine()`

- **Parameters:** None
- **Returns:** `string`
- **Description:** Reads one line.

### `seek(position)`

- **Parameters:**
  - `position`: Target position.
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Moves file cursor.

### `getPosition()`

- **Parameters:** None
- **Returns:** `number`
- **Description:** Gets current file position.

### `getFileSize()`

- **Parameters:** None
- **Returns:** `number`
- **Description:** Gets current file size.

### `isEndOfFile()`

- **Parameters:** None
- **Returns:** `boolean`
- **Description:** Reports whether cursor reached end of file.

### `fileExists(filename)`

- **Parameters:**
  - `filename`: File to check.
- **Returns:** `boolean`
- **Description:** Checks whether file exists.

### `deleteFile(filename)`

- **Parameters:**
  - `filename`: File to remove.
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Deletes a file.

### `getCardType()`

- **Parameters:** None
- **Returns:** [CardType](../enum_cardtype/)
- **Description:** Returns detected SD card type.

### `getFilesystemType()`

- **Parameters:** None
- **Returns:** [FSType](../enum_fstype/)
- **Description:** Returns detected filesystem type.

### `isReady()`

- **Parameters:** None
- **Returns:** `boolean`
- **Description:** Reports whether storage stack is initialized.

### `isFileOpen()`

- **Parameters:** None
- **Returns:** `boolean`
- **Description:** Reports whether a file is currently open.

### `flush()`

- **Parameters:** None
- **Returns:** [ErrorCode](../enum_errorcode/)
- **Description:** Flushes buffered data to card.

## Low-level calls

These calls are exported for protocol/control internals and advanced scenarios.

- `select()`
- `deselect()`
- `waitReady(timeout = 500)`
- `sendCommand(cmd, arg)`
- `sendAppCommand(cmd, arg)`
- `initializeCard()`
- `_initializeCard(fastMode = false)`
- `initializeFilesystem()`

## Related enums

- [SD Command Enum](../enum_command/)
- [R1 Response Enum](../enum_r1response/)
- [Data Response Enum](../enum_dataresponse/)
- [Data Token Enum](../enum_datatoken/)
- [Card Type Enum](../enum_cardtype/)
- [Error Code Enum](../enum_errorcode/)
- [Filesystem Type Enum](../enum_fstype/)
- [File Mode Enum](../enum_filemode/)
