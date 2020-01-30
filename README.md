## 指令：指令 (Directives) 是带有 v- 前缀的特殊特性。
* v-model：双向绑定值  【v-model="msg"】
* v-once：只渲染一次，包含字标签  【<p v-once>msg：{{msg}}</p>】
* v-html：将数据当做html加载  【v-html="msg"】
* v-bind：绑定html属性   【v-bind:checked="isChecked"】 简写 【:checked="isChecked"】
* v-on：监听事件 【v-on:click="handleClick"】简写【@click="handleClick"】； 支持动态参数【v-on:[event]="handleClick"】。
```
事件修饰符：
.stop(阻止单击事件继续传播)
.prevent（阻止事件默认行为）
.capture（添加事件监听器时使用事件捕获模式）
.self（只当在 event.target 是当前元素自身时触发处理函数 ）
.once（点击事件将只会触发一次）
.passive（滚动事件的默认行为 (即滚动行为) 将会立即触发 ）
example：v-on:click.stop="handleClick"

按键修饰符：
.enter
.tab
.delete (捕获“删除”和“退格”键)
.esc
.space
.up
.down
.left
.right
example：v-on:keyup.enter="alert('你按了enter,确定输入完毕？')"   or   v-on:keyup.13="alert('你按了enter,确定输入完毕？')"

系统特定的组合功能键：如 ctrl+c 、ctrl+v 。可以用如下修饰符来实现仅在按下相应按键时才触发鼠标或键盘事件的监听器。
.ctrl
.alt
.shift
.meta
@click.ctrl="alert('你同时按了鼠标点击和ctrl')"

exact：精确按键
@click.ctrl="alert('你不单单只按了鼠标左键和 Ctrl键，同时按其他键我也可以触发')"
@click.ctrl.exact="alert('你只按ctrl键+鼠标左键，才能触发我')"

鼠标按钮修饰符：
@click.left="alert('你按了鼠标左击键')"
@click.middle="alert('你按了鼠标滚轮')"
@click.right="alert('你按了鼠标右击键')"

```