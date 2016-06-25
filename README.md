
# JS编写代码规范<br/>
  1. 对于业务插件及功能插件需要编写注释；可以如下格式：<br/>
     /**<br/>
      @fileoverview 测试列子(对插件的用途说明)<br/>
      @author 空智<tu.genhua@tongbanjie.com><br/>
      @module TestB<br/>
      @version 1.0.0<br/>
      @date 2016-06-25<br/>
     */<br/>

  2. 对于单个的方法或者函数可以如下编写注释；格式如下：<br/>
     /**<br/>
      @fileoverview (方法用途的说明)<br/>
      @param {type} 参数字段 字段的说明<br/>
      @public 或 @private -- (代表该方法是公有的还是私有的)<br/>
      @return {type} obj 返回类型的说明<br/>
     */ <br/>


# 对代码生成文档，使用gulp-jsdoc;<br/>
  具体可以看git上的文档： https://github.com/jsBoot/gulp-jsdoc<br/>
  简单的gulp-jsdoc打包如下：<br/>
  var gulp = require('gulp'),<br/>
      jsdoc = require("gulp-jsdoc");<br/>

  gulp.task('generate', function(){<br/>
       return gulp.src("./src/js/*.js")<br/>
              .pipe(jsdoc('./doc'))<br/>
  });<br/>
  gulp.task('watch', function(){<br/>
       gulp.watch('./src/js/*.js', ['generate']);<br/>
  });<br/>
  gulp.task('default', ['generate']);<br/>

  
