Reformat in vim for a nice column layout:

      :%!column -t
      :%!column -s $'\t' -t

Add 1 to all the number in the text:

      :%s/\d\+/\=submatch(0)+1/g
