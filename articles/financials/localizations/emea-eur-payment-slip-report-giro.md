---
title: "Zahlungsbelegbericht für Europa"
description: "Dieses Thema enthält Informationen zu Zahlungsbelegberichten für Europa."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 07d09512ef612b41bf527b74496fa440f23851fc
ms.openlocfilehash: 2afdc11b428ffe5d2ca0f65d040507e89e0b8c02
ms.contentlocale: de-de
ms.lasthandoff: 02/14/2018

---

# <a name="payment-slip-report-for-europe"></a>Zahlungsbelegbericht für Europa

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu Zahlungsbelegberichten für Europa.

Die Funktionen für Zahlungsbelegberichte sind für die juristische Personen verfügbar, deren primäre Adresse sich in Dänemark, in Belgien, Norwegen, in der Schweiz oder in Finnland befindet. Unternehmen fügen oft Rechnungen in der Regel gedruckte Zahlungsbelege bei, um Debitoren zu unterstützen und einen Zahlungsnachweis für Buchungen und den Ausgleich von Konten zur Verfügung zu haben. Der Zahlungsbeleg kann neben Verkaufsrechnungen und Freitextrechnungen auch für Projekt- oder Servicerechnungen, Mahnschreiben, Zinsrechnungen und Kontoauszüge verwendet werden.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Einrichten einer Kreditorenkennung (Nur Dänemark)
Gehen Sie folgendermaßen vor, um Gläubigerkennung (ID)- Nummer des Unternehmens eingeben. Ihr Finanzinstitut stellt diese Nummer bereit. Diese Nummer wird als Referenz verwendet, wenn Debitorenzahlungen über Finanzinstitutionen empfangen werden.

1.  Klicken Sie auf **Organisationsverwaltung** &gt; **Einrichten**&gt; **Organisationen** &gt; **Juristische Personen**.
2.  Im Inforegister **Bankkontoinformationen** Wählen Sie das Feld **FI-Gläubiger-Kennung** und geben Sie die eindeutige achtstellige Kreditorenkennung ein.
3.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Einrichten eines Zahlungsbelegformats für Rechnungen, Zinsrechnungen, Inkassoschreiben und Kontoauszüge
Folgen Sie diesen Schritten und richten Sie ein Format für einen Zahlungsbeleg ein, der Verkaufsrechnungen, Freitextrechnungen, Zinsrechnungen, Mahnschreiben und Kontoauszügen beigelegt werden soll.

1.  Klicken Sie auf **Debitoren** &gt; **Einstellungen** &gt; **Formulare** &gt; **Formularnotizen**.
2.  In der Registerkarte **Rechnung** wählen Sie das Feld **Zugeordnetr Zahlungsanhang für  Debitorenrechnung** und wählen Sie das Zahlungsbelegformat aus.
3.  In den Registerkarten **Freitextrechnung,**, **Zinsrechnung**, **Mahnschreiben** und **Bankauszug** wählen Sie ein Format für einen Zahlungsbeleg, der für den Dokumenttyp verwendet werden soll.
4.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.

Folgen Sie diesen Schritten und richten Sie ein Format für einen Zahlungsbeleg ein, der Projektrechnungen beigelegt werden soll.

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung**&gt; **Einrichten** &gt; **Formular** &gt; **Formulareinstellungen**.
2.  Klicken Sie auf die Registerkarte **Zugeordnete Zahlungsbeilagen** und wählen Sie im Feld das Format für den Zahlungsbeleg aus.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Zuweisen einer Zahlungsbelegsbeilage zu einem Debitorenkonto
Nach dem Einrichten des Zahlungsbelegformats für Verkaufsrechnungen, Freitextrechnungen, Zinsrechnungen, Mahnschreiben, Projektrechnungen, Kontoauszüge und Projektrechnungen können einem ausgewählten Debitor bestimmte Formate zugewiesen werden.

1.  Klicken Sie auf **Debitoren** &gt; **Allgemein** &gt; **Kunden** &gt; **Alle Kunden**.
2.  Dient zum Erstellen eines neuen Debitors oder zum Auswählen eines vorhandenen Debitors.
3.  Im Inforegister in den Feldern **Rechnung und Lieferung** unter **Auf einer Debitorenrechnung**, **Auf einer Freitextrechnung**, **Für eine Zinsrechnung**, **Auf einem Mahnschreiben**, **Auf einer Projektrechnung** und **Auf einem Kontoauszug** wählen Sie das Format für Zahlungsbelegsanhänge aus, die Dokumente jeden Typs begleiten, die an den ausgewählten Debitor gesendet werden.
4.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.





