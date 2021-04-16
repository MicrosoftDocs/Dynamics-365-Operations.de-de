---
title: Servicevorlagen
description: Sie können eine Servicevereinbarung als Vorlage definieren und später die Positionen dieser Vorlage in eine andere Servicevorlage oder in einen Serviceauftrag kopieren.
author: ShylaThompson
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 409c15ae9c8f5f3c9c72adf3313f4594ba3c1764
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819015"
---
# <a name="service-templates"></a>Servicevorlagen

[!include [banner](../includes/banner.md)]

Sie können eine Servicevereinbarung als Vorlage definieren und später die Positionen dieser Vorlage in eine andere Servicevorlage oder in einen Serviceauftrag kopieren.

## <a name="example"></a>Beispiel

Ein Debitor, für den Sie eine Serviceleistung erbringen, besitzt fünf identische Lastenaufzüge an fünf unterschiedlichen Standorten.

Für den Debitor sollen fünf einzelne Servicevereinbarungen eingerichtet werden – pro Standort jeweils eine.
Hierzu erstellen Sie eine Servicevereinbarung und geben diese als Vorlage für die Servicearbeiten an den Aufzügen an. Dadurch ersparen Sie sich nicht nur das wiederholte Ausführen der gleichen Schritte, sondern stellen überdies sicher, dass die Servicevereinbarungen identische Informationen enthalten.

Nun können die Vorlagenpositionen in die fünf neuen Servicevereinbarungen kopiert werden, sodass jede Servicevereinbarung mit den Positionen aus der Vorlage ausgefüllt wird.

## <a name="create-a-template"></a>Eine Vorlage erstellen

Gehen Sie zum Erstellen einer Servicevorlage folgendermaßen vor: Erstellen Sie eine Servicevereinbarung, erstellen Sie die erforderlichen Positionen, und ordnen Sie die Servicevereinbarung anschließend einer Servicevorlagengruppe zu.

> [!NOTE]
> Eine Servicevereinbarung kann nur dann als Vorlage fungieren, wenn ihr keine Serviceaufträge zugeordnet sind. Umgekehrt lassen sich keine Serviceaufträge auf Basis einer Servicevereinbarung erstellen, die als Vorlage definiert ist.

## <a name="copy-template-lines"></a>Vorlagenpositionen kopieren

Die Positionen einer Vorlage können aus einer Servicevorlage in eine andere Servicevorlage oder in ein einen Serviceauftrag kopiert werden.

Beim Kopieren von Vorlagenpositionen in einen Serviceauftrag oder in eine Servicevereinbarung wird eine Strukturdarstellung der Vorlagengruppen angezeigt, in der die einzelnen Gruppen erweitert werden können. Diese Darstellung ermöglicht das Anzeigen sämtlicher Vorlagen und Vorlagenpositionen.

Zur Vereinfachung der Suche nach den zu kopierenden Positionen empfiehlt es sich, die Vorlagen unter aussagekräftigen Namen zu gruppieren.

## <a name="related-topics"></a>Verwandte Themen

[Kopieren von Servicevorlagenpositionen](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]