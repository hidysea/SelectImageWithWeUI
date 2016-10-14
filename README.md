# SelectImageWithDescription
基于微信风格的选择图片并添加描述。

###选择相同文件不显示的问题
使用 input 选择文件时，当选择的文件与前一次选择的完全相同时, 将不会触发 onchange 事件。
因此，每次添加完图片之后 替换一个新的 input。

		// 每次添加完图片之后 替换一个新的 input
        // input 选择的文件与前一次选择的完全相同时, 将不会触发 onchange 事件
        var inputDivHtml='<div class="weui_uploader_input_wrp">'+
                '<input class="weui_uploader_input" id="input" type="file" accept="image/*" multiple="multiple" />'+
                '</div>';
        $("#inputDiv").html(inputDivHtml);