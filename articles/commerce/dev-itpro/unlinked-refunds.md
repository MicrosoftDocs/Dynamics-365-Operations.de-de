---
title: Nicht verknüpfte Rückerstattungen mit dem Dynamics 365 Commerce Payment Connector für Adyen verarbeiten
description: In diesem Artikel wird beschrieben, wie nicht verknüpfte Rückerstattungen funktionieren, wenn Microsoft Dynamics 365 Payment Connector für Adyen verwendet wird.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 2b2bee7ad45bbff82c8b7de2741925fde29d8583
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284310"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Nicht verknüpfte Rückerstattungen mit dem Dynamics 365 Commerce Payment Connector für Adyen verarbeiten

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie nicht verknüpfte Rückerstattungen funktionieren, wenn [Microsoft Dynamics 365 Payment Connector für Adyen](adyen-connector.md) verwendet wird. Es bespricht auch die Möglichkeit, eine Rückerstattung für eine neue Zahlungsmethode am Point of Sale (POS) oder Callcenter zu verarbeiten.

Der Dynamics 365 Payment Connector für Adyen unterstützt die Möglichkeit, Rückerstattungen mit einer anderen Zahlungsmethode als der zu verarbeiten, die für die ursprüngliche Transaktion verwendet wurde. Obwohl wir empfehlen, dass Sie [verknüpfte Rückerstattungen](linked-refunds.md) verwenden, um eine Rückerstattung für die ursprünglich angegebene Zahlungsmethode zu verarbeiten, sind in einigen Szenarien Rückerstattungen auf eine andere Methode erforderlich. Beispielsweise kann die Karte, die für die ursprüngliche Zahlung verwendet wurde, jetzt abgelaufen oder verloren gegangen oder vom Benutzer storniert worden sein.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen müssen erfüllt sein, bevor der Dynamics 365 Payment Connector für Adyen nicht verknüpfte Rückerstattungen verarbeiten kann:

- Richten Sie [Zahlungsmethoden](../payment-methods.md) ein.
- Richten Sie [Omni-Channel-Zahlungen](../omni-channel-payments.md) ein.

## <a name="additional-configuration"></a>Zusätzliche Konfiguration

Der Dynamics 365 Payment Connector für Adyen stellt eine vordefinierte Implementierung für jedes unterstützte Rückerstattungsszenario zur Verfügung, das in diesem Abschnitt beschrieben wird. Kunden, die nicht die vorkonfigurierte Implementierung des Dynamics 365 Payment Connector für Adyen verwenden, müssen den Connector einrichten, der die Tokenisierung von Kreditkarten unterstützt.

## <a name="supported-refund-scenarios"></a>Unterstützte Rückerstattungsszenarien

Dynamics 365 Commerce unterstützt Rückerstattungen von zuvor genehmigten und bestätigten Transaktionen. Rückerstattungen können entweder aus einer vollständigen Rückerstattung oder einer teilweisen Rückerstattung der Transaktion bestehen. Rückerstattungen dürfen den vollen Betrag der ursprünglichen Zahlungsautorisierung nicht überschreiten. Nicht verknüpfte Rückerstattungen werden nur in POS und Callcenter unterstützt.

## <a name="enable-unlinked-refunds-functionality"></a>Funktion für nicht verknüpfte Rückerstattungen aktivieren

Führen Sie die folgenden Schritte aus, um die Funktion für nicht verknüpfte Rückerstattungen in der Commerce-Zentralverwaltung zu aktivieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter**.
1. Legen Sie auf der Registerkarte **Omni-Channel-Zahlungen** die Option **Omni-Channel-Zahlungen verwenden** auf **Ja** fest.

### <a name="supported-payment-method-variants"></a>Unterstützte abweichende Zahlungsmethoden

Die folgenden Zahlungsmethodenvarianten unterstützen sofort nicht verknüpfte Rückerstattungen:

- Karten
- Brieftasche

Nicht alle Zahlungsmethodenvarianten unterstützen nicht verknüpfte Rückerstattungen. Die folgende Tabelle enthält eine Liste gängiger Zahlungsmethoden und zeigt die Supportfähigkeit jeder Methode für verknüpfte und nicht verknüpfte Rückerstattungen.

| Zahlungsweise        | Verknüpfte Rückerstattung | Nicht verknüpfte Rückerstattung |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Ja           | Ja             |
| amexconsumer          | Ja           | Ja             |
| amexcorporate         | Ja           | Ja             |
| amexdebit             | Ja           | Ja             |
| amexprepaid           | Ja           | Ja             |
| amexprepaidreloadable | Ja           | Ja             |
| amexsmallbusiness     | Ja           | Ja             |
| discover              | Ja           | Ja             |
| maestro               | Ja           | Ja             |
| maestrouk             | Ja           | Ja             |
| mc                    | Ja           | Ja             |
| mcalphabankbonus      | Ja           | Ja             |
| mcprepaidanonymous    | Ja           | Ja             |
| visa                  | Ja           | Ja             |
| visaalphabankbonus    | Ja           | Ja             |
| visacheckout          | Ja           | Ja             |
| visadankort           | Ja           | Ja             |
| visahipotecario       | Ja           | Ja             |
| visasaraivacard       | Ja           | Ja             |
| vpay                  | Ja           | Ja             |
| givex                 | **Nr.**        | Ja             |
| svs                   | **Nr.**        | Ja             |
| cup                   | Ja           | Ja             |
| diners                | Ja           | Ja             |
| interac               | **Nr.**        | Ja             |
| jcb                   | Ja           | Ja             |
| jcb_applepay          | Ja           | Ja             |
| unionpay              | Ja           | Ja             |

### <a name="process-an-unlinked-refund-in-pos"></a>Eine nicht verknüpfte Rückerstattung in POS verarbeiten

Ein Kunde gibt einen Artikel innerhalb der für die Rücksendung zulässigen Frist an einen POS-Kassierer zurück und verfügt über einen gültigen Beleg. Bei der Bearbeitung der Rückgabe enthält das Dialogfeld **Retourenzahlung** eine Option **Zahlungsmethode auswählen**. Der Kassierer kann dann unter den unterstützten Zahlungsmethoden für Rückerstattungen (Karten und Wallet) eine Zahlungsmethode auswählen.

### <a name="process-an-unlinked-refund-in-call-center"></a>Eine nicht verknüpfte Rückerstattung im Callcenter verarbeiten

Wenn eine nicht verknüpfte Rückerstattung für eine Bestellung im Callcenter verarbeitet wird, wählt ein Callcenter-Mitarbeiter eine Zahlungsmethode aus, die sich von der ursprünglichen Zahlungsmethode unterscheidet. Der Mitarbeiter wird dann aufgefordert, eine persönliche Identifikationsnummer (PIN) zum Außerkraftsetzen des Administrators zu erhalten. Die PIN ist erforderlich, bevor die andere Zahlungsmethode für die Rückerstattung verarbeitet werden kann.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Administratoraußerkraftsetzungs-PIN für das Callcenter einrichten

Gehen Sie folgendermaßen vor, um eine Administratoraußerkraftsetzungs-PIN für das Callcenter in der Commerce headquarters einzurichten.

1. Gehen Sie zu **Retail und Commerce \> Kanaleinstellungen \> Callcenter-Einrichtung**, oder suchen Sie nach „Berechtigungen überschreiben“.
1. Wählen Sie die Rolle aus, für die die nicht verknüpften Verarbeitungsberechtigungen für Rückerstattungen zugelassen werden sollen.
1. Setzen Sie im Inforegister **Retouren** die Option **Alternative Zahlung zulassen** auf **Ja**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Payment Connector für Adyen](adyen-connector.md)

[Verknüpfte Rückerstattungen von zuvor genehmigten und bestätigten Transaktionen](linked-refunds.md)
