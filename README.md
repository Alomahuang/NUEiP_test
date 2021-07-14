# NUEiP_test

##1
======
```javascript
// 繼承：物件能夠繼承一個類別的屬性與方法，也就是物件的抽象
class 交通工具{
  constructor(種類, 車輪數) {
    this.種類 = 種類;
    this.車輪數 = 車輪數
  }

  showTiresAmount() {
    return this.種類 + '有車輪數：' + this.車輪數;
  }
}
var car=new 交通工具("汽車",4)
var scooter=new 交通工具("機車",2)
//此時汽車是 交通工具類別的一個物件，並且擁有種類與車輪數的屬性，以及showTiresAmount方法
// 介面：不同類別能繼承的方法，也就是對方法的抽象
// 因js並沒有介面的使用，以文字解說：如果今天有一個介面叫做加速前進，交通工具類別可以繼承此介面；另一個類別「動物」也能夠繼承此介面，並且實作。
```
##2
======

```javascript
let str="人易科技:上 機 測 驗 - 演算法"
//1. 
let answer=str.replace(":","：")
//2. 
let answer=str.replaceAll(" ","").replace("-"," - ")
//3. 
let answer=str.slice(0,x.indexOf("-"))
```

##3
======

```javascript
let num_arr=[0,1,2,3,4,5,6,7,8,9]
//1.
let odd_amount=0
let even_amount=0
for (let i=0;i<num_arr.length;i++){
  if(num_arr[i]%2===0){
    odd_amount=odd_amount+num_arr[i]
} else{
    even_amount=even_amount+num_arr[i]
}
}
let answer=odd_amount-even_amount
//2.
let odd_num=[]
let even_num=[]
for (let i=0;i<num_arr.length;i++){
  if(num_arr[i]%2===0){
    odd_num.push(num_arr[i])
  } else{
    even_num.push(num_arr[i])
  }
}
```

##4
======
```javascript
function sortArray(arr) {
  var temp = [];
    if (Array.isArray(arr)) {
      for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr.length; j++) {
          if (arr[i] < arr[j]) {
            temp = arr[j];
            arr[j] = arr[i];
            arr[i] = temp;
        }
      }
    }
    return arr;
  }
}
sortArray([2, 6, 0, 4, 3, 4, 3, 5, 9, 6, 12, 43, 6])
```
##5
======
```javascript
var x=[77,5,5,22,13,55,97,4,796,1,0,9]
var y=[0,1,2,3,4,5,6,7,8,9]
//交集
x.filter(i => y.indexOf(i)>0);
//聯集 
x.concat(y)
[...new Set(x.concat(y))]
//差集 
x.filter(i => y.indexOf(i)<0);
//此語法並非現成函式取交集聯集與差集；若要純使用for迴圈等基礎方法，請再告知。
```
