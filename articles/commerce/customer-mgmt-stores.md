---
title: Debitorenverwaltung in Geschäften
description: In diesem Thema wird erläutert, wie Einzelhändler Debitorenverwaltungsfunktionen an der Verkaufsstelle (POS) in Microsoft Dynamics 365 Commerce aktivieren können.
author: gvrmohanreddy
ms.date: 12/10/2021
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
ms.openlocfilehash: 29e45419f712e25092b473e34144ac1146e4ed9b
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913625"
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
> Der Wert **Empfangs-E-Mail** wird nur dann vom Standardkunden kopiert, wenn die Empfangs-E-Mail-ID für die neu erstellten Kunden nicht angegeben ist. Dies bedeutet, dass, wenn die Empfangs-E-Mail-ID beim Standardkunden vorhanden ist, alle auf der E-Commerce-Website erstellten Kunden dieselbe Empfangs-E-Mail-ID erhalten, da keine Benutzeroberfläche zum Erfassen der Empfangs-E-Mail-ID vom Kunden vorhanden ist. Wir empfehlen Ihnen, das Feld **Empfangs-E-Mail** für den Standardkunden des Geschäfts leer zu lassen und es nur zu verwenden, wenn Sie einen Geschäftsprozess haben, der von der Anwesenheit einer Empfangs-E-Mail-Adresse abhängt. 

Vertriebsmitarbeiter können mehrere Adressen für einen Kunden erfassen. Der Name und die Telefonnummer des Kunden werden von den Kontaktinformationen geerbt, die jeder Adresse zugeordnet sind. Das Inforegister **Adressen** eines Debitordatensatzes enthält ein **Zweck**-Feld, das Vertriebsmitarbeiter bearbeiten können. Wenn der Debitortyp **Person** ist, ist der Standardwert **Zuhause**. Wenn der Debitortyp **Organisation** ist, ist der Standardwert **Unternehmen**. Andere Werte, die dieses Feld unterstützt, sind **Zuhause**, **Büro** und **Postfach**. Der Wert des **Land**-Felds für eine Adresse wird von der primären Adresse geerbt, die auf der Seite **Organisationseinheit** in der Commerce-Zentrale unter **Organisationsverwaltung \> Organisationen \> Organisationseinheiten** angegeben ist.



## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Asynchroner Debitorerstellungsmodus](async-customer-mode.md)

[Asynchrone Debitoren in synchrone Debitoren konvertieren](convert-async-to-sync.md)

[Debitorattribute](dev-itpro/customer-attributes.md)

[Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
