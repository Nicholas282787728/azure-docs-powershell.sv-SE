---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758301"
---
# <span data-ttu-id="75446-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="75446-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="75446-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75446-102">SYNOPSIS</span></span>
<span data-ttu-id="75446-103">Exporterar en logg från en instans av Analysis Services-servern i den aktuella inloggade miljön som angiven i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="75446-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75446-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75446-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="75446-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75446-105">DESCRIPTION</span></span>
<span data-ttu-id="75446-106">Export-AzureAnalysisServicesInstance cmdlet exporterar loggen från en instans av Azure Analysis Services-servern till filen</span><span class="sxs-lookup"><span data-stu-id="75446-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="75446-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75446-107">EXAMPLES</span></span>

### <span data-ttu-id="75446-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75446-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="75446-109">Det här kommandot exporterar logg från servern ' testserver ' i den miljö som anges i kommandot Add-AzureAnalysisServicesAccount och sparar den i filen som anges i OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="75446-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="75446-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75446-110">PARAMETERS</span></span>

### <span data-ttu-id="75446-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="75446-111">-Instance</span></span>
<span data-ttu-id="75446-112">Namn på Analysis Services-serverinstansen</span><span class="sxs-lookup"><span data-stu-id="75446-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75446-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="75446-113">-OutputPath</span></span>
<span data-ttu-id="75446-114">Sökväg till fil som ska exporteras</span><span class="sxs-lookup"><span data-stu-id="75446-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75446-115">-Force</span><span class="sxs-lookup"><span data-stu-id="75446-115">-Force</span></span>
<span data-ttu-id="75446-116">Skriv över filen om den finns utan att fråga</span><span class="sxs-lookup"><span data-stu-id="75446-116">Overwrite file if exists without asking</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="75446-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75446-117">INPUTS</span></span>

## <span data-ttu-id="75446-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75446-118">OUTPUTS</span></span>

## <span data-ttu-id="75446-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75446-119">NOTES</span></span>
<span data-ttu-id="75446-120">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="75446-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="75446-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75446-121">RELATED LINKS</span></span>

