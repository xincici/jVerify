jVerify
=======

A jQuery based verify component

#### 功能说明

>    简化页面内对输入框值的有效性校验等问题  
>    目前可以支持email,string,int,mobile类型的检测

#### 参数更新
``` javascript
var something = jQuery('selector').jVerify({
    type : string          //期望类型
    ,emptyOk : boolean       //是否可以为空
    ,tipMsg : string        //输入提示信息
    ,emptyMsg : string      //空白的提示信息
    ,minValue : number      //当为int型时所能输入的最小值
    ,maxValue : number      //当为int型时所能输入的最大值
    ,warnMsg : string       //警告信息
    ,maxLength : number     //最大长度
    ,minLength : number     //最小长度
    ,vEvent : event type     //触发校验的事件 默认为keyup
    ,warnElement : Object       //提示信息显示容器
    ,tipMsgInit : boolean       //初始化时是否显示提示信息
    ,callback : function        //随着vEvent事件校验通过时触发的事件
    ,errorback : function       //随着vEvent事件校验不通过时触发的事件
    ,blurback : function        //随着blur事件校验通过时触发的事件
});
```

#### 使用说明

``` javascript
var something = jQuery('selector').jVerify({
    type : string          //期望类型
    ,emptyOk : boolean       //是否可以为空
    ,tipMsg : string        //输入提示信息
    ,emptyMsg : string      //空白的提示信息
    ,minValue : number      //当为int型时所能输入的最小值
    ,maxValue : number      //当为int型时所能输入的最大值
    ,warnMsg : string       //警告信息
    ,maxLength : number     //最大长度
    ,minLength : number     //最小长度
    ,vEvent : event type     //触发校验的事件 默认为keyup
    ,warnElement : Object       //提示信息显示容器
    ,tipMsgInit : boolean       //初始化时是否显示提示信息
});
```

>    提交时可通过校验something.data('status') == 'false'即可得到该输入框值是否符合要求  
>    对于不符合要求的可以直接调用something.showMsg()方法显示警告信息  
>    请参考demo
