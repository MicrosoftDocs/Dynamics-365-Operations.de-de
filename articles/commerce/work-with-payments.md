---
title: Zahlungsmethoden in Callcentern
description: Dieses Thema behandelt verschiedene Zahlungsmethoden, die in einem Callcenter in Dynamics 365 Commerce verwendet werden können.
author: josaw1
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ff1cf8619bc94c35e416b2c7dcf2350d2238dbf5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793896"
---
# <a name="payment-methods-in-call-centers"></a>Zahlungsmethoden in Callcentern

[!include [banner](includes/banner.md)]

In Dynamics 365 Commerce umfasst die Konfiguration des Callcenterkanals eine Einstellung, die mit **Aktivieren Sie Auftragsabschluss** bezeichnet wird. Diese Einstellung stellt sicher, dass alle Aufträge, die Benutzer des Kanals erstellen, zur Verarbeitung der Bestellung nur dann freigegeben wird, nachdem sie eine Vorauszahlung oder eine vor-autorisierte Bezahlung getätigt haben, die in der genehmigten Toleranz ist. Wenn die Einstellung **Aktivieren Sie Auftragsabschluss** aktiviert ist, können Callcenterbenutzer Zahlungen mit Aufträgen für die Debitoren eingeben, indem Sie die Funktionen des Callcenters der Zahlung verwenden möchten. Wenn die Einstellung deaktiviert ist, können die Callcenternutzer die Callcenterzahlung nicht nutzen, aber sie können die Vorauszahlungen für Aufträge trotzdem anwenden, indem die Standarddebitorfunktionen verwendet werden.

Im Rahmen von Kanalkonfigurationen kann ein Unternehmen die Zahlungsmethoden definieren, die für einen Callcenterkanal zulässig sind. Der Callcenterkanal verwendet die gleichen Zahlungsmethoden, die für die Shopkanäle definiert werden.

Um die Zahlungsmethoden für einen Callcenterkanal zu konfigurieren, wechseln Sie zu **Einzelhandel und Handel** \> **Kanäle** \> **Callcenter** \> **Alle Callcenter** und wählen Sie dann im Menü **Einstellungen** die Option **Zahlungsmethoden**.

Achten Sie bei der Auswahl einer Zahlungsmethode darauf, dass Sie fünf Zahlungsmethodenfunktionen zuordnen können.

| Funktion            | Beschreibung |
|---------------------|-------------|
| Normal              | Verwenden Sie die Funktion **Normal** auf der Zahlungsmethode, wenn Sie Zahlungsmethoden wie Barzahlung oder Belege definieren. Wenn diese Arten von Zahlungen in einem Auftrag im Callcenter angewendet werden, ist die Markierung **Vorab bezahlen** standardmäßig auf **Ja** festgelegt. Dadurch wird sofort ein Vorauszahlungsbeleg dem Debitorenkonto gebucht, falls dieser Auftrag übermittelt wird. Benutzer können die Markierung **Vorab bezahlen** auf **Nein** ändern, sofern gewünscht, sodass der Zahlungsbeleg erst bei Rechnungsbuchung erstellt wird. Der Vorauszahlungsbeleg wird im Debitorenbuchungsverlauf gebucht, in der er systematisch für die Rechnung für den Auftrag ausgeglichen wird, wenn Rechnungen erstellt werden. |
| Scheck               | Verwenden Sie die Funktion **Scheck**, wenn Sie ein Bankscheckinstrument als Zahlungsweise definieren. Wenn dieser Typ der Zahlung an einen Auftrag übernommen wird, muss der Benutzer die Nummer des Debitors als Teil des Zahlungsanwendungsprozesses eingeben. Scheckzahlungen werden immer als Vorauszahlungen behandelt, wenn sie angewendet werden und Zahlungsbelege werden direkt nach Auftragsunterordnung erstellt. Dese Vorauszahlungsbelege werden systematisch ausgeglichen für die Rechnungen, die für den Auftrag erstellt werden. |
| Karten               | Kartenzahlungstypen stellen alle Typen von Zahlung dar, die die Eingabe einer Kartennummer benötigen, die auf der Zahlungsmethode des Debitors definiert wurde. Hierzu gehören Kreditkarten und Geschenkkarten. Wenn Sie die verschiedenen Typen von Zahlungen konfigurieren, müssen Sie das **Karteneinstellungen** Menü verwenden, um die Karten-Ids zu definieren, die dieser Zahlungsmethode zugeordnet werden. Zum Zeitpunkt der Verkaufserfassung kann der Benutzer angeben, ob die Kartenzahlung vorausbezahlt wird, indem die Option **Vorab bezahlen** auf der Zahlungseintragsseite angegeben wird. Sofern die Vorauszahlungen vom Unternehmen gerfordert wird, ist der Ablauf einer typischen echten Kreditkartenzahlung in zwei Schritten aufgeteilt, die Autorisierung erfolgt zum Zeitpunkt der Verkaufserfassung und die Zahlung wird über die Karte des Debitors bei Rechnungsstellung ausgeglichen und übernommen. Für Geschenkkartezahlungen Vorauszahlung wird empfohlen, da der Geschenkkartensaldo sofort verringert werden soll, damit der Debitor nicht gelten kann dass derselbe Wert an. |
| Kunde            | Die Funktion **Debitor** für eine Zahlungsmethode bedeutet, dass die Zahlung für das Kreditlimit des Debitors oder für die Krediterweiterung angewendet wird. In Commerce kann einem Kunden ein Kreditlimit zugewiesen werden, das bei der Auftragserfassung geprüft werden kann. Zahlungen, die erfolgen, indem eine Zahlungsmethode gebucht werden kann, die mit der Funktion **Debitor** verknüpft wird, erstellt Verbindlichkeiten für das Debitorenkonto. Wird der Auftrag fakturiert, wird ein fälliger Saldo angezeigt. In solchen Fällen senden Debitoren in der Regel eine Zahlung, entsprechend den Bedingungen, die angegeben wurden. Alternativ kann ein vorheriger Blankokreditbeleg im Feld Debitorenkonto angewendet werden, um den Saldo zu begleichen, der fällig ist. Beachten Sie, dass, wenn Sie diese Zahlungsmethode definieren, sie nicht mehr auf den Zahlungs-Auswahloptionen in der Callcenterauftragserfassung angezeigt wird, es sei denn, die Markierung ist auf **Ermöglichen Sie Krediterweiterung** ist im Debitorendatensatz für den Debitor festgelegt, mit dem Sie arbeiten. Diese Markierung findet man auf der Registerkarte **Standardwerte für Zahlungen** des Debitorendatensatzes. |
| Zahlungsmittel entfernen/Wechselgeld | Die Funktion **Zahlungsmittel entfernen/Wechselgeld** wird nicht durch das Callcenter verwendet. Sie trifft jedoch nur zu, wenn Sie die Zahlungsmethode definieren, die die Verkaufsstelle (POS)- Anwendung in einem Shopkanal verwendet. |

Während Zahlungsmethoden definiert werden, sollten sie mit einem Sachkonto oder einem Bankkonto verknüpft werden. Wenn Sie diesen Schritt auslassen, erhalten Benutzer Fehler, wenn Sie versuchen, den Zahlungstyp zu speichern.

## <a name="refund-payment-methods"></a>Rückzahlungsmethoden

Für die Preiserstattung-Szenarien, die verarbeitet werden, verwendet das Callcenter auch einige der Zahlungsmethoden, die im Modul "Debitoren" definiert werden. Um diese Zahlungsmethoden zu konfigurieren, gehen Sie zu **Einzelhandel und Handel** \> **Kanaleinrichtung** \> **Callcentereinrichtung** \> **Callcenter-Rückerstattungsmethoden**. Sie müssen diese Konfiguration ausführen, um Rückerstattungsschecks an Kunden zu verarbeiten. Wenn beispielsweise ein Kunde, der ursprünglich für einen Auftrag bezahlt wird, indem er Bargeld oder einen Scheck nutzt, der Benutzer ihm einen Rückerstattungsscheck über das Kreditorenkonto senden soll. In diesem Fall müssen das Bargeld und die Schecks im Callcenter der korrekte Zahlungsmethode des Debitors zugeordnet werden, um sicherzustellen, dass die Preiserstattung ordnungsgemäß verarbeitet wird.

Wenn ein Benutzer darüber hinaus eine Rücklieferung als Callcenterbenutzer in Commerce verarbeitet, aber für die Rücklieferung für einen ursprüngliches Verkauf keine Verknüpfung erstellen kann, muss die **Rückzahlungs**-Methode in den Callcenter-Parametern definiert werden. Gehen Sie zu **Einzelhandel und Handel** \> **Kanaleinrichtung** \> **Callcentereinrichtung** \> **Callcenter-Parameter**, und klicken Sie dann auf der Registerkarte **Rücksendung/Rückgabe** ins Feld **Zahlungsmethode**, und überprüfen Sie, ob eine Zahlungsmethode definiert wird. Die Zahlungsmethode ist die Zahlungsmethode, die für Rückerstattungen verwendet wird. Normalerweise wird sie entweder als Scheck- oder Debitorenkontomethode definiert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]