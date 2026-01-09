# Svg-path-editor-lib

Library yang menjadi inti dari aplikasi [SvgPathEditor app](https://mcikadu-dev.github.io/svg-path-editor/).

## Penggunaan


### Parse path

```typescript
import { SvgPath } from 'svg-path-editor-lib';

// Akan melempar error jika path tidak valid
const parsedPath = new SvgPath(path);
```

### Menghasilkan path

```typescript
parsedPath.asString(
    decimals,       // default `4`
    minifyOutput    // default `false`
)
```

### Operasi global

Semua operasi dilakukan langsung pada objek (in place).

Skala:
```typescript
parsedPath.scale(x, y);
```

Geser:
```typescript
parsedPath.translate(x, y);
```

Rotasi:
```typescript
parsedPath.rotate(x, y, angle);
```

Ubah ke relatif:
```typescript
parsedPath.setRelative(true);
```

Ubah ke absolut:
```typescript
parsedPath.setRelative(false);
```

Balikkan urutan perintah path:
```typescript
import { reversePath } from 'svg-path-editor-lib';
reversePath(parsedPath);
```

Ubah titik asal:
```typescript
import { changePathOrigin } from 'svg-path-editor-lib';
changePathOrigin(parsedPath, indexOfNewOrigin);
```

Pengoptimal lanjutan:
```typescript
import { optimizePath } from 'svg-path-editor-lib';
optimizePath(parsedPath, {
  removeUselessCommands,         // default `false`
  useShorthands,                 // default `false`
  useHorizontalAndVerticalLines, // default `false`
  useRelativeAbsolute,           // default `false`
  useReverse,                    // default `false`
  removeOrphanDots,              // default `false`, bisa merusak path dengan stroke
  useClosePath,                  // default `false`, bisa merusak path dengan stroke
});
```


### Operasi lokal

Gunakan `parsedPath.path` untuk mendapatkan array dari semua item path.
```typescript
const item = parsedPath.path[0];
```

Sisipkan setelah:
```typescript
// Sisipkan di akhir:
parsedPath.insert(SvgItem.Make(['M', '1', '1']));
// Sisipkan setelah `item`:
parsedPath.insert(SvgItem.Make(['M', '1', '1']), item);
```

Ubah item:
```typescript
item.values[index] = val;
parsedPath.refreshAbsolutePositions();
```

Ubah ke relatif:
```typescript
item.setRelative(true);
```

Ubah ke absolut:
```typescript
item.setRelative(false);
```

Ubah ke tipe lain:
```typescript
parsedPath.changeType(item, 'L');
```

Hapus item:
```typescript
parsedPath.delete(item);
```