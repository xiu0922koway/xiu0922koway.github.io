# 自定义字体文件夹

## 如何使用自定义字体

1. **准备字体文件**
   - 将您的字体文件（.ttf, .otf, .woff, .woff2 格式）放到这个 `fonts/` 文件夹中
   - 推荐使用 `.woff2` 格式（体积最小，加载最快）
   - 如果没有，`.woff` 或 `.ttf` 格式也可以

2. **修改字体文件名称**
   - 如果您使用的字体文件名不是 `typewriter`，需要修改 `index.html` 中的字体定义
   - 找到 CSS 中的 `@font-face` 规则，修改 `src` 中的文件路径

3. **示例：添加打字机字体**
   
   假设您的字体文件叫 `my-typewriter.ttf`：
   
   ```css
   @font-face {
       font-family: 'Typewriter';
       src: url('fonts/my-typewriter.woff2') format('woff2'),
            url('fonts/my-typewriter.woff') format('woff'),
            url('fonts/my-typewriter.ttf') format('truetype');
       font-weight: normal;
       font-style: normal;
       font-display: swap;
   }
   ```

4. **字体格式说明**
   - `.woff2` - 最新格式，压缩比最高，推荐使用
   - `.woff` - 广泛支持，压缩比较好
   - `.ttf` - 传统格式，文件较大但兼容性最好
   - `.otf` - OpenType 格式，支持高级特性

5. **在线字体转换工具**
   - 如果您的字体文件格式不对，可以使用在线工具转换：
     - [CloudConvert](https://cloudconvert.com/) - 支持多种格式转换
     - [Font Squirrel Webfont Generator](https://www.fontsquirrel.com/tools/webfont-generator)

## 注意事项

- 确保字体文件的路径正确（相对于 `index.html` 的位置）
- 如果有多个字体文件（如粗体、斜体），可以添加多个 `@font-face` 规则
- 自定义字体文件会增加页面加载时间，建议文件大小控制在 500KB 以内
- 某些字体可能不支持中文字符，请确保您使用的字体支持中文显示

## 添加更多自定义字体

如果您想添加更多自定义字体选项：

1. 在 `fonts/` 文件夹中添加字体文件
2. 在 `index.html` 的 CSS 部分添加 `@font-face` 规则
3. 在 `fontConfig` 对象中添加字体配置
4. 在字体选择器 HTML 中添加选项

