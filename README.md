-------------********RECAPITULATIF DE MON DEVOIR*******-------------

---

 Devoir : Programmation géométrique en C++

Structure du projet

Crée un dossier nommé par exemple GeometryProject, contenant :

GeometryProject/
│
├── point.h
├── point.cpp
├── vector.h
├── vector.cpp
└── main.cpp


---
//DECLARATION DES FICHIERS EXECUTABLES
 1* Fichier : point.h

#ifndef POINT_H
#define POINT_H

#include <iostream>
using namespace std;

struct Point {
    float x;
    float y;
};

Point translate(Point p, float dx, float dy);
Point interpolate(Point p1, Point p2, float t);

#endif


---

2* Fichier : point.cpp

#include "point.h"

Point translate(Point p, float dx, float dy) {
    Point result;
    result.x = p.x + dx;
    result.y = p.y + dy;
    return result;
}

Point interpolate(Point p1, Point p2, float t) {
    Point result;
    result.x = (1 - t) * p1.x + t * p2.x;
    result.y = (1 - t) * p1.y + t * p2.y;
    return result;
}


---

3* Fichier : vector.h

#ifndef VECTOR_H
#define VECTOR_H

#include <iostream>
#include <cmath>
using namespace std;

struct Vector {
    float x;
    float y;
};

Vector add(Vector v1, Vector v2);
Vector subtract(Vector v1, Vector v2);
Vector homothety(Vector v, float k);
float norm(Vector v);
Vector rotate(Vector v, float angleDeg);

#endif


---

4*  Fichier : vector.cpp

#include "vector.h"

Vector add(Vector v1, Vector v2) {
    Vector result;
    result.x = v1.x + v2.x;
    result.y = v1.y + v2.y;
    return result;
}

Vector subtract(Vector v1, Vector v2) {
    Vector result;
    result.x = v1.x - v2.x;
    result.y = v1.y - v2.y;
    return result;
}

Vector homothety(Vector v, float k) {
    Vector result;
    result.x = v.x * k 
    result.y = v.y * k HBHHHHBHB
    return result;
}

float norm(Vector v) {
    return sqrt(v.x * v.x + v.y * v.y);
}

Vector rotate(Vector v, float angleDeg) {
    float angleRad = angleDeg * M_PI / 180.0;
    Vector result;
    result.x = v.x * cos(angleRad) - v.y * sin(angleRad);
    result.y = v.x * sin(angleRad) + v.y * cos(angleRad);
    return result;
}


---

5* Fichier : main.cpp

#include <iostream>
#include "point.h"
#include "vector.h"
using namespace std;

int main() {
    Point p1 = {2, 3};
    Point p2 = {8, 6};
    Vector v1 = {2, 3};
    Vector v2 = {1, 1};

    cout << "=== GEOMETRY PROJECT ===" << endl;

    Vector sum = add(v1, v2);
    Vector diff = subtract(v1, v2);
    Vector scaled = homothety(v1, 2);
    float length = norm(v1);
    Vector rotated = rotate(v1, 90);

    cout << "\n--- VECTEURS ---" << endl;
    cout << "Addition: (" << sum.x << ", " << sum.y << ")" << endl;
    cout << "Soustraction: (" << diff.x << ", " << diff.y << ")" << endl;
    cout << "Homothétie (k=2): (" << scaled.x << ", " << scaled.y << ")" << endl;
    cout << "Norme: " << length << endl;
    cout << "Rotation (90°): (" << rotated.x << ", " << rotated.y << ")" << endl;

    Point translated = translate(p1, 3, -1);
    Point interp = interpolate(p1, p2, 0.5);

    cout << "\n--- POINTS ---" << endl;
    cout << "Translation du point p1: (" << translated.x << ", " << translated.y << ")" << endl;
    cout << "Interpolation entre p1 et p2: (" << interp.x << ", " << interp.y << ")" << endl;

    cout << "\n=== FIN DU PROGRAMME ===" << endl;
    return 0;
}


---

6* Fonctions incluses

 Vecteurs :

Addition

Soustraction

Homothétie (agrandir/réduire)

Norme (longueur)

Rotation (autour de l’origine)


 Points :

Translation

Interpolation linéaire

DURANT CETTE SEANCE D'EXERCICE J'AI PU APPRENDRE DE NOUVELLES CHOSES PATIONNANTES CONCERNANT LE LANGAGE C++.
GAME PROGRAMMING I GOT IT 

---
LE LANGAGE C++ DEMANDE BEAUCOUP DE CONCENTRATION ET UNE BONNE FORMATION POUR ESPERER S'Y IMMERGER PLAINEMENT
HAVE A NICE DAY . SEE YOU SOON
