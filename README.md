# Reverse-dictionary-by-value-of-string-frequency
def most_frequent(value):
    x = dict()
    for i in value:
        if i not in x:
            x[i] = 1
        else:
            x[i] += 1
    return x

x = input("Enter a value : ")

y = most_frequent(x)

y_sorted_keys = sorted(y, key=y.get, reverse=True)
for r in y_sorted_keys:
    print(r,"=", y[r])
