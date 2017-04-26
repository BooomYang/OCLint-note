# OCLint-note
##### ps OCLint链接: http://oclint.org

#### `一.配置`
* homebrew安装 : (MacOs用户) <br>
```c
$ brew tap oclint/formulae
$ brew install oclint
```
* 更新 :
```c
$ brew update
$ brew upgrade oclint
```
* 安装xcpretty:
```c
$ gem install xcpretty
```
#### `二.使用`

* 1) 分析code并生成compile_commands.json文件
```c
$ xcodebuild analyze | xcpretty -r json-compilation-database -o compile_commands.json
```
* 2) 用oclint分析json文件并生成报表
```c
$ oclint-json-compilation-database -- -report-type html -o analyzeReport.html
```
