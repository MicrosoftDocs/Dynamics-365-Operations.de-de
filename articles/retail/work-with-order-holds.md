---
title: Callcenter-Auftragssperren konfigurieren und mit ihnen arbeiten
description: "In diesem Thema wird beschrieben, wie Sie mit Sperren auf Aufträgen arbeitet, indem Microsoft Dynamics 365 for Retail verwendet wird."
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ba8fade84358c960dcfd1e8d9ffef1ffede34871
ms.contentlocale: de-de
ms.lasthandoff: 01/04/2019

---

# <a name="configure-and-work-with-call-center-order-holds"></a>Callcenter-Auftragssperren konfigurieren und mit ihnen arbeiten

[!include [banner](includes/banner.md)]

In diesem Thema werden die Auftragssperrfunktionen beschrieben, die Microsoft Dynamics 365 for Retail für Callcenteraufträge hat.

## <a name="configuring-call-center-order-holds"></a>Callcenter-Auftragssperren konfigurieren

Um die Callcenterauftrags-Sperrfunktionen zu verwenden, müssen Sie zunächst Sperrcodes definieren. Um einen Satz benutzerdefinierter Sperrcodes zu erstellen, basierend auf Ihren geschäftlichen Anforderungen, gehen Sie zu **Vertrieb und Marketing** \> **Einstellungen** \> **Aufträge** \> **Sperrcodes**. Sie können einen Sperrcode optional kennzeichnen wie der Standardsperrcode, indem Sie die Option **Standard für Auftrag** auf **Ja** festlegen. Dieser Sperrcode wird jederzeit verwendet, wenn ein Auftrag gesperrt wird. Wenn ein Auftrag reservierten Lagerbestand hat und die Reservierungen automatisch entfernt werden, wenn der Auftrag für einen bestimmten Grund gesperrt wird, entsprechend die Option **Entfernen Sie Lagerreservierungen** auf **Ja** für Ursachencodes.

Um den Typ des zu erstellenden Hinweises anzugeben der beim Melden aufgezeichnet wird, geben Benutzer, die einen Auftrag sperren, optionale Hinweise ein. Gehen Sie zu **Debitoren** \> **Einstellungen** \> **Debitorenparameter**, und klicken Sie dann auf dem Inforegister **Vertriebseinstellung**, auf der Registerkarte, Satz **Allgemeines** **Hinweistyp**. Verwenden Sie das Feld **Gesperrter Auftragsstatus**, um die Farbe festzulegen, die verwendet wird, um Aufträge hervorzuheben, die gesperrt sind, wenn sie auf der Seite **Kundendienst** angezeigt werden.

Um einen optionalen Ursachensperrcodes zu erstellen, wechseln Sie zu **Retail** \> **Kanaleinstellung** \> **Infocodes** Diese Infocodes können als sekundäre Ursachencode verwendet werden, um den Hautsperrcode wieter zu definieren. Wählen Sie **Neu**, um einen Ursachencodesatz zu erstellen, und wählen Sie dann **Untercodes** um die Liste weiterer Gründe zu definieren. Um sämtliche Infocodes zu verknüpfen, die Sie im Callcenterkanal definieren, wechseln Sie zu **Retail** \> **Kanäle** \> **Callcenter** \> **Alle Callcenter**. Auf dem Inforegister **Allgemeines** legen Sie das Feld **Sperrcode** fest.

## <a name="putting-orders-on-hold"></a>Gesperrte Aufträge

Aufträge, die Callcenterbenutzer im Backofficekleinprogramm erstellen, können in bestimmten Situationen automatisch oder manuell manuell gesperrt werden.

Während der Verkaufserfassung aber vor Auftragsunterordnung und Bestätigung, sollten Callcenterbenutzer einen Auftrag manuell sperren, um ihn an freigegeben werden dem Lagerort das für die weitere Verarbeitung verhindert. Zum Beispiel ist der Debitor, der den Auftrag platziert, noch nicht bereit oder es fehlen zentrale Daten, um den Prozess erfolgreich zu verarbeiten.

Auf der Auftragserfassungsseite kann der Callcenterbenutzer einen Auftrag sperren, indem er die Option **Auftragsgriffe** der Registerkarte **Auftrag** Auftragserfassungsmenüs verwendet. Alternativ kann der Benutzer die Menüoption **Sperren** auf der Seite **Auftragszusammenfassung** auswählen, die angezeigt wird, wenn sie bei einem Callcenterauftrag **Vollständig** auswählen.

In beiden Fällen wird die Seite **Auftragssperre** angezeigt. Der Benutzer kann dann **Neu** auswählen, um eine Sperre für den Auftrag zu erstellen. Im Feld **Code sperren** sollte der Benutzer den Code auswählen, der den Grund für die Sperre am besten beschreibt. Im Feld **Ursachencode** kann der Benutzer einen zusätzlicher optionalen Code auswählen, um eine zweite Sperre des Werts bereitzustellen.

Unter Inforegister unter **Hinweise** im Feld **Sperre-Hinweise**, kann der Benutzer die zusätzlichen Freihandnotizen eingeben, um zusätzliche Informationen oder Informationen zur Sperre bereitzustellen. Diese Notizen können andere Benutzer unterstützen, die dem Sperrauftrag später überprüfen.

Nachdem Sie die Sperrinformationen eingegeben und gespeichert haben, kann der Benutzer die Seite **Auftragssperre** schließen. Der Benutzer kehrt dann zur Auftragseintragserfassung zurück. Wenn keine weiteren Aktivitäten für den Auftrag erforderlich sind, kann der Benutzer die Auftragseintragsseite schließen.

Wenn die Markierung **Aktivieren Sie Auftragsabschluss** im Callcenterkanal aktiviert ist, wird die Zahlung für einen gesperrten Auftrag nicht angewendet. Durch Kontrast für einen Auftrag, der nicht gesperrt ist, können Benutzer die Auftragseintragsseite nicht verlassen, bis die Zahlung angewendet wird. Selbstverständlich ist Zahlung erforderlich, bevor die Auftragssperre freigegeben wird.

Darüber hinaus können Callcenterbenutzer eine manuelle Sperre für Aufträge erstellen, die aus einem bestimmten Grund verdächtig erscheinen. Aufträge können auch automatisch gesperrt werden, wenn sie mit Betrugskriterien und aktiven Regeln übereinstimmen. Weitere Informationen zu diesen Auftragssperrtypen, finden Sie unter [Einstellungsbetrugswarnungen](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Aufträge anzeigen und verwalten, die gesperrt sind

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Anzeigen von Sperrinformationen für einen einzelnen Auftrag

Auf der Seite **Kundendienst** können Benutzer Aufträge ansehen, die gesperrt sind, da die Auftragspositionen mit einer bestimmten Farbe hervorgehoben werden. Diese Farbe wird im Feld **Gesperrter Auftragsstatus** auf der Seite **Debitorenparameter** definiert.

> [!NOTE]
> Wenn die Position auf der Seite aktiviert ist, ist die Hervorhebungsfarbe nicht sichtbar.

Benutzer können auch detaillierte Statusinformationen für einen Auftrag anzeigen, um zu erfahren, ob der Auftrag gesperrt ist. Die detaillierten Statusinformationen können über die Seite **Alle Aufträge** oder **Kundendienst** angezeigt werden. Wenn ein Auftrag gesperrt ist, ist die Markierung **Nicht verarbeiten** festgelegt, und das Feld **Detaillierter Status** zeigt entweder den Status **Gesperrt** oder **Betrugssperre**, je nach Szenario.

Um die Details eines bestimmten Auftrags anzuzeigen, kann der Benutzer eine detaillierte Ansicht der Seite **Auftragssperre** auf der Seite **Kundendienst** anzeigen, indem das Menü **Optionen** für den ausgewählten Auftrag verwendet wird. Benutzer können auf die Ansicht von der Seite **Jeder Auftrag** zugreifen, indem die Menüoption **Auftragssperre** auf der Registerkarte **Auftrag** ausgewählt wird.

### <a name="viewing-all-orders-that-are-on-hold"></a>Alle Aufträge anzeigen und verwalten, die gesperrt sind

Um alle Aufträge anzuzeigen, die manuellen oder automatischen Sperre zugeordnet wurden, gehen Sie zu **Retail** \> **Debitoren** \> **Auftragssperre**.

Workbench enthält eine Listenansicht **Auftragssperren**, die alle Aufträge enthält, die aufgrund von manuellen oder Betrug-zugeordneten Aktivitäten gesperrt sind. Mithilfe der Standardfilterungs- und Sortierfunktionen auf der Seite können Benutzer Ansichten erstellen, mit denen sie arbeiten mit oder bestimmte Sperrcodes verwalten lassen, für die Sie für die Überprüfung zuständig sind. Der Workbench **Aufträge sperren** gibt auch die Anzahl von Tagen an, für die ein Auftrag gesperrt war. Diese Informationen können Benutzer unterstützen, die Warteschlange zu priorisieren.

Um eine detailliertere Ansicht der Aufträge abzurufen die gesperrt sind, können Benutzer auf die Option **Auftragssperre** im Menü klicken. Diese Ansicht gibt Informationen zum Debitor, enthält Hinweise, dass der Auftrag angewendet wurde, Kunden oder Sperraktivitäten. Die Ansicht bietet auch Details zur Ursache für ein automatischen Sperre, wenn der Auftrag gesperrt wurde, da er einer Betrugsregel entsprach.

In der Listenansicht und der detaillierten Ansicht der Seite **Auftragssperre** können Benutzer auftragsbezogene zusätzliche Informationen, wie Zahlungen, Summen und Hinweise anzeigen oder bearbeiten.

Die Optionen auf der Registerkarte **Sperre auschecken an** ist unter Umständen hilfreich, falls mehrere Benutzer in Ihrem Unternehmen an der Sperrwarteschlange gleichzeitig arbeiten. Wenn Sie die Option **Auschecken** auswählen, können Benutzer angeben, dass sie arbeiten, um die Auftragssperre zu überprüfen und zu untersuchen. Dadurch verlieren andere Benutzer nicht Zeit, wenn Sie versuchen, dieselbe Arbeit zu tun. Von der detaillierten Ansicht der Seite **Auftragssperre** können Benutzer Informationen zum Auscheckdatum und den Zeitaufwand anzeigen sowie den Benutzer, der den Sperrdatensatz ausgecheckt hat.

Nachdem ein Sperrdatensatz ausgecheckt ist, kann nur der Benutzer, der sie ausgecheckt hat, das Auschecken löschen."" Diese Einschränkung soll verhindern, dass Benutzer Datensätze nehmen, an denen andere Benutzer bereits arbeiten. Um einen Auftrag wieder in der Warteschlange freizugeben damit andere Benutzer sie bearbeiten können, wählt der Benutzer, der den Datensatz prüfte, die Option **Auschecken deaktivieren** aus.

> [!NOTE]
> Der Sperre wird nicht freigegeben, wenn das Auschecken deaktiviert ist.

In bestimmten Situationen, beispielsweise, wenn ein Benutzer krank ist oder das Unternehmen verlassen hat, müssen möglicherweise Datensätze, die für diesen Benutzer ausgecheckt sind, neu zugeordnet werden. Ein Manager kann Datensätze neu zuweisen, indem er die Option **Auschecken außerkraftsetzen** verwendet.

## <a name="releasing-orders-that-are-on-hold"></a>Alle Aufträge anzeigen und verwalten, die gesperrt sind

In der Listenansicht und der detaillierten Ansicht der Seite **Auftragssperre** enthält die Registerkarte **Sperre deaktivieren** die Optionen, die verwendet werden, um eine Auftragssperre freizugeben. Verwenden Sie die Option **Sperre deaktivieren**, um einen Auftrag vom ausgewählten Sperrcode freizugeben.

Callcenteraufträge benötigen Zahlung. Daher kann ein Sperre nicht vollständig deaktiviert werden, wenn die Zahlung nicht in den Auftrag übernommen wurde. Auf der Seite **Callcenterparameter** auf der Registerkarte **Sperren** überprüfen Sie, ob der **Senden, wenn diese Option deaktiviert ist** Parameter aktiviert ist. Diese Einstellung stellt sicher, dass die deaktivierte Sperre durch die korrekte Auftragsübermittlungslogik geht, um Zahlungen zu überprüfen und zu autorisieren. Wenn Zahlungen fehlen, erhält der Benutzer eine Fehlermeldung, und der Sperrcode wird nicht gelöscht.

Wenn der Parameter **Senden, wenn deaktiviert ist** nicht festgelegt wurde, können Benutzer die Option **Deaktivieren und übermitteln** im Menü **Sperre deaktivieren** auswählen, um sicherzustellen, dass der Auftrag alle erforderlichen Zahlungsprüfungen durchläuft. Wenn die Übermittlung fehlschlägt, wenn **uftragsabschluss aktivieren** im Callcenterkanal aktiviert ist, wird der Auftrag von seinem Sperrstatus freigegeben, jedoch die Markierung **nicht verarbeiten** beibehalten. Daher wird der Auftrag nicht freigegeben für den Lagerort, bis korrekte Zahlungen berücksichtigt und überprüft wurden.

Wenn Benutzer einen Sperre verrechnen aber zusätzliche Änderungen am Auftrag vornehmen möchten, bevor er für das spätere Verarbeiten freigegeben wurde, können sie die Option **deaktivieren und ändern** auswählen. Diese Option entfernt den Sperrcode und öffnet die Auftragsdetails, damit Benutzer zusätzliche Änderungen am Auftrag vornehmen können. Benutzer können Zahlung auch übernehmen und die Reihenfolge von Zahlungsprüfungslogik senden, wenn die den Callcenterkanal-Markierung **Aktivieren Sie Auftragsabschluss** aktiviert ist.

## <a name="reporting-options"></a>Sonstige Berichtsoptionen

Geheb Sie zu **Retail** \> **Abfragen und Berichte** \> **Callcenterberichte** \> **Auftragsgriffbericht**, um einen Bericht zu Auftragssperren nach Datumsbereich, Sperrcode oder zugehörigen Kriterien auszuführen.

