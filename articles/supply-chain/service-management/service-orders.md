---
title: "Serviceaufträge"
description: "Ein Serviceauftrag steht für den Besuch eines Servicetechnikers am Standort eines Debitors zu einem bestimmten Datum."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 647bbe9cca0167d33048ad07e092708f90b41fc3
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="service-orders"></a>Serviceaufträge   

[!include [banner](../includes/banner.md)]


Ein Serviceauftrag steht für den Besuch eines Servicetechnikers am Standort eines Debitors zu einem bestimmten Datum. Jeder Serviceauftrag besteht aus mindestens einer Serviceauftragsposition. Serviceauftragspositionen repräsentieren die Arbeitsstunden, die vom Servicetechniker ausgeführt werden müssen, und die zugehörigen Artikel, Ausgaben und Gebühren.

Sie können Aufgaben und Objekte zu einer Serviceauftragsposition zuordnen. Sie können dann Serviceauftragspositionen nach Aufgaben oder nach Objekten gruppieren. Darüber hinaus lassen sich Serviceauftragspositionen auch mit Artikeln aus dem Lager versehen.

## <a name="create-service-orders"></a>Erstellen von Serviceaufträgen

Die Serviceaufträge werden auf der Grundlage des Servicevertrags und der Positionen in diesem Vertrag erstellt. Sie können jedoch Serviceaufträge erstellen, die mit einer Servicevereinbarung nur in der Periode zugeordnet sind, die in der Vereinbarung angegeben ist. Wenn beispielsweise eine Servicevereinbarung während des Kalenderjahres 2011 gültig ist, können Sie Serviceaufträge für die Vereinbarung ab dem 1. Januar 2011 und 31. Dezember 2011 erstellen.

Serviceaufträge können auch einzeln erstellt werden, ohne sie einer Vereinbarung zuzuordnen. Diese Serviceaufträge können verwendet werden, um ungeplante oder einmalige Servicebesuche zu behandeln. Zum Beispiel: Im März beschließt Ihr Debitor, dass für zwei Maschinen, die nicht in der Servicevereinbarung enthalten sind, Serviceaufgaben ausgeführt werden sollen. Für diese Aufgabe erstellen Sie Serviceaufträge, aber ordnen sie keiner Vereinbarung zu.


> [!NOTE]
> <P>Um Serviceaufträge zu erstellen die nicht einer Servicevereinbarung zugeordnet sind, müssen Sie das Kontrollkästchen <STRONG>Ohne Servicevertrag zulassen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG> auswählen.</P>

**Szenario**

Im folgenden Szenario wird eine andere Situation beschrieben, in der es nützlich ist, einen Serviceauftrag zu erstellen, der nicht einer Servicevereinbarung zugeordnet ist.

Der Unternehmensdisponent erhält einen Anruf, in dem der Notfallservice für einen Aufzug verlangt wird. Es ist keine Zeit vorhanden, eine Servicevereinbarung und ein Projekt für den Service einzurichten. Daher erstellt der Disponent einen Serviceauftrag direkt im Formular **Serviceaufträge**, fügt den Serviceauftrag einem vorhandenen Projekt hinzu und erstellt die Serviceauftragspositionen. Darüber hinaus erstellt er eine Aufgaben- oder Objektbeziehung für einen vorhandenen Serviceauftrag. Auf diese Weise können Arbeiten erfasst werden, die nicht mit der Servicevereinbarung in Verbindung stehen. Weitere Informationen finden Sie unter [Manuelles Erstellen von Serviceaufträgen](create-service-orders-manually.md) und [Erstellen von Serviceaufgabenbeziehungen](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Überwachen des Fortschritts von Serviceaufträgen

Zur Überwachung des Fortschritts eines Auftrags durch die einzelnen Teams und Arbeitsprozesse können Sie ein System von Phasen und Ursachecodes einrichten. Für jede Phase können Sie die Aktivitäten angeben, die zulässig sind. Weitere Informationen zu Ursachencodes finden Sie unter [Erstellen von Ursachencodes](create-reason-codes.md).

**Beispiel**

Ein Serviceauftrag wird von dem Disponenten genehmigt. Der Disponent aktualisiert die Phase des Serviceauftrags und gibt einen Ursachencode an, der angibt, dass der Serviceauftrag für den Servicetechniker freigegeben wurde. Der Servicetechniker begibt sich an den Standort des Debitors und führt den Serviceauftrag aus.

## <a name="specify-item-requirements-for-service-orders"></a>Festlegen von Artikelbedarf für Serviceaufträge

Sie können die Lagerartikel angeben, die für Serviceaufträge erforderlich sind. Allerdings muss der Serviceauftrag einem Projekt zugeordnet sein. Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet. 

**Beispiel**

Die auf der Grundlage der Servicevereinbarung erstellten Serviceaufträge werden durch den Disponenten verarbeitet. Beim ersten Serviceauftrag erkennt der Disponent, dass der Techniker ein wichtiges Ersatzteil benötigt, das nicht vorrätig ist. Aus diesem Grund erstellt er direkt im Serviceauftrag einen Artikelbedarf für das Ersatzteil.

## <a name="move-and-post-lines"></a>Verschieben und Buchen von Positionen

Ein Servicetechniker kommt von einem Servicebesuch zurück und ändert und aktualisiert die Serviceauftragspositionen. Während des Servicebesuchs führte der Techniker eine Serviceaufgabe durch, die für den nächsten Servicebesuch geplant war. Aus diesem Grund verschiebt er die Positionen aus dem nächsten Servicebesuch in den aktuellen Servicebesuch. Der Techniker bucht dann den Serviceauftrag. Weitere Informationen finden Sie unter [Serviceauftragspositionen verschieben](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Serviceaufträge stornieren

Einer der für Januar generierten Serviceaufträge wird nicht mehr benötigt, da der Auftrag storniert wurde. Aus diesem Grund storniert der Servicedisponent den Serviceauftrag. Weitere Informationen finden Sie unter [Serviceaufträge stornieren](cancel-service-orders.md).

## <a name="post-from-projects"></a>Buchen vom Modul "Projekt" aus

Am Ende jeder Woche möchte der Disponent alle Serviceaufträge buchen, die einem bestimmten Projekt zugeordnet sind. Daher sucht er das entsprechende Projekt im Formular **Projekte** und bucht die Serviceaufträge, die abgeschlossen wurden. Weitere Informationen finden Sie unter [Klassenformular "Serviceaufträge buchen"](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Serviceaufträge löschen

In der zweiten Jahreshälfte teilt Ihnen Ihr Debitor mit, dass die Servicebesuche häufiger stattfinden sollen. Für die restliche Zeit der Servicevereinbarung muss also eine neue Serie von Servicebesuchen mit kürzeren Intervallen erstellt werden. Zu diesem Zweck müssen die vorhandenen erstellten Serviceaufträge gelöscht und neue Serviceaufträge erstellt werden. Weitere Informationen finden Sie unter [Serviceaufträge löschen](delete-service-orders.md).

## <a name="see-also"></a>Siehe auch

[Formular "Serviceaufträge"](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))

  



