Voici un document complet qui intègre des exemples détaillés de résolution pour chacun des thèmes mentionnés dans votre test de mathématiques :

### 1. Méthode de Gauss pour les Systèmes Linéaires

**Exemple**: Résoudre le système suivant en utilisant la méthode de Gauss.
\[
\begin{align*}
2x + 3y - z &= 5 \\
4x + 6y - 3z &= 9 \\
-2x - 3y + 3z &= -1
\end{align*}
\]

#### Résolution:
1. **Forme matricielle et opérations élémentaires** pour obtenir une forme échelonnée:
   \[
   \begin{pmatrix}
   2 & 3 & -1 & | & 5 \\
   4 & 6 & -3 & | & 9 \\
   -2 & -3 & 3 & | & -1
   \end{pmatrix}
   \]
   - Diviser la première ligne par 2.
   - Soustraire le double de la première ligne de la deuxième ligne et ajouter la première ligne à la troisième ligne.
   - Réduire la troisième ligne pour obtenir un pivot.

2. La forme échelonnée réduite permet de trouver que \( z = 2 \), puis remonter pour trouver \( y \) et \( x \).

### 2. Système Singulier

**Exemple**: Vérifier si le système suivant est singulier et pourquoi.
\[
\begin{align*}
x + 2y - z &= 0 \\
2x + 4y - 2z &= 0 \\
3x + 6y - 3z &= 0
\end{align*}
\]

#### Résolution:
1. **Forme matricielle**:
   \[
   \begin{pmatrix}
   1 & 2 & -1 \\
   2 & 4 & -2 \\
   3 & 6 & -3
   \end{pmatrix}
   \]
2. **Échelonnage**:
   - Les lignes sont proportionnelles, indiquant une matrice de rang 1.

3. **Conclusion**:
   - Le système est singulier car il n'a pas de solution unique (il a une infinité de solutions ou aucune, selon les termes constants).

### 3. Méthode de Cramer

**Exemple**: Résoudre le système suivant en utilisant la méthode de Cramer, si possible.
\[
\begin{align*}
x + y + z &= 6 \\
2x + 3y + z &= 11 \\
3x + 3y + 2z &= 14
\end{align*}
\]

#### Résolution:
1. **Matrice des coefficients** \( A \) et déterminant \( \text{det}(A) \):
   \[
   A = \begin{pmatrix}
   1 & 1 & 1 \\
   2 & 3 & 1 \\
   3 & 3 & 2
   \end{pmatrix}
   \]
   - Calculons \( \text{det}(A) \).

2. **Déterminants pour \( x, y, z \)**:
   - Remplaçons les colonnes respectives par le vecteur des termes constants et calculons les déterminants.

3. **Application de la méthode de Cramer**:
   - \( x = \frac{\text{det}(A_x)}{\text{det}(A)} \), et de même pour \( y \) et \( z \).

### 4. Développement Limité d'ordre n pour Taylor

**Exemple**: Développement limité de la fonction \( \sin(x) \) autour de \( x = 0 \) jusqu'à l'ordre 5.

#### Résolution:
1. **Calcul des dérivées nécessaires**:
   \[
   \sin(x), \quad \cos(x), \quad -\sin(x), \quad -\cos(x), \quad \sin(x)
   \]
2. **Évaluation à \( x = 0 \)**:
   - \( \sin(0) = 0, \quad \cos(0) = 1, \quad -\sin(0) = 0, \quad -\cos(0) = -1 \)
3. **Développement**:
   \[
   \sin(x) \approx x - \frac{x^3}{6} +

 \frac{x^5}{120}
   \]

### 5. Courbes: Donner l'Équation Cartésienne d'une Courbe à partir d'un Vecteur

**Exemple**: Trouver l'équation cartésienne de la courbe représentée par le vecteur position \( \mathbf{r}(t) = \begin{pmatrix} t \\ t^2 \end{pmatrix} \).

#### Résolution:
1. **Paramétrisation**:
   - \( x = t \), \( y = t^2 \)
2. **Élimination de \( t \)**:
   - \( y = x^2 \)

