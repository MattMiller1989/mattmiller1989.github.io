---
layout: post
title:  "Blast From The Past"
date:   2020-4-16 21:28:15 +0700
---

# Sorting Algorithms

My next step in The Odin Project is to develop and program sorting algorithms. The last time that i worked on sorting algorithms was in my introductory programming course in college. While the simple ones like selection, bubble, and insertion sort were easy enough to learn. Merge Sort and Quick Sort were much more challenging. 

```
def bubble_sort(arr)

    sorted = true
    
    while sorted 
        sorted=false
        (0...arr.length-1).each do |ind|
            
            if arr[ind].to_i > arr[ind+1].to_i
                arr[ind],arr[ind+1]=arr[ind+1],arr[ind]
                sorted=true
            end
            
        end
        
        
    end
     arr
end



def bubble_sort_by(arr)
    sorted =true
    while sorted 
        sorted = false
        (0...arr.length-1).each do |ind|
            if yield(arr[ind],arr[ind+1])>0
                arr[ind],arr[ind+1]=arr[ind+1],arr[ind]
                sorted=true
            end
        end
    end
    puts arr
    
end
```
The above code is a simple bubble sort algorithm. It was in writing this code that the beauty of ruby was really starting to click. While code legibility is always a focus regardless of which programming language you decide to use, when using ruby, it is almost an afterthought. All of the code is pretty self-explanitory and isnt jam-packed with needless syntax.


# Merge Sort

My next task was to successfuly write a merge sort algorithm. While the idea of merge sort is relatively simple, recursion is something that can be rather hard to visualize. When it comes to data structures and algorithms, my favorite resource has been [Abdul Bari](https://www.youtube.com/channel/UCZCFT11CWBi3MHNlGf019nw). His video on [Merge Sort](https://www.youtube.com/watch?v=mB5HXBb_HY8) really helped explain everything to me. 

```
def split(arr)
    if arr.length<=1
       return arr
    else
        mid= (arr.length/2).floor
        arr1=split(arr[0..mid-1])
        arr2=split(arr[mid..arr.length])
        merge(arr1,arr2)
    end
end



def merge(arr1,arr2)
    new_arr=[]
    done=false
    #10.times do
    while arr1.length>0 || arr2.length>0

        if arr1.length==0
            min=arr2
        elsif arr2.length==0
            min=arr1
        else
            min =arr1.first < arr2.first ? arr1 : arr2
        end
        #puts "before push arr1: #{arr1}  arr2:#{arr2} new_arr:#{new_arr} "
        new_arr.push(min.shift)
        #puts "after push arr1: #{arr1}  arr2:#{arr2} new_arr:#{new_arr}"
    end
    return new_arr
end


arr=[6,1,8,3,23,62,1,6]
puts split(arr)
```

The code above is pretty self explanitory thanks to the work of art that is Ruby. 


I think that i will reward myself tonight with some Witcher 3 and some pasta.

Chaire,
MM
