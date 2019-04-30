# mobileDatePicker
基于移动端的时间控件，可自定义时间类型（年、月、日、时）

# 使用步骤

## 1、引入js

```js
<script src="mobile/js/datePicker.js"></script>
```

## 2、html

```html
<input type="text" id="day">
```

## 3、js

```js
var calendarDay = new datePicker();
    calendarDay.init({
        'trigger': '#day', /*按钮选择器，用于触发弹出插件*/
        'type': 'date',/*模式：date日期；datetime日期时间；time时间；ym年月；y年；*/
        'minDate':'1900-1-1',/*最小日期*/
        'maxDate':$scope.today,/*最大日期*/
        'onSubmit':function(){/*确认时触发事件*/
            $scope.today = calendarDay.value;
        },
        'onClose':function(){/*取消时触发事件*/
        }
    });
```

