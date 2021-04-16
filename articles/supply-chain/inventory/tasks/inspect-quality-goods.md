---
title: Qualität der Waren inspizieren
description: In diesem Thema wird erläutert, wie Sie einen Qualitätsprüfungsauftrag verarbeiten.
author: perlynne
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47e7156e5c57d5f983564cc966b4108f1180ff8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825914"
---
# <a name="inspect-the-quality-of-goods"></a>Qualität der Waren inspizieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Qualitätsprüfungsauftrag verarbeiten. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Bevor Sie diese Beispielprozedur beginnen, müssen Sie Bestellung „000016“ bestätigen und einen Produktzugang buchen. Dies erstellt automatisch einen Qualitätsprüfungsauftrag. Qualitätsinspektionen werden normalerweise von einem Sachbearbeiter für die Qualitätskontrolle ausgeführt.


## <a name="select-a-quality-order"></a>Wählen Sie einen Qualitätsprüfungsauftrag aus.
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Periodische Aufgaben > Qualitätsmanagement > Qualitätsprüfungsaufträge**.
2. Wählen Sie den Qualitätsprüfungsauftrag, der erstellt wurde, bevor Sie dieses Verfahren gestartet haben.  

## <a name="record-test-results"></a>Erfassen von Testergebnissen
1. Wählen Sie **Ergebnisse** aus.
2. Wählen Sie **Bearbeiten** aus.
3. Geben Sie im Feld **Ergebnismenge** eine Zahl ein.
4. Wählen Sie im Feld **Ergebnis** den gewünschten Datensatz im Dropdownmenü aus.  
- In diesem Beispiel basiert das Ergebnis auf einem vordefinierten Ergebnis. Normalerweise erfassen Sie ein spezifischeres Testergebnis, z. B. eine Größe oder eine andere Dimension.  
5. Wählen Sie **Speichern**.
6. Schließen Sie die Seite.

## <a name="validate-the-quality-order"></a>Qualitätsprüfungsauftrag überprüfen
1. Wählen Sie **Überprüfen** aus.
2. Wählen Sie im Feld **Geprüft von** im Dropdownfeld den Benutzer aus, der die Prüfung ausführt.  
3. Klicken Sie auf **Auswählen**.
4. Wählen Sie **OK**.
5. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]