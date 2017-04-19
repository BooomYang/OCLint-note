# OCLint-note
使用oclint结合xcode做静态代码检验的笔记.
OCLint链接: http://oclint.org
OCLint默认代码规则: http://docs.oclint.org/en/stable/rules/index.html

一.配置
homebrew安装 : (MacOs用户) 
$ brew tap oclint/formulae
$ brew install oclint

更新 :
$ brew update
$ brew upgrade oclint

安装xcpretty:
$ gem install xcpretty

二.使用 
1).分析code并生成compile_commands.json文件

$ xcodebuild analyze | xcpretty -r json-compilation-database -o compile_commands.json

2).用oclint分析json文件并生成报表

$ oclint-json-compilation-database -- -report-type html -o analyzeReport.html
