# hand-coding
한글로 한다 손 코 딩 용 코 드

## sorting

### mergesort

<!-- 추가 최적화 배열의길이가 0면 바로 합치기 -->
<!-- 각 arr 별 index 가르키rl  -->
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

### TSP(boj)
