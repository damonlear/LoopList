# LoopList

----
### Don't Index Out Of Bounds ArrayList From get object value
### 不会索引越界的arraylist

## java.util.LoopArrayList
## 循环取值Arraylist

    when get_index > list.size And get_index = index % list.size
    
## java.util.LastArrayList
## 越界取最后一个值的ArrayList

    when get_index > list.size And get_index = last_index = list.size -1


## How To Use

   	allprojects {
   		repositories {
   			...
   			maven { url 'https://jitpack.io' }
   		}
   	}
   
	dependencies {
        implementation 'com.github.damonlear:LoopList:1.0.0
	}
	
# How To Code

    List<String> list = new LoopArrayList<>();
    list.add("1");
    list.add("2");
    list.add("3");
    for(int i=0;i<100;i++){
        //It is all right
        list.get(i);
    }
    