---
title: Entwicklung und Etablierung einer Übersicht über Serviceverträge
description: In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden, und festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf28619e66fa5d3e86bdbb3838dc7f711916bcec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905601"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Entwicklung und Etablierung einer Übersicht über Serviceverträge

[!include [banner](../includes/banner.md)]

In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden, und festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen.

Jeder Servicevertrag ist einem Projekt zugeordnet, durch das Buchungen ausgeführt und fakturiert werden. Sie haben jedoch auch die Möglichkeit, zum direkten Ausführen von Serviceauftragsbuchungen durch das Projekt, ohne zuvor eine Verbindung des Serviceauftrags mit einem Servicevertrag herstellen zu müssen. Dies ist möglicherweise hilfreich, wenn es sich bei dem Serviceauftrag um einen einmaligen Servicebesuch handelt und die schnelle Bearbeitung der Servicebuchungen einen höheren Stellenwert einnimmt als die Erfassung ausführlicher Servicevereinbarungsdaten zum Debitor über einen längeren Zeitraum.

## <a name="service-agreement"></a>Servicevereinbarung

In jedem Servicevertrag müssen ein Projekt, eine Servicevertragskennung sowie eine Servicevertragsgruppe angegeben werden. Die Servicevertragsgruppe dient zum Sortieren und Organisieren von Serviceverträgen.

Ein Servicevertragskopf enthält Einstellungen für alle zugeordneten Vertragspositionen:

-  Aussetzungsstatus der Servicevereinbarung. Ist die Servicevereinbarung ausgesetzt, können auf Basis dieser Servicevereinbarung keine Serviceaufträge generiert werden.
-  Dauer der Servicevereinbarung
-  Angaben zur Kombinierung von Serviceauftragspositionen zu Serviceaufträgen
-  Vorlagenstatus des Servicevertrags.

Im Kopf der Servicevereinbarung werden auch alle Serviceobjekte und -aufgaben eingerichtet, die für die Servicevereinbarung zur Verfügung stehen sollen. Geben Sie dazu die jeweiligen Serviceaufgaben oder Serviceobjekte ein, die den verschiedenen Positionen des Vertrags zugeordnet werden soll.

Aus dem Kopf des Servicevertrags lassen sich auch Servicevertrags- oder Servicevorlagenpositionen in den aktuellen Servicevertrag kopieren.

Sie können Serviceverträge aussetzen und einzelne Servicevertragspositionen beenden.

Wenn Sie das Kontrollkästchen **Unterbrochen** für eine Servicevertragsposition aktivieren, können Sie Folgendes nicht durchführen:

-    Serviceaufträge aus der Servicevereinbarung automatisch oder manuell erstellen.

Wenn Sie das Kontrollkästchen **Anhalten** für eine Servicevertragsposition aktivieren, können Sie Folgendes nicht durchführen:

-    Serviceaufträge aus der Servicevereinbarungsposition automatisch oder manuell erstellen.
-    Servicevereinbarungsposition in eine andere Servicevereinbarung oder einen anderen Serviceauftrag kopieren.


> [!NOTE]
> Wenn ein Servicevertrag ausgesetzt ist, werden alle zugeordneten Positionen unabhängig von ihrem jeweiligen Status beendet.

## <a name="service-agreement-lines"></a>Servicevertragspositionen

In jeder Servicevertragsposition wird der Inhalt der erforderlichen Servicearbeiten ausführlich beschrieben. Die Positionen enthalten die folgenden Einstellungen:

-  Die Buchungsart sowie eine Beschreibung der Buchungsart
-  Den Mitarbeiter, von dem die Servicearbeiten ausgeführt werden
-  Die Objekte, für die der Service im Rahmen der Servicevereinbarung erbracht werden soll
-  Die Häufigkeit, mit der die Arbeiten ausgeführt und die Artikel-, Spesen- und Gebührenbuchungen erfasst werden
-  Das Zeitfenster für die Gruppierung von Serviceauftragspositionen zu einem Serviceauftrag.
-  Die Serviceaufgaben zum Gruppieren von Vertragspositionssätzen zu Arbeitsaufgaben sowie für Zusammenfassungen der auszuführenden Serviceaufgaben für Servicetechniker und Debitoren.
-  Den Status einer Position. Wurde eine Position beendet, können für diese Position keine Serviceaufträge erstellt werden.
-  Die Projekteinstellungen wie Kategorie oder Abrechnungscode.

## <a name="related-articles"></a>Zugehörige Artikel

[Erstellen von Servicevereinbarungen](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]