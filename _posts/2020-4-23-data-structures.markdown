---
layout: post
title:  "Data Structures"
date:   2020-4-23 21:28:15 +0700
---

# Linked-List and Binary Trees

## Linked-List
Next on the docket for TOP (The Odin Project) is to go over data structures and some of the accompanying algorithms used for said data structures. My two introductory programming classes that i took for electrical engineering did not spend any real time covering data structures. 

My first mini-project was to create a linked list class with the accompanying methods. One of the methods involved returning an element at a given index.

```
def at(index)
        num_node=0
        curr_node=@head
        until num_node==index
            curr_node=curr_node.next_node
            num_node+=1
        end

        return curr_node
    end
```
this is a pretty simple algorithm made even easier by ruby's awesome syntax. 

Going through all of the Linked-List algorithms and writing code for them was relatively easy. Linked Lists, as a data structure, are pretty easy to understand so i did not have too much trouble with them.

## Binary-Tree
I had a similar assignment for Binary-Trees. This [task](https://github.com/MattMiller1989/Binary-Tree) was considerably more complicated and less intuitive than the linked list assignment. Luckily, i had help from my good friend [Abdul](https://www.youtube.com/channel/UCZCFT11CWBi3MHNlGf019nw). 

The algorithm for each of the traversals was relatively simple: 
```
def preorder(root=@root)
        
        if root == nil 
            return
        end
        puts root
        preorder(root.left)
        preorder(root.right)

    end
    def inorder(root=@root)
        


        if root==nil 
            return
        end
        inorder(root.left)
        puts root
        inorder(root.right)
    end

    def postorder(root=@root)
        if root==nil 
            return
        end
        postorder(root.left)
        postorder(root.right)
        puts root
    end            

    def level_order(root=@root)
        node_queue=[]
        if root == nil
            return
        end

        node_queue.push(root)
        while node_queue.length>0
            current_node= node_queue.shift
            node_queue.push(current_node.left) unless current_node.left ==nil
            node_queue.push(current_node.right) unless current_node.right ==nil
            puts current_node
        end


    end
```
Figuring out the algorithm for each of these helped reinforce my understanding of recursion. The hardest one by far was the algorithm for rebalancing an unbalanced tree. This one involved using a similar method to the one that we used for level order traversal. This algorithm invloved storing each of the nodes at a given level inside of a queue but instead of printing them, we compare them against whichever branch we are currently traversing and assign the "front" of the queue to a separate array. That array is then used to rebuild the tree from scratch.

```
def rebalance!()
        node_queue=[]
        level_arr=[]
        if @root == nil
            return
        end

        node_queue.push(@root)
        while node_queue.length>0
            current_node= node_queue.shift
            node_queue.push(current_node.left) unless current_node.left ==nil
            node_queue.push(current_node.right) unless current_node.right ==nil
            level_arr.push(current_node.value)
        end
        
        @root=build_tree(level_arr)
    end
```

# Praise for Abdul

This guy and his [channel](https://www.youtube.com/channel/UCZCFT11CWBi3MHNlGf019nw) have saved me from countless hours of banging my head against the wall.


Chaire,
MM

