---
title: Översikt över Azure Stack PowerShell | Microsoft Docs
description: Översikt över installation och konfiguration av Azure Stack PowerShell.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 3f55ff613004f0726e20255126b29bf7f64662b8
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820212"
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="25683-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="25683-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="25683-104">Azure Stack kräver följande två PowerShell-moduler:</span><span class="sxs-lookup"><span data-stu-id="25683-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="25683-105">Den Azure Stack-kompatibla **AzureRM**-modulen som blir tillgänglig genom att installera API-versionsprofilen **2017-03-09-profile**.</span><span class="sxs-lookup"><span data-stu-id="25683-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="25683-106">De cmdletar som installerats med den här profilen kan användas av Azure Stack-användare och -operatörer.</span><span class="sxs-lookup"><span data-stu-id="25683-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="25683-107">Den senaste versionen är **1.2.11**-installationen av **AzureStack**-modulen.</span><span class="sxs-lookup"><span data-stu-id="25683-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="25683-108">De cmdletar som installerats med den hör modulen kan endast användas av Azure Stack-operatörer.</span><span class="sxs-lookup"><span data-stu-id="25683-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="25683-109">Administratörer kan utföra åtgärder som att hantera erbjudanden, planer, tjänster, kvoter och annat med de PowerShell-cmdletar som tillhandahålls i modulen.</span><span class="sxs-lookup"><span data-stu-id="25683-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="25683-110">Mer information om PowerShell-cmdletarna i den här modulen finns i [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin)- och [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage)-referensinnehållet.</span><span class="sxs-lookup"><span data-stu-id="25683-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="25683-111">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="25683-111">Next Steps</span></span>

* [<span data-ttu-id="25683-112">Installera PowerShell för Azure Stack</span><span class="sxs-lookup"><span data-stu-id="25683-112">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="25683-113">Konfigurera PowerShell för användning med Azure Stack</span><span class="sxs-lookup"><span data-stu-id="25683-113">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
