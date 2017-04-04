---
title: Zahlungsmethoden das einem Callcenter
description: "Dieses Thema behandelt verschiedene Zahlungsmethoden, die in einem Callcenter in Einzelhandel und Handel verwendet werden können."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 636d83ecc7732a164924352853603588cded0db4
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods-in-a-call-center"></a>Zahlungsmethoden das einem Callcenter

Dieses Thema behandelt verschiedene Zahlungsmethoden, die in einem Callcenter in Einzelhandel und Handel verwendet werden können.

Die Zahlungsmethoden, die in anderen Kanälen im Einzelhandel und Handel in Microsoft Dynamics AX verwendet werden, wie Bargeld, Schecks, Kreditkarten und Geschenkkarten, können auch in Callcentern verwendet werden. Nachdem Sie eine Zahlungsmethode für ein Callcenter eingerichtet haben, wird es Callcenterbenutzern als eine der Optionen im Abschnitt **Zahlungen** der Seite **Auftrag** angezeigt. Sie können Coupons einrichten, um Rabatte für Debitoren anzubieten, die einen Auftrag bei dem Callcenter Ihrer Organisation aufgeben. Coupons können ein Rabatt mit festem Betrag oder ein Prozentsatz eines Artikelpreises oder der Gesamtsumme der Bestellung sein. Beispielsweise bietet ein betragsbasierter Coupon dem Debitor einen Rabatt von EUR 75,00, wenn dieser EUR 750,00 oder mehr ausgibt. Sie können verschiedene Arten von Coupons erstellen, übergeordnete/untergeordnete Coupons einrichten und Gutscheine kopieren oder stornieren. Verwenden Sie die Optionen in der folgenden Tabelle zum Erstellen von Gutscheinen.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Attribut**             | Geben Sie im Feld **Tilgungsrate **den Wert der erwarteten Tilgungsquote für den Coupon in Prozent ein, und wählen Sie dann aus, ob der Coupon ein Coupon zur einmaligen Verwendung ist, automatisch neu oder speziell für einen Debitor ausgestellt wird.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Gültig**                 | Geben Sie in den Feldern **Startdatum** und **Enddatum** das Datum der ersten und letzten Tage ein, an denen der Coupon gültig ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Einbeziehungs-/Ausschlussregeln** | Wählen Sie in den Feldern **Kataloge** und **Artikel** aus, ob Kataloge oder Artikel im Coupon enthalten oder ausgeschlossen sind. Wenn Sie **Einschließen** oder **Ausschließen** wählen, klicken Sie auf **Einrichten**,wählen **Kataloge einbeziehen/ausschließen** oder **Produkte einbeziehen/ausschließen** und geben Informationen über den Katalog oder Artikel ein. Wenn Sie **Keine** in diesen Feldern auswählen, werden alle Kataloge oder Artikel in den Coupon einbezogen.                                                                                                                                                                                                                          |
| **Sonstiges**         | Wenn dieser Gutschein nicht zusammen mit anderen Rabatten verwendet werden kann, wählen Sie das Kontrollkästchen **Exklusiv**. Wählen Sie anschließend im Feld **Ursprung** aus, wo der Gutschein verwendet werden kann. Aktivieren Sie das Kontrollkästchen **Herstellercoupon**, wenn es sich um den Coupon eines Herstellers handelt.                                                                                                                                                                                                                                                                                                                                                                |
| **Künftiger Coupon**         | Wenn dieser Coupon anderen Coupons übergeordnet ist, wählen Sie das Kontrollkästchen **Übergeordneter Coupon**. Wenn dieser Coupon einem vorhandenen Coupon untergeordnet ist, wählen Sie den übergeordneten Coupon im Feld **Kennung des übergeordneten Coupons** aus. Beispielsweise erstellen Sie einen Coupon für den bevorstehenden Frühlingskatalog. Alle anderen Coupons, die Sie für den Frühlingskatalog erstellen, wären untergeordnete Coupons des Frühlingskatalogcoupons. Untergeordnete Coupons beinhalten möglicherweise einen 20-Prozent-Rabatt für neue Kundenaufträge, einen 10-Prozent-Rabatt auf einen neuen Artikel oder EUR 95,00 Rabatt auf Aufträge ab EUR 1.000,00 oder mehr. |

Wenn Sie eine Kreditkartenzahlung vom Formular **Auftrag** übermitteln und eine Meldung erhalten, die angibt, dass die Karte nicht autorisiert wurde, können Sie die Autorisierung manuell ausführen. Sie können eine Kreditkartentransaktion auf der Seite **Autorisierungsmanagement** autorisieren, ablehnen oder erneut übermitteln. Die Seite "Callcenterparameter " wird verwendet, um zusätzliche Zahlungsabwicklungsoptionen zu konfigurieren:

-   Mit Schecksperren können Finanzmitarbeiter Aufträge verarbeiten, die gesperrt wurden, wenn die Zahlungsmethode "Scheck" eingegeben wurde und der Schwellenwertbetrag der Schecksperre überschritten wurde. Die Sperre kann manuell freigegeben werden oder automatisch am Ende des konfigurierten Zeitraums ablaufen.
-   Sie können durch Schwellenwerte festlegen, welche Rückerstattung über Scheck oder Kreditkarte manuell genehmigt werden muss. Jede Rückerstattung, die größer als der Schwellenbetrag ist, wird der Genehmigungswarteschlange hinzugefügt. Nachdem Sie die Rückerstattung genehmigt haben, kann die Auftragsrücksendung fakturiert werden.



