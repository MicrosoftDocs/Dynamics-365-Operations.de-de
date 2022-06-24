---
title: Arbeitskräfte, die für die Genehmigung von Qualitätsmängeln verantwortlich sind
description: Dieser Artikel beschreibt, wie Sie Arbeitskräfte konfigurieren, die für die Genehmigung von Qualitätsmängeln zuständig sind.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a108fc1f8954e32719c93656a64d1d27fda03fb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907405"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Arbeitskräfte, die für die Genehmigung von Qualitätsmängeln verantwortlich sind

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Arbeitskräfte konfigurieren, die für die Genehmigung von Qualitätsmängeln zuständig sind.

Qualitätsmängel müssen genehmigt werden, bevor Benutzer mit der Eingabe von Details wie Korrekturen oder Vorgängen beginnen können. Bevor Benutzer Qualitätsmängel genehmigen oder ablehnen können, muss ihre Benutzer-ID (Benutzer-Datensatz) mit einem worker-Datensatz verknüpft sein. Sie können optional Arbeitskräfte konfigurieren, die für die Qualität verantwortlich sind und dann zulassen, dass eine Arbeitskraft die Arbeit im Namen einer anderen Arbeitskraft genehmigt.

## <a name="enable-a-user-for-nonconformance-processing"></a>Aktivieren Sie einen Benutzer für die Verarbeitung von Qualitätsmängeln

Bevor ein Benutzer Qualitätsmängel genehmigen oder ablehnen kann, müssen Sie seinen Datensatz mit einem worker-Datensatz verknüpfen. Die Genehmigungsfelder können dann automatisch festgelegt werden, und der aktuelle Benutzer kann automatisch für den Stundenzettel ausgefüllt werden. Bevor der Benutzer die Dokumentennotizen verwenden kann, müssen Sie die Dokumentenbearbeitung in seinen Benutzeroptionen aktivieren.

1. Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.
1. Suchen und öffnen Sie den Benutzer, der in der Lage sein soll, Qualitätsmängel zu genehmigen oder abzulehnen.
1. Legen Sie das Feld **Person** auf den Namen der Arbeitskraft fest, die mit dem aktuellen Datensatz des Benutzers verbunden ist.
1. Wählen Sie im Aktivitätsbereich **Benutzeroptionen**.
1. Legen Sie auf der Seite **Optionen** für den aktuellen Datensatz auf der Registerkarte **Einstellungen** die Option **Dokumentenbehandlung aktivieren** auf *Ja* fest.
1. Schließen Sie die Seiten.

## <a name="define-workers-that-are-responsible-for-quality"></a>Definieren Sie Arbeitskräfte, die für die Qualität verantwortlich sind

1. Übergehen zu **Bestandsmanagement \> Einrichten \> Qualitätskontrolle \> Qualitätsverantwortliche Arbeitskräfte**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Arbeiter** die Arbeitskraft aus, die Qualitätsdaten eingibt.
4. Wählen Sie im Feld **Verantwortliche Arbeitskraft** die Arbeitskraft aus, für die die ausgewählte Arbeitskraft die Arbeit eingibt. Wenn Qualitätsmängel erstellt und aktualisiert werden, wird diese Arbeitskraft standardmäßig in die Felder **Arbeiter** eingetragen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Belastungen für Qualität](quality-charges.md)
- [Quarantänezonen für Qualitätsmängel](quality-quarantine-zones.md)
- [Diagnosetypen für Qualitätsmängel](quality-diagnostic-types.md)
- [Qualitätsbelastungen für Qualitätsmängel](quality-charges.md)
- [Vorgänge für Qualitätsmängel](quality-operations.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
