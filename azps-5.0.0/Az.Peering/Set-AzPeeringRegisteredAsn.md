---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324558"
---
# <span data-ttu-id="bf75d-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="bf75d-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="bf75d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf75d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf75d-103">Anger eller uppdaterar ett registrerat ASN från den överordnade peering-resursen.</span><span class="sxs-lookup"><span data-stu-id="bf75d-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="bf75d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf75d-104">SYNTAX</span></span>

### <span data-ttu-id="bf75d-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="bf75d-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf75d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bf75d-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf75d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf75d-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf75d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf75d-108">DESCRIPTION</span></span>
<span data-ttu-id="bf75d-109">Gör det möjligt att uppdatera ett registrerat ASN från en överordnad peering-resurs.</span><span class="sxs-lookup"><span data-stu-id="bf75d-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="bf75d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf75d-110">EXAMPLES</span></span>

### <span data-ttu-id="bf75d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf75d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="bf75d-112">Uppdaterar ASN efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bf75d-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="bf75d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf75d-113">PARAMETERS</span></span>

### <span data-ttu-id="bf75d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf75d-114">-AsJob</span></span>
<span data-ttu-id="bf75d-115">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="bf75d-115">Run in the background.</span></span>

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

### <span data-ttu-id="bf75d-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="bf75d-116">-Asn</span></span>
<span data-ttu-id="bf75d-117">ASN som ska registreras</span><span class="sxs-lookup"><span data-stu-id="bf75d-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="bf75d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf75d-118">-DefaultProfile</span></span>
<span data-ttu-id="bf75d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf75d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf75d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf75d-120">-InputObject</span></span>
<span data-ttu-id="bf75d-121">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="bf75d-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="bf75d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf75d-122">-Name</span></span>
<span data-ttu-id="bf75d-123">ASN som ska registreras</span><span class="sxs-lookup"><span data-stu-id="bf75d-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="bf75d-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="bf75d-124">-PeeringName</span></span>
<span data-ttu-id="bf75d-125">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="bf75d-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="bf75d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf75d-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf75d-127">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="bf75d-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="bf75d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf75d-128">-ResourceId</span></span>
<span data-ttu-id="bf75d-129">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bf75d-129">The resource id string name.</span></span>

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

### <span data-ttu-id="bf75d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf75d-130">-Confirm</span></span>
<span data-ttu-id="bf75d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf75d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf75d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf75d-132">-WhatIf</span></span>
<span data-ttu-id="bf75d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf75d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf75d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf75d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf75d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf75d-135">CommonParameters</span></span>
<span data-ttu-id="bf75d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf75d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf75d-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf75d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf75d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf75d-138">INPUTS</span></span>

### <span data-ttu-id="bf75d-139">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="bf75d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="bf75d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf75d-140">System.String</span></span>

## <span data-ttu-id="bf75d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf75d-141">OUTPUTS</span></span>

### <span data-ttu-id="bf75d-142">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="bf75d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="bf75d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf75d-143">NOTES</span></span>

## <span data-ttu-id="bf75d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf75d-144">RELATED LINKS</span></span>
