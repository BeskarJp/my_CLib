# 🛠️ my_CLib

## 📖 About

**my_CLib** est ma bibliothèque personnelle de fonctions en C, développée au cours de ma **première année à Epitech (2025-2026)**. 

L'objectif de ce projet est de **réimplémenter les fonctions standard de la libc** sans utiliser la bibliothèque d'origine. Ce travail m'a permis d'approfondir mes connaissances en :

* **Programmation C bas niveau** (manipulation de descripteurs de fichiers, appels système).
* **Gestion de la mémoire** et manipulation des pointeurs.
* **Algorithmique** liée aux chaînes de caractères et aux nombres.
* **Architecture modulaire** pour des projets réutilisables.

---

## 🚀 Project Overview

La bibliothèque centralise toutes les fonctions (strings, nombres, affichage, utilitaires) via un header unique :

📂 **`include/my.h`**

Le projet respecte les standards d'Epitech avec une architecture propre et un **Makefile** robuste.

### 🖨️ my_printf
Une implémentation personnalisée du `printf` est incluse dans cette lib.
* **Specifiers supportés :** `%d`, `%s`, `%c`, `%i`, `%u`, `%x`, `%X`, `%o`, `%p`, `%b` (binaire), `%%`, etc.
* **Précision :** Bien que non identique à 100% à la fonction originale, elle couvre la quasi-totalité des besoins standards des projets Epitech.

---

## 🛠️ Compilation

Utilisez le Makefile pour gérer la compilation de la bibliothèque :

| Commande | Action |
| :--- | :--- |
| `make` | Compile la totalité du projet. |
| `make clean` | Supprime les fichiers objets (`.o`). |
| `make fclean` | Supprime les objets et le projet compilé. |
| `make re` | Recompile la totalité du projet (après des modifications). |

---

## 🧪 Testing

Le fichier `src/main.c` est fourni vide par défaut. Pour tester la bibliothèque, modifiez-le comme suit :

```c
#include "my.h"

int main(void)
{
    my_printf("Hello %s! Number: %d\n", "world", 42);
    return 0;
}