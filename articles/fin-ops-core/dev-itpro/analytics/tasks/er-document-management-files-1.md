---
title: 'ER – Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Datenmodell vorbereiten)'
description: In diesem Artikel wird beschrieben, wie Sie ein elektronisches Berichtsformat (EB) für die Verwendung von Dokumentenverwaltungsdateien (Anhängen) in der EB-Ausgabe konfigurieren. (Teil 1)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable, ERSolutionCreateDropDialog
ms.openlocfilehash: f407555eca4c4bd08d09047e9d8f8512cb99d254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291023"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER – Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Datenmodell vorbereiten)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.

    Überprüfen Sie, ob "Litware, Inc." Anbieter ist verfügbar und markiert als aktiv.  

2. Wählen Sie den "Litware, Inc."- Anbieter.
3. Klicken Sie auf Repositorys.

    Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.  

4. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
5. Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.
6. Klicken Sie auf "Repository erstellen".
7. Klicken Sie auf "OK".

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Die Debitorenrechnungsmodell-Konfigurationen von Microsoft abrufen
1. Klicken Sie auf "Filter anzeigen".
2. Wenden Sie die nachfolgenden Filter an: Geben Sie den Filterwert "Operations-Ressourcen" im Feld " Name" ein, indem Sie den "beginnt mit"-Filteroperator verewnden; Geben Sie den Filterwert "" im Feld "Beschreibungs" ein, indem Sie den "beginnt mit"-Filteroperator verwenden.
3. Klicken Sie auf "Filter anzeigen".
4. Klicken Sie auf "Öffnen".
5. Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.

    Wählen Sie die Modellkonfiguration "Debitorenrechnungsmodell" aus, um sie zu importieren.  

6. Klicken Sie auf Import.

    Klicken Sie auf "Importieren" für Version 1 der ausgewählten Konfiguration.  

7. Klicken Sie auf "Ja".
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Klicken Sie auf "Berichterstellungskonfigurationen".
11. Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Erstellen Sie das abgeleitete Modell, um den Zugriff auf die Dokumentverwaltungsdateien zu unterstützen.
Sie erstellen eine eigene Konfiguration des Debitorenrechnungmodells, die von der Konfiguration von Microsoft abgeleitet ist. Sie verwenden diese Konfiguration, um den Zugriff auf die Dokumentverwaltungsdateien zu implementieren und diese für elektronische Dokumente bereitzustellen, die Sie auf Basis dieses Modell erstellen.  
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Neu" "Von Name 'Debitorenrechnungsmodell Microsoft' abgeleitet" ein.
3. Geben Sie im Feld "Name" "Debitorenrechnungsmodell (benutzerdefiniert)" ein.
4. Klicken Sie auf Konfiguration erstellen.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
