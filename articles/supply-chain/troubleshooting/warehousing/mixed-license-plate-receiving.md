---
title: Der Empfang von gemischten Ladungsträgern funktioniert nicht für alle Dispositionscodes
description: Wenn das Feld Aktion für einen Dispositionscode auf Kredit oder Schrott festgelegt ist, können Sie nur den Menüpunkt Mischkennzeichen-Empfang verwenden, um zurückgegebene Elemente zu verarbeiten.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476469"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Der Empfang von gemischten Ladungsträgern funktioniert nicht für alle Dispositionscodes außer Guthaben

## <a name="symptoms"></a>Symptome

Wenn das Feld **Aktion** für einen Dispositionscode auf *Kredit* oder *Schrott* festgelegt ist, können Sie nur den Menüpunkt [Mischkennzeichen-Empfang](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) verwenden, um zurückgegebene Elemente zu verarbeiten.

## <a name="resolution"></a>Lösung

Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Derzeit werden für den gemischten Ladungsträger-Empfang nur [Positionscodes](/dynamics365/supply-chain/service-management/set-up-disposition-codes) unterstützt, bei denen das Feld **Aktion** auf *Gutschrift* oder *Ausschuss* festgelegt ist.
