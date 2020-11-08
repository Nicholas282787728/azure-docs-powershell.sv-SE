---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "94093113"
---
# <span data-ttu-id="e619f-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e619f-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="e619f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e619f-102">SYNOPSIS</span></span>


## <span data-ttu-id="e619f-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e619f-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e619f-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e619f-104">DESCRIPTION</span></span>


## <span data-ttu-id="e619f-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e619f-105">EXAMPLES</span></span>

### <span data-ttu-id="e619f-106">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="e619f-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="e619f-107">Ta bort ett borttaget lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e619f-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="e619f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e619f-108">PARAMETERS</span></span>

### <span data-ttu-id="e619f-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e619f-109">-AsJob</span></span>


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

### <span data-ttu-id="e619f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e619f-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="e619f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e619f-111">-Force</span></span>


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

### <span data-ttu-id="e619f-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="e619f-112">-Location</span></span>


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

### <span data-ttu-id="e619f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e619f-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e619f-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="e619f-114">-NewAccountName</span></span>


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

### <span data-ttu-id="e619f-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e619f-115">-NoWait</span></span>


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

### <span data-ttu-id="e619f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e619f-116">-PassThru</span></span>


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

### <span data-ttu-id="e619f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e619f-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="e619f-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e619f-118">-Confirm</span></span>
<span data-ttu-id="e619f-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e619f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e619f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e619f-120">-WhatIf</span></span>
<span data-ttu-id="e619f-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e619f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e619f-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e619f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e619f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e619f-123">CommonParameters</span></span>
<span data-ttu-id="e619f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e619f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e619f-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e619f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e619f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e619f-126">INPUTS</span></span>

## <span data-ttu-id="e619f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e619f-127">OUTPUTS</span></span>

### <span data-ttu-id="e619f-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e619f-128">System.Boolean</span></span>



## <span data-ttu-id="e619f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e619f-129">NOTES</span></span>

## <span data-ttu-id="e619f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e619f-130">RELATED LINKS</span></span>

