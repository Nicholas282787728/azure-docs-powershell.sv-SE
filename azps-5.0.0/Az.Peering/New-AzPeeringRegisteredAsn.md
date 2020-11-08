---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270447"
---
# <span data-ttu-id="42393-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="42393-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="42393-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42393-102">SYNOPSIS</span></span>
<span data-ttu-id="42393-103">Skapa registrerade ASN för peering</span><span class="sxs-lookup"><span data-stu-id="42393-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="42393-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42393-104">SYNTAX</span></span>

### <span data-ttu-id="42393-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="42393-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42393-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="42393-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42393-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42393-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42393-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42393-108">DESCRIPTION</span></span>
<span data-ttu-id="42393-109">Skapa registrerade ASNs för peering-objekt.</span><span class="sxs-lookup"><span data-stu-id="42393-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="42393-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42393-110">EXAMPLES</span></span>

### <span data-ttu-id="42393-111">Bli peering and skapa ett registrerat ASN</span><span class="sxs-lookup"><span data-stu-id="42393-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="42393-112">Skaffa den peering du vill lägga till ett registrerat ASN.</span><span class="sxs-lookup"><span data-stu-id="42393-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="42393-113">Överför sedan till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42393-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="42393-114">Använda peering resourceId för att skapa ett registrerat ASN</span><span class="sxs-lookup"><span data-stu-id="42393-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="42393-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42393-115">PARAMETERS</span></span>

### <span data-ttu-id="42393-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42393-116">-AsJob</span></span>
<span data-ttu-id="42393-117">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="42393-117">Run in the background.</span></span>

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

### <span data-ttu-id="42393-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="42393-118">-Asn</span></span>
<span data-ttu-id="42393-119">ASN som ska registreras</span><span class="sxs-lookup"><span data-stu-id="42393-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="42393-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42393-120">-DefaultProfile</span></span>
<span data-ttu-id="42393-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42393-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42393-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42393-122">-InputObject</span></span>
<span data-ttu-id="42393-123">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="42393-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42393-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="42393-124">-Name</span></span>
<span data-ttu-id="42393-125">ASN som ska registreras</span><span class="sxs-lookup"><span data-stu-id="42393-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42393-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="42393-126">-PeeringName</span></span>
<span data-ttu-id="42393-127">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="42393-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="42393-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42393-128">-ResourceGroupName</span></span>
<span data-ttu-id="42393-129">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="42393-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="42393-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42393-130">-ResourceId</span></span>
<span data-ttu-id="42393-131">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="42393-131">The resource id string name.</span></span>

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

### <span data-ttu-id="42393-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42393-132">-Confirm</span></span>
<span data-ttu-id="42393-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42393-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42393-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42393-134">-WhatIf</span></span>
<span data-ttu-id="42393-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42393-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42393-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42393-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42393-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42393-137">CommonParameters</span></span>
<span data-ttu-id="42393-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42393-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42393-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42393-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42393-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42393-140">INPUTS</span></span>

### <span data-ttu-id="42393-141">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="42393-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="42393-142">System. String</span><span class="sxs-lookup"><span data-stu-id="42393-142">System.String</span></span>

## <span data-ttu-id="42393-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42393-143">OUTPUTS</span></span>

### <span data-ttu-id="42393-144">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="42393-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="42393-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42393-145">NOTES</span></span>

## <span data-ttu-id="42393-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42393-146">RELATED LINKS</span></span>
