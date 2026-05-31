1. **原始类型**：`string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`
2. **特殊类型**：
   - `any`：关闭类型检查（项目中应通过 ESLint 严格禁止）
   - `unknown`：类型安全的 `any`
   - `void`：表示函数没有返回值
   - `never`：表示永远不会正常结束（如抛出异常、死循环）
3. **复合类型**：Array, Tuple（元组）, Enum（枚举）, Union（联合 `｜`）, Intersection（交叉 `&`）
4. **高级类型**：
   - **字面量类型**
   - **类型推导**
   - **泛型**
   - **条件类型**
   - **映射类型**
   - **关键字操作符**：
     - `keyof`：获取对象键的联合类型
     - `typeof`：从值反推类型
     - `infer`：在条件类型中**提取**子类型
     - `as`：重映射
5. **内置工具类型**：
   - `Partial<T>` / `Required<T>`：可选/必选转换
   - `Pick<T, K>` / `Omit<T, K>`：选取/剔除属性
   - `Record<K, V>`：构造键值对类型
   - `Extract<T, U>` / `Exclude<T, U>`：联合类型过滤
   - `ReturnType<T>` / `Parameters<T>`：函数签名提取
   - `Awaited<T>`：解包 Promise（TS 4.5+）
