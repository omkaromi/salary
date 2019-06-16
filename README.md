# salary
how to code salary slip in Linux 
clear
echo "enter employee details"
echo "-------------------------"
echo "enter name"
read name
echo "enter department"
read dept
echo "enter basic salary"
read basic
if [ $basic -le 1500 ]
        then

          hra=`expr $basic\* 10/100`
          da=`expr $basic\* 90/100`
        else

          hra=500
          da=`expr $basic\* 98/100`
fi

cca=1000
it=`expr $basic\* 40/100`
ptax=200
gross=`expr $basic + $da + $hra + $cca`
ded=`expr $it + $ptax`
net=`expr $basic - $ded`
echo "pay slip"
echo
echo "employee name:$name"
echo "employee dept:$dept"
echo
echo "--------------------------"
echo "basic salary slip:$basic"
echo
echo "addition"
echo "-------------------------"
echo "HAR:$hra"
echo "DA:$da"
echo "CCA:$cca"
echo "Deduction"
echo "-------------------------"
echo "income tax:$it"
echo "PTAX:$ptax"
echo
echo "gross salary:$gross"
echo "Deduction:$ded"
echo
echo "net salary:$net"
echo "---------------------------------"
#end
