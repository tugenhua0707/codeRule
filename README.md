
# JS编写代码规范
  1. 对于业务插件及功能插件需要编写注释；可以如下格式：
     /**
      @fileoverview 测试列子(对插件的用途说明)
      @author 空智<tu.genhua@tongbanjie.com>
      @module TestB
      @version 1.0.0
      @date 2016-06-25
     */

  2. 对于单个的方法或者函数可以如下编写注释；格式如下：
     /**
      @fileoverview (方法用途的说明)
      @param {type} 参数字段 字段的说明
      @public 或 @private -- (代表该方法是公有的还是私有的)
      @return {type} obj 返回类型的说明
     */ 


# 对代码生成文档，使用gulp-jsdoc;
  具体可以看git上的文档： https://github.com/jsBoot/gulp-jsdoc
  简单的gulp-jsdoc打包如下：
  var gulp = require('gulp'),
      jsdoc = require("gulp-jsdoc");

  gulp.task('generate', function(){
       return gulp.src("./src/js/*.js")
              .pipe(jsdoc('./doc'))
  });
  gulp.task('watch', function(){
       gulp.watch('./src/js/*.js', ['generate']);
  });
  gulp.task('default', ['generate']);

  
