# veriyapilariodevi(faktoriyelhesabi)
Bu depo Karadeniz Teknik Üniversitesi Bilgisayar Mühendisliği Veri Yapıları dersi ödevi için hazırlanmıştır


#ITERATIVE SOLUTION
from time import time

start_time = time()                    #programımızın çalısma suresini görebilmek icin olusturdugumuz baslangıc zaman degeri
fact = 1                               #fact degiskenine deger ataması

print("Enter the number to be calculated with a factorial:") #Faktoriyeli alınacak degerin girilmesi isteminin yazdırılması

n = int(input())                       #kullanıcıdan deger girebilmesi icin yazılan tanım

if n==0 or n==1:                       #degerin 0 ya da 1 olma durum kıyasına bakılarak bu sartın saglanması durumunda faktoriyel degerinin 1 olacagının ekrana yazdırımı
  print("Factorial of ",n,"=1")
elif n<0:                              #degerin 0 dan kucuk olması durumunda ekranda uyarı görebilmemizi saglayan yazdırım
  print("Factorial calculations are not made for numbers less than 0!")
else:                        
  for i in range(1,n+1):               #sartların saglanmaması durumunda her i degeri icin n+1 e kadar birer arttırım yaparak factoriyel hesabına çarpan olarak ekleyecek tanım
    fact = fact * i          
  print("Factorial of",n,"=",fact)     #hesaplanan faktoriyel hesabının yazdırılması

end_time= time()                       #programın bitiş zamanının belirtimi
print(end_time - start_time)           #harcanan sürenin ekrana yazdırılımı

#RECURSIVE SOLUTION
from time import time         
start_time = time()             #programımızın çalısma suresini görebilmek icin olusturdugumuz baslangıc zaman degeri

def fact(num):                  #faktoriyel hesabını yapacak olan fonksiyonumuzun tanımı
  if num==0 or num==1:       
    return 1                    #degerin 0 ya da 1 olma durum kıyasına bakılarak bu sartın saglanması durumunda 1 degerinin döndürüleceginin belirtimi

  elif num < 0:                 
    return "error"              #girilen degerin 0 veya 1 olmadıgı bilindigi takdirde, 0 dan kücük olması durumunda hata verilmesinin gösterimi

  else:                        
    return num * fact(num-1)    #eger belirtilen durumlar saglanmıyorsa "num * fact(num-1)" ifadesinin uygulanacagı belirtimi

print("Enter the number to be calculated with a factorial:") #Faktoriyeli alınacak degerin girilmesi isteminin yazdırılması

n = int(input())                 #klavyeden girilmesi icin olusturulan tanım                             

print(fact(n))                   #hesaplanan faktoriyel hesabının yazdırılması

end_time= time()                 #programın bitiş zamanının belirtimi
print(end_time - start_time)     #harcanan sürenin ekrana yazdırılımı
