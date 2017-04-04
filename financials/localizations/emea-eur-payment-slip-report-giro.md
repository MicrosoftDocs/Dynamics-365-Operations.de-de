---
title: "Zahlungsbelegbericht für Europa"
description: "Dieses Thema enthält Informationen zu Zahlungsbelegberichte für Europa bereit."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264604
ms.assetid: 551e047b-4581-4a77-b470-c4f8d395c375
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c795466753ca1515790b7961b989aac6e7d63c2c
ms.lasthandoff: 03/31/2017


---

# <a name="payment-slip-report-for-europe"></a>Zahlungsbelegbericht für Europa

Dieses Thema enthält Informationen zu Zahlungsbelegberichte für Europa bereit.

Die Funktionen für Zahlungsbelegberichte sind für die juristische Personen verfügbar, deren primäre Adresse sich in Dänemark, in Belgien, Norwegen, in der Schweiz in Finnland oder haben. Unternehmen fügen häufig gedruckte Zahlungsbelege zu den Rechnungen, um einen Zahlungsnachweis für Buchungen und den Ausgleich von Konten zur Verfügung zu stellen. Der Zahlungsbeleg kann neben Verkaufsrechnungen und Freitextrechnungen auch für Projekt- oder Servicerechnungen, Mahnschreiben, Zinsrechnungen und Kontoauszüge verwendet werden.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Einrichten einer Kreditorenkennung nur (Dänemark)
Gehen Sie folgendermaßen vor, um Gläubigerkennung (ID)- Nummer des Unternehmens eingeben. Ihrem Finanzinstitut stellt diese Nummer angeben. Sie hat als Referenz verwendet, wenn Debitorenzahlungen über Finanzinstitutionen empfangen werden.

1.  ** Auf Organisationsverwaltung ** ** &gt; Einstellungen ** ** &gt; Organisation ** ** &gt; ** juristische Personen.
2.  ** Bankkontoinformationen ** Wählen Sie im Inforegister im FI-Gläubiger ** Kennung ** Feld, geben Sie die eindeutige achtstellige Kreditorenkennung ein.
3.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Richten Sie ein Zahlungsbelegformat für Rechnungen, Zinsrechnungen, Mahnschreiben und Kontoauszügen
Gehen Sie folgendermaßen vor, um ein Format für Zahlungsbelegsanhänge einzurichten, der Verkaufsrechnungen, Freitextrechnungen, Zinsrechnungen, Mahnschreiben und Kontoauszügen zuordnen.

1.  ** Auf Debitor ** &gt; ** Einstellungen ** &gt; ** Formulare ** &gt; ** Formulareinstellung **.
2.  ** ** Rechnung auf der Registerkarte im Feld Zahlungsanhang ** Spesen- auf Debitorenrechnung ** Feld, wählen Sie das Zahlungsbelegformat aus.
3.  Auf ** Freitextrechnung **, ** Zinsrechnung ** ** **, Mahnschreiben und Kontoauszügen ** ** Registerkarten, wählen Sie für jeden Dokumenttyp ein Zahlungsbelegformat aus.
4.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.

Gehen Sie folgendermaßen vor, um ein Format für Zahlungsbelegsanhänge einzurichten, der Projektrechnungen zuordnen.

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Einstellungen ** &gt; ** Formulare ** &gt; ** Formulareinstellung **.
2.  ** Wählen Sie im Zahlungsanhang Spesen- ** Feld das Zahlungsbelegformat aus.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Weisen Sie ein Zahlungsbelegformat zu einem Debitorenkonto
Nach dem Einrichten des Zahlungsbelegformats für Verkaufsrechnungen, Freitextrechnungen, Zinsrechnungen, Mahnschreiben, Projektrechnungen und Kontoauszüge einrichten, können Sie für einen ausgewählten Debitor bestimmte Formate zugewiesen werden.

1.  ** Auf Debitor ** &gt; ** Common ** &gt; ** Debitoren ** &gt; ** ** alle Debitoren.
2.  Neuen Debitor erstellen, oder zum Auswählen eines vorhandenen Debitors.
3.  ** Rechnung und auf dem Inforegister in Lieferung ** ** auf einer Debitorenrechnung **, ** auf einer Freitextrechnung **, ** für eine Zinsrechnung **, ** auf einem Mahnschreiben **, ** auf einer Projektrechnung ** **, und auf einem Kontoauszug ** den Feldern, indem Sie das Format für Zahlungsbelegsanhänge aus, aus, wie Dokumente jeden Typs begleiten, die an den ausgewählten Debitor gesendet werden.
4.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.



