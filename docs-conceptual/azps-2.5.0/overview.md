---
title: Översikt över Azure PowerShell
description: En översikt över Azure PowerShell Az-modulen med information om hur du installerar och kommer igång.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657628"
---
# <a name="overview-of-azure-powershell"></a>Översikt över Azure PowerShell

Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser. Azure PowerShell använder .NET Standard, vilket gör det tillgängligt för Windows, macOS och Linux.
Azure PowerShell är också tillgängligt i Azure Cloud Shell.

## <a name="about-the-new-az-module"></a>Om den nya Az-modulen

I den här dokumentationen beskrivs den nya Az-modulen för Azure PowerShell. Den nya modulen skrivs från grunden i .NET Standard. Med.NET Standard kan du köra Azure PowerShell under PowerShell 5.1 i Windows och PowerShell 6 och senare på valfri plattform. Az-modulen är nu rätt sätt att interagera med Azure via PowerShell.
Vi fortsätter göra felkorrigeringar i AzureRM men inga nya funktioner läggs till.

Fullständig information om den nya modulen, som nya kommandonamn och underhållsplaner för AzureRM, finns i [Introduktion till Azure PowerShell Az-modulen](new-azureps-module-az.md). Om du vill komma igång med den nya modulen direkt läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).

[AzureRM-dokumentationen](/powershell/azure/azurerm) finns också tillgänglig.

> [!IMPORTANT]
>
> Medan Azure-dokumentationen uppdateras för att återspegla de nya modul-cmdlet-namnen kan det hända att AzureRM-kommandona fortfarande används i artiklarna. När du har installerat Az-modulen rekommenderar vi att du aktiverar AzureRM-cmdlet-aliasen med `Enable-AzureRmAlias`. Mer information finns i artikeln [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="run-or-install"></a>Köra eller installera

Du kan installera Azure PowerShell på PowerShell 5.1 eller senare i Windows och PowerShell 6.x och senare, på valfri plattform, och köra det i Azure Cloud Shell.

* Om du vill köra det i webbläsaren med Azure Cloud Shell läser du [Snabbstart för PowerShell i Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Om du vill installera Azure PowerShell på datorn läser du [Installera Azure PowerShell](install-az-ps.md).

Information om den senaste versionen av Azure PowerShell finns i [Viktig information](release-notes-azureps.md).

## <a name="get-started"></a>Kom igång

Läs artikeln [Komma igång med Azure PowerShell](get-started-azureps.md) om du vill lära dig grunderna i Azure PowerShell. Om du inte känner till PowerShell kan en introduktion vara till hjälp:

* [Installera PowerShell](/powershell/scripting/install/installing-powershell)
* [Köra skript med PowerShell](/powershell/scripting/powershell-scripting)
* [PowerShell-grunder: (Del 1) Komma igång med PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

Följande exempel kan hjälpa dig med några vanliga användningsområden för Azure:

* [Virtuella Linux-datorer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Virtuella Windows-datorer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL-databaser](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Utveckla dina färdigheter med Microsoft Learn

- [Automatisera Azure-uppgifter med hjälp av skript med PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Mer interaktiv inlärning...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Andra Azure PowerShell-moduler

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
