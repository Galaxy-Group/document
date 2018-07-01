# PHP标准规范 

## 说明

良好的编码习惯可以增强应用代码的扩展性和可维护性，严格规范的注释方便自己和后来者阅读，从而高效开发。

## 规范
 * 基本编码规范
   * PHP代码文件 必须 以 <?php 或 <?= 标签开始
   * PHP代码文件 必须 以 不带 BOM 的 UTF-8 编码
   * 全局常量，类中的常量所有字母都必须 大写，单词间用下划线分隔
   * 方法名称 必须 符合 camelCase 式的小写开头驼峰命名规范。
   * 类的命名 必须 遵循 StudlyCaps 大写开头的驼峰命名规范
   * 普通函数和变量以及属性以下划线分隔式命名 $under_score
   * 操作符两边要空格
   * if，foreach等关键字两边要空格，开始中括号在条件同一行   
   
   ```php
   if (！ $var === 1234) {
   } elseif ($var > 1213) {
   } else {
   }
   ```
   
   * 函数和类方法中括号换行
   
   ```php
   function () 
   {
   }
   class ClassName
   {
   }
   ```
   
   * 一定要规范代码缩进一致，保持代码整齐
   * 函数或方法多参数规范
   
   ```php
   $noArgs_longVars = function () use (
        $longVar1,
        $longerVar2,
        $muchLongerVar3
   ) {
   // body
   };
   ```
   
   * 对象方法链式执行时需要每个方法一行，清晰明了
   
   ```php
     $model->select()
           ->where()
           ->asArray()
   ```
   
 * 注释规范 
    ```php
    function foo()
    {
    }
    
    /**
     * 出现非错误性的异常。
     *
     * 例如：使用了被弃用的API、错误地使用了API或者非预想的不必要错误。
     *
     * @param string $message
     * @param array $context
     * @return null | boolean
     */
     function foo2()
     {
         //这是赋初值
         $var = "aaa";
     }   
     ```
 
    * 函数注释。开始要有一个空行， 注释段首先写函数功能，再空行写函数的使用demo或者注意事项
    再空行对参数和返回值做生命，@param + 参数类型 + 参数变量名称，返回值则时 @return + 返回数据类型名称，多种类型时用 | 隔开
    * 普通代码段的注释。统一写在要注释代码的上一行并保持缩减一致，和要注释代码对齐
    
 * 自动加载规范
 * Http规范
 
