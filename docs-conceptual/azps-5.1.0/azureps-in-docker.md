---
title: Använda Azure PowerShell i Docker
description: Så här använder du Azure PowerShell som är förinstallerat i en Docker-avbildning.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715866"
---
# <a name="using-azure-powershell-in-docker"></a>Använda Azure PowerShell i Docker

Vi publicerar Docker-avbildningar med Azure PowerShell förinstallerat. Den här artikeln visar hur du kommer igång med Azure PowerShell i Docker-containern.

## <a name="finding-available-images"></a>Hitta tillgängliga avbildningar

De publicerade avbildningarna kräver Docker 17.05 eller senare. Det förväntas också att du kan köra Docker utan `sudo` eller lokal administratörsbehörighet. Följ Dockers officiella [instruktioner][install] för att installera `docker` korrekt.

Den senaste containeravbildningen innehåller den senaste versionen av PowerShell och de senaste Azure PowerShell-modulerna som stöds med AZ-modulen.

För varje ny version av AZ-modulen släpper vi en avbildning för följande operativsystem:

- Ubuntu 18.04 (standard)
- Debian 9
- CentOs 7

En fullständig lista över tillgängliga avbildningar finns på sidan [Docker-avbildning][az image].

## <a name="using-azure-powershell-in-a-container"></a>Använda Azure PowerShell i en container

Följande steg visar de Docker-kommandon som krävs för att ladda ned avbildningen och starta en interaktiv PowerShell-session.

1. Ladda ned den senaste azure-powershell-avbildningen.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Kör azure-powershell-containern i interaktivt läge:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

För Windows Docker-värdar måste du aktivera Docker-fildelningen för att tillåta att lokala enheter i Windows delas med Linux-containrar. Mer information finns i [Kom igång med Docker för Windows][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Köra azure-powershell-containern interaktivt med hjälp av värdautentisering

Om du redan har Azure PowerShell installerat i det system som är värd för Docker kan du ha cachelagrade autentiseringsuppgifter för Azure. De här autentiseringsuppgifterna kan användas i PowerShell-sessionen som körs i Docker-containern.

Som standard finns cachelagrade autentiseringsuppgifter i `$HOME/.Azure`-katalogen hos värden. Docker-tjänsten måste ha åtkomst till den här platsen för att få åtkomst till autentiseringsuppgifterna. Följande kommando startar containern med cachen för autentiseringsuppgifter monterad och startar en interaktiv PowerShell-session.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Ta bort avbildningen när den inte längre behövs

Följande kommando används för att ta bort Docker-containern när du inte längre behöver den.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Next steps

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
