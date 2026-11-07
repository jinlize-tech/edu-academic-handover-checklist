# G5/G9 产品修改记录

- 产品编号：$(@{number=55; product_id=JLZ-EDU-SK-045; chinese_name=教务交接清单; english_name=Academic Handover Checklist; repository_name=edu-academic-handover-checklist; repository_url=https://github.com/jinlize-tech/edu-academic-handover-checklist; product_type=Skill; category_code=04; category=04 教务运营中心; description=教务工作交接清单。; target_users=System.Object[]; core_input=交接岗位、在办事项、班级/学生概况、资料位置、风险和截止时间; main_output=交接清单、责任人、状态、风险、验收签名和缺失资料表; product_risk=敏感资料过度转移或遗漏关键事项; dedup_label=存在部分功能交叉; dedup_note=与教务交接审计区别：本产品编制交接清单；审计核查交接是否达标。; development_status=Planned / 待研发; license=Apache-2.0; spec_version=1.0.0; workbuddy_status=PLANNED_FOR_WORKBUDDY}.product_id)
- 产品名称：教务交接清单
- 基线：EDUCATION_BASELINE_V1.0.0
- 基线提交：$BaselineCommit
- 原版本：1.0.0
- 新版本：1.0.1

## 本次修改

1. 强化产品专属执行流程、输入核对和输出验收规则。
2. 新增 scripts/validate_input.js，实际检查必填字段、冲突、未确认数据和敏感信息。
3. 新增正常、缺失、冲突、敏感信息和非法JSON场景输入。
4. 测试升级为 T1–T7 分层并保存逐项检查结果。
5. 安装包加入 Apache-2.0 LICENSE 和 THIRD_PARTY_NOTICES.md。
6. 安装包升级为 1.0.1，加入许可证、第三方声明和输入校验脚本，保留 1.0.0 ZIP。
7. 按本产品冻结规格补充专属处理规则、输入到成果的核对矩阵和去重边界。

## 产品专属增强

- 核心任务：教务工作交接清单。
- 主要风险：敏感资料过度转移或遗漏关键事项
- 去重边界：与教务交接审计区别：本产品编制交接清单；审计核查交接是否达标。

- 先提取班级、教师、教室、时间、学生约束和硬性规则，再生成排程草案。
- 硬冲突不得被软约束覆盖；无法消解时列出冲突、影响和升级责任人。
- 所有变更保留原状态、目标状态、生效时间和回退方式。
- 正式课表、考勤和审批结果必须由有权限人员确认后生效。

## 运行边界

- 本地模型行为：NOT_RUNTIME_VERIFIED
- WorkBuddy平台验证：WORKBUDDY_VALIDATION_NOT_IN_SCOPE
- 本轮不执行上传、安装、审核或正式发布。
