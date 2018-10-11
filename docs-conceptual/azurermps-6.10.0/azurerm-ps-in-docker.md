---
title: Köra Azure PowerShell i en Docker-behållare
description: Så här kör du Azure PowerShell i en Docker-behållare.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882169"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="f1c19-103">Köra Azure PowerShell i en Docker-behållare</span><span class="sxs-lookup"><span data-stu-id="f1c19-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="f1c19-104">Microsoft publicerar Docker-avbildningar med Azure PowerShell förinstallerat.</span><span class="sxs-lookup"><span data-stu-id="f1c19-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="f1c19-105">De här avbildningarna gör det möjligt att experimentera med Azure PowerShell eller köra det i en isolerad miljö.</span><span class="sxs-lookup"><span data-stu-id="f1c19-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="f1c19-106">Det finns avbildningar med både PowerShell Core och PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="f1c19-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="f1c19-107">Miljö</span><span class="sxs-lookup"><span data-stu-id="f1c19-107">Environment</span></span> | <span data-ttu-id="f1c19-108">Docker-avbildning</span><span class="sxs-lookup"><span data-stu-id="f1c19-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="f1c19-109">PowerShell på Windows</span><span class="sxs-lookup"><span data-stu-id="f1c19-109">PowerShell on Windows</span></span> | [<span data-ttu-id="f1c19-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="f1c19-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="f1c19-111">PowerShell Core på Windows</span><span class="sxs-lookup"><span data-stu-id="f1c19-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="f1c19-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="f1c19-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="f1c19-113">PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="f1c19-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="f1c19-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="f1c19-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="f1c19-115">Använd `docker run -it $ImageName` för att hämta en interaktiv terminal och köra någon av dessa containrar.</span><span class="sxs-lookup"><span data-stu-id="f1c19-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="f1c19-116">Om du till exempel vill köra en Linux-container med PowerShell Core:</span><span class="sxs-lookup"><span data-stu-id="f1c19-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="f1c19-117">Om du vill köra en Windows-container i Docker måste OS-värden vara Windows och Docker måste konfigureras för att köra Windows-containrar.</span><span class="sxs-lookup"><span data-stu-id="f1c19-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="f1c19-118">Mer information om att växla mellan Windows- och Linux-miljöer i Docker finns i Docker-dokumentationen [Växla mellan Windows- och Linux-containrar](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="f1c19-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="f1c19-119">Använda en PowerShell Core-behållare</span><span class="sxs-lookup"><span data-stu-id="f1c19-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="f1c19-120">PowerShell Core-behållarna som levereras med PowerShell Core v6 och modulen `AzureRM.NetCore` förinstallerad.</span><span class="sxs-lookup"><span data-stu-id="f1c19-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="f1c19-121">Kör cmdleten [Import-Module](/powershell/module/microsoft.powershell.core/import-module) och logga in med ditt Azure-konto:</span><span class="sxs-lookup"><span data-stu-id="f1c19-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="f1c19-122">Använda Windows-behållaren med PowerShell</span><span class="sxs-lookup"><span data-stu-id="f1c19-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="f1c19-123">Windows-behållaren har modulen `AzureRM` förinstallerad.</span><span class="sxs-lookup"><span data-stu-id="f1c19-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="f1c19-124">Kör cmdleten [Import-Module](/powershell/module/microsoft.powershell.core/import-module) och logga in med ditt Azure-konto:</span><span class="sxs-lookup"><span data-stu-id="f1c19-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
