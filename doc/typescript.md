---
layout: layouts/catalog-page
title: Rib:bit Datalogger TypeScript Reference
---

## Overview

This page documents the TypeScript-facing API for Rib:bit Datalogger.

If you are learning, start with [Rib:bit Datalogger](../) and [Rib:bit Datalogger Blocks Guide](../blocks/).

## Quick call summary

- Startup: `initializeCard()`, `initializeFilesystem()`, `initialize()`, `isReady()`
- File operations: `openFile()`, `closeFile()`, `writeString()`, `writeBuffer()`, `writeLine()`, `readBytes()`, `readString()`, `readLine()`
- Position/state: `seek()`, `getPosition()`, `getFileSize()`, `isEndOfFile()`, `isFileOpen()`, `flush()`
- Management: `fileExists()`, `deleteFile()`, `getCardType()`, `getFilesystemType()`

## Example

```ts
if (SDCard.initialize()) {
  if (SDCard.openFile("log.txt", SDCard.FileMode.APPEND) === SDCard.ErrorCode.OK) {
    SDCard.writeLine("timestamp,latitude,longitude")
    SDCard.writeLine("0,51.5074,-0.1278")
    SDCard.closeFile()
  }
}
```

## API details

- API index: [Rib:bit Datalogger API Index](../api/)
- Namespace details: [SD Card Namespace](../namespace_sdcard/)
- Enum details: [Error Code Enum](../enum_errorcode/), [File Mode Enum](../enum_filemode/)
