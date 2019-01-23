``` ini

BenchmarkDotNet=v0.11.3, OS=Windows 10.0.17763.288 (1809/October2018Update/Redstone5)
Intel Core i7-6700HQ CPU 2.60GHz (Skylake), 1 CPU, 8 logical and 4 physical cores
.NET Core SDK=3.0.100-preview-009812
  [Host] : .NET Core 2.2.1 (CoreCLR 4.6.27207.03, CoreFX 4.6.27207.03), 64bit RyuJIT
  Core   : .NET Core 2.2.1 (CoreCLR 4.6.27207.03, CoreFX 4.6.27207.03), 64bit RyuJIT

Job=Core  Runtime=Core  

```
|                                    Method |      N |        Mean |      Error |     StdDev | Ratio | RatioSD |
|------------------------------------------ |------- |------------:|-----------:|-----------:|------:|--------:|
|   **DictContainsKey_String_False_IgnoreCase** |   **1000** |    **57.39 us** |  **0.3320 us** |  **0.2943 us** |  **1.00** |    **0.00** |
| PooledContainsKey_String_False_IgnoreCase |   1000 |    65.09 us |  1.2893 us |  1.6306 us |  1.13 |    0.03 |
|                                           |        |             |            |            |       |         |
|   **DictContainsKey_String_False_IgnoreCase** |  **10000** |   **567.45 us** |  **1.3624 us** |  **1.2078 us** |  **1.00** |    **0.00** |
| PooledContainsKey_String_False_IgnoreCase |  10000 |   607.02 us | 11.7553 us | 16.0907 us |  1.06 |    0.03 |
|                                           |        |             |            |            |       |         |
|   **DictContainsKey_String_False_IgnoreCase** | **100000** | **5,859.31 us** | **19.1169 us** | **16.9466 us** |  **1.00** |    **0.00** |
| PooledContainsKey_String_False_IgnoreCase | 100000 | 7,150.20 us | 48.9513 us | 43.3940 us |  1.22 |    0.01 |