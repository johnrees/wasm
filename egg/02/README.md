https://wasdk.github.io/WasmFiddle/

C:
```
#include <math.h>

float getSqrt (float num) {
  return sqrt(num);
}
```

WAST:
```
(module
  (type $FUNCSIG$ff (func (param f32) (result f32)))
  (table 0 anyfunc)
  (memory $0 1)
  (export "memory" (memory $0))
  (export "getSqrt" (func $getSqrt))
  (func $getSqrt (param $0 f32) (result f32)
    (f32.sqrt
      (get_local $0)
    )
  )
)

```
