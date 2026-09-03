# 通用目录润色任务模板

把下面内容交给任何能够访问文件的 AI，并替换尖括号中的值。该请求不依赖 Claude Code、Codex 或其他特定产品。

```text
请先完整读取：<SKILL_DIR>/SKILL.md，并按其中引用的全部规则执行。

任务模式：polish
输入文件或目录：<INPUT_PATH>
输出目录：<OUTPUT_PATH；留空则使用输入目录旁的“原目录名_polished”>
润色强度：standard
目标语言：<English / 中文 / 保持原语言>
学科：<DISCIPLINE>
目标期刊或会议：<VENUE；未知则写 unspecified>
风格样本目录：<STYLE_SAMPLE_PATH；不用则写 none>
排除项：<不处理的文件、目录或段落；没有则写 none>

要求：
1. 不覆盖源文件，保持相对目录和文件格式。
2. 完整执行 Academic Style、Writing Judgment、Writing Quality Check 和 Semantic Fidelity Check，不省略任何润色规则。
3. 不改变论点、证据强度、引用、数值、公式、术语、表图和交叉引用，不新增事实或文献。
4. 完成后生成 POLISHING_REPORT.md，列出处理、未改、跳过、失败文件及需要作者确认的问题。
```

仅审查不改写时，把 `任务模式` 改成 `audit`。仅生成个人风格画像时，改成 `style-profile` 并填写风格样本目录。需要先建画像再润色时，改成 `polish-with-profile`。
