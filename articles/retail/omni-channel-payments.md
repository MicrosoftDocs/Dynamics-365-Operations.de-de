---
title: Übersicht Omni-Channel-Zahlungen
description: Dieses Thema bietet einen Überblick über die Omni-Kanalzahlungen in Microsoft Dynamics 365 for Retail.
author: rubendel
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 78a4538d5b4854a4c87417acc156bcfb7c0da01d
ms.sourcegitcommit: 45eeca48c6cb4f3f94d61392f4f99a52dc443a97
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2019
ms.locfileid: "1606191"
---
# <a name="omni-channel-payments-overview"></a>Übersicht Omni-Channel-Zahlungen

[!include [banner](../includes/banner.md)]

Dieses Thema bietet einen Überblick über die Omni-Kanalzahlungen in Microsoft Dynamics 365 for Retail. Er umfasst eine umfangreiche Liste von unterstützten Szenarien, Informationen über Funktionalität und Problembehandlung und Beschreibungen einige typischer Probleme.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Beschreibung |
|---|---|
| Token  | Eine Zeichenfolge von Daten, die ein Zahlungsprozessor als Referenz bereitstellt. Tokens können Zahlungs-Kartennummern, Zahlungsautorisierungen oder früheren Zahlungserfassungen darstellen. Token sind wichtig, da sie beitragen, sensible Daten vom Verkaufsstellen-System (POS) fernzuhalten. Sie werden manchmal auch als *Referenzen* bezeichnet. |
| Kartentoken | Ein Token, den ein Zahlungsprozessor zum Aufbewahren im POS-System angegeben hat. Ein Kartentoken kann nur von dem Einzelhändler verwendet werden, der ihn erhält. Kartentoken werden manchmal auch als *Kartenreferenzen* bezeichnet. |
| Autorisierungstoken (auth) | Eine eindeutige Kennung, die ein Zahlungsvorgang als Antwort bereitstellt, die an ein POS-System übermittelt wird, nachdem das POS-System einen Autorisierungsantrag stellt. Ein Autorisierungstoken kann später verwendet werden, wenn der Prozessor aufgerufen wird, um Aktivitäten wie Stornieren oder Stornieren der Autorisierung auszuführen. Oftmals werden sie dazu verwendet, Fonds zu erfassen, wenn ein Auftrag erfüllt oder eine Trasaktion abgeschlossen ist. Authorisierungstoken werden manchmal auch als *Authorisierungsreferenzen* bezeichnet. |
| Token erfassen | Eine Referenz, die ein Zahlungsprozessor einem POS-System bereitstellt, wenn eine Zahlung abgeschlossen oder aufgezeichnet wird. Das Erfassungstoken kann dann verwendet werden, um auf die Zahlung in nachfolgenden Arbeitsgängen wie Rückerstattungsanforderungen zu erfassen. | 
| Karte nicht vorhanden | Eine Bedingung, die sich auf eine Zahlungsbuchungen bezieht, wenn keine physische Karte vorhanden ist. Beispielsweise können diese Transaktionen in E-Commerce- oder Callcenterszenarien auftreten. Für diese Transaktionen werden die den Zahlungen zugeordneten Informationen manuell auf eine E-Commerce-Website, in einen Callcenterfluss oder im POS oder Zahlungsterminal eingegeben. |
| Karte vorhanden | Eine Bedingung, die sich auf Zahlungstransaktionen bezieht, in denen eine physischen Karte auf einem Zahlungsterminal vorgewiesen und verwendet wird, der mit dem Microsoft Dynamics 365 POS-System verbunden ist. |

## <a name="overview"></a>Übersicht

Im Allgemeinen beschreibt der Begriff *Omni-Kanal-Zahlungen* die Möglichkeit, einen Auftrag in einem Kanal zu erstellen und diesen in einem anderen Kanal zu erfüllen. Der Schlüssel zur Omni-Kanal-Zahlungunterstützung behält Zahlungsdetails zusammen mit den Restbetrag der Auftragsdetails und verwendet dann jene Zahlungsdetails, wenn der Auftrag zurückgerufen oder in einem anderen Kanal verarbeitet wird. Ein klassisches Beispiel ist das Szenarion „Einkauf online, Abholen im Geschäft“. In diesem Szenario werden die Zahlungsdetails hinzugefügt, wenn der Auftrag online erstellt wird. Sie werden dann am POS erneut aufgerufen, um die Zahlungskarte des Debitors bei der Abholung zu belasten. 

Alle Szenarien, die in diesem Thema beschrieben werden, können implementiert werden, wenn das Standardzahlungs-Software-Development Kit (SDK) verwendet wird, das mit Retail bereitgestellt wird. Die [Dynamics 365 Zahlungsverbindung für Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) stellt eine vordefinierte Implementierung jedes Szenarios zur Verfügung, das hier beschrieben wird. 

### <a name="prerequisites"></a>Voraussetzungen

Alle Szenarien, die in diesem Thema beschrieben werden, benötigen einen Zahlungskonnektor, der Omni-Kanalzahlungen unterstützt. Der vordefinierte Adyen-Konnektor kann auch verwendet werden, weil er die Szenarien unterstützt, die über das Zahlungen SDK bereitgestellt werden. Weitere Informationen dazu, wie Zahlungskonnektoren implementiert werden und Informationen zu Retail SDK im Allgemeinen finden Sie unter [Retail für It Pros und Entwickler-Startseite.](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Unterstützten Versionen

Die Omnikanal-Zahlungsfunktionen, die in diesem Thema beschrieben sind, wurden im Rahmen der Microsoft Dynamics 365 for Retail Version 8.1.3 freigegeben. 

#### <a name="card-present-and-card-not-present-connectors"></a>„Karte vorhanden“ und „Karte nicht vorhanden“ Verbindungen

Das Zahlungen-SDK basiert auf zwei Sätzen von Anwendungsprogrammierschnittstellen (APIs) für Zahlungen. Das erste Set von APIs nennt man **iPaymentProcessor**. Sie wird verwendet, um „Karte nicht vorhandene“ Zahlungskonnektoren zu implementieren, die in Callcentern und der Microsoft Dynamics e-Commerce-Plattform verwendet werden können. Weitere Informationen zur**iPaymentProcessor** Schnittstelle finden Sie im [Implementieren Sie einen Zahlungskonnektor und ein Zahlungsgerät](https://download.microsoft.com/download/4/D/7/4D7C6B05-0C23-4C6C-BA13-AB62ED08AA61/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device.docx) Whitepaper, das Zahlungen umfasst. 

Das zweite Set von APIs nennt man **iNamedRequestHandler**. Er unterstützt die Implementierung von „Karte vorhandenen“ Zahlungsintegrationen, die als Zahlungsterminal verwendet werden. Weitere Informationen zur **iNamedRequestHandler**-Schnittstelle finden Sie unter [Erstellen Sie eine Zahlungsintegration für ein Zahlungsterminal](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Einrichtung und Konfiguration

Die folgenden Komponenten und Einrichtungsschritte sind erforderlich:

- **eCommerce Integration:** Eine Integration mit Retail ist erforderlich, um Szenarien zu unterstützen, in denen ein Auftrag aus einem Online-Geschäft stammt. Weitere Informationen zu Retail-E-Commerce SDK finden Sie unter[E-Commerce-Plattform-Software Development Kit (SDK)](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). In einer Vorführungsumgebung unterstützt das Bezugsschaufenster das Omnikanal-Zahlungsszenarien. 
- **Online-Zahlungskonfiguration:** Die Einstellung des Online-Kanals muss einen Zahlungskonnektor enthalten, der aktualisiert wurde, um Omnikanalzahlungen zu unterstützen. Alternativ kann der vordefinierten Zahlungskonnektor verwendet werden. Informationen darüber, wie der für Adyen-Zahlungskonnektor für Onlineshops konfiguriert wird, finden Sie unter. [Adyen-Zahlungskonnektor](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) Zusätzlich zum Einrichtungsschritt für eCommerce, der in diesem Thema beschrieben sind, muss der Parameter **Speichern von Zahlungsinformationen in eCommerce zulassen** auf **Wahr** in den Einstellungen für den Adyen-Konnektor festgelegt werden. 
- **Omnikanal-Zahlungskonfiguration:** Im Back Office gehen Sie zu **Retail \> Headquarters Einstellung \>-Parameter \> Freigegebene Retail-Parameter**. Legen Sie anschließend auf der Registerkarte **Omnikanal-Zahlungen** die Option **Omnikanal-Zahlungen verwenden** auf **Ja** fest.
- **Zahlungsdienstleistungen:** Das Callcenter verwendet den Standardzahlungskonnektor auf der Seite **Zahlungsdienste** um Zahlungen zu verarbeiten. Um Szenarien wie „Einkauf im Callcenter, Abholung im Shop“ zu unterstützen, muss dieser Standardzahlungskonnektor der Adyen-Zahlungskonnektor oder ein Zahlungskonnektor sein, der die Implementierungsbedingungen für Omnikanal-Zahlungen erfüllt.
- **Überweisungs-Dienstleistungen:** Zahlungen über einen Zahlungsterminal müssen im Inforegsiter **Elektronische Überweisung** des Hardwareprofils eingerichtet werden. Der Adyen-Konnektor unterstützt Omnikanal-Zahlungs-Szenariostandards. Andere Zahlungskonnektoren, die die Schnittstelle **iNamedRequestHandler** unterstützen, können auch verwendet werden, wenn sie Omnikanal-Zahlungen unterstützen.
- **Zahlungskonnektorverfügbarkeit:** Wenn ein Auftrag erneut aufgerufen wird, enthalten die Zahlungsmittelpositionen, die zusammen mit dem Auftrag aufgerufen werden, den Namen des Zahlungskonnektors, der verwendet wurde, um die Autorisierungen zu erstellen, die diesem Auftrag zugeordnet sind. Wenn der Auftrag abgeschlossen ist, versucht das SDK Zahlungen, den gleichen Konnektor zu verwenden, der verwendet wurde, um die ursprüngliche Autorisierung zu erstellen. Daher muss ein Zahlungskonnektor, der dieselben Handelseigenschaften hat, zur ERfassung verfügbar sein. 
- **Kartentypen:** Damit Omnikanal-Szenarien einwandfrei funktionieren, muss jeder Kanal die gleiche Einstellung für Zahlungsmitteltypen haben, die für Omnikanal verwendet werden können. Diese Einstellung beinhaltet Zahlungsmethoden-Kennungen und Kartentyp-Kennungen. Wenn beispielsweise der Zahlungsmitteltyp **Karten** eine Kennung **2** in der Onlineshopeinstellung hat, sollten sie dieselbe Kennung in der Ladengeschäftseinstellung haben. Dieselbe Anforderung gilt für Kartentyp-Kennungen. Wenn die Kartennummer **12** auf **VISUM** im Onlineshop festgelegt wurde, muss dieselbe Kennung für den Retail Shop eingerichtet werden. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Grundlegende Prinzipien, die Omnikanal-Zahlungen unterstützen

Zahlungskonnektoren und Zahlungsverarbeitungsstellen verwenden Token oder Referenzen, um auf Interaktionen zu verweisen, die den Kartenzahlungen zugeordnet werden. Wenn beispielsweise eine Zahlungsautorisierung angefordert wird, wird eine Referenz zu dieser Autorisierung bereitgestellt. Daher kann später auf die Autorisierung verwiesen werden, wenn Mitteln zum Zeitpunkt der Erfüllung erfasst werden. Diese Autorisierung ist für den Einzelhändler, den Zahlungskonnektor und den Prozessor eindeutig. 

Wenn ein Auftrag, der online erstellt wurde, im Shop abgeholt wird, müssen dieselben Zahlungsdetails für diesen Auftrag erneut aufgerufen und verwendet werden. Wenn die Originaldetails als Teil der Anforderung, eine Zahlung durch die ursprüngliche Autorisierung aufzuzeichnen, bereitgestellt werden, ist der Zahlungsprozessor in der Lage, die Anforderung zu bearbeiten und die Zahlung zu erfassen. 

Um auf die Onlinebestellung korrekt zu verweisen, muss ein Zahlungskonnektor „Karte nicht vorhanden“, der denselben Prozessor unterstützt, auch verfügbar sein. Auf diese Weise kann das POS-System einen Prozessor für Zahlungen „Karte vorhanden“ haben, aber er kann auch auf andere Zahlungsahlungskonnektoren zugreifen, damit er Aufträge erfüllen kann, die in anderen Kanälen erstellt werden, indem verschiedene Zahlungsverarbeitungsstellen verwendet werden. 

## <a name="supported-scenarios"></a>Unterstützte Szenarien

Die folgenden Omnikanal-Zahlungsszenarien werden unterstützt:

- Online kaufen und im Shop abholen
- Im Callcenter kaufen und In einem Shop abholen
- Im Callcenter kaufen und Im Shop B abholen
- Im Shop A kaufen und an den Debitor versenden

Abweichungen dieser Szenarien werden ebenfalls unterstützt. So kann eine Onlinebestellung beide Positionen umfassen nämlich jene, die an den Debitor versendet wird und jene, die im Shop abgeholt wird. Alle Auftragserfüllungsoptionen werden über Omnikanal-Zahlungen unterstützt. 

In den folgenden Abschnitten werden die Schritte für jedes Szenario beschrieben und es wird aufgezeigt, wie die Szenarien mithilfe von Demodaten verwendet werden. 

### <a name="buy-online-pick-up-in-store"></a>Online kaufen und im Shop abholen

Bevor Sie starten, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Sie haben ein Bezugsschaufenster, in dem der Adyen-Konnektor konfiguriert wird.
- Die Option **Omnikanal-Zahlungen** auf der Seite **Freigegebene Einzelhandelsparameter** wird auf **Wahr** festgelegt.
- Der Adyen-Zahlungskonnektor wird für das Houston-POS-Register konfiguriert.

Um das Szenario auszuführen, führen Sie folgende Schritte aus:

1. Im Bezugsschaufenster erstellen Sie einen Auftrag für eine Abholung im Shop. Achten Sie darauf, das Sie den Shop **Houston** auswählen. 
2. Führen Sie die Zahlungsschritte aus und bezahlen Sie, indem Sie eine Testkreditkartennummer verwenden. Sie können finden Testkreditkartennummern auf der [Adyen-Test-Kartennummerseite](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. In Retail verwenden Sie den Stapelverarbeitungsauftrag **Aufträge synchronisieren** und den **P-001** Verteilungszeitplan, um die Aufträge im Back Office zu erstellen.
4. Im POS auf der Willkommensseite wählen Sie den Vorgang **Aufträge zur Abholung** aus, um die Aufträge zur Abholung im Shop anzuzeigen. 
5. Wählen Sie eine oder mehrere Zeilen aus dem Auftrag auf, der im Bezugsschaufenster erstellt wurde, und wählen Sie dann **Abholen**.

    Der Auftrag wird im Back Office abgerufen. 

6. Wenn die Auftragspositionsdetails im Back Office abgerufen werden und eine Kartenzahlung, die für Omnikanal verwendet werden kann erkannt wurde, Sie darüber informieren, dass eine Zahlungsmethode verfügbar ist.
7. Wählen Sie **Verfügbare Zahlungsmethode**, um die Buchung ausführen, indem die Kartendetails verwenden, die in das Bezugsschaufenster eingegeben wurden.

    Die Auftragspositionen werden auf der Transaktionsseite geladen und der fällige Saldo ist 0 (null). 

8. Wählen Sie die Registerkarte **Zahlungen** aus, um die Positionsbeträge anzuzeigen, die aus der Onlinebestellung gezogen wurden. 
9. Wählen Sie eine beliebige Zahlungsmethode aus, um die Transaktion abzuschließen. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Im Callcenter kaufen und In einem Shop abholen

1. Im Retail auf der Seite **Kundendienst** geben Sie **Karen-Berg** in der Suchenleiste ein, und wählen Sie dann **Suchen**. 
3. Wählen Sie **Karen-Berg** in den Suchergebnisse aus.
4. Nachdem Karen auf der Seite **Kundendienst** geladen ist, wählen Sie **Neuer Auftrag** aus.
5. Wählen Sie auf der Seite „Neuer Auftrag“ die **Kopfzeile**, um den Bestellkopf anzuzeigen. 
6. Auf der Seite **Auftragskopf** können Sie den Standort auf **Zentral** und den Lagerort auf **Houston** festlegen.
7. Auf der Registerkarte **Liefern** muss das Datum im Feld **Lieferart** für Debitorenaufnahme auf **60** festgelegt werden.
8. Wählen Sie **Positionen** aus und fügen Sie anschließend eine oder mehrere Position im Auftrag hinzu. 
9. Wählen Sie **Vollständig**, um den Auftragsabschlussfluss einzugeben.
10. Navigieren Sie nach unten zum Zahlungsabschnitt, wählen Sie **Hinzufügen** und wählen Sie dann eine Position aus, in der die  Zahlungsmethode auf **Karten** festgelegt wird. 
11. Wählen Sie das Pluszeichen (**+**) um eine Kartenzahlung hinzuzufügen. 
12. Hier können Sie die Details für eine Testkreditkartennummer eingeben, die Sie auf der [Adyen-Test-Kartennummerseite](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) gefunden haben und dann wählen Sie **OK**.

    > [!NOTE]
    > Wenn die Kartenmarke für die Kartennummer, die Sie eingegeben haben, von der Marke abweicht, die ausgewählt wurde, als die Zahlung ausgelöst wurde, wird die Zahlung dennoch ausgeführt. Allerdings wird sie auf die Konten gebucht, die der Kartenmarke zugeordnet werden, die Sie in Schritt 10 ausgewählt haben.

12. Wählen Sie **OK**aus, um das Dialogfeld **Auftragsabschlusszahlungen** zu schließen.
13. Wählen Sie auf der Seite **Auftragszusammenfassung** **Übermitteln** aus.
14. Im POS auf der Willkommensseite wählen Sie den Vorgang **Aufträge zur Abholung** aus, um die Aufträge zur Abholung im Shop anzuzeigen. 
15. Wählen Sie eine oder mehrere Zeilen aus dem Auftrag auf, der im Bezugsschaufenster erstellt wurde, und wählen Sie dann **Abholen**.

    Der Auftrag wird im Back Office abgerufen. 

16. Wenn die Auftragspositionsdetails im Back Office abgerufen werden und eine Kartenzahlung, die für Omnikanal verwendet werden kann erkannt wurde, Sie darüber informieren, dass eine Zahlungsmethode verfügbar ist.
17. Wählen Sie **Verfügbare Zahlungsmethode**, um die Buchung ausführen, indem die Kartendetails verwenden, die in das Bezugsschaufenster eingegeben wurden.

    Die Auftragspositionen werden auf der Transaktionsseite geladen und der fällige Saldo ist 0 (null).

18. Wählen Sie die Registerkarte **Zahlungen** aus, um die Positionsbeträge anzuzeigen, die aus der Onlinebestellung gezogen wurden. 
19. Wählen Sie eine beliebige Zahlungsmethode aus, um die Transaktion abzuschließen. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Im Callcenter kaufen und Im Shop B abholen

1. Starten Sie den POS für den Houston-Shop.
2. Auf der Seite **Transakltion** fügen Sie Karen Berg der Transaktion hinzu, indem Sie die Nummerauflage verwenden, um **2001** einzugeben.
3. Fügen Sie eine oder mehrere Zeilen der Transaktion hinzu.
4. Wählen Sie **Aufträge**, um die Auftragsoptionen anzuzeigen.
5. Wählen Sie **Alle abholen** und dann aus, wenn Sie dazu aufgefordert werden, wählen Sie **Debitorenauftrag** aus.
6. In der Suchenleiste geben Sie **Seattle** ein und wählen anschließend den Shop**Seattle** für die Abholung aus. 
7. Wählen Sie **OK**, um das aktuelle Datum als Datum der Abholung zu akzeptieren.
9. Wählen Sie **Mit Karte bezahlen** aus, um die Zahlung auszulösen.
10. Zahlungsmittel Kartenzahlung für den Betrag, der für die Anzahlung fällig ist. 
11. Beenden Sie die Einzahlung am Zahlungsterminal. 
12. Nachdem die Summe bezahlt ist, wählen Sie die Option, die selbe Karte für Erfüllung nutzen und warten Sie, bis der Auftrag abgeschlossen ist. 
13. Starten Sie den POS für den Seattle-Shop.
14. Im POS auf der Willkommensseite wählen Sie den Vorgang **Aufträge zur Abholung** aus, um die Aufträge zur Abholung im Shop anzuzeigen. 
15. Wählen Sie eine oder mehrere Zeilen aus dem Auftrag auf, der im Bezugsschaufenster erstellt wurde, und wählen Sie dann **Abholen**.

    Der Auftrag wird im Back Office abgerufen. 

16. Wenn die Auftragspositionsdetails im Back Office abgerufen werden und eine Kartenzahlung, die für Omnikanal verwendet werden kann erkannt wurde, Sie darüber informieren, dass eine Zahlungsmethode verfügbar ist.
17. Wählen Sie **Verfügbare Zahlungsmethode**, um die Buchung ausführen, indem die Kartendetails verwenden, die in das Bezugsschaufenster eingegeben wurden.

    Die Auftragspositionen werden auf der Transaktionsseite geladen und der fällige Saldo ist 0 (null).

18. Wählen Sie die Registerkarte **Zahlungen** aus, um die Positionsbeträge anzuzeigen, die aus der Onlinebestellung gezogen wurden. 
19. Wählen Sie eine beliebige Zahlungsmethode aus, um die Transaktion abzuschließen. 

### <a name="buy-in-store-a-ship-to-customer"></a>Im Shop A kaufen und an den Debitor versenden

1. Starten Sie den POS für den Houston-Shop.
2. Auf der Seite **Transakltion** fügen Sie Karen Berg der Transaktion hinzu, indem Sie die Nummerauflage verwenden, um **2001** einzugeben.
3. Fügen Sie eine oder mehrere Zeilen der Transaktion hinzu.
4. Wählen Sie **Aufträge**, um die Auftragsoptionen anzuzeigen.
5. Wählen Sie **Alle abholen** und dann aus, wenn Sie dazu aufgefordert werden, wählen Sie **Debitorenauftrag** aus.
6. In der Suchenleiste geben Sie **Seattle** ein und wählen anschließend den Shop**Seattle** für die Abholung aus. 
7. Wählen Sie **OK**, um das aktuelle Datum als Datum der Abholung zu akzeptieren.
8. Wählen Sie **Mit Karte bezahlen** aus, um die Zahlung auszulösen.
9. Zahlungsmittel Kartenzahlung für den Betrag, der für die Anzahlung fällig ist. 
10. Beenden Sie die Einzahlung am Zahlungsterminal. 
11. Nachdem die Summe bezahlt ist, wählen Sie die Option, die selbe Karte für Erfüllung nutzen und warten Sie, bis der Auftrag abgeschlossen ist.

Wenn der Auftrag im Back Office entnommen, verpackt und fakturiert wurde, werden die Zahlungsdetails, die am POS bereitgestellt werden verwendet, um die Ressourcen für die Waren zu erfassen, die an den Debitor gesendet werden. 

## <a name="scenario-details"></a>Szenariodetails

Neben den grundlegenden Szenarien, die derzeit beschrieben wurden, wurden einige Erweiterungen für die SDK Zahlungen vorgenommen, um die Omnikanal-Zahlungen zu unterstützen. 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>Einzelne Karte durch Lesegerät ziehen / Karte hineinstecken für Kundenufträge

Bevor die Omnikanal-Zahlungsfunktion implementiert wurde, mussten Debitorenbestellung, die Einzahlungen umfassten, am POS erstellt werden, Debitoren mussten ihre Karte zweimal durch das Lesegerät ziehen (oder hineinstecken), um die Anzahlung zu leisten und einmal,  um die Karte zur nachträglichen Auftragserfüllung zu zerlegen. Wenn die Omnikanal-Tokenisierungsfunktion aktiviert ist, müssen Debitoren ihre Karte nur einmal durch das Lesegerät ziehen, um die Anzahlung zu bezahlen und den Betrag zu autorisieren, der für Waren fällig ist, die später erfüllt werden. Zum Zeitpunkt der Erfüllung wird die autorisierte Deckung aufgezeichnet. Bevor die Omnikanal-Tokenisierungsfunktion implementiert wurde, konnte nur ein wiederkehrendes Kartentoken für nachfolgende Auftragserfüllung erstellt wurde. Daher wurden die Mittel für die ausstehende Erfüllung nicht autorisiert und weil diese Mittel nicht für diese bestimmte Bestellung vorgesehen war, war es weniger wahrscheinlich, dass sie später aufgezeichnet werden konnten.

> [!NOTE]
> Karte nur einmal durch das Lesegerät ziehen ist in Retail Version 8.1.3 nicht unterstützt. Debitorenaufträge in Version 8.1.3 verwenden den gleichen Ablauf, der verwendet wurde, bevor die Omnikanal-Tokenisierungsfunktion implementiert wurde. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Karten, die keine wiederkehrenden Kartentoken ausgeben können

Einige Karten können nicht für Omnikanal-Zahlungen verwendet werden, da sie keine wiederkehrende Kartentoken unterstützen. Wenn ein Auftrag am POS erstellt wird, wenn die Anzahlung vorgenommen wird, indem eine Karte verwendet wird, die keine wiederkehrende Kartentoken unterstützt, wird der vorherige Kartentokenisierungsfluss verwendet. Daher muss ein Debitor, der eine Zahlung bereitstellen möchte,, die für die nachfolgende Auftragserfüllung verwendet wird, eine zweite Karte vorweisen. Wenn die zweite Karte keine wiederkehrenden Kartentoken unterstützt, wird die Tokenisierungsaktivität abgelehnt, und der Kassierer wird aufgefordert, den Debitor zu bitten, eine andere Karte bereitzustellen. 

### <a name="using-a-different-card"></a>Eine andere Karte verwenden

Ein Debitor, der in den Shop kommt, um den Auftrag abzuohlen, hat die Option, eine andere zu verwenden. Wenn der Kassierer zum Zeitpunkt der Abolung der Bestellung die Aufforderung erhält **Verfügbare Zahlungsmethode verwenden** kann er oder sie den Kunden fragen, ob er die selbe Karte verwenden möchte. Wenn der Debitor die Karte verloren hat, die verwendet wurde, um einen Auftrag zu erstellen und für den Auftrag bezahlt möchte, indem er eine andere Karte verwendet, kann der Kassierer **Eine andere Zahlungsmethode verwenden** auswählen. Wenn der Kunde später zurückkehrt, um mehr Artikel für denselben Auftrag abzuholen, kann der Kassier, wenn die ursprüngliche Kartenautorisierung noch gültig ist, erneut fragen, ob der Debitor diese Karte verwenden möchte.

### <a name="invalid-authorizations"></a>Ungültige Autorisierungen

Wenn die Karte, die verwendet wurde, um einen Auftrag zu erstellen, nicht mehr gültig ist, wenn Produkte für die Abholung ausgewählt werden, wird die Zahlungs-Anforderung fehlschlagen. Der POS-Zahlungskonnektor versucht dann, eine neue Autorisierung aufzuzeichnen und zu erstellen, indem er die gleichen Kartendetails verwendet. Wenn die neue Autorisierung oder Erfassung fehlschlägt, wird der Kassierer informiert, dass die Zahlung nicht verarbeitet werden kann. Der Kassierer muss dann eine neue Zahlung vom Debitor erhalten. 

### <a name="multiple-available-payments"></a>Mehrere verfügbare Zahlungen

Wenn ein Auftrag, der mehrere Zahlungsmittel und mehrere Positionen beinhaltet, verarbeitet wird, wird der Kassierer aufgefordert zuerst die **Verfügbare Zahlungsmethode zu verwenden**. Sind mehrere Karten vorhanden, wenn der Kassierer **Verfügbare Zahlungsmethode verwenden** auswählt, werden bestehende Karten (Zahlungsmittel) erfasst, bis der Saldo für die Waren, die abgeholt werden, ausgeglichen ist. Der Kassierer hat nicht die Option, die Karte auszuwählen, die für die Waren verwendet werden soll, die abgeholt werden. 

## <a name="related-topics"></a>Verwandte Themen

- [FAQs zu Zahlungen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Connector für Adyen-Zahlungen für Dynamics 365](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
