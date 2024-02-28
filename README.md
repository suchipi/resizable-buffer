# `@suchipi/resizable-buffer`

Helper class for "resizing" an ArrayBuffer.

- When reducing the size, ArrayBuffer.slice is used (cheap).
- When increasing the size, a new ArrayBuffer is created and the contents are copied over (expensive).

```ts
export declare class ResizableBuffer {
  constructor(byteLength: number);
  buffer: ArrayBuffer;
  resizeTo(byteLength: number): void;
  resizeBy(bytes: number): void;
}
```
