#Prime Number

def isPrime(num):
  a = num // 2
  for i in range(2, a):
    if num % i == 0:
      return False
  return True # check if number is prime

def checkPrimeForm(num):
  if num % 6 == 1 or num % 6 == 5:
    return True
  return False # check if number is in 6k+-1 form

newlist1 = []
for i in range(1100, 1200):
    if isPrime(i):
      if checkPrimeForm(i):
        newlist1.append((i, "Yes")) # append as a tuple
      else:
        newlist1.append((i, "No")) # append as a tuple
print(newlist1)
