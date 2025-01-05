# noktalr
point = [(1,2), (4,6), (5,8), (2,3)]

# mesafe bulma 
def eucdis(p1, p2):
    x = (p2[0] - p1[0])**2
    y = (p2[1] - p1[1])**2
    mesafe = (x + y) ** 0.5
    return mesafe

# mesafeler listesi
distanes = []
for i in range(len(point)):
    for j in range(len(point)):  # yanlışlıkla aynı noktaları da karşılaştırıyor
        if i != j:  # ekledim çünkü hata vardı
            dist = eucdis(point[i], point[j])
            distanes.append(dist)

# min bul
mnn_dist = min(distanes) # yanlış yazılmış değişken isimleri, kafa karışıklığı
print("minimum uzaklık", mnn_dist)  # yazım hatasıyla sade bir çıktı
