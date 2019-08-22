---
title: Arbeitspläne erstellen (Februar 2016)
description: Diese Aufgabe konzentriert sich auf das Erstellen der Produktionsarbeitspläne für ein fertiges Produkt und ein halbfertiges Produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844560"
---
# <a name="create-routes-february-2016"></a>Arbeitspläne erstellen (Februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabe konzentriert sich auf das Erstellen der Produktionsarbeitspläne für ein fertiges Produkt und ein halbfertiges Produkt. Es ist die fünfte Aufgabe in der Stücklistenberechnungsserie. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Arbeitsplan für ein halbfertiges Produkt erstellen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Artikelnummer BOM_2 aus.  
3. Klicken Sie im Aktivitätsbereich auf "Entwickler".
4. Klicken Sie auf "Arbeitsplan".
5. Klicken Sie auf "Neu".
6. Klicken Sie auf Arbeitsplan und Arbeitsplanversion.
7. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Geben Sie beispielsweise ROUTE_2 ein.  
8. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.  
9. Klicken Sie auf "OK".
10. Klicken Sie auf "Neu".
11. Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Zusammenstellung” aus.  
12. Geben Sie im Feld "Laufzeit" eine Zahl ein.
    * Geben Sie beispielsweise "1" ein. Ausführungszeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.  
13. Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „STD” aus.  
14. Klicken Sie auf die Registerkarte "Einstellungen".
15. Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Zusammenstellung” aus.  
16. Klicken Sie auf die Registerkarte 'Zeiten'.
17. Geben Sie im Feld „Rüstzeit” eine Zahl ein.
    * Geben Sie für dieses Beispiel 1 ein. Rüstzeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.  
18. Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.
19. Klicken Sie auf Genehmigen.
20. Wählen Sie „Ja” aus in „Möchten Sie auch den Arbeitsplan genehmigen?”.
21. Klicken Sie auf "OK".
22. Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.
23. Klicken Sie auf Aktivieren.
24. Schließen Sie die Seite.
25. Schließen Sie die Seite.

## <a name="create-a-route-for-a-finished-product"></a>Arbeitsplan für ein fertiges Produkt erstellen
1. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Artikelnummer BOM_1 aus.  
2. Klicken Sie im Aktivitätsbereich auf "Entwickler".
3. Klicken Sie auf "Arbeitsplan".
4. Klicken Sie auf "Neu".
5. Klicken Sie auf Arbeitsplan und Arbeitsplanversion.
6. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Geben Sie für dieses Beispiel ROUTE_1 ein.  
7. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie für dieses Beispiel „Standort 1” ein oder wählen Sie ihn aus.  
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Neu".
10. Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Verpackung” aus.  
11. Geben Sie im Feld "Laufzeit" eine Zahl ein.
    * Geben Sie für dieses Beispiel 1 ein.  
12. Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „STD” aus.  
13. Klicken Sie auf die Registerkarte "Einstellungen".
14. Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie für dieses Beispiel „Verpackung” aus.  
15. Klicken Sie auf die Registerkarte 'Zeiten'.
16. Geben Sie im Feld „Rüstzeit” eine Zahl ein.
    * Geben Sie für dieses Beispiel 1 ein.  
17. Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.
18. Klicken Sie auf Genehmigen.
19. Klicken Sie auf "OK".
20. Klicken Sie im Aktivitätsbereich auf „Arbeitsplanversion”.
21. Klicken Sie auf Aktivieren.
22. Schließen Sie die Seite.
23. Schließen Sie die Seite.

## <a name="enable-automatic-consumption-of-setup-time"></a>Automatischen Verbrauch der Rüstzeit aktivieren
1. Wechseln Sie zu „Produktionssteuerung” > „Einrichten”  >„Arbeitspläne” > „Arbeitsplangruppen”.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie STD in der Liste aus.  
3. Klicken Sie auf "Bearbeiten".
4. Wählen Sie „Ja” im Feld „Rüstzeit” aus.
    * Rüstzeiten sind oft Teil des Preises, der für einen Artikel berechnet wurde.  
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.

