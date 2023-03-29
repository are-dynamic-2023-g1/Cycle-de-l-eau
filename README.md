# Cycle-de-l-eau
Projet dans le cadre de l'ARE


import numpy as np
import matplotlib.pyplot as plt

monde = np.full((20,20),5)
monde = np.random.randint(0, 50,( 20, 20))
plt.imshow(monde, cmap="winter")
print(monde)
