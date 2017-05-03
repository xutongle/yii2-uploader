## 1.安装  
```
composer require yidashi/yii2-uploader:"*"
```
## 2.使用  
>直接使用
  
```
<?= \yidashi\markdown\Markdown::widget(['name' => 'xxx', 'language' => 'zh'])?>
```
>或者在activeForm里使用
  
```
<?= $form->field($model,'attributeName')->widget('yidashi\markdown\Markdown',['language' => 'zh']); ?>
```
语言参数language默认就是zh，可以不提供

如果需要上传图片功能,加`useUploadImage => true`,此功能依赖 `yidashi/yii2-webuploader`,见[https://github.com/yidashi/yii2-webuploader](https://github.com/yidashi/yii2-webuploader)

## 3.解析

```
<?= yii\helpers\Markdown::process($content, 'gfm')?>
```
