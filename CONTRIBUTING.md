# 贡献与迭代规则

## 新增提示词

1. 从 `templates/prompt-file-template.md` 复制模板。
2. 放入最匹配的 `prompts/<category>/` 目录。
3. 填写 frontmatter：`title/category/subcategory/source_section/author/version/created/status/tags`。
4. Prompt 正文只放可复制内容，教程链接、效果截图、长案例放到 `references/` 或后续案例目录。
5. 运行：

```bash
python3 scripts/check_repo.py
python3 scripts/generate_catalog.py
```

## 版本规则

- 小修文字、去冗余：`V1.0 -> V1.1`
- 明显改写结构或新增流程：`V1.x -> V2.0`
- 同一提示词不同方向的实验版：新建文件，并在标题中标注用途或模型。

## 评审标准

- 目标清楚：提示词解决的问题明确。
- 可执行：用户知道需要输入什么，模型知道需要输出什么。
- 可迁移：不要把一次性项目细节写死在通用提示词里。
- 可维护：保留版本、标签、适用场景和必要来源信息。
- 风险可控：涉及医疗、法律、金融、未成年人、第三方版权或规避检测等内容时，必须增加来源说明或评审备注。
