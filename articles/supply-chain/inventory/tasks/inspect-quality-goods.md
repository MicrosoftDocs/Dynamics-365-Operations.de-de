---
title: Qualität der Waren inspizieren
description: Diese Prozedur zeigt, wie ein Qualitätsprüfungsauftrag bearbeitet wird.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545404"
---
# <a name="inspect-the-quality-of-goods"></a>Qualität der Waren inspizieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie ein Qualitätsprüfungsauftrag bearbeitet wird. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Bevor Sie diese Beispielprozedur beginnen, müssen Sie Bestellung "000016 " bestätigen und einen Produktzugang buchen. Dies erstellt automatisch einen Qualitätsprüfungsauftrag. Qualitätsinspektionen werden normalerweise von einem Sachbearbeiter für die Qualitätskontrolle ausgeführt.


## <a name="select-a-quality-order"></a>Wählen Sie einen Qualitätsprüfungsauftrag aus.
1. Gehen Sie zu "Lagerverwaltung" > "Periodische Aufgaben" > "Qualitätsmanagement" > "Qualitätsprüfungsaufträge".
2. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den Qualitätsprüfungsauftrag, der erstellt wurde, bevor Sie dieses Verfahren gestartet haben.  

## <a name="record-test-results"></a>Erfassen von Testergebnissen
1. Klicken Sie auf "Ergebnis".
2. Klicken Sie auf "Bearbeiten".
3. Geben Sie im Feld "Ergebnismenge" eine Zahl ein.
4. Markieren Sie in der Liste die ausgewählte Zeile.
5. Klicken Sie im Feld "Ergebnis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * In diesem Beispiel basiert das Ergebnis auf einem vordefinierten Ergebnis. Normalerweise erfassen Sie ein spezifischeres Testergebnis, z. B. eine Größe oder eine andere Dimension.  
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.

## <a name="validate-the-quality-order"></a>Qualitätsprüfungsauftrag überprüfen
1. Klicken Sie auf "Überprüfen".
2. Klicken Sie im Feld "Überprüft von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den Benutzer aus, der die Inspektion ausführt.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf Auswählen.
5. Klicken Sie auf "OK".
6. Schließen Sie die Seite.

