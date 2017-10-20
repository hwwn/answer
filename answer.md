## Q1
function toGuess(val, num) {
    if(val < num) {
        console.log("Lower than my number");
    }else if(val > num) {
        console.log("Higher than my number");
    }else if(Math.abs(val-num)===1){
        console.log("You are very close");
    }
}


## Q2
for the importance in css:
valise < class < id
and closer to the text is more important
so seems there is no #black id,
the span will take the p and class (.note-this):
{
    font-size: 2.5em;
    font-weight: bolder;
    color: blue;
    background: yellow;
}


## Q3
function averageScore(scores) {
    for(var i = 0; i<scores.length; i++){
        var total += scores[i].score;
        return (total/scores.lenght);
    }
} 

## Q4
from 8 am to 10 pm there are 14 hours

1. so if for average, a song is 4 minutes

2. for every hour in the day, the MC or DJ will speak almost 30 minutes

3. for the rest 30 mintues in every hour, there will be 10 minutes for the advertisements

4. so in each hour, there will be almost 20 minutes for the songs

5. so for this question: 

   20 / 4 * 14 = 70 songs (from 8am to 10pm)



## Q5
// this is a poll function which makes the checkStatus(function return only ture or false), cb a callback function as the two.
// running checkStatus for an interval as long as it return false.
// Everytime the given function returns false, the interval length should be increasedby 1.5 times, and it starts from  second.
// When checkStatus return ture, the poll function calls callback and return.

function poll(checkStatus, cb){
  var statusBoolean = false ; 
  var timeInterval = 1000;
  innerFunction(statusBoolean,timeInterval,cb);
}

function innerFunction(statusBoolean,timeInterval,cb){
  setTimeout(function(){
    statusBoolean = checkStatus();
    if(statusBoolean){
        cb();
    }else{
        innerFunction(statusBoolean,timeInterval*1.5,cb);
    }
  },timeInterval);
}


## Q6

Promise is a new in ES6
there are three states: pending, fulfilled, rehjected 

I know just it is for asynchronous.

if asynchronous is success, the state will from pending to resolved

if asynchronous is fail, the state will from pending to rejected

I know just a little about it, like this:

var promise = new Promise(function(resolve, reject)) {
    if(true) {
        resolve(value);
    }else{
        reject(error);
    }
});
