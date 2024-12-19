def count_chars(s):
    result = {}
    for char in s:
        if char not in result:
            result[char] = 1
        else:
            result[char] += 1
    return result
