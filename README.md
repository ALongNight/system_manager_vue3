# system_manager_vue3
初始化项目
pnpm create vite

使用eslint校验插件
1.安装eslint依赖
pnpm i eslint -D
2.初始化eslint配置
npx eslint --init
3.安装eslint指令
pnpm install -D eslint-plugin-import eslint-plugin-vue eslint-plugin-node eslint-plugin-prettier eslint-config-prettier eslint-plugin-node @babel/eslint-parser

添加.eslintignore文件
dist
node_modules

在package.json文件中添加指令
{
  "script": {
      "lint": "eslint src",
      "fix": "eslint src --fix"
  }
}

二.配置pretter

1.安装依赖包
pnpm install -D eslint-plugin-prettier prettier eslint-config-prettier
2.prettierrc.json 添加规则
{
  "singleQuote": true,
  "semi": false,
  "bracketSpacing": true,
  "htmlWhitespaceSensitivity": "ignore",
  "endOfLine": "auto",
  "trailingComma": "all",
  "tabWidth": 2
}
3.创建.prettierignore忽略文件
  dist
  node_modules

三、配置stylelint
stylelint为css的lint工具，可以格式化css代码，检查css语法错误和不合理写法，指定css书写顺序。
项目中使用scss作为预处理器，安装一下依赖：
pnpm add sass sass-loader stylelint postcss postcss-scss postcss-html stylelint-config-prettier stylelint-config-recess-order stylelint-config-recommended-scss stylelint-config-standard stylelint-config-standard-vue stylelint-scss stylelint-order stylelint-config-standard-scss -D
