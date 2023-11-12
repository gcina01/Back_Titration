# Back_Titration
#Analyte
Analyte=input("Enter the Analyte : ")
Mm=input('Enter the molar mass of '+Analyte +" : " )

#Secondary Starndard
Secondary=input("Enter the Secondary starndard : ")
V_tsec=float(input("Enter the volume of " + Secondary +" : "))
c_tsec=float(input("Enter the concentration of " + Secondary +" : "))
n_tsec=c_tsec*V_tsec

#Primary Starndard 
Primary=input("Enter the Primary starndard : ")
V_primary=float(input("Enter the volume of " + Primary +" : "))
c_primary=float(input("Enter the concentration of " + Primary+" : "))
n_primary=c_primary*V_primary

print("for the reaction between "+Primary+" and "+Secondary+" : ")
CE10=float(input("Enter the coefficient of "+Primary+" : "))
CE12=float(input("Enter the coefficient of "+Secondary+" : "))
n_exc=n_primary*CE10/CE12
n_sec=n_tsec-n_exc

print("For the reaction between "+ Secondary +" and " + Analyte + " : ")
CE20=float(input("Enter the coefficient of "+ Analyte + " : "))
CE21=float(input("Enter the coefficient of " + Analyte + " : "))
n_ana=n_sec*CE20/CE21
print("The number of moles of " + Secondary + " = " + n_ana)
