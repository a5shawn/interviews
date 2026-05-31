1. **响应式系统**：
   - **Vue2**（`Object.defineProperty`）：本质是劫持属性访问器。
     - 无法监听对象属性的新增/删除（`Vue.set`/`Vue.delete`）
     - 无法监听数组索引变化
     - 初始化时需递归遍历整个对象树，大对象性能差
   - **Vue3**（`Proxy`）：本质是拦截整个对象的操作行为。
     - 原生支持对象/数组的所有操作
     - 实现懒代理，大幅提升初始化性能
2. **API 设计**：
   - **Vue2（Options API）**：
     - 按data/computed/methods分类。复杂组件中同一业务逻辑分散在不同的选项里，Mixins有命名冲突和来源不透明问题。
   - **Vue3（Composition API + `<script setup>`）**：
     - 按功能/业务逻辑组织代码。逻辑复用通过 Composables 实现
