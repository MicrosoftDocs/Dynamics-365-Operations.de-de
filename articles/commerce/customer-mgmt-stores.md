---
title: Debitorenverwaltung in Geschäften
description: In diesem Thema wird erläutert, wie Einzelhändler Debitorenverwaltungsfunktionen an der Verkaufsstelle (POS) in Microsoft Dynamics 365 Commerce aktivieren können.
author: josaw1
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea2953510d134be0d33a6afa65027a6c9d2816f7dc16ca669859e80ee40f4278
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754415"
---
# <a name="customer-management-in-stores"></a>Debitorenverwaltung in Geschäften

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Einzelhändler Debitorenverwaltungsfunktionen an der Verkaufsstelle (POS) in Microsoft Dynamics 365 Commerce aktivieren können.

Es ist wichtig, dass Filialmitarbeiter am POS Debitorendatensätze erstellen und bearbeiten können. Auf diese Weise können sie Aktualisierungen von Debitoreninformationen wie E-Mail-Adresse, Telefonnummer und Adresse erfassen. Diese Informationen sind in nachgelagerten Systemen wie dem Marketing hilfreich, da die Wirksamkeit dieser Systeme von der Genauigkeit ihrer Debitorendaten abhängt.

Vertriebsmitarbeiter können den Workflow zur Debitorenerstellung von zwei POS-Einstiegspunkten aus auslösen. Sie können eine Schaltfläche auswählen, die dem Vorgang **Debitor hinzufügen** zugeordnet ist, oder sie können **Debitor erstellen** in der App-Leiste auf der Suchergebnisseite auswählen. In beiden Fällen wird das Dialogfeld **Neuer Debitor** angezeigt, in dem Vertriebsmitarbeiter die erforderlichen Debitorendaten eingeben können, z. B. den Namen des Kunden, die E-Mail-Adresse, die Telefonnummer, die Adresse und alle zusätzlichen Informationen, die für das Unternehmen relevant sind. Diese zusätzlichen Informationen können mithilfe der Debitorenattribute erfasst werden, die dem Kunden zugeordnet sind. Weitere Informationen zu Kundenattributen finden Sie unter [Debitorattribute](dev-itpro/customer-attributes.md).

Vertriebsmitarbeiter können auch sekundäre E-Mail-Adressen und Telefonnummern erfassen. Darüber hinaus können sie die Präferenz des Kunden für den Empfang von Marketinginformationen über eine dieser sekundären E-Mail-Adressen oder Telefonnummern erfassen. Um diese Funktion zu aktivieren, müssen Einzelhändler die Funktion **Mehrere E-Mails und Telefonnummern sowie die Zustimmung zur Vermarktung für diese Kontakte erfassen** im Arbeitsbereich **Funktionsverwaltung** in der Commerce-Zentrale (**Systemadministration \> Arbeitsbereiche \> Funktionsverwaltung**) aktivieren.

## <a name="default-customer-properties"></a>Standard-Debitoreneigenschaften

Einzelhändler können die Seite **Alle Shops** in der Commerce-Zentrale (**Retail und Commerce \> Kanäle \> Shops**) verwenden , um jedem Geschäft einen Standarddebitor zuzuordnen. Commerce kopiert dann die für den Standarddebitor definierten Eigenschaften in alle neu erstellten Debitorendatensätze. Das Dialogfeld **Debitor erstellen** zeigt z. B. Eigenschaften an, die vom Standarddebitoren geerbt wurden, der dem Geschäft zugeordnet ist. Diese Eigenschaften umfassen den **Debitortyp**, die **Debitorengruppe**, die **Belegproption**, die **Empfänger-E-Mail**, die **Währung** und die **Sprache**. Alle **Zugehörigkeiten** (Gruppierungen von Debitoren) werden ebenfalls vom Standarddebitor geerbt. Aber **Finanzdimensionen** werden jedoch von der Debitorengruppe geerbt, die dem Standarddebitor zugeordnet ist, nicht vom Standarddebitor selbst.

> [!NOTE]
> Der Wert **Empfangs-E-Mail** wird nur dann vom Standardkunden kopiert, wenn die Empfangs-E-Mail-ID für die neu erstellten Kunden nicht angegeben ist. Dies bedeutet, dass, wenn die Empfangs-E-Mail-ID beim Standardkunden vorhanden ist, alle auf der E-Commerce-Website erstellten Kunden dieselbe Empfangs-E-Mail-ID erhalten, da keine Benutzeroberfläche zum Erfassen der Empfangs-E-Mail-ID vom Kunden vorhanden ist. Wir empfehlen Ihnen, das Feld **Empfangs-E-Mail** für den Standardkunden des Geschäfts leer zu behalten und es nur zu verwenden, wenn Sie einen Geschäftsprozess haben, der von der Anwesenheit einer Empfangs-E-Mail-Adresse abhängt. 

Vertriebsmitarbeiter können mehrere Adressen für einen Kunden erfassen. Der Name und die Telefonnummer des Kunden werden von den Kontaktinformationen geerbt, die jeder Adresse zugeordnet sind. Das Inforegister **Adressen** eines Debitordatensatzes enthält ein **Zweck**-Feld, das Vertriebsmitarbeiter bearbeiten können. Wenn der Debitortyp **Person** ist, ist der Standardwert **Zuhause**. Wenn der Debitortyp **Organisation** ist, ist der Standardwert **Unternehmen**. Andere Werte, die dieses Feld unterstützt, sind **Zuhause**, **Büro** und **Postfach**. Der Wert des **Land**-Felds für eine Adresse wird von der primären Adresse geerbt, die auf der Seite **Organisationseinheit** in der Commerce-Zentrale unter **Organisationsverwaltung \> Organisationen \> Organisationseinheiten** angegeben ist.

## <a name="sync-customers-and-async-customers"></a>Synchrone und asynchrone Debitoren

In Commerce gibt es zwei Arten der Debitorerstellung: synchron (oder sync) und asynchron (oder async). Standardmäßig werden Debitoren synchron erstellt. Mit anderen Worten, sie werden in Echtzeit in der Commerce-Zentrale erstellt. Der synchrone Modus für die Debitorerstellung ist von Vorteil, da neue Debitoren sofort kanalübergreifend durchsucht werden können. Es hat jedoch auch einen Nachteil. Weil es [Commerce Data Exchange: Echtzeitservice](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)-Aufrufe an die Commerce-Zentrale erzeugt, kann die Leistung beeinträchtigt werden, wenn viele Aufrufe zur Debitorerstellung gleichzeitig getätigt werden.

Wenn die Option **Debitor im asynchronen Modus erstellen** auf **Ja** gesetzt ist im Funktionsprofil des Geschäfts (**Retail und Commerce \> Kanaleinrichtung \> Einrichtung Onlineshop \> Funktionsprofile**), werden Echtzeit-Serviceaufrufe nicht zum Erstellen von Debitordatensätzen in der Debitordatenbank verwendet. Der asynchrone Debitorerstellungsmodus wirkt sich nicht auf die Leistung der Commerce-Zentrale aus. Jedem neuen Async-Debitordatensatz wird eine temporäre GUID (Globally Unique Identifier) zugewiesen und als Debitorenkontokennung verwendet. Diese GUID wird POS-Benutzern nicht angezeigt. Stattdessen werden diese Benutzer **Ausstehende Synchronisierung** als Debitorenkontokennung sehen. Obwohl diese Konfiguration die asynchrone Erstellung von Debitoren erzwingt, beachten Sie, dass Änderungen an Debitorendatensätzen immer synchron vorgenommen werden.

### <a name="convert-async-customers-to-sync-customers"></a>Asynchrone Debitoren in synchrone Debitoren konvertieren

Um asynchrone Debitoren in synchrone Debitoren zu konvertieren, müssen Sie zuerst den P-Einzelvorgang ausführen, um die asynchronen Debitoren an die Commerce-Zentrale zu senden. Dann führen Sie den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** zum Erstellen von Debitorenkonto-IDs aus. Führen Sie zum Schluss den Einzelvorgang **1010** zum Synchronisieren der neuen Debitorenkonto-IDs mit den Kanälen aus.

### <a name="async-customer-limitations"></a>Asynchrone Debitorenbeschränkungen

Die asynchrone Debitorenfunktionalität weist derzeit die folgenden Einschränkungen auf:

- Asynchrone Debitorendatensätze können nur bearbeitet werden, wenn der Debitor in der Commerce-Zentrale erstellt und die neue Debitorenkonto-ID wieder mit dem Kanal synchronisiert wurde.
- Mitgliedschaften können nicht mit asynchronen Debitoren verknüpft werden. Daher erben neue asynchrone Debitoren keine Zugehörigkeiten vom Standarddebitor.
- Kundenkarten können nur dann an asynchrone Debitoren ausgegeben werden, wenn die neue Debitorenkonto-ID wieder mit dem Kanal synchronisiert wurde.
- Sekundäre E-Mail-Adressen und Telefonnummern können für asynchrone Debitoren nicht erfasst werden.

### <a name="customer-creation-in-pos-offline-mode"></a>Debitorenerstellung im POS-Offlinemodus

Wenn der POS offline geschaltet wird, während der asynchrone Debitorenerstellungsmodus aktiviert ist, werden neue Debitorendatensätze asynchron erstellt. Wenn der POS offline geschaltet wird, während der asynchrone Debitorenerstellungsmodus deaktiviert ist, wechselt das System automatisch in den asynchronen Debitorenerstellungsmodus. Das bedeutet, dass Debitorendatensätze asynchron erstellt werden können, auch wenn der asynchrone Debitorenerstellungsmodus deaktiviert ist. Daher müssen Administratoren der Commerce-Zentrale einen wiederkehrenden Batchauftrag für den P-Einzelvorgang, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren in der Commerce-Zentrale in synchrone Debitoren konvertiert werden.

> [!NOTE]
> Wenn die Option **Gemeinsam genutzte Debitorendatentabellen filtern** auf **Ja** auf der Seite **Handelskanalschema** (**Retail und Commerce \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbankgruppe**) gesetzt ist, werden Debitorendatensätze nicht im POS-Offlinemodus erstellt. Weitere Informationen finden Sie unter [Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Debitorattribute](dev-itpro/customer-attributes.md)

[Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
