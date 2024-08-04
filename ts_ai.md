## 使用AI助手帮助你学习

有科学上网条件下目前推荐使用[ChatGPT 4o](https://chat.openai.com)版本。墙内可以用[Doubao](https://doubao.com)等替代。

## Win 11 + VS Code

win11配合vscode 如何配置ts开发环境
以下是在 Windows 11 系统中配合 Visual Studio Code（简称 VS Code）配置 TypeScript（简称 TS）开发环境的步骤：

### 安装 Node.js
访问 Node.js 官方网站（https://nodejs.org/）。
下载适合 Windows 11 的安装包并运行安装程序。
在安装过程中，建议选择默认设置，安装完成后，在命令提示符或 PowerShell 中输入 node -v 和 npm -v 来验证安装是否成功。

### 安装 TypeScript
打开命令提示符或 PowerShell，输入 npm install -g typescript 来全局安装 TypeScript。
配置 VS Code
打开 VS Code。
安装 TypeScript 扩展插件，在扩展商店中搜索 "TypeScript" 并安装。

### 创建项目文件夹
在您喜欢的位置创建一个新的文件夹来存放您的 TypeScript 项目。
初始化 TypeScript 项目
在命令提示符或 PowerShell 中，切换到您创建的项目文件夹，输入 tsc --init 来初始化 TypeScript 配置文件 tsconfig.json 。
编写和运行 TypeScript 代码
在项目文件夹中创建一个 .ts 文件，例如 index.ts 。

### 编写您的 TypeScript 代码。
要编译 TypeScript 代码为 JavaScript，在命令提示符或 PowerShell 中输入 tsc index.ts ，这将生成对应的 .js 文件。
例如，如果您的 index.ts 文件中有以下代码：

```typescript
function sayHello(name: string) {
    console.log(`Hello, ${name}!`);
}

sayHello('World');
```

编译后，会生成相应的 index.js 文件，您可以在支持 JavaScript 的环境中运行该文件。
```sh
node index.js
```

### 不编译情况下测试TS代码
为了方便也可以使用ts-node在不把ts文件编译成js文件情况下测试代码。
执行下面代码安装ts-node
```sh
npm install -D ts-node
```
这会生成一个package.json以及package-lock.json
打开package.json，添加一个script脚本，方便执行
```json
{
  "scripts":{
    "dev":"ts-node index.ts"
  },
  "devDependencies": {
    "ts-node": "^10.9.2"
  }
}
```
执行run dev测试index.ts中的代码
```sh
npm run dev
```

### 安装vscode中的AI开发助手
在vscode的插件中，搜索codeium点击install，可以帮助你安装一个智能AI助手，可以帮助你学习。
