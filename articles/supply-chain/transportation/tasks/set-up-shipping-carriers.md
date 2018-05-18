--- 
title: Einrichten von Spediteuren
description: "In diesem Verfahren wird gezeigt, wie einen Spediteur eingerichtet wird und Details wie Dienst, Lieferart, Transportzahlungsmittel, Transporteinschränkungen und Versandsatz definiert werden."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-shipping-carriers"></a>Einrichten von Spediteuren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Verfahren wird gezeigt, wie einen Spediteur eingerichtet wird und Details wie Dienst, Lieferart, Transportzahlungsmittel, Transporteinschränkungen und Versandsatz definiert werden. Ein Transportkoordinator kann dann einen Spediteur einer ein- und ausgehenden Ladung zuweisen.


## <a name="create-a-new-shipping-carrier"></a>Neuen Spediteur erstellen
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Spediteure" > "Spediteure".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Spediteur " einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie im Feld "Transportart" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Füllen Sie die allgemeinen Informationen für den Spediteur aus
1. Schalten Sie die Erweiterung des Abschnitts "Überblick" ein/aus.
2. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Spediteur aktivieren".
3. Klicken Sie im Feld "Händler" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie das Kreditorenkonto aus, das dem Spediteur zugeordnet werden soll.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Wählen Sie im Feld "Typ der Transportausschreibung" eine Option aus.
    * Wählen Sie "Manuell" aus, um die Seite "Transportausschreibung" zu verwenden, oder wählen Sie "EDI" aus, um das Zahlungsmittel zu aktualisieren, indem Sie elektronischen Datenaustausch (Electronic Data Interchange, EDI) verwenden.  
7. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Spediteursbewertung aktivieren".

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Erstellen Sie die erforderlichen Dienstleistungen für den Spediteur
1. Schalten Sie die Erweiterung des Abschnitts "Dienstleistungen" ein/aus.
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Spediteurdienstleistung " einen Wert ein.
5. Geben Sie im Feld "Name" einen Wert ein.
6. Klicken Sie im Feld "Transportmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Richten Sie die Adresse für den Spediteur ein (optional)
1. Schalten Sie die Erweiterung des Abschnitts "Adressen" ein/aus.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name oder Beschreibung" einen Wert ein.
4. Klicken Sie im Feld "Land/Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie im Feld "Postleitzahl" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Geben Sie im Feld "Straße" einen Wert ein.
10. Klicken Sie auf "OK".

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Richten Sie das Bewertungsprofil für den Spediteur ein.
1. Schalten Sie die Erweiterung des Abschnitts "Bewertungsprofile" ein/aus.
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Bewertungsprofil" einen Wert ein.
5. Geben Sie im Feld "Name" einen Wert ein.
6. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Klicken Sie im Feld "Tarifmodul" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie das Tarifmodul aus, das in Übereinstimmung mit dem Vertrag steht, den Sie mit dem Spediteur haben.  
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
15. Klicken Sie im Feld "Satzmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
16. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Klicken Sie im Feld "Transitzeitmodul" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
19. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
20. Klicken Sie auf "Speichern".


