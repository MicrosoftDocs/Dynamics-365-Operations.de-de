---
title: Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites
description: In diesem Thema wird beschrieben, wie Sie die Zahlungsmethode des Kundenkontos in Microsoft Dynamics 365 Commerce konfigurieren. Außerdem wird beschrieben, wie sich Kreditlimits auf die Erfassung von Auf-Rechnung-Zahlungen auf Business-to-Business-(B2B)-E-Commerce-Websites auswirken.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a55a5d4c9dbf7909af5219843fc4310b6cdd4ed7
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689636"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Zahlungsmethode des Kundenkontos in Microsoft Dynamics 365 Commerce konfigurieren. Außerdem wird beschrieben, wie sich Kreditlimits auf die Erfassung von Auf-Rechnung-Zahlungen auf Business-to-Business-(B2B)-E-Commerce-Websites auswirken.

Einzelhändler können für die von ihnen verkauften Produkte und angebotenen Dienstleistungen verschiedene Zahlungsformen in einem E-Commerce-Kanal akzeptieren. Jeder vom Einzelhändler akzeptierte Zahlungstyp muss beim Einrichten des Systems in Dynamics 365 Commerce konfiguriert werden. Die Zahlungsmethode „Kundenkonto“ (oder „Auf Rechnung“) muss auf B2B-E-Commerce-Websites unterstützt werden. 

## <a name="prerequisites"></a>Voraussetzungen

1. Fügen Sie die Zahlungsmethode „Kundenkonto“ in der Commerce-Zentralverwaltung hinzu.
2. Verknüpfen Sie die Zahlungsmethode „Kundenkonto“ mit dem E-Commerce-Kanal.
3. Stellen Sie sicher, dass die Eigenschaft **Auf Rechnung zulassen** für den Kunden unter **Einzelhandel und Handel \> Kunden \> Alle Kunden \> Zahlungsstandards** in der Commerce-Zentralverwaltung aktiviert ist.

    > [!NOTE]
    > Wenn für alle Kunden die Zahlung „Auf Rechnung“ aktiviert sein soll, können Sie die Eigenschaft **Auf Rechnung zulassen** auf **Ja** für den Standardkunden des Kanals einstellen, der der B2B-Site zugeordnet ist. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Aktivieren der Zahlungsmethode „Kundenkontos“ im Commerce-Website-Generator 

Führen Sie folgende Schritte aus, um die Zahlungsmethode „Kundenkontos“ im Commerce-Website-Generator zu aktivieren.

1. Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.
1. Stellen Sie die **Kundenkontenzahlungen aktivieren**-Eigenschaft auf **Für B2B-Kunden aktiviert**. 
1. Wählen Sie **Speichern und veröffentlichen**.

> [!NOTE]
> Die neuen Seiteneinstellungen werden erst wirksam, nachdem die Datei App.settings.json aktualisiert wurde. Weitere Informationen finden Sie unter [SDK- und Modulbibliothek-Updates](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Aktivieren der Zahlungsmethode „Kundenkonto“ auf der Auftragsabschlussseite für die B2B-E-Commerce-Website

Führen Sie diese Schritte aus, um die Zahlungsmethode „Kundenkonto“ auf der Auftragsabschlussseite für die B2B-E-Commerce-Website zu aktivieren.

1. Suchen und bearbeiten Sie im Commerce-Website-Generator die Auftragsabschlussseite oder das Fragment, das das Auftragsabschlussmodul für die B2B-E-Commerce-Website enthält.
1. Wählen Sie Im **Kassenbereichcontainer**-Slot **Modul hinzufügen** aus, und fügen Sie dann ein **Kundenkontozahlung**-Modul hinzu.
1. Positionieren Sie das **Kundenkontozahlung**-Modul durch Auswahl der Auslassungspunkte (**...**), und wählen Sie dann je nach Bedarf **Nach oben** oder **Nach unten**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Bestätigen, dass die Zahlungsmethode „Kundenkonto“ aktiviert und veröffentlicht wurde

Führen Sie diese Schritte aus, um zu bestätigen, dass die Zahlungsmethode „Kundenkonto“ aktiviert und veröffentlicht wurde.

1. Melden Sie sich bei der E-Commerce-Website an.
1. Fügen Sie ein Produkte zum Warenkorb hinzu.
1. Zur vorherigen Auftragsabschlussseite wechseln. Sie sollten die neue **Kundenkonto**-Zahlungsmethode sehen.

## <a name="work-with-credit-limits"></a>Mit Kreditlimits arbeiten

Wenn die Funktionen für Kundenkontozahlungen auf der B2B-Site aktiviert sind, möchten Unternehmen normalerweise während des Bestellerfassungsprozesses Informationen zu Kreditlimits und Kreditlimitsalden anzeigen. Das Kreditlimit für einen Kunden wird durch die Eigenschaft **Kreditlimit** auf dem Inforegister **Kredit und Inkasso** des Kundendatensatzes in der Commerce-Zentralverwaltung festgelegt. In B2B-Szenarien sollte ein Auftrag, den ein Kunde aufgibt, jedoch häufig dem Konto der Organisation in Rechnung gestellt werden, zu der der Kunde gehört. Daher muss die Eigenschaft **Rechnungskonto** im Inforegister **Rechnung und Lieferung** des Kundendatensatzes zur Kundenkonto-ID der Organisation. Wenn der Kunde dann ein Auftrag auf der B2B-Site aufgibt, wird der Auftrag der Organisation in Rechnung gestellt. Die B2B-Site verwendet auch das Kreditlimit der Organisation und nicht das Kreditlimit, das im Kundendatensatz definiert ist.

Die Kreditlimitberechnung und der Kreditlimitsaldo, die auf der B2B-Website angezeigt werden, hängen von der Einstellung der Eigenschaft **Kreditlimitart** in der Commerce-Zentralverwaltung ab. Die Lage dieser Eigenschaft variiert, je nachdem, ob die Funktion **Kreditmanagement** im Arbeitsbereich **Funktionsverwaltung** aktiviert ist:

- Wenn die Funktion **Kreditmanagement** aktiviert ist, befindet sich die Eigenschaft im Inforegister **Kreditlimits** unter **Kredit und Inkasso \> Einrichten \> Kredit- und Inkassoparameter \> Kredit**. 
- Wenn die Funktion **Kreditmanagement** deaktiviert ist, befindet sich die Eigenschaft unter **Kreditwürdigkeit** bei **Debitorenkonten \> Einrichten \> Debitorenkontoparameter \> Kreditwürdigkeit**.

Die Werte, die von der Eigenschaft **Kreditlimitart** unterstützt werden, sind **Keine**, **Saldo**, **Saldo + Lieferschein oder Produktzugang** und **Saldo + Alle**. Weitere Informationen zu diesen Werten finden Sie unter [Werte der Kreditlimitart](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Wir empfehlen Ihnen, die Eigenschaft **Kreditlimitart** auf **Saldo + Lieferschein oder Produktzugang** festzulegen, sodass offene Verkaufsaufträge nicht zur Saldenberechnung beitragen. Wenn Ihre Kunden dann in Zukunft Aufträge aufgeben, müssen sie sich keine Sorgen machen, dass diese Aufträge ihren aktuellen Kontostand beeinträchtigen.

Eine weitere Eigenschaft, die sich auf die Auf-Rechnung-Aufträge auswirkt, ist die Eigenschaft **Kreditlimit erforderlich** im Inforegister **Kredit und Inkasso** des Kundendatensatzes. Wenn Sie diese Eigenschaft für bestimmte Kunden auf **Ja** festlegen, können Sie das System dazu zwingen, ihr Kreditlimit zu prüfen, auch wenn die Eigenschaft **Kreditlimit-Typ** auf **Keiner** festgelegt wurde, um anzugeben, dass das Kreditlimit für keinen Kunden geprüft werden soll.

Aktuell kann ein Kunde mit der Akonto-Zahlungsmethode nicht mehr als das Restguthaben für eine Bestellung bezahlen. Wenn der verbleibende Habensaldo des Kunden beispielsweise 1.000 $ beträgt, der Auftrag aber einen Wert von 1.200 $ hat, kann der Kunde nur 1.000 $ mit der Akonto-Methode bezahlen. Der Kunde muss dann eine andere Zahlungsmethode verwenden, um den Restbetrag zu bezahlen. In einer zukünftigen Version wird eine Commerce-Konfiguration es den Benutzern ermöglichen, mehr als ihr Kreditlimit auszugeben, wenn sie Bestellungen aufgeben.

Das Modul **Kredit und Inkasso** verfügt über neue Kreditmanagementfunktionen. Um diese Funktionen zu aktivieren, aktivieren Sie die Eigenschaft **Kreditmanagement** im Arbeitsbereich **Funktionsverwaltung**. Eine der neuen Funktionen ermöglicht es, Verkaufsaufträge auf der Grundlage von Sperrregeln zu sperren. Die Persona des Kreditmanagers kann die Aufträge dann nach weiterer Analyse freigeben oder ablehnen. Die Möglichkeit, Verkaufsaufträge zu sperren, gilt jedoch nicht für E-Commerce-Aufträge, da Verkaufsaufträge oft eine Vorauszahlung haben und die Funktion **Kreditmanagement** Vorauszahlungsszenarien nicht vollständig unterstützt. 

Egal ob die Funktion **Kreditmanagement** aktiviert ist oder nicht, werden die Verkaufsaufträge nicht gesperrt, wenn ein Kundensaldo während der Auftragserfüllung das Kreditlimit überschreitet. Stattdessen generiert Commerce je nach Wert des Felds **Meldung bei Überschreitung des Kreditlimits** im Inforegister **Kreditlimits** entweder eine Warnmeldung oder eine Fehlermeldung.

Die Eigenschaft **Vom Kreditmanagement ausschließen**, die verhindert, dass Commerce-Verkaufsaufträge gesperrt werden, befindet sich in der Auftragskopfzeile (**Einzelhandel und Handel \> Kunden \> Alle Verkaufsaufträge**). Wenn diese Eigenschaft auf **Ja** (den Standardwert) für Commerce-Verkaufsaufträge eingestellt ist, werden die Aufträge vom gesperrten Workflow des Kreditmanagements ausgeschlossen. Obwohl die Eigenschaft **Von Kreditmanagement ausschließen** heißt, wird das festgelegte Kreditlimit weiterhin während der Auftragserfüllung verwendet. Die Aufträge werden nur nicht gesperrt.

Die Funktion, Commerce-Verkaufsaufträge basierend auf Sperrregeln zu sperren, ist für zukünftige Commerce-Versionen geplant. Bis dahin können Sie die folgenden XML-Dateien in Ihrer Visual Studio-Lösung anpassen, wenn Sie Commerce-Verkaufsaufträge erzwingen müssen, um die neuen Kreditmanagementflows zu durchlaufen. Ändern Sie in den Dateien die Logik so, dass die Markierung **CredManExcludeSalesOrder** auf **Nein** gesetzt ist. Auf diese Weise wird die Eigenschaft **Vom Kreditmanagement ausschließen** für Commerce-Verkaufsaufträge standardmäßig auf **Nein** gesetzt.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Wenn die Markierung **CredManExcludeSalesOrder** auf **Nein** gesetzt ist und ein B2B-Kunde in Geschäften einkaufen kann, indem er die Point-of-Sale-Anwendung (POS-Anwendung) verwendet, kann die Buchung von Cash-and-Carry-Transaktionen fehlschlagen. Zum Beispiel: Es gibt eine Sperrregel für die Zahlungsart „Bar“ und der B2B-Kunde hat einige Artikel im Geschäft bar bezahlt. In diesem Fall wird der resultierende Verkaufsauftrag nicht erfolgreich in Rechnung gestellt, da er gesperrt wird. Daher schlägt die Buchung fehl. Aus diesem Grund empfehlen wir Ihnen, nach der Implementierung dieser Anpassung End-to-End-Tests durchzuführen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Website für B2B-E-Commerce einrichten](set-up-b2b-site.md)

[B2B-Geschäftspartner mithilfe von Kundenhierarchien verstehen](partners-customer-hierarchies.md)

[Benutzer von Geschäftspartnern auf Websites für B2B-E-Commerce verwalten](manage-b2b-users.md)

[Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites](quantity-limits.md)

[SDK- und Modulbibliothekupdates](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
