
# -*- coding: utf-8 -*-
"""
Created on Thu Jun 19 20:36:08 2014

@author: Group 4-heath-REPORTER
"""
#SOME LIBRARIES THAT MIGHT COME IN HANDY ARE IMPORTED 
import csv
from pylab import *
from math import *
import os


mydata =[]#mydata is a list that is going to contain that read values in the file
while True:
    
    a= raw_input("Enter file name with extension:")
    print '\n'

    k=[]
    try:
        with open(a,"r")as csvfile:
            spamreader = csv.reader(csvfile,delimiter =',')    
            for row in spamreader:
                k.append(row[0]) 
                
   
         
        print '==================================================================================================================================================== '
        print '====================================================================================================================================================='
        print '=========================================================       PUBLIC HEALTH REPORT     ============================================================'
        print '====================================================================================================================================================='        
        print '====================================================================================================================================================='

        with  open(a,"r") as csvfile:
            spamreader = csv.reader(csvfile,delimiter =',')    
            for row in spamreader:
                row = [str(e) for e in row]
                print('\t'.join(row))
                
        with  open(a,"r") as csvfile:
            spamreader = csv.reader(csvfile)    
            for row in spamreader:
                r=row
                break
            del r[0]

    
    

        with  open(a,"r") as csvfile:
            spamreader = csv.DictReader(csvfile)    
            for row in spamreader:
                 for key in row.keys():                
                    try:
                        row[key]=int(row[key])
                    except:
                        continue
                 mydata.append(row)
            w=[[i] for i in range(len(mydata))]
            for element in range(len(mydata)):
                for value in r:
                    w[element].append(mydata[element][value]) 
                del w[element][0]
                plot(w[element],)
                
                xticks(range(len(r)),r)
        break
    except IOError:
        print "ERROR!!! FILE DOES NOT EXIST." 
        continue        

ylabel('Number of Cases Recorded')
xlabel('Months')
head = '' 
if a[0] == 'd':
    head = 'PLOT OF THE NUMBER OF CASES OF EACH DISEASE WITH TIME'
elif a[0] == 'c':
    head = 'PLOT OF THE NUMBER OF CASES OF MALARIA WITH TIME'
elif a[0] == 'h':
    head = 'PLOT OF THE NUMBER OF CASES OF MALARIA FOR THREE HOSPITALS WITH TIME'   

    
title(head)
print'\n'
print '===================================================================='
print '===================================================================='
print '============================     SUMMARY     ======================='
print '===================================================================='
print '===================================================================='

for values in range(len(mydata)):
    maximum=max(w[values])
    minimum=min(w[values])
    average=sum(w[values])/len(w[values])

    print str(k[values+1])+' :    Maximum = '+str( maximum)+'         '+ 'Minimum = '+str(minimum)+'       '+ 'Average = '+str(average)
    
show()
