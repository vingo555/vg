# vg language specification

vg language is a common computer language and it is not realistic so far. 
the following information is just some of thought about ideal computer language.

some of basic rule for the language should be :

* as easy/simple as possible
* as powerful as possible
* easy to learn and easy to use

## keywork for vg
`
  if else  for   
  return 
  id type sizeof
  nil true false string
`

## data type for vg

     int8  int16, int32 int64, int128, int256, int512
      uint8, uint16, uint64, uint128, uint256, uint512
      char , wchar float, double
      nil, string, wstring
      []  {}

## string defintion

    hello = 'you are welcome to here'
    hello = "you are welcome to here"
    hello = '''you are welcome to here'''

    hello:string = 'hello world'
    hello:wstring = 'hello,world'
    hello:wstring = '你好'

### function defition
+ fnName(argument list) return value {}
+ there may many return value
+ if argument no type declaration which mean template which match different type automatically.
+ no keywork for lambda function 

```c
  add(x:int32 , y: int32) int32 {
    return x + y;
  }
```

no template keyword (type declarition)

template function like 
```c
  add( x, y ) type(x) {
    return x + y ;
  }

  //anonymous function
  fn = (x,y) type(x) {
    return x + y ;
  }

```

## struct definiton
```c
  //4 bytes alignment structure

  struct:4 point {
    x : int32  
    y : int32
  }
  //1 byte alignemnt
  struct:1  coordination {
    top: int64
    left : int64
    right :int64
    botton : int64
  }

  fab(x) type (x)  {
    return x * fab(x - 1)
  }

```

```c
main() int {
   a = 5 
   fn = (a , b ) type (a) { return a + b ; }
   a: int8 = 5;
   str = "youare good"
   hello = 'you are back to "you are """'
   record = [10] ; 

  while( a > 0 ) {
       
  }
  return 0
}

```