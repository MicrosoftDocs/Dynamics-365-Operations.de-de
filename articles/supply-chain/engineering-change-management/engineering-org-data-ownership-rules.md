---
title: Engineering-Firmen und Datenbesitzregeln
description: Dieses Thema erklärt, wie Sie eine oder mehrere Engineering-Firmen verwenden können, um sicherzustellen, dass die Stammdaten für Produkte zentral erstellt und gepflegt werden. Eine Engineering-Firma stellt die Firma dar, die Eigentümerin der Engineering-Produkte und ihrer engineering-relevanten Daten ist.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ab5ca3bee65bb0ee8ce7f44ba97c00347fe38366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963662"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Engineering-Firmen und Datenbesitzregeln

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Engineering-Firmen und Betriebsfirmen

Um sicherzustellen, dass die Stammdaten für Produkte zentral erstellt und gepflegt werden, können Sie eine oder mehrere *Engineering-Firmen* verwenden. Eine Engineering-Firma ist Eigentümerin der Engineering-Produkte und ihrer Engineering-relevanten Daten. Sie ist immer mit (basierend auf) einer bestehenden *juristischen Entität* verbunden, die ebenfalls eine Firma ist. Durch diese Verbindung wird ein zentraler Einstiegspunkt für alle Engineering-relevanten Daten der Engineering-Produkte in der Engineering-Firma geschaffen. In diesem zentralen Einstiegspunkt werden die Engineering-Produkte erstellt und die Engineering-relevanten Daten gepflegt. Von dort aus werden die Engineering-Produkte und Engineering-relevanten Daten an *Betriebsfirmen*, die andere juristische Entitäten sind, freigegeben. (Weitere Informationen über das Freigabemanagement finden Sie unter [Freigabe von Produktstrukturen](release-product-structure.md).) Diese Betriebsfirmen werden die Engineering-Daten so verwenden, wie sie von der Engineering-Firma entworfen wurden. Alle logistischen Daten werden von jeder Engineering-Firma und Betriebsfirma lokal gepflegt.

Um eine Engineering-Firma zu erstellen, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Engineering-Organisationen**. Wählen Sie **Neu**, geben Sie einen Namen für die Engineering-Firma ein und wählen Sie die bestehende Firma (juristische Entität), auf der sie basiert.

Wenn Sie eine Integration mit externen Product-Lifecycle-Management-Systemen (PLM) vornehmen, müssen Sie eine Einheit (Unternehmenstyp) erstellen, die ein externes Unternehmen werden soll.

## <a name="engineering-product-categories-and-engineering-companies"></a>Engineering-Produktkategorien und Engineering-Firmen

*Engineering-Produktkategorien* helfen sicherzustellen, dass Engineering-Produkte gemäß den Geschäftsregeln Ihres Unternehmens erstellt werden und sich wie gewünscht verhalten. Weitere Informationen über Engineering-Produktkategorien finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).

Jede Engineering-Produktkategorie gehört zu einer bestimmten Engineering-Firma und kann nur Produkte erstellen, die zu dieser Firma gehören. Ebenso gehört das Recht, ein Engineering-Produkt zu pflegen, dem Unternehmen, das mit der Engineering-Produktkategorie dieses Produkts verbunden ist.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Daten, die im Besitz des Engineering-Firma sind

Da die Engineering-Firma Eigentümerin der Engineering-relevanten Daten ist, kontrolliert sie die folgenden Prozesse:

- **Erstellung von Engineering-Produkten:** Jede Engineering-Firma kann nur neue Engineering-Produkte erstellen, die auf einer Engineering-Produktkategorie basieren, deren Eigentümer sie ist. In einigen Fällen pflegen die Betriebsfirmen ihre eigenen lokalen Daten, die sich auf diese Produkte beziehen.
- **Erstellung von Engineering-Versionen:** Wenn eine Firma ein neues Engineering-Produkt erstellt, erstellt das System automatisch eine erste Engineering-Version dafür. Nur die besitzende Engineering-Firma ist in der Lage, neue Versionen für dieses Produkt zu erstellen.
- **Erstellung und Pflege von Engineering-Attributen:** Wenn eine Firma ein neues Engineering-Produkt erstellt, fügt das System ihm automatisch Engineering-Attribute hinzu. Nur die besitzende Engineering-Firma ist in der Lage, die Werte für diese Attribute zu erstellen und zu pflegen. Weitere Informationen über Engineering-Attribute finden Sie unter [Engineering-Attribute und Engineering-Attribut-Suche](engineering-attributes-and-search.md).
- **Erstellung und Pflege von Stücklisten, die mit den Engineering-Versionen verbunden sind:** Die besitzende Engineering-Firma kann eine Stückliste direkt mit einer Engineering-Produktversion verbinden. Wenn diese Stücklisten an andere juristische Entitäten freigegeben werden, sind Änderungen an den Engineering-Daten der Stücklisten auf folgende Weise eingeschränkt:

    - Die Betriebsfirma kann freigegebene Stücklistenzeilen nicht entfernen.
    - Die Engineering-Felder auf den Stücklisten-Zeilen sind für die Betriebsfirma schreibgeschützt. Alle anderen Felder sind Felder der logistischen Implementierung und können von der Betriebsfirma bearbeitet werden.
    - Die Betriebsfirma kann Stücklistenzeilen zu derselben Stückliste hinzufügen. Auf diese Weise kann sie lokale Zusätze hinzufügen, z. B. Verpackungsmaterialien oder Schmiermittel.
    - Die Betriebsfirma kann eine komplett neue, lokale Stückliste hinzufügen. Diese Änderung kann z. B. dann erforderlich sein, wenn bei der Freigabe keine Stückliste bereitgestellt wird. Die Betriebsfirma ist Eigentümerin dieser lokalen Stücklisten und pflegt sie. Weitere Informationen zur Freigabeverwaltung finden Sie unter [Produktstrukturen freigeben](release-product-structure.md).
    - Alle lokalen Stücklisten und Stücklistenzeilen bleiben erhalten, wenn die Engineering-Firma ihre Stückliste aktualisiert.

- **Erstellung und Pflege von Arbeitsplänen, die mit den Engineering-Versionen verbunden sind:** Die Engineering-Firma kann direkt einen Arbeitsplan mit jeder Engineering-Version verbinden. Wenn diese Arbeitspläne für andere juristische Entitäten freigegeben werden, sind Änderungen an den Daten der Arbeitspläne wie folgt eingeschränkt:

    - Die anderen juristischen Entitäten können die Engineering-Daten auf den Arbeitsplänen nicht entfernen.
    - Die anderen juristischen Entitäten können dem Arbeitsplan Vorgänge hinzufügen. Auf diese Weise können sie lokale Arbeitsplanschritte hinzufügen.
    - Die Betriebsfirmen können komplett neue, lokale Arbeitspläne hinzufügen. Diese Änderung kann erforderlich sein, wenn Sie z. B. bei der Freigabe keine Arbeitspläne aufgenommen haben. Die Betriebsfirmen besitzen und pflegen diese lokalen Arbeitspläne. Weitere Informationen zur Freigabeverwaltung finden Sie unter [Produktstrukturen freigeben](release-product-structure.md).
    - Alle Änderungen, die lokal vorgenommen werden, bleiben erhalten, wenn Updates von der Engineering-Firma wieder für die Arbeitspläne freigegeben werden.

- **Erstellung und Pflege von Engineering-Dokumenten:** Die Engineering-Firma kann an jede Engineering-Version Engineering-Dokumente anhängen.

    - Wenn diese Dokumente an andere juristische Entitäten freigegeben werden, sind die Dokumente davor geschützt, von der Betriebsfirma entfernt zu werden.
    - Andere juristische Entitäten können völlig neue, lokale Dokumente hinzufügen. Die Betriebsfirma ist Eigentümerin und Verwalterin dieser lokalen Dokumente.
