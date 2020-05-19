# VPP流表

## VPP流表原理


## 命令详解

1. classify table

```
  classify table 
            [miss-next|l2-miss_next|acl-miss-next <next_index>]
            mask <mask-value> 
            buckets <nn> 
            [skip <n>] 
            [match <n>]
            [current-data-flag <n>] 
            [current-data-offset <n>] 
            [table <n>]
            [memory-size <nn>[M][G]] 
            [next-table <n>]
            [del] 
            [del-chain]
```