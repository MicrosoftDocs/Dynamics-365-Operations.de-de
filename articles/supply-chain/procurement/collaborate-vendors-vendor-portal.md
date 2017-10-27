---
title: Zusammenarbeit mit Kreditoren mithilfe des Kreditorenportals
description: "In diesem Artikel wird beschrieben, wie Einkaufsvertreter das Kreditorenportal nutzen können, um mit externen Kreditoren während des Bestellungsbestätigungsprozesses zusammenzuarbeiten. Diese Informationen gelten nur für die Versionen Februar 2016 &amp; und Mai 2016 von Dynamics AX."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: b4628977ec7a88a698f7b5af55ff049f7f76ecd6
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Zusammenarbeit mit Kreditoren mithilfe des Kreditorenportals

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie Einkaufsvertreter das Kreditorenportal nutzen können, um mit externen Kreditoren während des Bestellungsbestätigungsprozesses zusammenzuarbeiten. Diese Informationen gelten nur für die Versionen Februar 2016 &amp; und Mai 2016 von Dynamics AX.

Die Informationen in diesem Thema betreffen nur die Versionen Februar 2016 und Mai 2016 von Microsoft Dynamics AX. Die Kreditorenportalfunktion wurde durch die erweiterte Kreditorenzusammenarbeitfunktion in Dynamics 365 for Operations Version 1611 ersetzt. Weitere Informationen über die neue Kreditorenzusammenarbeitsfunktion finden Sie unter [Nutzung der Kreditorenzusammenarbeit mit externen Kreditoren](vendor-collaboration-work-external-vendors.md)  

Das Kreditorenportal wendet sich an Kreditoren, die über keine EDI-Iintegration (Electronic Data Interchange) mit Microsoft Dynamics AX für den Austausch von Bestellungsinformationen (PO) verfügen. Das Portal ermöglicht Einkaufsvertretern, eine PO an den Kreditor zu senden und die Antwort „Bestätigt“ oder „Abgelehnt“ direkt in Dynamicx AX zu erhalten.  

Der Prozess kann so konfiguriert werden, dass eine Bestätigung vom Kreditor automatisch den Auftrag bestätigt. Das bedeutet, dass die Weiterverfolgung nur gelegentlich erforderlich ist, wenn ein Auftrag abgelehnt oder die Bestätigung des Kreditors als Antwort erfasst wird, der Status der Bestellung jedoch aufgrund eines Problems im Bestätigungsprozess nicht auf **Bestätigt** aktualisiert wird.

## <a name="po-confirmation-and-rejection"></a>Bestellbestätigung und -Ablehnung
PO werden in Dynamics AX vorbereitet. Wenn Sie eine Bestellung haben, die den Status **Genehmigt** aufweist, senden Sie sie an den Kreditor, indem Sie eine Bestätigungsanforderung generieren. Wenn Sie die Aufmerksamkeit des Kreditors auf die neue Bestellung lenken möchten, können Sie die Bestellung auch per E-Mail senden, indem Sie das Druckverwaltungssystem verwenden. Die Bestellung wird im Kreditorenportal angezeigt, mit einer Option, über die der Kreditor sie genehmigen oder ablehnen kann. Der Kreditor kann auch Kommentare hinzufügen, um Informationen wie Änderungen an der Bestellung mitzuteilen.  

Im Kreditorenportal kann der Kreditor Auftragspositionen sehen. Diese Positionen umfassen Informationen wie die externe Produktnummer, die Dimensionen, die Preisangaben, Menge, das Lieferdatum und die Lieferadresse. Der Kreditor kann einen Bericht generieren, um die Bestellinformationen anzuzeigen. Dieser enthält auch den Gesamtpreis. Belastungen, die für den Kreditor relevant sind, werden angezeigt, wenn der Kreditor auf die Schaltfläche **Belastungen** im Kopf oder in den Positionen klickt. Kreditoren können Bestellinformationen in ihr eigenes System importieren, indem die Funktion **Nach Excel exportieren** verwenden.  

In der folgenden Tabelle wird der übliche Nachrichtenaustausch angezeigt, abhängig davon, wie der Kreditor antwortet, wenn Sie ihm eine Bestellung zur Bestätigung senden:

| Antworttyp                                                                                                  | Ergebnis                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Kreditor bestätigt die Bestellung. Das System ist konfiguriert, um POs automatisch zu bestätigen, wenn der Kreditor bestätigt.    | Der Status einer Bestellstatus wird auf **Bestätigt** aktualisiert. Wenn der Auftrag aus einem bestimmten Grund nicht aktualisiert werden kann, wird die Antwort des Kreditors trotzdem als **Bestätigt** erfasst, die Bestellung bleibt aber im Status **Externe Prüfung**.                                                                       |
| Der Kreditor bestätigt die Bestellung. Das System ist nicht konfiguriert, um POs automatisch zu bestätigen, wenn der Kreditor bestätigt. | Die Antwort des Kreditors wird als **Bestätigt** erfasst, die Bestellung bliebt jedoch im Status **Externe Prüfung**.                                                                                                                                                                                      |
| Der Kreditor lehnt die Bestellung ab.                                                                                     | Die Antwort des Kreditors wird als **Abgelehnt** erfasst, die Bestellung bliebt jedoch im Status **Externe Prüfung**. Die Ablehnung wird zusammen mit der Ursache und einem Vorschlag für Änderung, wie ein alternatives Lieferdatum empfangen. Sie aktualisieren die Bestellung und Senden anschließend eine neue Version zur Bestätigung. |

## <a name="changes-to-a-po"></a>Änderungen an einer Bestellung
Wenn Sie eine Bestellung ändern müssen, die bereits bestätigt wurde, können Sie eine neue Bestellung über das Kreditorportal an den Kreditor senden. Die neue Bestellung weist einen Versionssuffix auf, der anzeigt, dass es sich um eine geänderte Version einer Bestellung handelt, die zuvor mitgeteilt wurde. Über das Kreditorenportal können Kreditoren die Historie jedes Auftrags verfolgen. Die zuvor bestätigte Version der Bestellung bleibt in der Liste bestätigter POs, bis die neue Bestellung bestätigt wurde.  

Wenn Sie eine Bestellung stornieren, wird der Status wieder zu **Genehmigt** geändert. Sie müssen sie über das Kreditorportal zurück an den Kreditor senden, sodass der Kreditor die Stornierung bestätigen oder ablehnen kann. Nachdem die Stornierung bestätigt wurde, wird die Bestellung in der Liste bestätigter PO des Kreditors als **Storniert** angezeigt.

## <a name="versions-status-transitions-and-change-management"></a>Versionen, Statusübergang und Änderungsmanagement
Wenn eine Bestellung an den Kreditor gesendet wird, wird sie im System als bestimmte Version der Bestellung registriert, und der Status wechselt von **Genehmigt** zu **Externe Prüfung**. Wenn die Bestellung später geändert wird, wird eine neue Version der Bestellung erstellt, und der Status wird zurück in **Genehmigt** geändert (oder der Status wird in **Entwurf** geändert, wenn das Änderungsmanagement aktiviert ist).  

Die folgende Tabelle enthält ein Beispiel der Änderungen des Status und der Version, die eine Bestellung durchlaufen kann.

| Aktion                                                   | Status und Version                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Die ursprüngliche Version der Bestellung wird in Dynamics AX erstellt. | Der Status ist **Genehmigt**.                                                                           |
| Die Bestellung wird an das Kreditorenportal gesendet.                     | Eine Version wird im Kreditorenportal erfasst, und der Status wird in **Externe Prüfung** geändert.    |
| Sie nehmen einige Änderungen vor, die vom Kreditor gefordert werden.  | Der Status wird zurückgeändert in **Genehmigt**.                                                            |
| Sie senden die neue Version der Bestellung an das Kreditorenportal. | Eine neue Version wird im Kreditorenportal erfasst, und der Status wird in **Externe Prüfung** geändert. |
| Der Kreditor genehmigt die neue Version der PO.           | Der Status wird zurückgeändert in **Bestätigt**.                                                                |

Um die Versionen der Bestellung anzuzeigen, die an den Kreditor gesendet wurden, sowie die Antworten des Kreditors, klicken Sie auf **Erfassungen** &gt; **Bestätigungsanforderungen**  der Bestätigungsanforderung  

Bestellungen, die dem Kreditor für eine Antwort zugesendet wurden und den Status **Externe Prüfung**“ haben, werden entweder in der Liste **Bestellungen wurden an das Kreditorenportal gesendet, Warten auf Antwort** oder **Bestellungen wurden an das Kreditorenportal gesendet, Antwort erfordert Aktivität** ausgewählt. Wenn Sie eine Bestellung, die an den Kreditor gesendet wurde, ändern, sodass der Status zurück zu **Genehmigt** wechselt, wird die Bestellung nicht mehr in diesen Listen angezeigt. Um sehen, ob es zuvor eine Antwort für den Auftrag vom Kreditor gab, klicken Sie auf **Erfassung** &gt; **Bestätigungsanforderungen**.  

Kreditoren müssen die Bestellung im Kreditorenportal nicht bestätigen. Sie können auch eine E-Mail-Nachricht senden oder ihrer Zustimmung zu einer Bestellung über andere Kanäle vermitteln. Sie können den Auftrag dann manuell in Dynamics AX bestätigen. In diesem Fall erhalten Sie eine Warnung, dass der Auftrag bestätigt wird, obwohl keine Antwort vom Kreditor vorhanden ist. Die Bestellung wird dann in der Bestätigungshistorie im Kreditorenportal als offener, bestätigter Auftrag ohne Antworten aufgeführt. Der Kreditor hat zusätzlich nicht mehr die Möglichkeit, die Bestellung zu bestätigen oder abzulehnen.  

**Hinweis:** Die Version der Bestellung, die anderen Prozessen in Dynamics AX zur Verfügung steht, ist immer die neueste Version, auch wenn diese Version noch nicht erfasst wurde.

### <a name="change-management"></a>Änderungsverwaltung

Wenn Sie das Änderungsmanagement für eine Bestellung aktiviert haben, durchläuft die Bestellung einen Genehmigungsworkflow bis zum Status **Genehmigt**. Dieser Prozess wird dem Kreditor nicht angezeigt.  

Wenn das Änderungsmanagement für eine Bestellung aktiviert ist, wird die Version erfasst, wenn die Bestellung genehmigt wird, nicht wenn die Bestellung an den Kreditor geschickt oder bestätigt wird.  

Die folgende Tabelle enthält ein Beispiel der Änderungen des Status und der Version, die eine Bestellung durchlaufen kann, wenn das Änderungsmanagement aktiviert ist:

| Aktion                                                                                                        | Status und Version                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die ursprüngliche Version der Bestellung wird in Dynamics AX erstellt.                                                      | Der Kopfstatus ist **Entwurf**.                                                                                                                                                                                                                                                                                                                                                                    |
| Die Bestellung wird zum Genehmigungsprozess übermittelt. (Dies ist ein interner Prozess, an dem der Kreditor nicht beteiligt ist.) | Der Status wird von in **Entwurf** auf **Wird überprüft** und **Genehmigung** geändert, wenn die Bestellung nicht bei der Genehmigungsprozedur abgelehnt wird. Die genehmigte Bestellung wird als eine Version erfasst.                                                                                                                                                                                                                     |
| Die Bestellung wird an das Kreditorenportal gesendet.                                                                           | Die Version wird im Kreditorenportal erfasst, und der Status wird in **Externe Prüfung** geändert.                                                                                                                                                                                                                                                                                        |
| Sie nehmen einige Änderungen vor, die vom Kreditor gefordert werden.                                                       | Der Status wird zurückgeändert in **Entwurf**.                                                                                                                                                                                                                                                                                                                                                    |
| Die Bestellung wird erneut zum Genehmigungsprozess übermittelt.                                                            | Der Status wird von in **Entwurf** auf **Wird überprüft** und **Genehmigung** geändert, wenn die Bestellung nicht bei der Genehmigungsprozedur abgelehnt wird. Alternativ kann das System so konfiguriert werden, dass bestimmte Feldänderungen keine erneute Genehmigung erfordern. In diesem Fall wird der Status zuerst in **Entwurf** geändert und wird dann automatisch auf **Genehmigt** aktualisiert. Die genehmigte Bestellung wird als eine neue Version erfasst. |
| Sie senden die neue Version der Bestellung an das Kreditorenportal.                                                      | Die neue Version wird im Kreditorenportal erfasst, und der Status wird in **Externe Prüfung** geändert.                                                                                                                                                                                                                                                                                    |
| Der Kreditor genehmigt die neue Version der PO.                                                                | Der Status wird entweder automatisch in **Bestätigt** geändert oder wenn Sie die Antwort vom Kreditor erhalten und die Bestellung dann bestätigen.                                                                                                                                                                                                                                                     |
<a name="see-also"></a>Siehe auch
--------

[Konfigurieren der Sicherheit für Kreditorenportalbenutzer](configure-security-vendor-portal-users.md)

[Arbeitsbereich für Kreditor-Kooperationsrechungen](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)




