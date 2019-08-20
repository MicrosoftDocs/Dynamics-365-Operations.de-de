---
title: Richten Sie Voraussetzungen für die Qualitätsmangelverwaltung ein
description: Verwenden Sie diese Prozedur, um Qualitätsmangelmanagementprozesse zu aktivieren.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9094be37e44b978db224b16c255d04a36c5cefff
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845324"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Richten Sie Voraussetzungen für die Qualitätsmangelverwaltung ein

[!include [task guide banner](../../includes/task-guide-banner.md)]

Verwenden Sie diese Prozedur, um Qualitätsmangelmanagementprozesse zu aktivieren. Ein Qualitätsmangel steht für eine Prozedur oder einen Artikel, bei dem ein Qualitätsproblem vorliegt; die beschreibenden Informationen enthalten die Quelle sowie die Art des Problems. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet. Normalerweise wird diese Prozedur von einem Qualitätsmanager ausgeführt.


## <a name="enable-quality-management-processes-within-the-company"></a>Aktivieren Sie Qualitätsmanagementprozesse innerhalb des Unternehmens
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Lager- und Lagerortverwaltungsparameter".
2. Klicken Sie auf die Registerkarte "Qualitätsmanagement".
3. Wählen Sie "Ja" im Feld "Qualitätsmanagement verwenden" aus.
    * Wählen Sie diesen Parameter aus, um Qualitätsmanagementprozesse für das Unternehmen zu aktivieren.  
4. Geben Sie im Feld "Stundensatz" eine Zahl ein.
    * Geben Sie im Feld "Stundensatz" einen Arbeitsstundensatz in lokaler Währung ein. Der Stundensatz wird zur Berechnung der Kosten für Arbeitsgänge verwendet, die sich auf eine Nichtübereinstimmung beziehen. Der Stundensatz sowie die berechneten Kosten fungieren als Referenzinformationen für eine Nichtübereinstimmung und haben keinerlei Auswirkungen auf andere Funktionen.  
5. Klicken Sie auf "Berichtseinstellungen".
    * Diese Seite ermöglicht es Ihnen, die Qualitätsberichts-Hinweistypen zu definieren, die für verschiedene Arten von Qualitätsmanagementberichten verwendet werden.  
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.

## <a name="enable-user-for-nonconformance-processing"></a>Aktivieren Sie den Benutzer für die Qualitätsmangelverarbeitung
1. Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".
    * Um die Genehmigung eines Qualitätsmangels zu verarbeiten, muss der Benutzer, der die Qualitätsmängel genehmigt oder ablehnt, veranlassen, dass ein Wert "Name" der Seite "Benutzer" zugewiesen wird. Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.  
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Name" mit dem Wert "Ricardo".
    * Verwenden Sie den Filter, um den Benutzer zu suchen, der die Qualitätsmangeldatensätze genehmigt oder ablehnt.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Um die Genehmigung eines Qualitätsmangels zu verarbeiten, stellen Sie sicher, dass der Benutzer, der die Qualitätsmängel genehmigt oder ablehnt, veranlasst, dass ein Wert "Name" der Seite "Benutzer" zugewiesen wird.  
4. Klicken Sie auf "Benutzeroptionen".
5. Klicken Sie auf die Registerkarte "Einstellungen".
6. Wählen Sie "Ja" im Feld "Handhabung von Dokumenten aktivieren" aus.
    * Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.  
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definieren Sie Diagnosetypen für die Qualitätsmangelverarbeitung
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätsmanagement" > "Diagnosetypen".
    * Verwenden Sie die Seite Diagnosetypen, um eine Klassifizierung von Diagnoseaktivitäten zu definieren. Durch eine Korrektur werden die Diagnoseaktivität für eine genehmigte Nichtübereinstimmung, die ausführende Person sowie das angeforderte und das voraussichtliche Abschlussdatum angegeben.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Diagnose" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Schließen Sie die Seite.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definieren Sie Belastungen für Qualität für die Qualitätsmangelverarbeitung
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätsmanagement" > "Belastungen für Qualität".
    * Verwenden Sie die Seite "Belastungen für Qualität", um eine Klassifizierung von Belastungen zu definieren, die in Arbeitsgängen verwendet werden, die sich auf Qualitätsmängel beziehen.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Belastungen" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Schließen Sie die Seite.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definieren Sie Arbeitsgänge für die Qualitätsmangelverarbeitung
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätsmanagement" > "Arbeitsgänge".
    * Definieren Sie mithilfe der Seite "Arbeitsgänge" eine Klassifizierung der Arbeit, die für einen genehmigten Qualitätsmangel ausgeführt werden kann. Beim Zuordnen eines Arbeitsgangs zu einem Qualitätsmangel können auch ausführliche Informationen zum zugeordneten Material, zu Arbeitsstunden sowie zu sonstigen Zuschlägen definiert werden, die zum Ausführen des Arbeitsgangs erforderlich sind. Diese Informationen bilden die Grundlage für die Berechnung der vorkalkulierten Kosten, die sich für den Arbeitsgang ergeben.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Arbeitsgang" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Schließen Sie die Seite.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definieren Sie Problemtypen für die Qualitätsmangelverarbeitung
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätsmanagement" > "Problemtypen".
    * Verwenden Sie die Seite "Problemtypen", um eine Klassifizierung der Qualitätsprobleme zu definieren, die in den verschiedenen Qualitätsmängeln auftreten. Zu den Qualitätsmangeltypen gehören "Intern", "Debitor", "Händler", "Serviceanforderung", "Produktion" und "Co-Produkt-Produktion". Ein einzelner Problemtyp kann mehreren Qualitätsmangeltypen zugeordnet werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Problemtyp" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Nichtübereinstimmungstypen".
    * Verwenden Sie die Seite "Nichtübereinstimmungstypen", um die Nutzung eines Problemtyps für einen oder mehrere Qualitätsmangeltypen zu autorisieren. Beispiel: Ein Problemtyp für einen fehlerhaften Code kann für alle Nichtübereinstimmungstypen gelten, wohingegen ein Problemtyp für Debitorenbeschwerden möglicherweise lediglich für die Nichtübereinstimmungstypen "Debitor" und "Serviceanforderung" gelten soll.  
6. Klicken Sie auf "Neu".
7. Markieren Sie in der Liste die ausgewählte Zeile.
8. Wählen Sie im Feld "Nichtübereinstimmungstyp" eine Option aus.
9. Schließen Sie die Seite.
10. Schließen Sie die Seite.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definieren Sie Quarantänezonen für die Qualitätsmangelverarbeitung
1. Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätsmanagement" > "Quarantänezonen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Quarantänezone" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Schließen Sie die Seite.

