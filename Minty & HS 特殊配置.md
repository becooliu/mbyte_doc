## www.afibel.com 这个store 应用一个可用code 后，更新Dom前约有几秒钟 total/subtotal/Shipping_fee/discount 等都不可见，插件获取的值都为0
解决办法：里面的选择的元素全部可见之后才会开始应用code； nodes_activation_required 配置的值是一个selector list
> minty 增加`nodes_activation_required`: ["要正常取值的 selector"]

## Minty 配置项 executor_tab_policy
有以下几个选项：
”ui_tab“  （在当前tab进行测试）
”background_tab“	（在background tab中进行测试）
不写或者”by_code_apply_method“ (默认值。默认apply_code_type为form时，在background进行测试；apply_code_type为ajax时在当前tab进行测试）