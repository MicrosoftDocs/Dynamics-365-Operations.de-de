---
title: Ermöglicht Qualitäts- und Qualitätsmangel-Management
description: Dieser Artikel bietet einen Überblick über den Prozess zum Einrichten und Konfigurieren der Funktionen zum Management von Qualitätsmängeln und Abweichungen in Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66229e3692e87f774c553eae955794330602598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874042"
---
# <a name="enable-quality-and-nonconformance-management"></a>Ermöglicht Qualitäts- und Qualitätsmangel-Management

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet einen Überblick über den Prozess zum Einrichten und Konfigurieren der Funktionen zum Management von Qualitätsmängeln und Abweichungen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Qualitäts- und Qualitätsmangel-Management aktivieren

Führen Sie diese Schritte aus, um das Qualitätsmanagement auf Ihrem System zu aktivieren.

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Parameter für Lager- und Lagerortverwaltung**.
1. Legen Sie auf der Registerkarte **Qualitätsmanagement** die Option **Qualitätsmanagement verwenden** auf *Ja* fest.
1. Geben Sie im Feld **Stundensatz** einen Arbeitsstundensatz in lokaler Währung ein. Der Stundensatz wird zur Berechnung der Kosten für Arbeitsgänge verwendet, die sich auf einen Qualitätsmangel beziehen. Der Stundensatz sowie die berechneten Kosten fungieren als Referenzinformationen für einen Qualitätsmangel. Sie interagieren nicht mit anderen Funktionen.
1. Wählen Sie **Bericht einrichten**.
1. Fügen Sie neue Zeilen für die verschiedenen Berichtstypen hinzu und wählen Sie die Art des Dokuments, das für jeden Bericht verwendet werden soll.
1. Schließen Sie die Seite.
1. Schließen Sie die Seite.

## <a name="quality-management-configuration-process"></a>Qualitätsmanagement Konfigurationsprozess

Bevor Sie beginnen können, die Funktionen des Qualitätsmanagements zu verwenden und Qualitätsprüfungsaufträge zu generieren, müssen Sie das System und die Voraussetzungen konfigurieren. Hier finden Sie eine Liste der Schritte, die für die Konfiguration des Qualitätsmanagements erforderlich sind.

1. [Qualitäts- und Qualitätsmangel-Management aktivieren](#enable-qm).
1. Optional: [Konfigurieren Sie Prüfgeräte](quality-test-instruments.md).
1. [Konfigurieren Sie Tests](quality-tests.md).
1. [Konfigurieren Sie Test-Variablen und -Ergebnisse](quality-test-variables.md).
1. [Konfigurieren Sie Testgruppen](quality-test-groups.md).
1. Optional: [Konfigurieren Sie Qualitätsgruppen, und verknüpfen Sie sie mit Produkten](quality-groups.md).
1. Optional: [Qualitätszuordnungen konfigurieren](quality-associations.md).

Nachdem die Konfiguration abgeschlossen ist, können Sie damit beginnen, Qualitätsprüfungsaufträge zu erstellen und zu verarbeiten. Weitere Informationen zum Erstellen und Arbeiten mit Qualitätsprüfungsaufträgen finden Sie unter [Qualitätsprüfungsaufträge](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Konfigurationsprozess für das Qualitätsmangel-Management

Bevor Sie beginnen können, die Funktionen zur Verwaltung von Qualitätsmängeln zu verwenden und Qualitätsmängel zu erzeugen, müssen Sie das System und die Voraussetzungen konfigurieren. Hier ist eine Liste der Schritte, die zur Konfiguration des Qualitätsmangels erforderlich sind.

1. [Qualitäts- und Qualitätsmangel-Management aktivieren](#enable-qm).
1. [Konfigurieren Sie Worker, die für die Genehmigung von Qualitätsmängeln zuständig sind](quality-responsible-workers.md).
1. [Konfigurieren Sie Problemtypen](quality-problem-types.md).
1. [Konfigurieren Sie Quarantänezonen](quality-quarantine-zones.md).
1. [Konfigurieren Sie Diagnosetypen](quality-diagnostic-types.md).
1. [Vorgänge konfigurieren](quality-operations.md).
1. Optional: [Konfigurieren Sie Qualitätsbelastungen](quality-charges.md).

Nachdem die Konfiguration abgeschlossen ist, können Sie beginnen, Qualitätsmängel zu erstellen und zu verarbeiten. Weitere Informationen über das Erstellen und Verarbeiten von Qualitätsmängeln finden Sie unter [Erstellen und Verarbeiten von Qualitätsmängeln](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
