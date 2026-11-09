# financial-mirror

## 用途
用于课程教学的理财产品文本风险识别与合规质检。

## 文件
SKILL.md：分析规则与输出模板。
test_cases/case_01.txt 至 case_20.txt：教学合成测试输入（case_01–case_10 为第一版，case_11–case_20 为扩展批次）。
results/case_11_report.txt 至 case_20_report.txt：扩展批次按 SKILL.md 六步工作流生成的体检报告。
results/financial-mirror-calibration-results.xlsx：案例库与运行结果汇总表。

## 运行
1. 在支持 Skill 的 Kimi 或 Claude 环境导入 financial-mirror。
2. 若平台不支持导入，在会话中提供完整 SKILL.md。
3. 输入一个案例全文，要求严格按模板输出体检报告。
4. 对照案例预期触发点检查证据、评分、缺失信息和边界声明。

## 复现验收
case_01 应识别保本保息、绝对化背书、个人账户收款和资产缺失。
case_10、case_16 作为对照，不应仅因收益或专业术语被误判为极高风险。
任何外部事实补写、无原文风险结论或缺少复核清单均记为失败。

## 边界
不处理未匿名化个人材料，不调用隐含数据库，不输出投资或法律结论。
