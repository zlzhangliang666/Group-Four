# 一城优团 · 全网酒店比价（MVP）

> 本地生活团购跨平台比价原型系统　|　AI 开发企业实习实训项目 4 组

## 在线体验

在线地址：**https://zlzhangliang666.github.io/Group-Four/**

点击上方链接即可直接在浏览器中打开原型（手机端 / 桌面端均可），无需安装任何环境。打开后即为原型首页，可在「首页 / 比价收藏 / 我的订单 / 我的」之间切换体验完整流程。

## 项目简介

日常选购酒店、餐饮、休闲娱乐等本地生活团购套餐时，优惠分散在美团、抖音团购、携程等多个平台，用户需要反复切换 App、手动记录价格，还要逐个比对退款规则、预约要求、节假日加价等使用限制，比价成本很高。

本项目将这些分散的套餐信息做标准化处理，把同一门店在多个平台的套餐聚合到同一页面，以表格形式展示价格、权益、使用限制等关键字段，并按价格、权益、退款灵活性、用户评价等维度自动计算综合性价比评分，自动推荐综合最优套餐。

本项目为课程小组原型项目，**全部使用模拟套餐数据**，仅做信息聚合展示与外部平台的跳转，不涉及下单、支付与券码核销。

## MVP 页面

| 页面 | 文件 | 说明 |
| --- | --- | --- |
| 首页 | `mvp/home.html` | 城市 / 商圈筛选，搜索酒店，同房型多平台价格聚合卡片 |
| 比价收藏 | `mvp/favorites.html` | 收藏的套餐集中查看、再次进入比价、取消收藏 |
| 我的订单 | `mvp/orders.html` | 模拟订单列表与状态展示 |
| 我的 | `mvp/profile.html` | 个人信息与功能入口 |
| 入口页 | `mvp/index.html` | 访问站点根路径时自动跳转到首页 |

## 目录结构

```
Group-Four/
├── docs/
│   └── requirement.md        # 项目需求文档（痛点、业务目标、功能清单、流程、边界）
├── mvp/
│   ├── index.html            # 站点入口，跳转到 home.html
│   ├── home.html             # 首页 / 比价列表
│   ├── favorites.html        # 比价收藏
│   ├── orders.html           # 我的订单
│   └── profile.html          # 我的
├── .github/workflows/
│   └── deploy-pages.yml      # 自动将 mvp/ 发布到 GitHub Pages
└── README.md
```

## 本地预览

方式一：直接双击打开 `mvp/home.html`。

方式二：在 `mvp` 目录下启动静态服务后访问 `http://localhost:8080`：

```bash
python -m http.server 8080
```

## 部署说明

`mvp/` 目录下的页面为纯静态 HTML（TailwindCSS + Iconify 通过 CDN 引入），无需打包构建。向仓库推送代码后，GitHub Actions 工作流 [deploy-pages.yml](.github/workflows/deploy-pages.yml) 会自动把 `mvp/` 目录发布到 GitHub Pages，稍后刷新在线地址即可看到最新原型。

## 协作方式

项目采用 Git + GitHub 协作：需求文档与原型分分支开发，通过 Issue 跟踪任务、Pull Request 评审合并。

## 相关文档

- 需求文档：[docs/requirement.md](docs/requirement.md)
