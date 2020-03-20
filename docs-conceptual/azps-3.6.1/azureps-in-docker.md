---
title: Använda Azure PowerShell i Docker
description: Så här använder du Azure PowerShell som är förinstallerat i en Docker-avbildning.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402688"
---
# <a name="using-azure-powershell-in-docker"></a>Använda Azure PowerShell i Docker

Vi publicerar Docker-avbildningar med Azure PowerShell förinstallerat. Den här artikeln visar hur du kommer igång med Azure PowerShell i Docker-containern.

## <a name="finding-available-images"></a>Hitta tillgängliga avbildningar

De publicerade avbildningarna kräver Docker 17.05 eller senare. Det förväntas också att du kan köra Docker utan `sudo` eller lokal administratörsbehörighet. Följ Dockers officiella [instruktioner][install] för att installera `docker` korrekt.

De utgivna containrarna skapas från officiella PowerShell-containrar och sedan läggs Az-modulen till som ett lager.

Den senaste stabila avbildningen innehåller:

- Ubuntu 18.04
- PowerShell version 6.2.4
- Azure PowerShells senaste Az-modul

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

## <a name="next-steps"></a>Nästa steg

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell