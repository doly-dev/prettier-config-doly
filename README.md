# prettier-config-doly

prettier的共享配置

## 安装

```bash
npm install --save-dev prettier-config-doly
```
这只是一个可共享的配置。它不会安装Prettier，Standard，ESLint或工具链的任何其他部分。

## 使用

package.json使用prettier属性引用它：

```json
{
  "name": "your-projects-name",
  "prettier": "prettier-config-doly",
  "devDependencies" : {
     "prettier-config-doly": "0.0.1-alpha.0"
  }
}
```


## 配置覆盖

prettier使用了`eslint`式覆盖格式。这允许您将配置应用于特定文件。

JSON：

```json
{
  "semi": false,
  "overrides": [
    {
      "files": ".prettierrc",
      "options": { "parser": "json" }
    }
  ]
}
```

YAML：

```yaml
semi: false
overrides:
  - files: ".prettierrc"
    options:
      parser: "json"
```

## License

MIT  license

MIT