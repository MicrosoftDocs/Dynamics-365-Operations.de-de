---
title: Manuelle Verpackung einrichten (Februar 2016 und Mai 2016)
description: Der Verpackungsprozess ermöglicht es Ihnen, Produkte zu überprüfen und in Container zu verpacken.
author: Mirzaab
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbcd9653f2f3752f067828918ee61d96f9307c6d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576063"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a>Manuelle Verpackung einrichten (Februar 2016 und Mai 2016)

[!include [banner](../../includes/banner.md)]

Der Verpackungsprozess ermöglicht es Ihnen, Produkte zu überprüfen und in Container zu verpacken. In diesem Prozess entnehmen Lagerarbeiter Produkte aus den Speicherorten und verschieben diese zu einer Verpackungsanlage, in der sie die Artikelmengen und Typen überprüfen, und weisen diese den entsprechenden Containern zu. Wenn ein Container vollständig gepackt ist, können sie ihn schließen und zu den Ausgangsrampen verschieben, und die Produkte sind bereit zum liefern. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Diese Prozedur ist nur für die Dynamics 365 for Operations-Versionen Februar 2016 und Mai 2016 gedacht.


## <a name="set-up-location-profiles"></a>Lagerplatzprofile einrichten
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerort" > "Lagerplatzprofile".
2. Klicken Sie auf "Neu".
    * Das Lagerplatzprofil wird für Verpackungsanlagen verwendet und enthält Informationen und Regeln für einen Lagerplatz.  
3. Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Lagerplatzformat" einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Lagerplatztyp" einen Wert ein, oder wählen Sie einen Wert aus.
7. Wählen Sie "Ja" im Feld "Gemischte Artikel zulassen" aus.
8. Wählen Sie "Ja" im Feld "Gemischte Bestandstatus zulassen" aus.
9. Wählen Sie "Ja" im Feld "Überschreibungsregeln für Chargentage" aus.
10. Schließen Sie die Seite.

## <a name="set-up-warehouse-management-parameters"></a>Richten Sie Parameter für Lagerortverwaltung ein 
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".
2. Klicken Sie auf die Registerkarte "Verpackung".
3. Geben Sie im Feld "Profilkennung für Verpackungslagerplatz" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie das Lagerplatzprofil aus, das Sie für das Packen verwenden möchten.  
4. Schließen Sie die Seite.

## <a name="set-up-container-types"></a>Richten Sie Containertypen ein
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containertypen".
2. Klicken Sie auf "Neu".
    * Sie können die Containertypen, die verwendet werden sollen, definieren. Sie können die physischen Dimensionen des Containers angeben, einschließlich Verpackungsgewicht, Höchstgewicht, maximales Volumen, Länge, Breite und Gewicht.  Die Attribute sind angepasste Felder, die es Ihnen ermöglichen, zusätzliche Dimensionen zum Containertyp hinzuzufügen.     
3. Geben Sie im Feld "Containertypcode" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.
6. Geben Sie im Feld "Höchstgewicht" eine Zahl ein.
7. Geben Sie im Feld "Volumen" eine Zahl ein.
8. Geben Sie im Feld Länge eine Zahl ein.
9. Geben Sie im Feld "Breite" eine Zahl ein.
10. Geben Sie im Feld "Höhe" eine Zahl ein.
11. Klicken Sie auf "Speichern".
12. Schließen Sie die Seite.

## <a name="set-up-packing-profiles"></a>Richten Sie Verpackungsprofile ein
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Verpackung" > "Verpackungsprofile".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Verpackungsprofilkennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Containerabschlussprofil-Kennung" einen Wert ein, oder wählen Sie einen Wert aus.
    * Eine Containerabschlussprofil-Kennung ist optional und ist das standardmäßige Profil zum Abschließen von Containern für dieses Verpackungsprofil.  
6. Wählen Sie im Feld "Containerkennungsmodus" eine Option aus.
    * Diese Option bestimmt, ob eine Containerkennung automatisch generiert wird, wenn ein Container erstellt wird, oder eine Containerkennung wird manuell erstellt.  
7. Geben Sie im Feld "Containertyp" einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Containertyp wird standardmäßig verwendet, wenn ein neuer Container erstellt wird.  
8. Aktivieren Sie das Kontrollkästchen "Container beim Schließen des Containers automatisch erstellen".
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.

## <a name="set-up-container-closing-profiles"></a>Richten Sie Containerabschlussprofile ein
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containerabschlussprofile".
    * Containerabschlussprofile definieren, was passiert, wenn ein Container geschlossen wird. Sie können mehrere Profile zum Abschließen von Containern einrichten.       
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Containerabschlussprofil-Kennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Manifestieren" eine Option aus.
    * Geben Sie an, ob Manifestierung geschieht, wenn Sie Container schließen oder wenn Sie die Lieferung bestätigen. Beachten Sie, dass eine Manifestierung "Transportverwaltung" benötigt. Manifestierung muss in den Transportmodulen implementiert werden, damit sie funktioniert.  
6. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
7. Geben Sie im Feld "Standardlagerplatz für letzte Lieferung" einen Wert ein, oder wählen Sie einen Wert aus.
    * Dies ist der Lagerplatz, zu dem Produkte verschoben werden, nachdem die Container geschlossen sind. Dieser Lagerplatz muss ein Lagerplatzprofil haben, das auf Lagerortparametern definiert ist.  
8. Geben Sie im Feld "Gewichtseinheit" einen Wert ein, oder wählen Sie einen Wert aus.
9. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]