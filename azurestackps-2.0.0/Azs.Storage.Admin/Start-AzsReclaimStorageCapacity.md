---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923074"
---
# <span data-ttu-id="7c5a6-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="7c5a6-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="7c5a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c5a6-102">SYNOPSIS</span></span>


## <span data-ttu-id="7c5a6-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c5a6-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c5a6-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c5a6-104">DESCRIPTION</span></span>


## <span data-ttu-id="7c5a6-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c5a6-105">EXAMPLES</span></span>

### <span data-ttu-id="7c5a6-106">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="7c5a6-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="7c5a6-107">Starta skräp insamling.</span><span class="sxs-lookup"><span data-stu-id="7c5a6-107">Start garbage collection.</span></span>

## <span data-ttu-id="7c5a6-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c5a6-108">PARAMETERS</span></span>

### <span data-ttu-id="7c5a6-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c5a6-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5a6-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="7c5a6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7c5a6-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c5a6-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-113">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7c5a6-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c5a6-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c5a6-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c5a6-116">-Confirm</span></span>
<span data-ttu-id="7c5a6-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c5a6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c5a6-118">-WhatIf</span></span>
<span data-ttu-id="7c5a6-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c5a6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c5a6-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c5a6-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c5a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5a6-121">CommonParameters</span></span>
<span data-ttu-id="7c5a6-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c5a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5a6-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c5a6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5a6-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c5a6-124">INPUTS</span></span>

## <span data-ttu-id="7c5a6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c5a6-125">OUTPUTS</span></span>

### <span data-ttu-id="7c5a6-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c5a6-126">System.Boolean</span></span>



## <span data-ttu-id="7c5a6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c5a6-127">NOTES</span></span>

## <span data-ttu-id="7c5a6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c5a6-128">RELATED LINKS</span></span>

