---
title: Richten Sie Voraussetzungen für die Qualitätsmangelverwaltung ein
description: Verwenden Sie dieses Thema, um Prozesse für das Nichtkonformitätsmanagement zu aktivieren.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c4de822dcda604241416165a961e4b0bacaeb5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428960"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Richten Sie Voraussetzungen für die Qualitätsmangelverwaltung ein

[!include [banner](../../includes/banner.md)]

Verwenden Sie dieses Thema, um Prozesse für das Nichtkonformitätsmanagement zu aktivieren. Ein Qualitätsmangel steht für eine Prozedur oder einen Artikel, bei dem ein Qualitätsproblem vorliegt; die beschreibenden Informationen enthalten die Quelle sowie die Art des Problems. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet. Normalerweise wird diese Prozedur von einem Qualitätsmanager ausgeführt.


## <a name="enable-quality-management-processes-within-the-company"></a>Aktivieren Sie Qualitätsmanagementprozesse innerhalb des Unternehmens
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Parameter für Lager- und Lagerortverwaltung**.
2. Wählen Sie die Registerkarte **Qualitätsmanagement**.
3. Wählen Sie **Ja** im Feld **Qualitätsmanagement verwenden**, um Qualitätsmanagementprozesse für das Unternehmen zu ermöglichen.
4. Geben Sie im Feld **Stundensatz** eine Zahl in Hauswährung ein. Der Stundensatz wird zur Berechnung der Kosten für Arbeitsgänge verwendet, die sich auf eine Nichtübereinstimmung beziehen. Der Stundensatz sowie die berechneten Kosten fungieren als Referenzinformationen für eine Nichtübereinstimmung und haben keinerlei Auswirkungen auf andere Funktionen.  
5. Wählen Sie **Berichtseinrichtung**, um die Notizarten für Qualitätsberichte zu definieren, die für verschiedene Arten von Qualitätsmanagementberichten verwendet werden sollen.

## <a name="enable-user-for-nonconformance-processing"></a>Aktivieren Sie den Benutzer für die Qualitätsmangelverarbeitung
1. Gehen Sie im Navigationsbereich zu **Module > Systemadministration > Benutzer > Benutzer**. 
2. Verwenden Sie den Schnellfilter, um den Benutzer zu finden, der die Fehlerprotokolle genehmigen oder ablehnen wird. Filtern Sie beispielsweise nach dem Feld **Name** mit dem Wert `Ricardo`. Um die Genehmigung einer Nichtkonformität zu bearbeiten, muss dem Benutzer, der Nichtkonformitäten genehmigt oder ablehnt, auf der Seite **Benutzer** ein Wert „Name“ zugewiesen werden. Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.  
3. Markieren Sie die Zeile des gewünschten Datensatzes.
4. Wählen Sie **Benutzeroptionen** aus.
5. Wählen Sie die Registerkarte **Voreinstellungen** aus.
6. Wählen Sie **Ja** im Feld **Dokumentbearbeitung aktivieren**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definieren Sie Diagnosetypen für die Qualitätsmangelverarbeitung
1. Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Qualitätsmanagement > Diagnosearten**. Verwenden Sie die Seite **Diagnosetypen**, um eine Klassifizierung von Diagnoseaktivitäten zu definieren. Durch eine Korrektur werden die Diagnoseaktivität für eine genehmigte Nichtübereinstimmung, die ausführende Person sowie das angeforderte und das voraussichtliche Abschlussdatum angegeben.  
2. Wählen Sie **Neu** aus.
3. Geben Sie in das Feld **Diagnose** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definieren Sie Belastungen für Qualität für die Qualitätsmangelverarbeitung
1. Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Qualitätsmanagement > Qualitätsgebühren**. Verwenden Sie die Seite **Qualitätsgebühren**, um eine Klassifizierung der Gebühren zu definieren, die bei Operationen im Zusammenhang mit Nichtkonformitäten verwendet werden.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Ladecode** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definieren Sie Arbeitsgänge für die Qualitätsmangelverarbeitung
1. Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Qualitätsmanagement > Betrieb**. Verwenden Sie die Seite **Operationen**, um eine Klassifizierung der Arbeiten zu definieren, die bei einer genehmigten Nichtkonformität durchgeführt werden können. Beim Zuordnen eines Arbeitsgangs zu einem Qualitätsmangel können auch ausführliche Informationen zum zugeordneten Material, zu Arbeitsstunden sowie zu sonstigen Zuschlägen definiert werden, die zum Ausführen des Arbeitsgangs erforderlich sind. Diese Informationen bilden die Grundlage für die Berechnung der vorkalkulierten Kosten, die sich für den Arbeitsgang ergeben.  
2. Wählen Sie **Neu** aus.
3. Geben Sie in das Feld **Operation** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definieren Sie Problemtypen für die Qualitätsmangelverarbeitung
1. Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Qualitätsmanagement > Problemtypen**. Verwenden Sie die Seite **Problemarten**, um eine Klassifizierung der Qualitätsprobleme zu definieren, die bei den verschiedenen Fehlertypen auftreten. Zu den Fehlertypen gehören **Intern**, **Kunde**, **Lieferant**, **Serviceanforderung**, **Produktion** und **Koppelproduktproduktion**. Ein einzelner Problemtyp kann mehreren Qualitätsmangeltypen zugeordnet werden.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Problemart** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie **Nichtkonformitätstypen**. Verwenden Sie die Seite **Nichtkonformitätstypen**, um die Verwendung eines Problemtyps für einen oder mehrere der Nichtkonformitätstypen zu erlauben. Beispiel: Ein Problemtyp für einen fehlerhaften Code kann für alle Nichtübereinstimmungstypen gelten, wohingegen ein Problemtyp für Debitorenbeschwerden möglicherweise lediglich für die Nichtübereinstimmungstypen "Debitor" und "Serviceanforderung" gelten soll.  
6. Wählen Sie **Neu** aus.
7. Wählen Sie im Feld **Nichtkonformitätstyp** der neuen Zeile eine Option aus.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definieren Sie Quarantänezonen für die Qualitätsmangelverarbeitung
1. Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Qualitätsmanagement > Quarantänezonen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Quarantänezone** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Schließen Sie die Seite.

