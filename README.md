# Excel 项目匹配统计系统

一个用于匹配两个 Excel 表并展示统计结果的 Web 应用。

## 功能特点

- 上传两个 Excel 文件进行项目匹配
- 以文件1的"系统项目名字"匹配文件2的"项目名称"
- 统计已调平（"是"）和未调平（"否"）的项目数量
- 按"所属地区公司/子公司"展示柱状图
- 导出 PDF 报告
- 支持 .xlsx、.xls、.csv 格式

## 技术栈

- HTML5 + CSS3
- Bootstrap 5
- SheetJS (xlsx) - Excel 文件处理
- Chart.js - 柱状图
- html2canvas + jsPDF - PDF 导出

## 本地运行

```bash
# 方式1：使用 Python
python3 -m http.server 8000

# 方式2：使用 Node.js
npx serve .

# 方式3：直接用浏览器打开 index.html
```

然后访问 `http://localhost:8000`

## 部署到 Cloudflare Pages

1. 登录 Cloudflare Dashboard
2. 进入 Workers & Pages → Create application → Pages → Connect to Git
3. 选择你的 GitHub 仓库
4. 构建配置：
   - Build command: 留空
   - Build output directory: `/` 或 `.`
5. 点击 Save and Deploy

## 文件结构

- `index.html` - 主页面（包含所有代码）
- `README.md` - 项目说明

## 使用方法

1. 上传第一个文件（UAT测试项目和人员收集表）
2. 上传第二个文件（2026年06月月度版）
3. 点击"开始匹配统计"
4. 查看统计结果和柱状图
5. 点击"导出PDF报告"下载报告
