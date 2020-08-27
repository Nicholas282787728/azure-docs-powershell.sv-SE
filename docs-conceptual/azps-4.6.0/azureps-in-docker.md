---
title: Använda Azure PowerShell i Docker
description: Så här använder du Azure PowerShell som är förinstallerat i en Docker-avbildning.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821904"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="67a54-103">Använda Azure PowerShell i Docker</span><span class="sxs-lookup"><span data-stu-id="67a54-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="67a54-104">Vi publicerar Docker-avbildningar med Azure PowerShell förinstallerat.</span><span class="sxs-lookup"><span data-stu-id="67a54-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="67a54-105">Den här artikeln visar hur du kommer igång med Azure PowerShell i Docker-containern.</span><span class="sxs-lookup"><span data-stu-id="67a54-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="67a54-106">Hitta tillgängliga avbildningar</span><span class="sxs-lookup"><span data-stu-id="67a54-106">Finding available images</span></span>

<span data-ttu-id="67a54-107">De publicerade avbildningarna kräver Docker 17.05 eller senare.</span><span class="sxs-lookup"><span data-stu-id="67a54-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="67a54-108">Det förväntas också att du kan köra Docker utan `sudo` eller lokal administratörsbehörighet.</span><span class="sxs-lookup"><span data-stu-id="67a54-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="67a54-109">Följ Dockers officiella [instruktioner][install] för att installera `docker` korrekt.</span><span class="sxs-lookup"><span data-stu-id="67a54-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="67a54-110">Den senaste containeravbildningen innehåller den senaste versionen av PowerShell och de senaste Azure PowerShell-modulerna som stöds med AZ-modulen.</span><span class="sxs-lookup"><span data-stu-id="67a54-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="67a54-111">För varje ny version av AZ-modulen släpper vi en avbildning för följande operativsystem:</span><span class="sxs-lookup"><span data-stu-id="67a54-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="67a54-112">Ubuntu 18.04 (standard)</span><span class="sxs-lookup"><span data-stu-id="67a54-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="67a54-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="67a54-113">Debian 9</span></span>
- <span data-ttu-id="67a54-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="67a54-114">CentOs 7</span></span>

<span data-ttu-id="67a54-115">En fullständig lista över tillgängliga avbildningar finns på sidan [Docker-avbildning][az image].</span><span class="sxs-lookup"><span data-stu-id="67a54-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="67a54-116">Använda Azure PowerShell i en container</span><span class="sxs-lookup"><span data-stu-id="67a54-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="67a54-117">Följande steg visar de Docker-kommandon som krävs för att ladda ned avbildningen och starta en interaktiv PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="67a54-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="67a54-118">Ladda ned den senaste azure-powershell-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="67a54-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="67a54-119">Kör azure-powershell-containern i interaktivt läge:</span><span class="sxs-lookup"><span data-stu-id="67a54-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="67a54-120">För Windows Docker-värdar måste du aktivera Docker-fildelningen för att tillåta att lokala enheter i Windows delas med Linux-containrar.</span><span class="sxs-lookup"><span data-stu-id="67a54-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="67a54-121">Mer information finns i [Kom igång med Docker för Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="67a54-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="67a54-122">Köra azure-powershell-containern interaktivt med hjälp av värdautentisering</span><span class="sxs-lookup"><span data-stu-id="67a54-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="67a54-123">Om du redan har Azure PowerShell installerat i det system som är värd för Docker kan du ha cachelagrade autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="67a54-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="67a54-124">De här autentiseringsuppgifterna kan användas i PowerShell-sessionen som körs i Docker-containern.</span><span class="sxs-lookup"><span data-stu-id="67a54-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="67a54-125">Som standard finns cachelagrade autentiseringsuppgifter i `$HOME/.Azure`-katalogen hos värden.</span><span class="sxs-lookup"><span data-stu-id="67a54-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="67a54-126">Docker-tjänsten måste ha åtkomst till den här platsen för att få åtkomst till autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="67a54-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="67a54-127">Följande kommando startar containern med cachen för autentiseringsuppgifter monterad och startar en interaktiv PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="67a54-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="67a54-128">Ta bort avbildningen när den inte längre behövs</span><span class="sxs-lookup"><span data-stu-id="67a54-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="67a54-129">Följande kommando används för att ta bort Docker-containern när du inte längre behöver den.</span><span class="sxs-lookup"><span data-stu-id="67a54-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="67a54-130">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="67a54-130">Next steps</span></span>

<span data-ttu-id="67a54-131">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="67a54-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
