import math

# 2D uzaydaki noktaları temsil eden demetler (tuple) içeren bir liste oluşturuldu
points = [(1, 2), (4, 6), (5, 8), (7, 9), (2, 1)]

def euclideanDistance(point1, point2):
    """
    İki nokta arasındaki Öklid mesafesini hesaplar.
    """
    return math.sqrt((point2[0] - point1[0]) ** 2 + (point2[1] - point1[1]) ** 2)

# Mesafeler için bir liste
distances = []

# Her nokta çifti arasındaki Öklid mesafesini hesaplama
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Minimum mesafenin bulunması ve yazdırılması
min_distance = min(distances)
print(f"Minimum Öklid mesafesi: {min_distance}")
