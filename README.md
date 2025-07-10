# pythontemel
def flatten(lst):
    result = []
    for item in lst:
        if isinstance(item, list):
            result.extend(flatten(item))  
        else:
            result.append(item)           
    return result
print(flatten([[1, 'a', ['cat'], 2], [[[3]], 'dog'], 4, 5]))


  def reverse_deep(lst):
    result = []
    for item in reversed(lst):
        if isinstance(item, list):
            result.append(reverse_deep(item))  # iç listeyse yine ters çevir
        else:
            result.append(item)
    return result

print(reverse_deep([[1, 2], [3, 4], [5, 6, 7]]))
