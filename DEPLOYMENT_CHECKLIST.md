# SEAMLESS 网站部署检查清单

## 网站文件结构

```
D:\Job\SeamLess\website\
├── 核心页面
│   ├── seamless-new.html      (主页)
│   ├── partner.html          (合伙人页面)
│   ├── business.html         (商务合作)
│   ├── media.html            (媒体中心)
│   ├── support.html          (技术支持)
│   ├── prod-1.html           (Honda Civic Type R FL5)
│   ├── prod-2.html           (产品2)
│   ├── prod-3.html           (产品3)
│   ├── phil-1.html           (理念1)
│   ├── phil-2.html           (理念2)
│   ├── phil-3.html           (理念3)
│   ├── insp-1.html           (案例1)
│   ├── insp-2.html           (案例2)
│   └── insp-3.html           (案例3)
│
├── 资源文件
│   ├── 4月4日.mp4             (主页视频)
│   ├── design/1.jpg           (产品图片)
│   ├── logo-A.png             (导航logo)
│   ├── logo-C.png             (页面logo)
│   ├── insp-1.png ~ insp-3.png/jpg  (案例图片)
│
└── 旧版本文件 (可忽略)
    ├── wireframe-prototype.html
    ├── wireframe-fixed.html
    └── seamless-new.entry.html
```

## 部署检查项

### 1. 路径检查 ✅
- [x] 视频文件 `hero-video.mp4` 存在 (185MB)
- [x] 产品图片 `design/1.jpg` 存在
- [x] Logo 图片存在 (`logo-A.png`, `logo-C.png`)
- [x] 视频文件名已从 `4月4日.mp4` 改为 `hero-video.mp4`

### 2. 功能检查 ✅
- [x] 主页静音按钮已添加
- [x] Logo 点击滚动到顶部 (smooth scroll)
- [x] 三语言切换 (EN/ZH/JA)
- [x] 合伙人页面已创建

### 3. 页面链接检查

| 页面 | 入口 |
|------|------|
| 主页 | 直接访问 `seamless-new.html` |
| 产品页 | prod-1.html, prod-2.html, prod-3.html |
| 合伙人 | partner.html |
| 理念 | phil-1.html, phil-2.html, phil-3.html |
| 案例 | insp-1.html, insp-2.html, insp-3.html |

## 部署步骤

### 方式一：直接上传 (Cloudflare Pages)

1. **创建 GitHub 仓库**，将 `website` 文件夹内容上传
2. **连接 Cloudflare Pages**：
   - 登录 cloudflare.com → Pages → 创建站点
   - 选择 GitHub 仓库
   - 构建命令留空（纯静态）
   - 输出目录：`/` 
3. **绑定域名**：`seamless.news`

### 方式二：ZIP 打包上传

1. 将 `website` 文件夹打包成 ZIP
2. 在 Cloudflare Pages 直接上传 ZIP 包
3. 绑定域名

## 注意事项

1. **视频文件编码**：确保 `.mp4` 是 web 友好格式 (H.264)
2. **相对路径**：所有链接使用相对路径，无需修改
3. **中文文件名**：建议将 `4月4日.mp4` 重命名为 `hero-video.mp4` 以避免编码问题
4. **字体加载**：Google Fonts 需要网络访问

## 建议操作

1. 将 `4月4日.mp4` 重命名为 `hero-video.mp4` (可选)
2. 删除不需要的旧文件 (wireframe-*.html)
3. 确认所有外链图片/CDN 可访问

---
*整理时间：2026-04-05*