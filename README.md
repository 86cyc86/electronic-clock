# electronic-clock
# use html and javascript

< !DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd" >
 < html xmlns = "http://www.w3.org/1999/xhtml" >
	 < head >
	 < meta http - equiv = "Content-Type" content = "text/html; charset=utf-8" /  >
	 < title > 电子时钟 <  / title >
	 < script >
	window.onload = function () {
	showTime();
}
function checkTime(i) {
	if (i < 10) {
		i = "0" + i;
	}
	return i;
}
function showTime() {
	var myDate = new Date();
	var year = myDate.getFullYear();
	var month = myDate.getMonth() + 1;
	var date = myDate.getDate();
	var day = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
	var hour = myDate.getHours();
	var minute = myDate.getMinutes();
	minute = checkTime(minute);
	var second = myDate.getSeconds();
	second = checkTime(second);
	document.getElementById("show").innerHTML = year + '年' + month + '月' + date + '日' + day[myDate.getDay()] + hour + ':' + minute + ':' + second;
	setTimeout(showTime, 1000);
}
 <  / script >
 <  / head >
 < body >
 < div id = "show" >  <  / div >
	 <  / body >
	<  / html >
