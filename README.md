# jquery.geolocation [![spm version](http://spmjs.io/badge/jquery.geolocation)](http://spmjs.io/package/jquery.geolocation)

AUTHOR WEBSITE: [http://ydr.me/](http://ydr.me/)

jquery.geolocation 获取地理位置

**五星提示：当前脚本未作优化、未完工，请勿用在生产环境**

__IT IS [A SPM PACKAGE](http://spmjs.io/package/jquery.geolocation).__





#USAGE
```
var $ = require('jquery');
require('jquery.geolocation')($);

// 1. get current position
$.geolocation("get",{...});

// 2. watch position
$.geolocation("watch",{...});

// 3. clear
$.geolocation("clear",watchId);
```




#OPTIONS
```
$.fn.validate.defaults = {
    // onsuccess回调
    // 参考：http://www.w3.org/TR/geolocation-API/#position
    // 参数1： latitude （纬度，单位°）
    // 参数2： longitude （经度，单位°）
    // 参数3： altitude （高度，单位m）
    // 参数4： accuracy （精度，单位m）
    // 参数5： altitudeAccuracy （高精度，单位m）
    // 参数6： heading （角度，[0,360)）
    // 参数7： speed （速度，单位m/s）
    onsuccess: function () {},

    // onerror回调
    // 参考：http://www.w3.org/TR/geolocation-API/#position-error
    // 参数1：code
    // 参数1值1：用户已禁止共享地理位置信息
    // 参数1值2：地理位置信息不可用
    // 参数1值3：地理位置信息获取超时
    onerror: function () {},
    // 参考：http://www.w3.org/TR/geolocation-API/#position-options
    
    options: {
        // 是否启用高精度请求，将开启GPS设备
        enableHighAccuracy: true,
        // 超时，1000ms
        timeout: 1000,
        // 有效期，60*60*1000ms
        maximumAge: 3600000
    }
};
```
