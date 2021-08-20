---
title: Nachverfolgung für Einlagerung aktualisieren
description: In diesem Thema wird beschrieben, wie Sie die periodische Aufgabe „Nachverfolgung für Einlagerung aktualisieren“ einrichten und ausführen.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d2e1e4596a6052ea80d6e578dccf2564269d97444cd5b302acb5968cca2c884f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782586"
---
# <a name="update-tracking-for-put-away"></a>Nachverfolgung für Einlagerung aktualisieren

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Die periodische Aufgabe *Nachverfolgung für Einlagerung aktualisieren* ist so konzipiert, dass sie jede Nacht als wiederkehrende Stapelverarbeitung ausgeführt wird. Sie identifiziert, welche Fahrten alle Lagerbuchungen erhalten haben und welche Fahrten keinen Wert für das tatsächliche Enddatum haben. Es setzt dann das tatsächliche Enddatum nach Bedarf auf das aktuelle Datum.

*Container-Aktivitäten* werden für jede *Etappe* einer Fahrt für jeden *Versandcontainer* erstellt. Diese Werte werden durch die Fahrtenvorlage definiert, die beim Erstellen einer Fahrt ausgewählt wird. Für jede Containeraktivitätsdatensatz können Werte für die Felder **Startdatum**, **Geschätzte Enddatum** und **Tatsächliches Enddatum**. Diese Felder können aktualisiert werden, wenn eine Bestätigung darüber eingegangen ist, dass eine Etappe begonnen oder abgeschlossen wurde.

In der Regel werden Informationen, die sich auf bestätigte Daten beziehen, von einem Drittanbieter bereitgestellt, z. B. einer Frachtweiterleitung, da diese Aktivitäten außerhalb von Microsoft Dynamics 365 Supply Chain Management verwaltet werden. Es sind jedoch keine Informationen von einem Drittanbieter erforderlich, um den Wareneingang von einer Fahrtetappe in das Lager (wie durch die Einlagerung von Waren gekennzeichnet) nachzuverfolgen. Daher kann die Nachverfolgung basierend auf Informationen in Dynamics 365 Supply Chain Management bestimmt werden.

Um die periodische Aufgabe *Nachverfolgung für Einlagerung aktualisieren* einzurichten und auszuführen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Gesamttransportkosten \> Periodische Aufgaben \> Nachverfolgung für Einlagerung aktualisieren**.
1. Im Dialogfeld **Nachverfolgung für Einlagerung aktualisieren** im Abschnitt **Parameter** legen Sie die folgenden Felder fest:

    - **Etappe**: Wählen Sie den Namen/die Nummer der eindeutigen Kennung für den Teil einer Fahrt aus, für den Sie die Nachverfolgung aktualisieren möchten. Der gewählte Wert muss die Ankunft der Fahrt im Lager darstellen.
    - **Aktivität**: Wählen Sie die Aktivität aus, die während der ausgewählten Etappe durchgeführt wurde. Diese Werte werden pro Fahrtenvorlagenposition im Tracking-Control-Center vergeben.

1. Um die Anzahl der Datensätze zu begrenzen, die in die Aktualisierung aufgenommen werden sollen, wählen Sie die Schaltfläche **Filter** auf dem Inforegister **Einzuschließende Datensätze**. Ein Standard-Abfragedialogfeld wird angezeigt, in dem Sie Auswahlkriterien, Sortierkriterien und Verknüpfungen definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen im Supply Chain Management. Die Felder hier sind schreibgeschützt und zeigen Werte an, die mit Ihrer Abfrage in Zusammenhang stehen.
1. Richten Sie auf dem Inforegister **Im Hintergrund ausführen** Stapel- und Planungsoptionen nach Bedarf ein, genau wie bei anderen Arten von Stapelverarbeitungsaufträgen in Supply Chain Management.
1. Wählen Sie **OK** um Ihre Einstellungen zu übernehmen und das Update auszuführen oder zu planen.
