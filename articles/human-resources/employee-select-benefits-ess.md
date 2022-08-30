---
title: Mitarbeiter wählen Pläne mit dem Mitarbeiter-Self-Service aus (optional)
description: In diesem Artikel wird beschrieben, wie Mitarbeitende ihre Leistungen auswählen oder aktualisieren können.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 162cf2bfb6d382d270e0a5af42a739a390397153
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324441"
---
# <a name="employees-select-plans-by-using-employee-self-service-optional"></a>Mitarbeiter wählen Pläne mit dem Mitarbeiter-Self-Service aus (optional)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Wenn ein neuer Mitarbeiter neu eingestellt wird oder ein Lebensereignis eintritt, kann der Mitarbeiter den **Mitarbeiter-Self-Service** verwenden, um ihre Leistungen während der offenen Registrierung auszuwählen oder zu aktualisieren.

Um auf seine Leistungen für die Registrierung zuzugreifen, wechselt der Mitarbeiter zu **Mitarbeiter Self-Service** und wählt dann **Leistungs-Self-Service** auf der Kachel **Leistungen** aus.

Auf der Seite **Leistungs-Self-Service** werden Leistungspläne nach Plantyp gruppiert. Um die Leistungspläne in einem Plantyp anzuzeigen, wählt der Mitarbeiter eine Kachel auf der Seite **Mitarbeiterleistungen** aus. Der Mitarbeiter sieht nur die Leistungen, auf die er Anspruch hat.

> [!IMPORTANT]
> Bevor ein Plantyp im **Mitarbeiter-Self-Service** angezeigt werden kann, muss er konfiguriert werden. Weitere Informationen finden Sie unter [Mitarbeiter Self-Service konfigurieren](/dynamics365/human-resources/hr-benefits-setup-employee-self-service).

Je nach Plantyp können ein oder mehrere Leistungen für die Registrierung ausgewählt werden. Beispielsweise kann ein Krankenversicherungsplantyp so konfiguriert werden, dass der Mitarbeiter auf einen Krankenversicherungsplan beschränkt wird. Ein Lebensversicherungsplantyp kann es dem Mitarbeiter ermöglichen, mehrere Lebensversicherungspläne auszuwählen.

Nachdem der Mitarbeiter entschieden hat, für welchen Plan er sich registrieren möchte, muss er möglicherweise Angehörige auswählen. Wenn der Mitarbeiter eine Versicherungsoption gewählt hat, die **Mitarbeiter +1**, **Mitarbeiter + Kinder** oder **Familie** lautet, müssen Angehörige ausgewählt werden. Weitere Informationen über die Deckungsoptionen finden Sie unter [Deckungsoptionen erstellen](/dynamics365/human-resources/hr-benefits-setup-coverage-options).

Um einen Leistungsplan auszuwählen, wählt der Mitarbeiter entweder die Schaltfläche mit den Auslassungspunkten (**...**) oder **In den Warenkorb legen**. Nachdem der Mitarbeiter alle Leistungsoptionen in den Warenkorb gelegt hat, wählt er **Warenkorb anzeigen**. Der Mitarbeiter gelangt dann auf die Seite **Pläne**, auf der er seine ausgewählten und verzichteten Leistungspläne einsehen kann.

Der Mitarbeiter muss die **Ich stimme zu**-Option auswählen, bevor er die **Kasse**-Schaltfläche auswählen kann. Die Anweisung, die rechts neben der **Ich stimme zu**-Option angezeigt wird, kann auf der **Leistungsverwaltung**-Registerkarte der Seite **Gemeinsam genutzte Parameter der Personalabteilung** angepasst werden.

Wenn der Mitarbeiter seine Leistungsplanauswahl mit **Mitarbeiter-Self-Service** bestätigt, wird diese Auswahl aufgezeichnet und auf den Seiten **Leistungspläne für Arbeitskräfte** und **Massen-Update der Leistungspläne für Arbeitskräfte** angezeigt.

Nachdem der Mitarbeiter seine Pläne ausgewählt hat, wird der Status der Leistungen als **Ausgewählt** angezeigt. Wenn der Mitarbeiter **Kasse** auf der Seite **Leistungs-Self-Service** auswählt, wird die **Ausgecheckt**-Option ausgewählt.

> [!IMPORTANT]
> Um die Registrierung abzuschließen, muss der Leistungsadministrator **Bestätigen** für jede ausgewählte Mitarbeiter bestätigen. Die Bestätigung kann auf der Seite **Leistungsplan für Arbeitskräfte** oder **Massen-Update der Leistungspläne für Arbeitskräfte** abgeschlossen werden.
>

Mitarbeiter müssen keine Leistungen über den **Mitarbeiter-Self-Service** auswählen. Leistungen können im Namen eines Mitarbeiters auf der Seite **Leistungsplan für Arbeitskräfte** oder **Massen-Update der Leistungspläne für Arbeitnehmerrentenpläne** ausgewählt werden. Der Mitarbeiter wird nicht für diese Leistungen angemeldet, bis der Leistungsadministrator sie bestätigt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
