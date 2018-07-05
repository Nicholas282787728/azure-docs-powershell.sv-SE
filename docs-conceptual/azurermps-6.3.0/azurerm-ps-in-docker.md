---
title: Köra Azure PowerShell i en Docker-behållare
description: Så här kör du Azure PowerShell i en Docker-behållare.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091635"
---
## <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="a8af0-103">Köra Azure PowerShell i en Docker-behållare</span><span class="sxs-lookup"><span data-stu-id="a8af0-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="a8af0-104">Det finns en uppsättning Docker-avbildningar som är förkonfigurerade med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8af0-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="a8af0-105">Två typer av behållare finns tillgängliga: de som kör traditionella PowerShell på Windows och en behållare som kör PowerShell Core på antingen Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="a8af0-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="a8af0-106">Miljö</span><span class="sxs-lookup"><span data-stu-id="a8af0-106">Environment</span></span> | <span data-ttu-id="a8af0-107">Docker-avbildning</span><span class="sxs-lookup"><span data-stu-id="a8af0-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="a8af0-108">PowerShell på Windows</span><span class="sxs-lookup"><span data-stu-id="a8af0-108">PowerShell on Windows</span></span> | [<span data-ttu-id="a8af0-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="a8af0-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="a8af0-110">PowerShell Core på Windows</span><span class="sxs-lookup"><span data-stu-id="a8af0-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="a8af0-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="a8af0-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="a8af0-112">PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="a8af0-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="a8af0-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="a8af0-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="a8af0-114">Använd `docker run -it $ImageName` för att hämta en interaktiv terminal och köra någon av dessa behållare.</span><span class="sxs-lookup"><span data-stu-id="a8af0-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="a8af0-115">Om du till exempel vill köra PowerShell Core på Linux-behållare använder du:</span><span class="sxs-lookup"><span data-stu-id="a8af0-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="a8af0-116">Om du vill köra en Windows-behållare i Docker måste OS-värden vara Windows och Docker måste konfigureras för att köra Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="a8af0-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="a8af0-117">Mer information om att växla mellan Windows- och Linux-miljöer i Docker finns i Docker-dokumentationen [Växla mellan Windows- och Linux-behållare](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="a8af0-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="a8af0-118">Använda en PowerShell Core-behållare</span><span class="sxs-lookup"><span data-stu-id="a8af0-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="a8af0-119">PowerShell Core-behållarna som levereras med PowerShell Core v6 och modulen `AzureRM.NetCore` förinstallerad.</span><span class="sxs-lookup"><span data-stu-id="a8af0-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="a8af0-120">Kör cmdleten [Import-Module](/powershell/module/microsoft.powershell.core/import-module) och logga in med ditt Azure-konto:</span><span class="sxs-lookup"><span data-stu-id="a8af0-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="a8af0-121">Använda Windows-behållaren med PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8af0-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="a8af0-122">Windows-behållaren har modulen `AzureRM` förinstallerad.</span><span class="sxs-lookup"><span data-stu-id="a8af0-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="a8af0-123">Kör cmdleten [Import-Module](/powershell/module/microsoft.powershell.core/import-module) och logga in med ditt Azure-konto:</span><span class="sxs-lookup"><span data-stu-id="a8af0-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```