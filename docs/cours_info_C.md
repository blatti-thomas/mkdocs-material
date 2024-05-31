
# Bibliothèques Standard du C 
## === Gestion des Erreurs et Assertions ===

```
#include <assert.h> --> Gestion des assertions 
```
```
#include <errno.h> --> Codes d'erreur standard 
```
## === Types et Limites ===
```
#include <complex.h> --> Opérations sur des nombres complexes 
```
```
#include <ctype.h> --> Fonctions de test et de mappage de caractères    
```
```
#include <float.h> --> Limites des types à virgule flottante    
```
```
#include <inttypes.h> --> Types entiers avec largeur fixe 
```
```
#include <limits.h> --> Limites des types fondamentaux   
```
```
#include <stdbool.h> --> Types booléen 
```
```
#include <stddef.h> --> Définitions de types et de macros générales  
```
```
#include <stdint.h> --> Types entiers à largeur fixe  
```


## === Localisation et Environnement ===
```
#include <locale.h> --> Localisation 
```
```
#include <fenv.h> --> Gestion de l'environnement flottant   
```
```
#include <setjmp.h> --> Gestion des rebonds d'environnement non local 
```
```
#include <signal.h> --> Gestion des signaux 
```

## === Entrées/Sorties et Manipulation de Chaînes ===
```
#include <stdio.h> --> Entrée/Sortie  
```
```
#include <stdlib.h> --> Utilitaires généraux
```
```
#include <string.h> --> Manipulation de chaînes 
```

## === Fonctions Mathématiques ===
```
#include <math.h> --> Fonctions mathématiques   
```
```
#include <tgmath.h> --> Fonctions mathématiques génériques
```

## === Gestion du Temps ===
```
#include <time.h> --> Fonctions liées au temps
```

## === Arguments Variables ===
```
#include <stdarg.h> --> Gestion des arguments à nombre variable
```

# Types de variables du C 
```
char a;  --> Entier sur 8 bits utilisé pour des caractères.

short b; --> short int: Entier en général sur 16 bits.

int c;   --> Entier en général sur 16 ou 32 bits, dépendant du système et du compilateur.

long d;

long int e; --> Entier en général sur 32 bits.

long long f;

long long int g; --> Entier sur 64 bits.
```

## === Types à Virgule Flottante ===
```
float h; --> Approximation de réels, sur 32 bits
            (1 bit de signe, 8 bits pour l'exposant et 23 bits pour la fraction).

double i; --> Approximation de réels sur 64 bits (1 bit de signe, 11 bits
              pour l'exposant et 52 bits pour la fraction).

long double j; --> Approximation de réels sur min. 80 bits, mais souvent
                   128 bits (1 bit de signe, 15 bits pour l'exposant et 112 bits pour la fraction).
```
# Formatage pour printf en C
```
  * %d, %i      : int en base 10  
  * %c          : caractère donné par son code de type int  
  * %f          : double, par défaut 6 chiffres significatifs  
  * %e, %E      : double en notation scientifique avec e ou E  
  * %g, %G      : choix automatique entre %f et %e ou entre %f et %E  
  * %s          : chaîne de caractères  
  * %u          : unsigned int  
  * %o, %x, %X  : int affichée en octal ou en hexadécimal  
  * %p          : adresse  
  * %%          : le caractère % lui-même  
```
# === Flags ===
```
- (flag)    : alignement à gauche
+ (flag)    : nombres imprimés avec le signe (sinon seul le signe négatif est imprimé)
0 (flag)    : ajoute des zéros devant
# (flag)    : avec type o, x, et X force l'écriture de 0, 0x ou 0X

devant. Avec f, e, E force le point décimal.
 
Width:
nombre ou * : nombre minimum de caractères utilisés pour l’impression (ajout d'espaces)
 
Precision:
.nombre ou *: nombre de chiffres après la virgule

Length:
l           : pour un entier long (ou L pour un long double), h pour un entier court
```
# Fonctions de Manipulation de Fichiers en C 
```
int fputc(int c, FILE *fp); --> Écrit un caractère 'c' dans le fichier pointé par 'fp'.
                                 Retourne le caractère écrit en cas de succès, sinon EOF.
```
```
int fgetc(FILE *fp); --> Lit et retourne le prochain caractère sous forme d'int
                         depuis le fichier pointé par 'fp' ou EOF en cas d'erreur ou de fin de fichier.
```
```
int ungetc(int char, FILE *fp); --> Remet le caractère 'char' dans le flux de 'fp', le rendant
                                    disponible pour la prochaine lecture avec fgetc(). Retourne
                                    le caractère en cas de succès, sinon EOF.
```
```
int fputs(const char *s, FILE *fp); --> Écrit la chaîne 's' dans le fichier pointé
                                          par 'fp' (le '\n' n'est pas nécessaire). Retourne une
                                          valeur non négative en cas de succès, sinon EOF.
```
```
char *fgets(char *buf, int n, FILE *fp); --> Lit au maximum 'n-1' caractères depuis le fichier 'fp', les
                                             stocke dans 'buf', et ajoute un '\0' final. S'arrête à '\n'
                                             ou à la fin du fichier. Retourne 'buf' en cas de succès, sinon NULL.
```
```
int fprintf(FILE *fp, const char *format, ...); --> Écrit des données formatées dans le fichier 'fp' selon le 'format'
                                                     spécifié, comme printf mais dans un fichier. Retourne le nombre de
                                                     caractères écrits, ou une valeur négative en cas d'échec.
```
```
int fscanf(FILE *fp, const char *format, ...); --> Lit des données formatées depuis le fichier 'fp' selon le 'format'
                                                    spécifié, comme scanf mais depuis un fichier. Retourne le
                                                    nombre d'éléments lus, 0 en cas d'erreur, ou EOF pour une fin de fichier.
```
```
void rewind(FILE *fp); -->Repositionne le curseur de fichier 'fp' au début du fichier.
```
 
## === Fonctions de Gestion Avancée des Fichiers en C === 
```
int fflush(FILE *fp); --> Vide le buffer de sortie du fichier pointé par 'fp' et
                            écrit toutes les données en attente.
                            Retourne 0 en cas de succès, EOF en cas d'erreur.
```
```
fflush(NULL); --> Vide tous les buffers de sortie de tous les fichiers ouverts.
```
```
int remove(const char *filename); --> Supprime le fichier désigné par 'filename'. Retourne 0 en cas
                                        de succès, -1 en cas d'erreur et
                                        définit errno.
```
```
int rename(const char *old_filename, const char *new_filename); --> Renomme le fichier 'old_filename' en 'new_filename'. Retourne 0
                                                                      en cas de succès, -1 en cas
                                                                      d'erreur et définit errno.
```
```
FILE *tmpfile(void); --> Crée un fichier temporaire en mode "wb+" qui sera supprimé
                           automatiquement à la fin de l'exécution du programme.
                           Retourne un pointeur vers ce fichier en cas de succès, ou NULL en cas d'échec.
```
 
## === Fonctions de Vérification et de Réinitialisation de l'État des Fichiers en C === 
```
void clearerr(FILE *fp); --> Efface les indicateurs d'erreur et de fin de fichier associés au
                               fichier pointé par 'fp'.
```
```
int feof(FILE *fp); --> Teste l'indicateur de fin de fichier pour le fichier pointé par 'fp' et
                          renvoie un résultat non nul si celui-ci est positionné, 0 sinon.
```
```
int ferror(FILE *fp); --> Teste l'indicateur d'erreur pour le fichier pointé par 'fp' et renvoie un
                            résultat non nul si celui-ci est positionné, 0 sinon.
```
 
# Structures et Création de Types en C 
 
  * Définition d'une structure
  ```
  struct NomStructure {
      type membre1;         --> Permet de regrouper plusieurs variables de types différents sous le même type.
      type membre2;   
  };
  ```


  * Création d'une instance de structure
   ```
  struct NomStructure variable; --> Déclare une variable de type 'struct NomStructure'.
   ```

  * Accès aux membres d'une structure
   ```
  variable.membre1 = valeur; --> Accède et modifie le membre 'membre1' de la structure 'variable'.
   ```

  * Pointeur sur une structure
   ```
  struct NomStructure *ptr = &variable; --> Crée un pointeur 'ptr' vers la structure 'variable'.
   ```
 
  * Accès aux membres d'une structure via un pointeur
   ```
  ptr->membre1 = valeur; --> Accède et modifie le membre 'membre1' via le pointeur 'ptr'.
   ```
 
  * Typedef pour les structures
   ```
  typedef struct NomStructure AliasStructure; --> Permet de définir un alias 'AliasStructure' pour 'struct NomStructure'.
   ```
 
  * Utilisation de l'alias de structure
   ```
  AliasStructure nouvelleVariable; --> Déclare une variable 'nouvelleVariable' de type 'AliasStructure'.
   ```

  * Définition d'un type enum
   ```
  enum NomEnum { CONST1, CONST2, ... }; --> Permet de définir un ensemble de constantes entières nommées.
   ```
 
  * Utilisation d'un enum
   ```
  enum NomEnum variableEnum = CONST1; --> Déclare une variable 'variableEnum' de type 'enum NomEnum' et
                                          l'initialise avec 'CONST1'.
   ```