# Cycles:

1) a.ts imports `default` from sub/index.ts which imports a.ts
2) sub/index.ts imports `default` from a.ts which imports sub/index.ts 
3) sub/c.ts imports `e` from sub/d.ts which imports sub/c.ts
4) sub/d.ts imports `c` from sub/c.ts which imports sub/d.ts
5) sub/c.ts imports `f` from sub/sub/f.ts which imports sub/index.ts which imports sub/c.ts
6) sub/sub/f.ts imports `d` from sub/index.ts which imports sub/c.ts which imports sub/sub/f.ts
7) sub/index.ts imports `c` from sub/c.ts which imports sub/sub/f.ts which imports /sub/index.ts