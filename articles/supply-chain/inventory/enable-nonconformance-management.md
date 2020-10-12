---
title: Qualitätsmangel-Verwaltung
description: In diesem Artikel werden die Basiseinstellungen beschrieben, die erforderlich sind, um Qualitätsmängel zu verwenden. Zusätzliche Einstellungen sind erforderlich, wenn Sie Testbestellungen verwenden möchten.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e66353dc3a4b4b7d9ff3c5f63bf3d4b0c70bda0
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829704"
---
# <a name="nonconformance-management"></a>Qualitätsmangel-Verwaltung

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Basiseinstellungen beschrieben, die erforderlich sind, um Qualitätsmängel zu verwenden. Zusätzliche Einstellungen sind erforderlich, wenn Sie Testbestellungen verwenden möchten.

Um die Verwaltung von Qualitätsmängeln zu aktivieren, führen Sie die folgenden Schritte aus:

1.  Definieren Sie die Bestands- und Lagerparameter, die sich auf Qualitätsmängel beziehen:
    -   Setzen Sie die Option **Qualitätsmanagement verwenden** auf **Ja**.
    -   Geben Sie im Feld **Stundensatz** einen Arbeitsstundensatz in lokaler Währung ein. Der Stundensatz wird zur Berechnung der Kosten für Arbeitsgänge verwendet, die sich auf einen Qualitätsmangel beziehen. Der Stundensatz sowie die berechneten Kosten fungieren als Referenzinformationen für einen Qualitätsmangel. Sie interagieren nicht mit anderen Funktionen.
    -   Auf der Registerkarte **Qualitätsmanagement** auf der Seite **Berichteinstellung** definiueren Sie den Dokumenttyp, der gedruckt werden soll. Sie können einen Nichtübereinstimmungsbericht, eine Nichtübereinstimmungsmarkierung oder einen Korrekturbericht drucken. Sie können mehrere Datensätze definieren, um unterschiedliche Dokumenttypen für einen Bericht bzw. interne oder externe Hinweise zu drucken. Eventuell hilft es, mithilfe der Seite **Dokumenttyp** einen eindeutigen Dokumenttyp für Qualitätsmängel sowie einen eindeutigen Dokumenttyp für Korrekturen zu definieren. Beispielsweise könnten Sie Hinweise zu einem Qualitätsmangel eingeben, indem Sie den eindeutigen Dokumenttyp für Qualitätsmängel verwenden. In diesem Fall kennzeichnen Sie den eindeutigen Dokumenttyp in den Berichtsoptionen.
    -   Aktivieren Sie Nummernkreise für Qualitätsmängel und Korrekturreferenzen.

2.  Aktivieren Sie die Benutzergenehmigung für einen Qualitätsmangel. Weisen Sie mithilfe des Felds **Name** auf der Seite **Benutzer** jedem Benutzer, von dem Qualitätsmängel genehmigt werden müssen, einen Mitarbeiter zu. Das System verwendet die Mitarbeiter, die den Status eines Qualitätsmangels ändern, um die Qualitätsmängelhistorie zu verfolgen. Benutzer können einen Qualitätsmangel nicht genehmigen, es sei denn, dass ihnen eine Mitarbeiterkennung zugewiesen wurde.
3.  Definieren Sie die Problemtypen, die Nichtübereinstimmungen zugewiesen werden. Verwenden Sie die Seite **Problemtypen**, um eine Klassifizierung der Qualitätsprobleme zu definieren, die für die verschiedenen Nichtübereinstimmungstypen auftreten. Sie können die folgenden Nichtübereinstimmungstypen einrichten: **Intern**, **Debitor**, **Kreditor**, **Serviceanforderung**, **Produktion** und **Co-Produkt- Produktion**. Verwenden Sie das Formular **Nichtübereinstimmungstypen**, um die Nutzung eines Problemtyps in einem oder mehreren Nichtübereinstimmungstypen zu ermöglichen. Beispiel: Ein Problemtyp für einen fehlerhaften Code kann für alle Nichtübereinstimmungstypen gelten, wohingegen ein Problemtyp für Debitorenbeschwerden möglicherweise lediglich für die Nichtübereinstimmungstypen **Debitor** und **Serviceanforderung** gelten soll.
4.  Definieren Sie die Quarantänezonen für den Umgang mit fehlerhaftem Material. Verwenden Sie die Seite **Quarantänezonen**, um Zonen zu definieren, die einer Nichtübereinstimmung zugewiesen werden können. Zur Regelung der Handhabung von fehlerhaftem Material sind die zugewiesene Quarantänezone und Informationen zur Verwendbarkeit aus der ausgedruckten Nichtübereinstimmungsmarkierung ersichtlich. Die Zonen können ggf. Lagerplätzen für Lagerbestand oder betrieblichen Ressourcen entsprechen.
5.  Definieren Sie die Diagnosetypen, die Korrekturen zugewiesen werden. Verwenden Sie die Seite **Diagnosetypen**, um eine Klassifizierung von Diagnoseaktivitäten zu definieren. Durch eine Korrektur werden die Diagnoseaktivität für eine genehmigte Nichtübereinstimmung sowie die ausführende Person angegeben. Außerdem werden das angeforderte und das geplante Abschlussdatum angezeigt.
6.  Definieren Sie die zugehörigen Arbeitsgänge, die Qualitätsmängeln zugewiesen werden. Definieren Sie mithilfe der Seite **Zugehörige Arbeitsgänge** eine Klassifizierung der Arbeiten, die für eine genehmigte Nichtübereinstimmung ausgeführt werden können. Beim Zuweisen eines zugehörigen Arbeitsgangs zu einer Nichtübereinstimmung können auch ausführliche Informationen, wie z. B. zum zugeordneten Material, zu Arbeitsstunden sowie zu sonstigen Zuschlägen definiert werden, die zum Ausführen des Arbeitsgangs erforderlich sind. Diese Informationen werden verwendet, um vorkalkulierte Kosten für den Arbeitsgang zu berechnen. Die ausführlichen Informationen sowie die vorkalkulierten Kosten dienen lediglich zu Referenzzwecken. Die zugehörigen Arbeitsgänge für die Qualität unterscheiden sich von den Arbeitsgängen, die für einen Produktionsarbeitsplan definiert werden können.


<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Übereinstimmung erstellen und verarbeiten](tasks/create-process-non-conformance.md)

[Qualitätsmanagementprozesse](quality-management-processes.md)

[Richten Sie Voraussetzungen für die Qualitätsmangelverwaltung ein](tasks/set-up-prerequisites-nonconformance-management.md)
