# sayi-bilme-oyunu
import random #rastgele sayi uretmek icin kutuphane

rsayi=random.randint(50,250) 
sayac=0
#print(rsayi)
dogrutahmin=0
tahminler=[]

while sayac<10:
  tahmin=int(input("rastgele secilen sayiyi tahmin et"))
  if tahmin<50 or tahmin>250:
     print("50 ile 250 arasinda bir tahmin yapin")
     continue
  else:
     sayac+=1
     tahminler.append(tahmin)
     
  if tahmin==rsayi:
       dogrutahmin+=1
       print("Dogru tahmin ettiniz tebrikler")
       print("dogru sayi=",rsayi)
       
       break

  elif rsayi>tahmin : 
           print("Tahmininiz yanlıs daha buyuk bir sayi tahmin edin")
  else:
           print("Tahmininiz yanlıs daha kucuk bir sayi tahmin edin")
     
if sayac== 10:
    print("Tahmin hakkınız bitti")
         
print("tahminleriniz:",tahminler)
print(sayac,". tahminiz dogru")
