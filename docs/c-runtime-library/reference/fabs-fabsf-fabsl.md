---
title: "fabs, fabsf, fabsl"
description: "API reference for fabs, fabsf, and fabsl; which calculate the absolute value of a floating-point value."
ms.date: "08/31/2020"
api_name: ["fabsf", "fabs", "fabsl", "_o_fabs"]
api_location: ["msvcrt.dll", "msvcr80.dll", "msvcr90.dll", "msvcr100.dll", "msvcr100_clr0400.dll", "msvcr110.dll", "msvcr110_clr0400.dll", "msvcr120.dll", "msvcr120_clr0400.dll", "ucrtbase.dll", "api-ms-win-crt-math-l1-1-0.dll", "api-ms-win-crt-private-l1-1-0.dll"]
api_type: ["DLLExport"]
topic_type: ["apiref"]
f1_keywords: ["fabs", "fabsf", "fabsl", "math\fabs", "math\fabsf", "math\fabsl"]
helpviewer_keywords: ["absolute values", "fabsf function", "calculating absolute values", "fabs function", "fabsl function"]
ms.assetid: 23bca210-f408-4f5e-b46b-0ccaaec31e36
---
# fabs, fabsf, fabsl

Calculates the absolute value of the floating-point argument.

## Syntax

```C
double fabs(
   double x
);
float fabs(
   float x
); // C++ only
long double fabs(
   long double x
); // C++ only
float fabsf(
   float x
);
long double fabsl(
   long double x
);

#define fabs(X) // Requires C11 or higher
```

### Parameters

*x*\
Floating-point value.

## Return Value

The **fabs** functions return the absolute value of the argument *x*. There's no error return.

|Input|SEH Exception|Matherr Exception|
|-----------|-------------------|-----------------------|
|± QNAN,IND|none|_DOMAIN|

## Remarks

C++ allows overloading, so you can call overloads of **fabs** if you include the \<cmath> header. In a C program, unless you're using the \<tgmath.h> macro to call this function, **fabs** always takes and returns a **`double`**.

If you use the \<tgmath.h> `fabs()` macro, the type of the argument determines which version of the function is selected. See [Type-generic math](../../c-runtime-library/tgmath.md) for details.

By default, this function's global state is scoped to the application. To change this, see [Global state in the CRT](../global-state.md).

## Requirements

|Function|Required C header|Required C++ header|
|--------------|-----------------------|---------------------------|
|**fabs**, **fabsf**, **fabsl**|\<math.h>|\<cmath> or \<math.h>|
|**fabs** macro | \<tgmath.h> ||

For additional compatibility information, see [Compatibility](../../c-runtime-library/compatibility.md).

## Example

See the example for [abs](abs-labs-llabs-abs64.md).

## See also

[Floating-Point Support](../../c-runtime-library/floating-point-support.md)<br/>
[abs, labs, llabs, _abs64](abs-labs-llabs-abs64.md)<br/>
[_cabs](cabs.md)<br/>
