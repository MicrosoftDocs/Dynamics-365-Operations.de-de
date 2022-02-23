---
title: Satzmaster einrichten
description: Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429165"
---
# <a name="set-up-rate-masters"></a>Satzmaster einrichten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird. Der Logistik-Manager legt normalerweise Satzmaster fest, abhängig von Verträgen mit den Spediteuren. In diesem Szenario richten Sie einen Satzmaster für eine Luftfahrtgesellschaft ein. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

## <a name="set-up-break-master"></a>Festlegen des Breakmasters

1. Gehen Sie zu **Transportverwaltung > Einrichten > Bewertung > Breakmaster**. Pausenmaster werden verwendet, um die Preisgestaltungsstruktur und die Breakpoints zu definieren. Die Preisgestaltungsstruktur verwendet abgestufte Preisgestaltung auf Grundlage der physischen Dimensionen.  
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Breakmaster** einen Wert ein.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Wählen Sie im Feld **Datentyp** den Datentyp.
1. Geben Sie im Feld **Vergleich** die Art des gewünschten Vergleichs ein (mit Operatoren).
1. Geben Sie im Feld **Aufteilungseinheit** die Aufteilungseinheit ein.
1. Erstellen Sie im Bereich **Details** so viele Breaks, wie für die Preisstruktur benötigt werden.
1. Wählen Sie **Speichern** aus.

## <a name="set-up-rate-master"></a>Satzmaster einrichten

1. Gehen Sie zu **Transportverwaltung > Einrichten > Tarif > Tarifmaster**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Ratemaster** einen Wert ein.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Wählen Sie im Feld **Bewertungs-Metadaten-ID** die Dropdown-Schaltfläche, um den Lookup zu öffnen. Die Rating-Metadaten-ID bestimmt die Daten, die für den Tarifmaster benötigt werden, da sie die Metadaten definiert, die von der Engine der Transportverwaltung erwartet werden, die diesen Tarifmaster verwendet.  
1. Wählen Sie für dieses Beispiel die Option P2P. Diese ist bereits in den Demodaten definiert.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie **Speichern** aus.

## <a name="set-up-rate-base"></a>Satzbasis einrichten

1. Wählen Sie **Tarifbasis**.
    * Die Satzbasis bestimmt den Satz des Spediteurs und kann verwendet werden, um eine Tarifstruktur einzurichten, da sie die Sätze in den Breakpoints strukturiert, die im Pausenmaster definiert werden.  
2. Wählen Sie **Neu** aus.
3. Geben Sie in das Feld **Tarifbasis** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie im Feld **Breakmaster** die Dropdown-Schaltfläche, um das Lookup zu öffnen.
    * Pausenmaster werden verwendet, um die Preisgestaltungsstruktur und die Breakpoints zu definieren. Die Preisgestaltungsstruktur verwendet abgestufte Preisgestaltung auf Grundlage der physischen Dimensionen.  
6. Verwenden Sie für dieses Beispiel Gewicht. Diese ist bereits in den Demodaten definiert.
7. Wählen Sie in der Liste die Verknüpfung in der markierten Zeile.
8. Erweitern Sie den Bereich **Details**.
9. Wählen Sie **Neu** aus.
10. Geben Sie in das Feld **Lieferungs-Postleitzahl von** „30301“ ein.
11. Geben Sie in das Feld **Lieferungs-Postleitzahl bis** „30318“ ein.
12. Geben Sie in das Feld **Lieferungsland Region** „USA“ ein.
13. Geben Sie in das Feld **<1,00 kg** „100“ ein.
    * Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 1 Kilogramm beträgt.  
14. Geben Sie in das Feld **<5,00 kg** „300“ ein.
    * Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 5 Kilogramm beträgt.  
15. Geben Sie in das Feld **<20,00 kg** „500“ ein.
    * Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 20 Kilogramm beträgt.  
16. Geben Sie in das Feld **<100,00 kg** „1000“ ein.
    * Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 100 Kilogramm beträgt.  
17. Geben Sie in das Feld **<1.000,00 kg** „3000“ ein.
    * Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 1000 Kilogramm beträgt.  
18. Wählen Sie **Speichern** aus.
19. Schließen Sie die Seite.

## <a name="assign-rate-base"></a>Satzbasis zuweisen

1. Erweitern Sie den Abschnitt **Satz-Basis-Zuweisungen**.
2. Wählen Sie **Neu** aus.
    * Sie können mehrere Satzbasiszuweisungen für jeden Satzmaster haben. Auf diese Weise ist es möglich, mehrere verschiedene Preispunkte für jeden Spediteur abhängig von Zielen, Dienstleistungen oder unterschiedlichen Satzbasen zu erstellen. In diesem Verfahren erstellen Sie nur eine Satzbasiszuweisung.  
3. Geben Sie im Feld **Name** einen Wert ein.
4. Wählen Sie im Feld **Tarifbasis** die Dropdown-Schaltfläche, um das Nachschlagefeld zu öffnen.
5. Wählen Sie in der Liste die Verknüpfung in der markierten Zeile.
6. Wählen Sie im Feld **Service** die Dropdown-Schaltfläche, um das Nachschlagefeld zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Wählen Sie in der Liste die Verknüpfung in der markierten Zeile.
9. Geben Sie in das Feld **Postleitzahl entnehmen** „98052“ ein.
    * Geben Sie an, für welche Postleitzahl diese Satzbasiszuweisung gültig sein soll aus.
10. Geben Sie in das Feld **Land Region** „USA“ ein.
11. Wählen Sie **Speichern** aus.
