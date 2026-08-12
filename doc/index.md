---
layout: layouts/catalog-page
title: Rib:bit Datalogger
mfn:
    - hwidx.org/2/1/1.0
    - hwidx.org/2/1/2.0
info: >-
    Rib:bit Datalogger adds SD card file and storage blocks for logging data from Rib:bit projects, with card initialization, file read/write support, and filesystem helpers.
plugins:
    - ts-to-blocks
tags:
    - software
    - api
    - makecode
    - blocks
---

## Overview

Rib:bit Datalogger helps you save and read project data on an SD card using MakeCode blocks.

This page is a learner-friendly overview. Start with blocks first, then move to TypeScript docs if you need deeper behavior or advanced workflows.

## What you can build

- Sensor logs you can remove and inspect later
- CSV exports for experiments and field tests
- Local configuration and notes files
- Reliable long-running data capture projects

## Learning path

- Start with blocks: [Rib:bit Datalogger Blocks Guide](blocks/)
- Use TypeScript when ready: [Rib:bit Datalogger TypeScript Reference](typescript/)
- Browse the full API structure: [Rib:bit Datalogger API Index](api/)

## Example

This example initializes storage and appends two CSV lines to a log file.

```ts
if (SDCard.initialize()) {
  if (SDCard.openFile("log.txt", SDCard.FileMode.APPEND) === SDCard.ErrorCode.OK) {
    SDCard.writeLine("timestamp,latitude,longitude")
    SDCard.writeLine("0,51.5074,-0.1278")
    SDCard.closeFile()
  }
}
```

## More resources

- TypeScript namespace docs: [SD Card Namespace](namespace_sdcard/)
- TypeScript enum docs: [Error Code Enum](enum_errorcode/), [File Mode Enum](enum_filemode/)
