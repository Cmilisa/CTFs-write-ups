# Treeeeeeee

Category : General skills

Points : 200

## Description

It appears that my cat has gotten itself stuck in a tree... It's really tall and I can't seem to reach it. Maybe you can throw a snake at the tree to find it?

Oh, you want to know what my cat looks like? I put a picture in the hints.

## Hint

Here, my cat looks like this:

```
#FFC90E#FFC90E#FFC90E#FFFFFF#FFFFFF#FFFFFF#FFFFFF#FFFFFF#FFC90E 
#FFC90E#000000#FFC90E#FFFFFF#FFFFFF#FFFFFF#FFFFFF#FFC90E#FFFFFF
#FFC90E#FFC90E#FFC90E#FFC90E#FFC90E#FFC90E#FFC90E#FFFFFF#FFFFFF 
#FFFFFF#FFFFFF#FFC90E#FFC90E#FFC90E#FFC90E#FFC90E#FFFFFF#FFFFFF
#FFFFFF#FFFFFF#FFC90E#FFC90E#FFC90E#FFC90E#FFC90E#FFFFFF#FFFFFF 
#FFFFFF#FFFFFF#FFFFFF#FFC90E#FFFFFF#FFC90E#FFFFFF#FFFFFF#FFFFFF 
```

## Solving

Here we have to find some cat in a tree, or to rephrase it, a certain file in a lot of directories, along with a lot of other not usefull files.
The thing to notice here is that the 2 files that we don't care about and present in all the directories are either 1718kB or 1496kB. So let's assume the file we are looking for has a different size than these two, and let's use linux commands to find it.

We'll use the command `find . -type f -exec ls -l {} \; | sort -k 5`. The `find .` command allows us to find all directories, all subdirectories and all the files inside them. We use `-type f` to only keep the files, as we are not interested in directories. `-exec ls -l {} \;` makes the find command execute ls on all found files, which will print their size. We then pipe it into `sort -k 5` which sort all the files entries along the 5th column, which is the file size column.

Execute the command and see what we got :

![image](https://user-images.githubusercontent.com/57148042/73140063-0ce66b00-4075-11ea-96eb-1b1eb4d9403e.png)

Here it is. Let's open the image and see what we got :

![image](https://user-images.githubusercontent.com/57148042/73140099-63ec4000-4075-11ea-8a63-3a0aeb1175f6.png)

flag : rtcp{meow_sharp_pidgion_rice_tree}
