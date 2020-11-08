---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262014"
---
# <span data-ttu-id="da12e-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="da12e-101">Remove-AzPeering</span></span>

## <span data-ttu-id="da12e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da12e-102">SYNOPSIS</span></span>
<span data-ttu-id="da12e-103">Ta bort en peering.</span><span class="sxs-lookup"><span data-stu-id="da12e-103">Delete or remove a peering.</span></span> <span data-ttu-id="da12e-104">Detta tar bort alla underordnade resurser eller aviseringar på resursen.</span><span class="sxs-lookup"><span data-stu-id="da12e-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="da12e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da12e-105">SYNTAX</span></span>

### <span data-ttu-id="da12e-106">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="da12e-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da12e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="da12e-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da12e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="da12e-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da12e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da12e-109">DESCRIPTION</span></span>
<span data-ttu-id="da12e-110">Perminently ta bort en peering-resurs.</span><span class="sxs-lookup"><span data-stu-id="da12e-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="da12e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da12e-111">EXAMPLES</span></span>

### <span data-ttu-id="da12e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="da12e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="da12e-113">Ta bort en peering efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="da12e-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="da12e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da12e-114">PARAMETERS</span></span>

### <span data-ttu-id="da12e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da12e-115">-AsJob</span></span>
<span data-ttu-id="da12e-116">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="da12e-116">Run in the background.</span></span>

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

### <span data-ttu-id="da12e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da12e-117">-DefaultProfile</span></span>
<span data-ttu-id="da12e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da12e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da12e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="da12e-119">-Force</span></span>
<span data-ttu-id="da12e-120">Tvinga åtgärden att slutföra</span><span class="sxs-lookup"><span data-stu-id="da12e-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="da12e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da12e-121">-InputObject</span></span>
<span data-ttu-id="da12e-122">Använd Get-AzPeering för att hämta det här objektet.</span><span class="sxs-lookup"><span data-stu-id="da12e-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da12e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="da12e-123">-Name</span></span>
<span data-ttu-id="da12e-124">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="da12e-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da12e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da12e-125">-PassThru</span></span>
<span data-ttu-id="da12e-126">Returnera True om den är klar</span><span class="sxs-lookup"><span data-stu-id="da12e-126">Return true if complete</span></span>

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

### <span data-ttu-id="da12e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da12e-127">-ResourceGroupName</span></span>
<span data-ttu-id="da12e-128">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="da12e-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da12e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da12e-129">-ResourceId</span></span>
<span data-ttu-id="da12e-130">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="da12e-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da12e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da12e-131">-Confirm</span></span>
<span data-ttu-id="da12e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da12e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da12e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da12e-133">-WhatIf</span></span>
<span data-ttu-id="da12e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da12e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da12e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da12e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da12e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da12e-136">CommonParameters</span></span>
<span data-ttu-id="da12e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da12e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da12e-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da12e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da12e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da12e-139">INPUTS</span></span>

### <span data-ttu-id="da12e-140">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="da12e-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="da12e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="da12e-141">System.String</span></span>

## <span data-ttu-id="da12e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da12e-142">OUTPUTS</span></span>

### <span data-ttu-id="da12e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da12e-143">System.Boolean</span></span>

## <span data-ttu-id="da12e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da12e-144">NOTES</span></span>

## <span data-ttu-id="da12e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da12e-145">RELATED LINKS</span></span>
