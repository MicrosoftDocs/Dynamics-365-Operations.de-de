---
title: Integration von Notizen
description: In diesem Thema wird die Integration von Notizdaten in dualem Schreiben erläutert
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186785"
---
# <a name="note-integration"></a>Integration von Notizen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Im Verlauf von Geschäftsprozessen sammeln Benutzer von Microsoft Dynamics 365 häufig Informationen über ihre Kunden. Diese Informationen werden als Aktivitäten und Notizen aufgezeichnet. In diesem Thema wird die Integration von Notizdaten in dualem Schreiben erläutert

Informationen über Kunden können folgendermaßen klassifiziert werden:

+ **Umsetzbare Informationen, die ein Dynamics 365-Benutzer im Auftrag eines Kunden bearbeitet** – Contoso (ein Dynamics 365-Benutzer) führt beispielsweise eine Spielshow durch. Ein Kunde von Contoso (ein Debitor) möchte an der Spielshow teilnehmen. Der Kunde bittet einen Contoso-Mitarbeiter, einen Platz in der Spielshow für ihn zu buchen. Die Buchung erfolgt im Veranstaltungskalender von Contoso.
+ **Umsetzbare Informationen für einen Dynamics 365-Benutzer** – Ein Kunde, der eine Surface-Einheit kauft, gibt beispielsweise spezielle Anweisungen ein, die darauf hinweisen, dass das Gerät vor der Lieferung in Geschenkverpackung verpackt werden sollte. Diese Anweisungen sind umsetzbare Informationen, die von dem Contoso-Mitarbeiter bearbeitet werden sollten, der für die Verpackung verantwortlich ist.
+ **Nicht umsetzbare Informationen** – Ein Kunde besucht beispielsweise das Contoso-Geschäft und zeigt während seines Gesprächs mit einem Shopmitarbeiter Interesse an *Halo*-Games und Gamingzubehör. Der Shopmitarbeiter notiert diese Informationen. Die Produktempfehlungsmodul nutzt sie dann, um dem Kunden Empfehlungen zu geben.

Im Allgemeinen werden umsetzbare Informationen als *Aktivitäten* in Finance and Operations- und Kundenbindungs-Apps erfasst. Nicht umsetzbare Informationen werden in Finance and Operations-Apps als *Notizen* und in Kundenbindungs-Apps als *Anmerkungen* erfasst.

> [!TIP]
> Obwohl Notizen für nicht umsetzbare Informationen gedacht sind, können Sie sie trotzdem zum Speichern und Verarbeiten von umsetzbaren Informationen in den Apps verwenden, wenn Sie es möchten.

Microsoft veröffentlicht derzeit Funktionen für die Integration von Notizen. (Die Funktionalität zur Integration von Aktivitäten wird später veröffentlicht.) Die Notizintegration ist für Debitoren, Kreditoren, Aufträge und Bestellungen verfügbar.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Eine Notiz in einer Kundenbindungs-App erstellen

Befolgen Sie diese Schritte zum Erstellen einer Notiz in einer Kundenbindungs-App und anschließendem Synchronisieren mit einer Finance and Operations-App.

1. Öffnen Sie in der Kundenbindungs-App den Kontodatensatz eines Debitoren.
2. Wählen Sie im Bereich **Zeitskala** das Pluszeichen (**+**) und anschließend **Notiz** aus, um eine Notiz zu erstellen.

    ![Erstellen einer Notiz in der Kundenbindungs-App](media/notes-ce-1.png)

3. Geben Sie einen Titel und eine Beschreibung ein, und wählen Sie anschließend **Notiz hinzufügen** aus.

    ![Eingeben eines Titels und einer Beschreibung](media/notes-ce-2.png)

    Die neue Notiz wird der Debitorenzeitskala hinzugefügt.

    ![Neuer Hinweis auf der Debitorenzeitskala](media/notes-ce-3.png)

4. Melden Sie sich bei der Finance and Operations-App, und öffnen Sie denselben Debitorendatensatz. Beachten Sie, dass die **Anhänge**-Schaltfläche (Büroklammersymbol) in der oberen rechten Ecke anzeigt, dass der Datensatz einen Anhang hat.

    ![Benachrichtigung über einen Anhang](media/notes-ce-4.png)

5. Wählen Sie die **Anhänge**-Schaltfläche zum Öffnen der **Anhänge**-Seite aus. Sie sollten nun die erstellte Notiz in der Kundenbindungs-App finden.

    ![Notiz in der Kundenbindungs-App](media/notes-ce-5.png)

Alle Aktualisierungen der Notiz werden zwischen der Finance and Operations-App und der Kundenbindungs-App hin und her synchronisiert.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Eine Notiz in einer Finance and Operations-App erstellen

Sie können eine Notiz ebenfalls in einer Finance and Operations-App erstellen, die dann mit einer Kundenbindungs-App synchronisiert wird.

Befolgen Sie diese Schritte zum Erstellen einer Notiz in einer Finance and Operations-App und anschließendem Synchronisieren mit einer Kundenbindungs-App.

1. Wählen Sie in der Finance and Operations-App auf der Seite **Anhänge** die Option **Neu** \> **Notiz** aus.

    ![Erstellen einer Notiz in der Finance and Operations-App](media/notes-fo-1.png)

2. Geben Sie einen Titel und eine kurze Anleitung ein. Wählen Sie dann **Speichern** aus.

    ![Eingeben eines Titels und einer Anleitung](media/notes-fo-2.png)

3. Aktualisieren Sie in der Kundenbindungs-App den Datensatz. Sie sollten die neue Notiz auf der Zeitskala finden.

    ![Neue Notiz auf der Zeitskala in der Kundenbindungs-App](media/notes-fo-3.png)

Sie können eine Notiz entweder als intern oder als extern klassifizieren.

- Öffnen Sie die Notiz in der Finance and Operations-App auf der Seite **Anhänge**, und wählen Sie anschließend im Feld **Einschränkung** die Option **Intern** oder **Extern** aus.

    ![Einschränkungsfeld](media/notes-fo-4.png)

Sie können auch eine URL erstellen

1. Wählen Sie in der Finance and Operations-App auf der Seite **Anhänge** die Option **Neu** \> **URL** aus.
2. Geben Sie einen Titel und die URL ein.
3. Wählen Sie im Feld **Einschränkung** die Option **Intern** oder **Extern** aus.

    ![Erstellen einer URL in der Finance and Operations-App](media/notes-fo-5.png)

4. Wählen Sie **Speichern** aus.

    Da Kundenbindungs-Apps keinen URL-Typ enthalten, wird die URL als Notiz über duales Schreiben integriert.

    ![Als Notiz erscheinende URL in der Kundenbindungs-App](media/notes-ce-6.png)

> [!NOTE]
> Dateianhänge werden nicht unterstützt.

## <a name="templates"></a>Vorlagen

Die Notizintegration enthält eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten – wie in der folgenden Tabelle dargestellt.

| Finance and Operations-App | Customer Engagement-App | Beschreibung |
|----------------------------|-------------------------|-------------|
| [Debitorenanhänge](mapping-reference.md#230) | Anmerkungen | Unternehmen, die Klartext und URLs zum Erfassen debitorspezifischer Informationen verwenden (sowohl für Organisationen als auch für Personen). |
| [Kreditorendokumentanhänge](mapping-reference.md#231) | Anmerkungen | Unternehmen, die Klartext und URLs zum Erfassen kreditorspezifischer Informationen verwenden (sowohl für Organisationen als auch für Personen). |
| [Auftragskopfdokument-Anhänge](mapping-reference.md#229) | Anmerkungen | Unternehmen, die Klartext und URLs zum Erfassen auftragsspezifischer Informationen verwenden. |
| [Anhänge des Bestellkopfdokuments](mapping-reference.md#232) | Anmerkungen | Unternehmen, die Klartext und URLs zum Erfassen bestellungsspezifischer Informationen verwenden. |

## <a name="limitations"></a>Einschränkungen

Nachdem Sie die Notes-Lösung installiert haben, können Sie sie nicht mehr deinstallieren. 

Weitere Informationen finden Sie unter [Referenz für die Zuordnung von dualem Schreiben](mapping-reference.md).
