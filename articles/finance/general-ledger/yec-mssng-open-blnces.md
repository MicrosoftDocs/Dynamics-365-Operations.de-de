---
title: Fehlende Anfangssalden für den Jahresabschluss
description: In diesem Thema wird erläutert, warum beim Jahresabschluss möglicherweise Anfangssalden fehlen und wie diese Salden ggf. neu erstellt werden.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 582363ba6c5f6e63e695d41e73ee2f0b382cf26e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727171"
---
# <a name="year-end-close-missing-opening-balances"></a>Fehlende Anfangssalden für den Jahresabschluss

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, warum beim Jahresabschluss möglicherweise Anfangssalden fehlen und wie diese Salden ggf. neu erstellt werden.

### <a name="symptom"></a>Symptom

Warum gibt es nach dem Jahresabschluss des Hauptbuchs keine Anfangssalden? 

### <a name="resolution"></a>Lösung

Im Folgenden finden Sie die zu prüfenden Elemente, wenn Sie ein Jahr im Hauptbuch abgeschlossen und dann eine Zwischenbilanz erstellt haben, bei der Anfangssalden für das nächste Geschäftsjahr nicht angezeigt werden.

Wenn das Feld **Vorherigen Abschluss rückgängig machen** auf **Ja** eingestellt ist, wird der vorherige Abschluss für das gleiche Geschäftsjahr rückgängig gemacht. Beim Prozess des Rückgängigmachens werden alle Einträge der Abschluss- und Anfangssalden gelöscht, als wäre der Jahresendabschluss nie erfolgt. Belege werden ebenfalls gelöscht. Der Jahresendabschlussprozess wird nicht automatisch erneut ausgeführt. Vielmehr muss der Vorgang manuell erneut gestartet werden, wobei die Option **Vorherigen Abschluss rückgängig machen** auf **Nein** aktualisiert wird.

Dieses Szenario wird im FAQ-Thema zum Jahresabschluss behandelt. Weitere Informationen finden Sie unter [Häufig gestellte Fragen zu Aktivitäten am Jahresende](faq-year-end-activities.md).

### <a name="symptom"></a>Symptom

Ich habe den Jahresabschluss durchgeführt, während die Option **Vorherigen Abschluss rückgängig machen** auf **Nein** festgelegt war, und ich habe noch keine Anfangssalden für mein Geschäftsjahr.

### <a name="resolution"></a>Lösung

Prüfen Sie zunächst den Status des Stapelverarbeitungsauftrags. Der Jahresabschluss umfasst eine Reihe separater Aufgaben. Der wichtigste Schritt ist jedoch der Stapelverarbeitungsauftrag mit der Aufgabenbeschreibung **Schritt 5.0.0**. Während dieses Schritts erfolgt die Buchung der Primobuchungen und optional der Abschlussbuchungen im Hauptbuch. 

[![Historie der Stapelverarbeitungen.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Wenn dieser Schritt erfolgreich beendet wurde, jedoch keine Anfangssalden auf der Seite **Zwischenbilanzermittlung** (**Hauptbuch > Abfragen und Berichte > Zwischenbilanz**) angezeigt werden, überprüfen Sie die Ergebnisse des Batchauftrags zum Jahresabschluss, um festzustellen, ob der Schritt „Salden neu erstellen“ erfolgreich abgeschlossen wurde.

[![Ergebnisse des Batchauftrags zum Jahresabschluss.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Wenn dieser Schritt aus irgendeinem Grund fehlgeschlagen ist, wurden die Primobuchungen (und optional Abschlussbuchungen) wahrscheinlich erfolgreich gebucht. Sie können überprüfen, ob die Hauptbuchbuchungen erfolgreich auf der Seite **Belegbuchungsabfrage** gebucht wurden, indem Sie die Belegnummer und das Datum angeben, die im Dialogfeld zum Jahresabschluss für das Jahr angegeben sind, das Sie abgeschlossen haben (**Hauptbuch > Abfragen und Berichte > Belegbuchungen**).

[![Belegbuchungsabfrage.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Wenn die Eröffnungsbelege (und optional Abschlussbelege) vorhanden sind, müssen Sie den Jahresabschluss nicht erneut ausführen. Informationen zum weiteren Vorgehen finden Sie im nächsten Abschnitt.

### <a name="symptom"></a>Symptom

Der Schritt „Salden neu erstellen“ beim Jahresabschluss ist fehlgeschlagen. Muss ich den gesamten Jahresabschlussprozess erneut ausführen?

### <a name="resolution"></a>Lösung

Der Schritt „Salden neu erstellen“ aktualisiert die Hauptbuchsalden, die beim Generieren der Zwischenbilanzermittlung verwendet werden.  Dies ist der letzte Schritt im Jahresabschlussprozess.  Wenn dieser Schritt der einzige Schritt ist, der fehlgeschlagen ist, wurden die Hauptbuchbuchungen erfolgreich gebucht.  Sie müssen den Jahresendabschluss nicht erneut ausführen. Sie können den Prozess ausführen, um die Salden manuell über die Seite **Finanzdimensionssätze** (**Hauptbuch > Kontenplan > Dimensionen > Finanzdimensionssätze**) neu zu erstellen.

[![Schaltfläche „Salden neu erstellen“ auf der Seite „Finanzdimensionssätze“.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Wenn die Verarbeitung dieses Schritts lange dauert, empfehlen wir, die bewährten Methoden für Finanzdimensionssätze zu überprüfen, wie unter [Bewährte Methoden für die Aktualisierung von Finanzdimensionssätzen](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets) beschrieben. 

