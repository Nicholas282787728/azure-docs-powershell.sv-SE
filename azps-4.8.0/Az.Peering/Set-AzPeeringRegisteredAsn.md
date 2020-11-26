---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262445"
---
# <span data-ttu-id="63fda-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="63fda-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="63fda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63fda-102">SYNOPSIS</span></span>
<span data-ttu-id="63fda-103">Anger eller uppdaterar ett registrerat ASN från den överordnade peering-resursen.</span><span class="sxs-lookup"><span data-stu-id="63fda-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="63fda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63fda-104">SYNTAX</span></span>

### <span data-ttu-id="63fda-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="63fda-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fda-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="63fda-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fda-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63fda-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fda-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63fda-108">DESCRIPTION</span></span>
<span data-ttu-id="63fda-109">Gör det möjligt att uppdatera ett registrerat ASN från en överordnad peering-resurs.</span><span class="sxs-lookup"><span data-stu-id="63fda-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="63fda-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63fda-110">EXAMPLES</span></span>

### <span data-ttu-id="63fda-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63fda-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="63fda-112">Uppdaterar ASN efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="63fda-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="63fda-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63fda-113">PARAMETERS</span></span>

### <span data-ttu-id="63fda-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63fda-114">-AsJob</span></span>
<span data-ttu-id="63fda-115">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="63fda-115">Run in the background.</span></span>

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

### <span data-ttu-id="63fda-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="63fda-116">-Asn</span></span>
<span data-ttu-id="63fda-117">ASN som ska registreras</span><span class="sxs-lookup"><span data-stu-id="63fda-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fda-118">-DefaultProfile</span></span>
<span data-ttu-id="63fda-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63fda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63fda-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63fda-120">-InputObject</span></span>
<span data-ttu-id="63fda-121">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="63fda-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63fda-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="63fda-122">-Name</span></span>
<span data-ttu-id="63fda-123">ASN som ska registreras</span><span class="sxs-lookup"><span data-stu-id="63fda-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="63fda-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="63fda-124">-PeeringName</span></span>
<span data-ttu-id="63fda-125">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="63fda-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="63fda-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fda-126">-ResourceGroupName</span></span>
<span data-ttu-id="63fda-127">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="63fda-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="63fda-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63fda-128">-ResourceId</span></span>
<span data-ttu-id="63fda-129">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="63fda-129">The resource id string name.</span></span>

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

### <span data-ttu-id="63fda-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63fda-130">-Confirm</span></span>
<span data-ttu-id="63fda-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63fda-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fda-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fda-132">-WhatIf</span></span>
<span data-ttu-id="63fda-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63fda-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63fda-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63fda-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fda-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fda-135">CommonParameters</span></span>
<span data-ttu-id="63fda-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fda-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fda-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63fda-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fda-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63fda-138">INPUTS</span></span>

### <span data-ttu-id="63fda-139">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="63fda-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="63fda-140">System. String</span><span class="sxs-lookup"><span data-stu-id="63fda-140">System.String</span></span>

## <span data-ttu-id="63fda-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63fda-141">OUTPUTS</span></span>

### <span data-ttu-id="63fda-142">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="63fda-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="63fda-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63fda-143">NOTES</span></span>

## <span data-ttu-id="63fda-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63fda-144">RELATED LINKS</span></span>