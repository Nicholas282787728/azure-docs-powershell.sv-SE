---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527179"
---
# <span data-ttu-id="982b3-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="982b3-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="982b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="982b3-102">SYNOPSIS</span></span>
<span data-ttu-id="982b3-103">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="982b3-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="982b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="982b3-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="982b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="982b3-105">DESCRIPTION</span></span>
<span data-ttu-id="982b3-106">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="982b3-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="982b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="982b3-107">EXAMPLES</span></span>

### <span data-ttu-id="982b3-108">Exempel 1: initiera Project-FileFolder</span><span class="sxs-lookup"><span data-stu-id="982b3-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="982b3-109">Initiera förbereder en resurs för användning och anger den till ett standard tillstånd</span><span class="sxs-lookup"><span data-stu-id="982b3-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="982b3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="982b3-110">PARAMETERS</span></span>

### <span data-ttu-id="982b3-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="982b3-111">-CodeDir</span></span>
<span data-ttu-id="982b3-112">Namnet på robot resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="982b3-112">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982b3-113">-DefaultProfile</span></span>
<span data-ttu-id="982b3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="982b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982b3-115">-Språk</span><span class="sxs-lookup"><span data-stu-id="982b3-115">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982b3-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="982b3-116">-ProjFileName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982b3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="982b3-117">-SubscriptionId</span></span>
<span data-ttu-id="982b3-118">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="982b3-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982b3-119">CommonParameters</span></span>
<span data-ttu-id="982b3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="982b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982b3-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="982b3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982b3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="982b3-122">INPUTS</span></span>

## <span data-ttu-id="982b3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="982b3-123">OUTPUTS</span></span>

### <span data-ttu-id="982b3-124">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="982b3-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="982b3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="982b3-125">NOTES</span></span>

<span data-ttu-id="982b3-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="982b3-126">ALIASES</span></span>

## <span data-ttu-id="982b3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="982b3-127">RELATED LINKS</span></span>

