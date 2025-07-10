# python temel
def flatten(lst):
    result = []
    for item in lst:
        if isinstance(item, list):
            result.extend(flatten(item))
        else:
            result.append(item)
    return result

def reverse_deep(lst):
    result = []
    for item in reversed(lst):
        if isinstance(item, list):
            result.append(reverse_deep(item))
        else:
            result.append(item)
    return result

if __name__ == "__main__":
    print(flatten([[1, 'a', ['cat'], 2], [[[3]], 'dog'], 4, 5]))
    print(reverse_deep([[1, 2], [3, 4], [5, 6, 7]]))
