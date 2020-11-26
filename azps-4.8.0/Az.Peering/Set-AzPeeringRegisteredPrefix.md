---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260658"
---
# <span data-ttu-id="887ad-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="887ad-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="887ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="887ad-102">SYNOPSIS</span></span>
<span data-ttu-id="887ad-103">Anger eller uppdaterar ett registrerat prefix från den överordnade peering-resursen.</span><span class="sxs-lookup"><span data-stu-id="887ad-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="887ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="887ad-104">SYNTAX</span></span>

### <span data-ttu-id="887ad-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="887ad-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887ad-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="887ad-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887ad-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="887ad-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887ad-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="887ad-108">DESCRIPTION</span></span>
<span data-ttu-id="887ad-109">Gör det möjligt att uppdatera ett registrerat prefix från överordnad peering-resurs.</span><span class="sxs-lookup"><span data-stu-id="887ad-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="887ad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="887ad-110">EXAMPLES</span></span>

### <span data-ttu-id="887ad-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="887ad-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="887ad-112">Uppdaterar prefixet efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="887ad-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="887ad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="887ad-113">PARAMETERS</span></span>

### <span data-ttu-id="887ad-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="887ad-114">-AsJob</span></span>
<span data-ttu-id="887ad-115">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="887ad-115">Run in the background.</span></span>

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

### <span data-ttu-id="887ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887ad-116">-DefaultProfile</span></span>
<span data-ttu-id="887ad-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="887ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="887ad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="887ad-118">-InputObject</span></span>
<span data-ttu-id="887ad-119">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="887ad-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="887ad-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="887ad-120">-Name</span></span>
<span data-ttu-id="887ad-121">Prefixets namn.</span><span class="sxs-lookup"><span data-stu-id="887ad-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ad-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="887ad-122">-PeeringName</span></span>
<span data-ttu-id="887ad-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="887ad-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ad-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="887ad-124">-Prefix</span></span>
<span data-ttu-id="887ad-125">Prefix för session IPv4</span><span class="sxs-lookup"><span data-stu-id="887ad-125">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="887ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="887ad-127">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="887ad-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ad-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="887ad-128">-ResourceId</span></span>
<span data-ttu-id="887ad-129">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="887ad-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887ad-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="887ad-130">-Confirm</span></span>
<span data-ttu-id="887ad-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="887ad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887ad-132">-WhatIf</span></span>
<span data-ttu-id="887ad-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="887ad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="887ad-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="887ad-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="887ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887ad-135">CommonParameters</span></span>
<span data-ttu-id="887ad-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887ad-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="887ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887ad-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="887ad-138">INPUTS</span></span>

### <span data-ttu-id="887ad-139">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="887ad-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="887ad-140">System. String</span><span class="sxs-lookup"><span data-stu-id="887ad-140">System.String</span></span>

## <span data-ttu-id="887ad-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="887ad-141">OUTPUTS</span></span>

### <span data-ttu-id="887ad-142">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="887ad-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="887ad-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="887ad-143">NOTES</span></span>

## <span data-ttu-id="887ad-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="887ad-144">RELATED LINKS</span></span>