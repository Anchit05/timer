//In this I have searched for the font-family for timer-name, opacity property,font-weight and box-shadow.
var current;
var getFinalDate;
var getEventDate = function(){
    //Here you can enter custom input from user
    return "09-30-2015 23:59:59";
};
var getMilliSec = function(){
    var currentDate = new Date().getTime();
    getFinalDate = new Date(getEventDate()).getTime();
    var remTime = getFinalDate - currentDate;
    return (remTime/1000);
};
var getSec = getMilliSec();
var months = ["January", "Feburary", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];

var counter = function(){
    getSec = getSec -1;
    updateCounter();
    checkEvent();
};

var getString = function(){
    current = new Date();
    var month = months[current.getMonth()];
    var day = current.getDate();
    var year = current.getFullYear();
    return month + " " + day + ", " + year;
};

var checkEvent = function(){
    if (current.getTime() >= getFinalDate) {
      clearInterval(timer);
    }  
  };

var checkDate = function(common){
    if (common < 10){
        common = "0" + common;
    }
    else{
    }
    return common;
};

var updateCounter = function(){
    var seconds = Math.floor(getSec%60),
        minutes = Math.floor(getSec/60)%60,
        hours = Math.floor(getSec/(60*60))%24,
        days = Math.floor(getSec/(24*60*60))%31;
    $('#days').html(checkDate(days));
    $('#hours').html(checkDate(hours));
    $('#minutes').html(checkDate(minutes));
    $('#seconds').html(checkDate(seconds));
    $('#current').html(getString());
};
var timer = setInterval(counter,1000);
