def comp(array1, array2):
    if type(array1) == list and type(array2) == list:
        b = 0
        if len(array1) == 0 and len(array2) == 0:
            return True
        if len(array1) == 0 and len(array2) >0:
            return False
        if len(array1) != 0 and len(array2) == 0:
            return False
        for r in array1:
            if (r ** 2) in array2:
                b = b + 1
                array2.remove(r**2)
        if b == len(array1):
            return True
        else:
            return False
    else:
        return False
