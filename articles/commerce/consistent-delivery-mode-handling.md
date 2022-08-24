---
title: Konsistente Behandlung von Liefermodi in E-Commerce-Kanälen ermöglichen
description: In diesem Artikel wird beschrieben, wie Sie eine konsistente Handhabung des Liefermodus aktivieren, um mögliche Probleme im Zusammenhang mit den Flows für Belastungen in den E-Commerce-Kanälen von Microsoft Dynamics 365 Commerce zu beheben.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279649"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Konsistente Behandlung von Liefermodi in E-Commerce-Kanälen ermöglichen 

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine konsistente Handhabung des Liefermodus aktivieren, um mögliche Probleme im Zusammenhang mit den Flows für Belastungen in den E-Commerce-Kanälen von Microsoft Dynamics 365 Commerce zu beheben.

In Dynamics 365 Commerce werden in E-Commerce-Kanälen standardmäßig keine anteiligen Belastungen auf Kopfebene angewendet. Dieses Verhalten kann in E-Commerce-Kanälen eines oder beide der folgenden Probleme verursachen:

- Nicht anteilige Belastungen auf Kopfebene werden nicht angezeigt.
- Belastungen für Lieferarten sind nicht konsistent zwischen der Auswahl der Lieferart und der Bestellzusammenfassung an der Kasse.

Um diese Probleme zu beheben, müssen Sie die Funktion **Konsistente Behandlung des Zustellungsmodus im Channel aktivieren** aktivieren. Diese Funktion stellt sicher, dass in E-Commerce-Kanälen nicht anteilige Belastungen auf Kopfebene angezeigt werden und dass Informationen zur Lieferung von Verkaufsaufträgen durch denselben Anfrage-Workflow einheitlich behandelt werden.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Aktivieren Sie die Funktion Behandlung des konsistenten Zustellungsmodus im Channel aktivieren

Um die Funktion **Konsistente Handhabung des Liefermodus im Channel aktivieren** in der Commerce-Zentrale zu aktivieren, führen Sie diese Schritte aus.

1. Öffnen Sie den Arbeitsbereich **Funktionsverwaltung** (**Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**).
1. Suchen Sie in der Liste der verfügbaren Funktionen nach und wählen Sie **Konsistente Behandlung des Zustellungsmodus im Channel aktivieren**.
1. Wählen Sie im rechten Fensterbereich **Jetzt aktivieren**.
