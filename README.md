# Assignment-6
# Stress When depth is constant
Q=float(input("Enter the value of Load in kN:"))
N=int(input("Number of data values of radial distance:"))
pi=3.14159265359
Z=float(input("Depth:"))
r=[]
for i in range(1, N + 1):
   print("Enter radial distance in m".format (i))
   Value_r=float(input())
   r.append(Value_r)
# this line was not indented correctly, causing the error
   Stress=((3*Q)/(2*pi*Z*Z))*(((1/(1+((Value_r/Z)*2))))*2.5)
# Q was missing and pi needs to be called from the math module
   print("Stress: ",Stress,"kN/m^2")
#Q-2
# Calculating the stress by Boussineq's Theory
Q=int(input("Enter the value of given load :"))
z=int(input("Enter the distance of vertical stress :"))
r=int(input("Enter the distance of horizntal stress:"))
stress = (3*Q*(1/(1+(r/z)*2))*2.5)/(2*3.14*(z**2))
print("The value of stress is",stress)
