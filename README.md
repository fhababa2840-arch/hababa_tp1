# hababa_tp1
mon premier projet
# TP1
Nom: HABABA
Prénom: FAISSEL
## Exercice 1:
CONST CODE_PIN ← "1234"
tentatives ← 0

DEBUT
    TANT QUE tentatives < 3 FAIRE
        ECRIRE ("Entrez votre code PIN : ")
        LIRE saisie

        SI saisie = CODE_PIN ALORS
            ECRIRE(" Accès autorisé. Carte débloquée.")
            ARRET
        SINON
            tentatives ← tentatives + 1
            ECRIRE (" Code PIN incorrect.")

            SI tentatives = 3 ALORS
                ECRIRE (" Carte bloquée après 3 tentatives.")
            FIN SI
        FIN SI
    FIN TANT QUE
FIN
## Exercice 2:
DEBUT
    ECRIRE ("Entrez a : ")
    LIRE a
    ECRIRE ("Entrez b : ")
    LIRE b

    temp ← a
    a ← b
    b ← temp

    ECRIRE ("Après échange : a = ", a " b =",b)
FIN

## Exercice 3:
DEBUT
    LIRE a, b

    TANT QUE b ≠ 0 FAIRE
        r ← a MOD b
        a ← b
        b ← r
    FIN TANT QUE

    ECRIRE ("PGCD =", a)
FIN
version recursive
FONCTION PGCD(a, b)
    SI b = 0 ALORS
        RETOURNER a
    SINON
        RETOURNER PGCD(b, a MOD b)
    FIN SI
FIN FONCTION
## Exercice 4:
methode 1
DEBUT
    LIRE (n)
    POUR d ← 1 JUSQU'A n FAIRE
        SI (n MOD d = 0) ALORS
            ECRIRE (d)
        FIN SI
    FIN POUR
FIN
methode 2
DEBUT
    LIRE (n)
    POUR d ← 1 JUSQU'A racineCarree(n) FAIRE
        SI (n MOD d = 0) ALORS
            ECRIRE (d)
            SI (d ≠ n / d) ALORS
                ECRIRE (n / d)
            FIN SI
        FIN SI
    FIN POUR
FIN
## Exercice 5:
DEBUT

REPETER
    secret ← aleatoire(1,100)
    tentatives ← 0
    trouve ← FAUX

    TANT QUE tentatives < 5 ET trouve = FAUX FAIRE
        ECRIRE ("Devinez le nombre : ")
        LIRE (x)
        tentatives ← tentatives + 1

        SI x = secret ALORS
            ECRIRE (" Félicitations !")
            trouve ← VRAI
        SINON SI x < secret ALORS
            ECRIRE ("Trop petit.")
        SINON
            ECRIRE ("Trop grand.")
        FIN SI
    FIN TANT QUE

    SI trouve = FAUX ALORS
        ECRIRE ("Le nombre était ", secret)
    FIN SI

    ECRIRE ("Voulez-vous rejouer ? (oui/non)")
    LIRE (choix)

JUSQU'A choix ≠ "oui"

FIN
## Exercice 6:








