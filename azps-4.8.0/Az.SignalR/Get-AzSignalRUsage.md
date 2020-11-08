---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100816"
---
# <span data-ttu-id="cfa6c-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="cfa6c-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="cfa6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfa6c-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa6c-103">Hämta användnings kvoten för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="cfa6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfa6c-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa6c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfa6c-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa6c-106">Hämta användnings kvoten för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="cfa6c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfa6c-107">EXAMPLES</span></span>

### <span data-ttu-id="cfa6c-108">Skaffa användnings kvoten genom att ange platsen</span><span class="sxs-lookup"><span data-stu-id="cfa6c-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="cfa6c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfa6c-109">PARAMETERS</span></span>

### <span data-ttu-id="cfa6c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa6c-110">-DefaultProfile</span></span>
<span data-ttu-id="cfa6c-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa6c-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="cfa6c-112">-Location</span></span>
<span data-ttu-id="cfa6c-113">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa6c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa6c-114">CommonParameters</span></span>
<span data-ttu-id="cfa6c-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa6c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa6c-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfa6c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa6c-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfa6c-117">INPUTS</span></span>

### <span data-ttu-id="cfa6c-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="cfa6c-118">None</span></span>

## <span data-ttu-id="cfa6c-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfa6c-119">OUTPUTS</span></span>

### <span data-ttu-id="cfa6c-120">Microsoft. Azure. commands. signaler. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="cfa6c-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="cfa6c-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfa6c-121">NOTES</span></span>

## <span data-ttu-id="cfa6c-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfa6c-122">RELATED LINKS</span></span>
