def first_fit_decreasing(lengths, bar_length):
    # Triez les longueurs en ordre décroissant
    lengths.sort(reverse=True)

    # Initialisez les barres et les espaces restants
    bars = []
    remaining_space = []

    # Parcourez chaque longueur
    for length in lengths:
        # Essayez de la placer dans une barre existante
        for i in range(len(bars)):
            if remaining_space[i] >= length:
                bars[i].append(length)
                remaining_space[i] -= length
                break
        else:
            # Si elle ne rentre dans aucune barre existante, créez une nouvelle barre
            bars.append([length])
            remaining_space.append(bar_length - length)

    return bars, remaining_space

# Les longueurs requises et leurs quantités
lengths = [157]*30 + [182]*90 + [193]*70 + [200]*30 + [184]*30

# La longueur des barres
bar_length = 600

# Appliquez l'algorithme FFD
bars, remaining_space = first_fit_decreasing(lengths, bar_length)

# Affichez le résultat
for i, (bar, space) in enumerate(zip(bars, remaining_space)):
    print(f"Barre {i+1} : {bar}, Chute restante : {space} cm")
