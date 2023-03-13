# Lab 5: Options for the ls command
By Jonathan Xiang

## The -a option - [Source](https://www.rapidtables.com/code/linux/ls.html)
`-a` is an option for the ls command that allows you to also see hidden files, which are files that begin with a ".".

![](lsaOption.png)

As you can see in the image above, using the `ls` command without `-a` yields no files that start with a ".", but using `ls -a` shows many files that start with a ".". You can also see that all the files resulting from the normal `ls` command are also listed in the results of `ls -a`.

## The -l option

`-l` is an option for the ls command that lists the files in "logn format". "Long format" includes additional information about the files that using ls normally wouldn't give you. This additional information includes owner, file size, and date and time of creation or last modificiation.

![](lslOption.png)
