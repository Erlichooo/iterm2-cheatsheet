# iTerm2 快捷键完整清单

> 本文档基于本机 iTerm2 实际配置文件整理，非凭记忆。
> **无任何自定义键绑定**，全部为默认值。

---

## 一、菜单栏快捷键

**来源文件：** `/Applications/iTerm.app/Contents/Resources/MainMenu.nib`

**提取命令：**
```bash
# MainMenu.nib 为 NIBArchive v1 二进制格式，ibtool 无法直接解析
# 用 strings 提取可读文本（菜单动作名）
strings /Applications/iTerm.app/Contents/Resources/MainMenu.nib | grep -E "^[a-z][A-Za-z:]+$" | head -100

# 快捷键字符嵌入二进制 values section，需手动反向工程 NIBArchive 格式解析
```

### Cmd 组

| 快捷键 | 功能 |
|--------|------|
| `Cmd+,` | 偏好设置 |
| `Cmd+/` | 高亮光标位置（Find Cursor） |
| `Cmd+0` | 恢复默认字体大小 |
| `Cmd+;` | 自动补全 |
| `Cmd+?` | 帮助 |
| `Cmd++` | 字体变大 |
| `Cmd+-` | 字体变小 |
| `Cmd+[` | 上一个 Pane |
| `Cmd+\` | 显示注释 |
| `Cmd+]` | 下一个 Pane |
| `Cmd+A` | 全选 / 选中上条命令输出 |
| `Cmd+B` | 显示工具栏 |
| `Cmd+C` | 复制 / 进入 Copy Mode |
| `Cmd+D` | 垂直分屏 / 水平分屏 |
| `Cmd+E` | 显示时间戳 / 用选区搜索 |
| `Cmd+Escape` | 缩小 |
| `Cmd+F` | 查找 / 全局查找 |
| `Cmd+G` | 下一个匹配 / 上一个匹配 |
| `Cmd+H` | 隐藏 iTerm2 / 粘贴历史 |
| `Cmd+I` | 编辑会话 / 广播输入到所有 Pane |
| `Cmd+J` | 跳到标记 / 跳到选区 |
| `Cmd+K` | 清空缓冲区 / 清空滚动缓冲区（彻底清除历史） |
| `Cmd+L` | 打开位置 / 折叠行 / 清除到选区起点 |
| `Cmd+M` | 最小化 / 设置标记 |
| `Cmd+N` | 新建窗口 |
| `Cmd+O` | 打开 Profile / 快速打开 |
| `Cmd+Q` | 退出 iTerm2 |
| `Cmd+R` | 重置 |
| `Cmd+S` | 保存选中文字 / 保存窗口排列 |
| `Cmd+T` | 新建标签页 / 全屏显示标签页 |
| `Cmd+U` | 切换透明度 |
| `Cmd+V` | 粘贴 / 粘贴选区 |
| `Cmd+W` | 关闭标签页 / 关闭终端窗口 |
| `Cmd+X` | 剪切 |
| `Cmd+Y` | 历史 / AI 对话 |
| `Cmd+Z` | 撤销 / 重做 |

### Cmd+Shift 组

| 快捷键 | 功能 |
|--------|------|
| `Cmd+Shift+-` | 固定热键窗口 |
| `Cmd+Shift+.` | 显示 Composer |
| `Cmd+Shift+0` | 缩放 |
| `Cmd+Shift+;` | 打开命令历史 |
| `Cmd+Shift+[` | 上一个标签页 |
| `Cmd+Shift+]` | 下一个标签页 |
| `Cmd+Shift+↑` | 上一个标记 |
| `Cmd+Shift+↓` | 下一个标记 |
| `Cmd+Shift+Return` | 最大化当前 Pane |

### Cmd+Opt 组

| 快捷键 | 功能 |
|--------|------|
| `Cmd+Opt+/` | 打开最近目录 |
| `Cmd+Opt+0` | 恢复文字和会话大小 |
| `Cmd+Opt+A` | 下个标记时提醒 |
| `Cmd+Opt+B` | 开始即时回放 / 隐藏会话 |
| `Cmd+Opt+C` | 带样式复制 |
| `Cmd+Opt+E` | 本地渲染选区 |
| `Cmd+Opt+F` | 密码管理器 / 过滤 |
| `Cmd+Opt+H` | 隐藏其他窗口 / 水平分屏 |
| `Cmd+Opt+I` | 广播输入到当前 Tab 所有 Pane |
| `Cmd+Opt+J` | 控制台 |
| `Cmd+Opt+K` | 清除即时回放 |
| `Cmd+Opt+L` | 清除到上一个标记 |
| `Cmd+Opt+M` | 设置命名标记 / 添加注释 |
| `Cmd+Opt+N` | 用当前 Profile 新建窗口 |
| `Cmd+Opt+O` | 打开选区 |
| `Cmd+Opt+R` | 运行 Coprocess |
| `Cmd+Opt+Return` | 选择所有匹配 |
| `Cmd+Opt+S` | 安全键盘输入 / 保存窗口排列 |
| `Cmd+Opt+T` | 用当前 Profile 新建标签页 |
| `Cmd+Opt+V` | 垂直分屏 / 高级粘贴 |
| `Cmd+Opt+W` | 关闭 Tab 内所有 Pane |
| `Cmd+Opt+Y` | 自动命令补全 / AI 解释输出 |
| `Cmd+Opt+Z` | 缩放选区 |
| `Cmd+Opt+↑` | 选择上方 Pane |
| `Cmd+Opt+↓` | 选择下方 Pane |
| `Cmd+Opt+←` | 选择左侧 Pane |
| `Cmd+Opt+→` | 选择右侧 Pane |

### Cmd+Ctrl 组

| 快捷键 | 功能 |
|--------|------|
| `Cmd+Ctrl+D` | 分离（Detach） |
| `Cmd+Ctrl+F` | 切换全屏 |
| `Cmd+Ctrl+N` | 新建 Tmux 窗口 |
| `Cmd+Ctrl+P` | 暂停 Pane |
| `Cmd+Ctrl+T` | 新建 Tmux 标签页 |
| `Cmd+Ctrl+Y` | 打开 AI 聊天 |
| `Cmd+Ctrl+↑` | 向上移动分割线 |
| `Cmd+Ctrl+↓` | 向下移动分割线 |
| `Cmd+Ctrl+←` | 向左移动分割线 |
| `Cmd+Ctrl+→` | 向右移动分割线 |

### Cmd+Shift+Opt 组

| 快捷键 | 功能 |
|--------|------|
| `Cmd+Shift+Opt+[` | 向左移动标签页 |
| `Cmd+Shift+Opt+]` | 向右移动标签页 |
| `Cmd+Shift+Opt+.` | 自动 Composer |
| `Cmd+Shift+Opt+↑` | 上一个注释 |
| `Cmd+Shift+Opt+↓` | 下一个注释 |

### 其他

| 快捷键 | 功能 |
|--------|------|
| `Cmd+Shift+Ctrl+Return` | Dashboard |

---

## 二、全局默认键映射

**来源文件：** `/Applications/iTerm.app/Contents/Resources/DefaultGlobalKeyMap.plist`

**提取命令：**
```bash
plutil -convert xml1 /Applications/iTerm.app/Contents/Resources/DefaultGlobalKeyMap.plist -o -
```

| 快捷键 | 功能 |
|--------|------|
| `Cmd+Home` | 滚动到顶部 |
| `Cmd+End` | 滚动到底部 |
| `Cmd+PageUp` / `Shift+PageUp` | 向上翻页 |
| `Cmd+PageDown` / `Shift+PageDown` | 向下翻页 |
| `Cmd+NumPad↑` | 上滚一行 |
| `Cmd+NumPad↓` | 下滚一行 |
| `Cmd+NumPad←` | 上一个标签页 |
| `Cmd+NumPad→` | 下一个标签页 |
| `Shift+Cmd+NumPad←` | 下一个 Pane |
| `Shift+Cmd+NumPad→` | 上一个 Pane |
| `Ctrl+Shift+Tab` | 切换热键窗口 |

---

## 三、系统级配置

**来源文件：** `~/Library/Preferences/com.googlecode.iterm2.plist`

**提取命令：**
```bash
plutil -convert xml1 ~/Library/Preferences/com.googlecode.iterm2.plist -o - \
  | grep -A3 "Hotkey\|SwitchPaneModifier\|SwitchTabModifier\|SwitchWindowModifier"
```

| 快捷键 | 功能 | 原始值 |
|--------|------|--------|
| `Opt+Space` | 全局热键：显示/隐藏 iTerm2 | `HotkeyChar=32, HotkeyModifiers=524576` |
| `Ctrl+数字` | 切换到第 N 个 Pane | `SwitchPaneModifier=4` |
| `Opt+Ctrl+数字` | 切换到第 N 个标签页 | `SwitchTabModifier=6` |
| —（已禁用） | 切换窗口 | `SwitchWindowModifier=9` |

---

## 四、鼠标 / 触控板手势

**来源文件：** `~/Library/Preferences/com.googlecode.iterm2.plist`（`PointerActions` 字段）

**提取命令：**
```bash
plutil -convert xml1 ~/Library/Preferences/com.googlecode.iterm2.plist -o - \
  | grep -A5 "PointerActions"
```

| 手势 | 功能 |
|------|------|
| 三指左滑 | 上一个标签页 |
| 三指右滑 | 下一个标签页 |
| 三指上滑 | 下一个窗口 |
| 三指下滑 | 上一个窗口 |
| 中键单击 | 粘贴剪贴板 |
| 右键单击 | 右键菜单 |

---

## 五、Copy Mode（Vim 风格）

**来源文件：** `/Applications/iTerm.app/Contents/Resources/iTermCopyModeKeyBindings.dict`

**提取命令：**
```bash
plutil -convert xml1 /Applications/iTerm.app/Contents/Resources/iTermCopyModeKeyBindings.dict -o -
```

> 通过 `Cmd+C`（无选区时）进入 Copy Mode。

| 键 | 功能 |
|----|------|
| `h` / `←` | 左移一字符 |
| `j` / `↓` | 下移一行 |
| `k` / `↑` | 上移一行 |
| `l` / `→` | 右移一字符 |
| `w` / `Tab` | 下一个词 |
| `W` | 下一个大词（WORD） |
| `b` / `Opt+←` | 上一个词 |
| `B` | 上一个大词 |
| `0` | 行首 |
| `^` | 行首非空字符 |
| `$` | 行尾 |
| `g` / `Home` / `Cmd+↑` | 内容顶部 |
| `G` / `End` / `Cmd+↓` | 内容底部 |
| `H` | 可见区域顶部 |
| `M` | 可见区域中间 |
| `L` | 可见区域底部 |
| `Cmd+←` | 移到行首 |
| `Cmd+→` | 移到行尾 |
| `PageUp` / `Ctrl+B` | 向上翻页 |
| `PageDown` / `Ctrl+F` | 向下翻页 |
| `Ctrl+U` | 向上翻半页 |
| `Ctrl+D` | 向下翻半页 |
| `Ctrl+Y` | 向上滚动一行 |
| `Ctrl+E` | 向下滚动一行 |
| `v` / `Space` | 开始字符选择 |
| `V` | 开始行选择 |
| `Ctrl+V` / `Ctrl+Space` | 矩形块选择 |
| `o` | 交换选区端点 |
| `y` / `Ctrl+K` | 复制选区 |
| `[` | 上一个标记 |
| `]` | 下一个标记 |
| `/` | 打开搜索 |
| `1–9` | 重复计数前缀 |
| `q` / `Escape` / `Ctrl+C` | 退出 Copy Mode |

---

## 六、预设键映射（未启用）

**来源文件：** `/Applications/iTerm.app/Contents/Resources/PresetKeyMappings.plist`

**提取命令：**
```bash
plutil -convert xml1 /Applications/iTerm.app/Contents/Resources/PresetKeyMappings.plist -o -
```

> 以下三套预设均**未在本机启用**，需在 Settings → Profiles → Keys → Load Preset 手动加载。

### Natural Text Editing（自然文本编辑）

| 快捷键 | 发送内容 | 效果 |
|--------|----------|------|
| `Cmd+Backspace` | `0x15` | 删除到行首（同 Ctrl+U） |
| `Opt+Backspace` | `ESC+0x7f` | 向后删除一个词 |
| `Opt+←` | ESC seq `b` | 向左移动一个词 |
| `Cmd+←` | `0x01` | 移到行首（同 Ctrl+A） |
| `Opt+→` | ESC seq `f` | 向右移动一个词 |
| `Cmd+→` | `0x05` | 移到行尾（同 Ctrl+E） |
| `Delete(Fwd)` | `0x04` | 删除下一个字符（同 Ctrl+D） |
| `Opt+Delete(Fwd)` | ESC seq `d` | 向前删除一个词 |

### Terminal.app Compatibility（兼容 Terminal.app）

| 快捷键 | 发送内容 |
|--------|----------|
| `Ctrl+Shift+^` | `0x1e`（RS） |
| `Shift+↑/↓` | `[A` / `[B` 标准 ANSI 序列 |
| `Opt+↑/↓` | `\e\e[A` / `\e\e[B` |
| `Ctrl+←/→` | `[1;5D` / `[1;5C` |
| `Opt+←/→` | ESC seq `b` / `f` |
| `Shift+Home/End` | `[H` / `[F` |
| `Ctrl+Home/End` | 滚动到顶部/底部 |
