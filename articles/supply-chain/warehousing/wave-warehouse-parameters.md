---
title: Lagerparameter für Zyklusverarbeitung
description: In diesem Artikel wird beschrieben, wie Lagerortparameter für Wellenverarbeitung eingerichtet werden. Sie können Wellenverarbeitung verwenden, um Entnahmearbeit für mehrere Arbeitsaufträge in eine einzige Welle zu gruppieren.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2a64cba837faf84f3e8470a9831d1641213a5cc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909611"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Lagerparameter für Zyklusverarbeitung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Lagerortparameter für Wellenverarbeitung eingerichtet werden. Sie können Wellenverarbeitung verwenden, um Entnahmearbeit für mehrere Arbeitsaufträge in eine einzige Welle zu gruppieren.

Um die Wellenverarbeitung zu verwenden, geben Sie auf der Seite **Lagerortverwaltungsparameter** Folgendes an:

- Ob Sie Wellen bearbeiten können, indem Sie einen Stapelverarbeitungsauftrag verwenden.
- Ob Sie Informationen in einer Protokolldatei sammeln, wenn Wellen verarbeitet werden.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Lagerortverwaltungsparameter für Wellenverarbeitung einrichten

Um Lagerortparameter für Wellenverarbeitung einzurichten, führen Sie folgende Schritte aus:

1. Gehen Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerortverwaltungsparameter**.

1. Nehmen Sie im Inforegister **Wellenverarbeitung** die folgenden Einstellungen vor:

    - **Wellenverarbeitungs-Stapelverarbeitungsgruppe** – Wählen Sie die Stapelverarbeitungsgruppe aus, die verwendet wird, wenn Sie Wellen verarbeiten, indem Stapelverarbeitungsaufträge verwendet werden. Die Stapelverarbeitungsgruppe gibt den Server an, auf dem Stapelverarbeitungsaufträge ausgeführt werden.
    - **Wellen in einem Stapel verarbeiten** – Wählen Sie aus, ob Wellen automatisch mit einem Stapelverarbeitungsauftrag verarbeitet werden sollen. Sie müssen hier *Ja* einstellen, um eine parallele Verarbeitung verwenden zu können. Sie richten den Stapelverarbeitungsauftrag auf der Seite **Wellen verarbeiten** ein. (Siehe auch den Hinweis am Ende dieser Liste.)
    - **Wellenfortschrittsprotokoll erstellen** – Wählen Sie aus, ob das System immer einen Protokolldatensatz erstellen soll, wenn eine Zuteilung für einen Artikel und dessen Dimensionen beginnen und enden. Sie sollten dieses Protokoll nur aktivieren, wenn Sie es benötigen, z. B. während des ersten Tests oder zur Problembehandlung. Weitere Informationen finden Sie unter [Wellenzuteilung](wave-allocation-method.md).
    - **Protokoll für Wellenverarbeitungsverlauf erstellen** – Wählen Sie aus, ob Informationen zu einer Welle nach der Verarbeitung der Welle automatisch in einer Protokolldatei gespeichert werden sollen, auch während der parallelen Verarbeitung ausstehender Zuteilungen. Normalerweise sollten Sie dies nur während der Problembehandlung aktivieren, da dies einen Mehraufwand verursacht. Um das Protokoll anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Protokoll für Wellenverarbeitungsablauf**. Weitere Informationen finden Sie unter [Wellen erstellen und verarbeiten](wave-processing.md).
    - **Containerisierungsverlaufsprotokoll** – Wählen Sie aus, ob Informationen zur Containerisierung für eine Welle nach der Verarbeitung der Welle automatisch in einer Protokolldatei gespeichert werden sollen. Um das Protokoll anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Containerisierungsverlauf**.
    - **Auf Sperre (ms) warten** – Geben Sie die Uhrzeit ein, in Millisekunden, die ein Zuteilungsschritt auf eine Systemressource wartet, die von einem anderen Zuteilungsschritt gesperrt ist. Bei Überschreitung dieser Zeit wird, wird die Welle nicht verarbeitet und eine Fehlermeldung wird angezeigt.

1. Nehmen Sie auf dem Inforegister **An Lager freigeben** folgende Einstellung vor:

    - **Fehler zu fehlgeschlagener Stapelverarbeitung** – Wählen Sie aus, ob ein Fehler generiert werden soll, wenn eine Freigabe für eine Lagerortstapelverarbeitung fehlschlägt. Wenn dies aktiviert ist, enden fehlgeschlagene Aufträge mit dem Status *Fehler*. Wenn dies deaktiviert ist, enden fehlgeschlagene Aufträge mit dem Status *Beendet*.

> [!NOTE]
> Auf der Wellenvorlage, die verwendet wird, um die Welle zu verarbeiten, können Sie die Einstellungen angeben, die das Wellenverarbeiten automatisieren. Wenn Sie einen Zeitplan für den Batchauftrag einrichten, sollten Sie den Zeitpunkt mit den Einstellungen für Automatisieren in der Wellenvorlage koordinieren. Weitere Informationen finden Sie unter [Wellenvorlage erstellen](wave-templates.md).
>
> Wenn Sie *Transportverwaltung* und *Erweiterte Lagerortverwaltung* verwenden, können Sie angeben, ob Ladungen konsolidiert werden, wenn Sie eine Welle verarbeiten. Beispielsweise ist dieses hilfreich, wenn mehrere kleinere Ladung gleichzeitig versendet werden können. Um Ladungen zu konsolidieren, wenn Sie eine Welle verarbeiten, klicken Sie auf die Registerkarte **Ladungen** und wählen Sie das Kontrollkästchen **Ladungen während der Wellenverarbeitung konsolidieren** aus.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Einrichten einer vollständigen oder teilweisen Reservierung für Produktionswellen

Bei Aufträgen und Kanbanaufträgen muss Lagerbestand reserviert werden, bevor der Auftrag an den Lagerort freigegeben wird. Andernfalls können die Artikel oder der Verteilungspositionen nicht in einer Welle verarbeitet werden. Einige Produktionsaufträge sind jedoch etwas flexibler. Bei Produktionsaufträgen kann Folgendes angegeben werden:

- Zulassen, dass Produktionsaufträge für den Lagerort freigegeben werden, obwohl nicht alle Materialien reserviert werden können. Wenn Sie diese Option auswählen, müssen Sie den Prozess der Freigabe für den Lagerort manuell wiederholen, wenn die zusätzlichen Materialien verfügbar werden. Dies ist beispielsweise hilfreich, wenn Sie die Materialien haben, die Sie zum Starten der Produktion benötigen, und warten können, bis die zusätzlichen Materialien verfügbar werden.
- Anfordern, dass alle Materialien reserviert werden, bevor ein Auftrag für den Lagerort freigegeben werden kann.

Um vollständige Reservierung anzufordern oder teilweise Reservierung zu ermöglichen, führen Sie folgende Schritte aus:

1. Wechseln Sie zu **Produktionssteuerung** \> **Einstellungen** \> **Produktionssteuerungsparameter**.
1. Wählen Sie auf der Registerkarte **Allgemein** im Feld **An Lager freigeben** die Standardeinstellung aus.
