# hand-coding
한글로 한다 손 코 딩 용 코 드

## sorting

### mergesort

<!-- immutable 원칙 안지킴, index저장하는 변수 만드는게 더 효율적이지만 간편한 코딩을위해  -->
function merge(arrA, arrB) {
  ret = [];
  while(arrA.length !=0 || arrB.length != 0)
    if(arrA.length == 0 || arrA[0] >= arrB[0]) ret.push(arrB.shift());
    else ret.push(arrA.shift());
  return ret;
}

function mergeSort(inputArr) {
  if(inputArr.length < 2) return inputArr;

  return merge(
    mergeSort(inputArr.slice(0, inputArr.length/2)),
    mergeSort(inputArr.slice(inputArr.length/2))
  );
}

## search

## named problem
