---
title: Verwalten vone Änderungen in Formeln und deren Substanzen
description: In diesem Artikel wird beschrieben, wie Sie die Formelverwaltung durchführen und Änderungen an den Stammdaten der Prozessfertigung verwalten.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8105ebc7f3698a6baaa04b6548dac18a7bf81a47
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904071"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Verwalten vone Änderungen in Formeln und deren Substanzen

[!include [banner](../includes/banner.md)]

Wenn Sie die Prozessherstellungsfunktionen von Microsoft Dynamics 365 Supply Chain Management verwenden, können Sie auch die zugehörigen Funktionen zur Formelverwaltung verwenden, um die folgenden Änderungen zu verwalten:

- **Formel- und Planungselemente:** Verwalten Sie Änderungen an Inhaltsstoffen in Formeln und deren Nebenprodukten und Nebenprodukten.
- **Co-Produkte und Nebenprodukte:** Bearbeiten Sie Mengen und andere Informationen der Co-Produkte und Nebenprodukte in einer Formel.
- **Artikelgewicht:** Verwalten Sie Änderungen an Artikelgewichten.

## <a name="turn-this-feature-on-or-off"></a>Schalten Sie diese Funktion ein oder aus

Für die in diesem Artikel beschriebene Funktionalität müssen die Funktionen *Verwaltung für technische Änderung* und *Änderungen an Formeln und ihren Substanzen verwalten* für Ihr System eingeschaltet sein. Einzelheiten zum Ein- und Ausschalten dieser Funktionen finden Sie unter [Verwaltung für technische Änderung – Übersicht](product-engineering-overview.md).

## <a name="feature-naming-conventions"></a>Namenskonventionen für Funktion

In der Dokumentation und in der Supply Chain Management-Benutzeroberfläche wird die Änderungsverwaltungsfunktionalität normalerweise als *Engineering Change Management* bezeichnet und die handhabbaren Produkte werden typischerweise als *technische Produkte* bezeichnet. Obwohl diese Terminologie normalerweise nicht mit der Verwaltung von Formeln für die Prozessfertigung verbunden ist, sollten Sie sich das Änderungsmanagement als einfaches Änderungsmanagement und das Engineering von Produkten als versionierte Produkte vorstellen.

## <a name="work-with-formula-change-management-features"></a>Arbeiten Sie mit Funktionen zur Verwaltung von Formeländerungen

In der folgenden Liste wird zusammengefasst, wie die Funktionen zur Verwaltung technischer Änderungen für die Formelverwaltung gelten. Es enthält auch Links zu weiteren Informationen. Da das Änderungsmanagement von Formeln die Funktionen des Änderungsmanagements nutzt, sollten Sie lernen, wie das Änderungsmanagement im Allgemeinen funktioniert, damit Sie damit Ihre Formeln und deren Inhaltsstoffe verwalten können.

- **Zentrales Produktdatenmanagement** – Richten Sie eine Organisation ein, die durch einen verwalteten Freigabeprozess sicherstellt, dass Benutzern im gesamten Unternehmen genaue und relevante Produktdaten zur Verfügung stehen. Weitere Informationen finden Sie unter [Engineering-Unternehmen und Dateneigentumsregeln](engineering-org-data-ownership-rules.md).
- **Produktversionierung** – Verfolgen Sie Änderungen an Produkten anhand von Produktversionen und steuern Sie das Produkt in allen Phasen der Lieferkette. Auf diese Weise können Sie die Änderungen in Ihren Formulierungen verfolgen. Weitere Informationen finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).
- **Produktlebenszyklusmanagement** – Verwalten Sie die Sichtbarkeit von Produktdaten im gesamten Unternehmen und kontrollieren Sie die Verfügbarkeit von Produktversionen in jeder Phase der Lieferkette. Sie haben detaillierte Kontrolle darüber, wann eine Produktversion in bestimmten Geschäftsprozessen verwendet werden kann, und Sie können Ihren eigenen Lebenszyklusstatus erstellen, der Ihren Geschäftsanforderungen entspricht. Weitere Informationen finden Sie unter [Produktlebenszyklusstatus und Transaktionen](product-lifecycle-state-transactions.md).
- **Formeländerungsmanagement** – Benutzer in Ihrer gesamten Organisation können Änderungen an Formeln anfordern. Verwenden Sie Änderungsaufträge, um die Auswirkungen vorgeschlagener Änderungen zu bewerten und zu dokumentieren. Fügen Sie Workflows hinzu, um den Änderungsprozess und die Veröffentlichung neuer Versionen des Produkts und seiner Formel zu verwalten. Weitere Informationen finden Sie unter [Verwalten von Änderungen an Engineering-Produkten](engineering-change-management.md).
- **Bereitschaftskontrolle** – Verwenden Sie Systemprüfungen und Benutzeranleitungen (Fragebögen und Checklisten), um sicherzustellen, dass alle erforderlichen Produktdaten vollständig eingegeben wurden, bevor das Produkt freigegeben wird. Weitere Informationen finden Sie unter [Produktbereitschaft](product-readiness.md).
- **Erweiterte Produktfreigabefunktionalität** – Geben Sie vollständig definierte Versionen eines Produkts und seiner Formel von einer Organisation (juristische Person) an andere juristische Personen weiter. Sie können sogar entscheiden, ob die Produktinformationen vor der Veröffentlichung überprüft oder bearbeitet werden müssen. Weitere Informationen finden Sie unter [Produktstrukturen freigeben](release-product-structure.md).

Beachten Sie, dass die meisten Artikel, auf die in der vorherigen Liste verwiesen wird, Beispiele enthalten, die auf Stücklisten basieren. Formeln funktionieren jedoch auf ähnliche Weise. Im Folgenden finden Sie einige zusätzliche Konzepte, die hilfreich sind, wenn Sie das Änderungsmanagement (oder nur das Formeländerungsmanagement) zum Verwalten von Formeln und Stücklisten verwenden:

- Für jede [Produktentwicklungskategorie](engineering-versions-product-category.md) können Sie die Produktionsart (Stückliste, Formel oder Planungsposition) angeben. Sie können auch angeben, ob für Produkte, die diese Kategorie verwenden, eine Unterstützung des Artikelgewichts erforderlich ist.
- Co-Produkte und Nebenprodukte sind keine technischen Produkte. Daher sind sie nicht versioniert. Wenn Sie sie ändern müssen, erstellen Sie einfach ein neues Produkt. Dieser Ansatz erleichtert die Wartung.
- Sie können Endelemente verwalten, die Stücklisten sind und untergeordnete Formelelemente enthalten. Die Funktionalität funktioniert für jede Kombination von Stücklisten, die Formeln enthalten, und/oder Formeln, die Stücklisten enthalten.
