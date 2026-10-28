# Design Directions · Recipkg

**为产品任务选择合适的视觉方向，并验证设计结果。**

[标准库](https://github.com/recipkg/standard-library) · [配方清单](RECIPE.md) · [构建要求](BUILD_PROMPT.md) · [验收条件](ACCEPTANCE.md) · [评估方法](EVALUATION.md)

![从软件与依赖整理配方，再交给 Agent 重建](https://raw.githubusercontent.com/recipkg/recipkg/main/assets/recipkg-cover.png)

这份配方根据用户、任务、内容和平台选择视觉方向，覆盖阅读、工作台、服务、沉浸、品牌、原生、数据和 Agent 协作等场景。[Agent 界面合同](AGENT-INTERACTION.md)提供任务、状态与验收案例。它递归依赖设计基础合同；产品应有自己的内容和视觉判断，不应套用一张通用界面模板。

## 使用

在产品配方中声明本仓库的完整 Git 提交作为依赖，并在构建说明中写清适用的界面及验收方式。打包时会收集 `foundation` 的递归材料。具体界面仍须在目标设备和实际状态下验收；打包通过不等于产品设计完成。

```sh
recipe_dir="$(mktemp -d)"
recipkg pack . -o "$recipe_dir/design-directions.recipe.tar.gz"
recipkg check "$recipe_dir/design-directions.recipe.tar.gz"
recipkg build "$recipe_dir/design-directions.recipe.tar.gz" --lang zh-CN --output "$recipe_dir/build.md"
printf '提示词：%s\n' "$recipe_dir/build.md"
```
