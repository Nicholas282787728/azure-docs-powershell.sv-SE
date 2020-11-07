---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 99cf5e96e859932863236eacc1ad83a0b73ceecf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919910"
---
# <span data-ttu-id="8a9cb-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="8a9cb-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="8a9cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9cb-103">Hämta användnings kvoten för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a9cb-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="8a9cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a9cb-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a9cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a9cb-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9cb-106">Hämta användnings kvoten för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a9cb-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="8a9cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a9cb-107">EXAMPLES</span></span>

### <span data-ttu-id="8a9cb-108">Skaffa användnings kvoten genom att ange platsen</span><span class="sxs-lookup"><span data-stu-id="8a9cb-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="8a9cb-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a9cb-109">PARAMETERS</span></span>

### <span data-ttu-id="8a9cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9cb-110">-DefaultProfile</span></span>
<span data-ttu-id="8a9cb-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9cb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9cb-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a9cb-112">-Location</span></span>
<span data-ttu-id="8a9cb-113">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="8a9cb-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="8a9cb-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9cb-114">CommonParameters</span></span>
<span data-ttu-id="8a9cb-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9cb-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9cb-116">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a9cb-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9cb-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a9cb-117">INPUTS</span></span>

### <span data-ttu-id="8a9cb-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a9cb-118">None</span></span>

## <span data-ttu-id="8a9cb-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a9cb-119">OUTPUTS</span></span>

### <span data-ttu-id="8a9cb-120">Microsoft. Azure. commands. signaler. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="8a9cb-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="8a9cb-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a9cb-121">NOTES</span></span>

## <span data-ttu-id="8a9cb-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a9cb-122">RELATED LINKS</span></span>
