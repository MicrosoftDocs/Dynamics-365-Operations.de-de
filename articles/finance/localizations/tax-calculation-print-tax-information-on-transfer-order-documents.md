---
title: Steuerinformationen auf Überweisungsauftragsdokumenten drucken
description: In diesem Artikel wird erläutert, wie die vom Steuerberechnungsservice ermittelten Steuerinformationen auf Transportauftragsbelegen gedruckt werden können.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ca7a610162c539a0ecd74cf9e663f08ea80a7e44
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855201"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Steuerinformationen auf Überweisungsauftragsdokumenten drucken

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Steuerinformationen auf Transportauftragsdokumenten gedruckt werden. Sie können den Proforma-Rechnungsbeleg eines Transportauftrags für Umlagerungen drucken, die nach den Mehrwertsteuervorschriften der Europäischen Union (EU) als innergemeinschaftliche Lieferungen und innergemeinschaftliche Erwerbe gelten. 

Die Transportauftragsbelege werden um folgende steuerrelevante Daten ergänzt:

- Die Namen sowie die Absender- und Lieferadresse für die Umlagerung
- Die Steueridentifikationsnummern des Lieferanten und des Empfängers
- Der Einheitspreis und der steuerpflichtige Betrag der gelieferten Waren
- Steuercode, Steuersatz, Steuerbetrag und Steuerrichtlinien

Um diese Daten zu konfigurieren, müssen Sie die folgenden Hauptschritte ausführen.

1. [Aktivieren und Einrichten der Steuerfunktion für Überweisungsaufträge](tasks/Tax-feature-support-for-transfer-order.md).
2. [Erstellen und Einrichten mehrerer Steuerregistrierungsnummern für eine juristische Person](emea-multiple-vat-registration-numbers.md).
3. Richten Sie den Befreiungscode, die Beschreibung, die Steuerrichtlinien und den Druckcode in Steuercodes ein. In diesem Beispiel werden drei Steuercodes in Microsoft Dynamics 365 Finance erstellt und synchronisiert: **NL-befreit**, **BE-RC-21** und **BE-RC+21**.

    1. Gehen Sie in Finance auf **Steuern** \> **Einrichtung** \> **Mehrwertsteuer** \> **Mehrwertsteuer-Befreiungscodes**.
    2. Wählen Sie **Bearbeiten**, und geben Sie eine Beschreibung für den **EC**-Befreiungsungscode ein. Geben Sie beispielsweise ein: **Steuerfreie EG-Sendungen mit Steueridentifikationsnummer**.
    3. Wechseln Sie zu **Steuern** \> **Direkte Steuern** \> **Umsatzsteuer** \> **Umsatzsteuercodes**.
    4. Wählen Sie den Steuercode **BE-RC-21** aus, und wählen Sie dann **Steuerrichtlinien**.
    5. Wählen Sie **Neu** aus.
    6. Wählen Sie im Feld **Sprache** **EN-US** aus. Geben Sie dann im Feld **Text** Folgendes ein: **Dokument über die Verbringung von Gegenständen im Sinne von Artikel 138. 2. c) der EU-Mehrwertsteuerrichtlinie 2006/112/EG**.
    7. Schließen Sie die Seite.
    8. Wählen Sie im Inforegister **Allgemein** im Feld **Drucken** die Option **Umsatzsteuersatz** aus.
    8. Wählen Sie den Steuercode **NL-Befreit** und dann im Inforegister **Allgemein** im Feld **Drucken** die Option **Umsatzsteuersatz**.

    > [!NOTE] 
    > Steuerkennzeichen, Steuersatz und Steuerbefreiungsbeschreibung werden nicht auf Transportauftragsdokumenten gedruckt, wenn keine Steuerbefreiungskennzeichenbeschreibung oder Steueranweisungen für das Steuerkennzeichen gepflegt sind.

## <a name="print-the-transfer-order---shipment-document"></a>Drucken Sie den Transportauftrag – Versanddokument

Führen Sie nach dem Versand einer Überweisung die folgenden Schritte aus, um den Überweisungsauftrag – Versanddokument – zu drucken.

1. Gehen Sie zu **Bestandsverwaltung** \> **Anfragen und Berichte** \> **Überweisungsaufträge** \> **Lieferung**.
2. Aktivieren Sie auf der Registerkarte **Parameter** in der Gruppe **Drucken** die Option **Steuerinformation**.
3. Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**, wählen Sie die Nummer des Überweisungsauftrags und dann **OK**.
4. Wählen Sie **OK** um den Transportauftrag – Versanddokument – zu drucken.

## <a name="print-the-transfer-order---receipt-document"></a>Drucken Sie den Transportauftrag – Empfangsdokument

Führen Sie nach dem Erhalt einer Überweisung die folgenden Schritte aus, um den Überweisungsauftrag – Empfangsdokument – zu drucken.

1. Gehen Sie zu **Bestandsverwaltung** \> **Anfragen und Berichte** \> **Überweisungsaufträge** \> **Empfangen**.
2. Aktivieren Sie auf der Registerkarte **Parameter** in der Gruppe **Drucken** die Option **Steuerinformation**.
3. Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**, wählen Sie die Nummer des Überweisungsauftrags und dann **OK**.
4. Wählen Sie **OK** um den Transportauftrag – Empfangsdokument – zu drucken.

## <a name="print-the-transfer-overview-document"></a>Drucken Sie das Überweisungsübersichtsdokument

Führen Sie diese Schritte aus, um das Überweisungsübersichtsdokument zu drucken.

> [!NOTE]
> Steuerinformationen sind nur verfügbar, wenn der Überweisungsauftrag versandt oder empfangen wurde.

1. Gehen Sie zu **Bestandsverwaltung** \> **Anfragen und Berichte** \> **Überweisungsaufträge** \> **Transferübersicht**.
2. Aktivieren Sie auf der Registerkarte **Parameter** in der Gruppe **Drucken** die Option **Steuerinformation**.
3. Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**, wählen Sie die Nummer des Überweisungsauftrags und dann **OK**.
4. Wählen Sie **OK** um den Transportübersichtsdokument zu drucken.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
