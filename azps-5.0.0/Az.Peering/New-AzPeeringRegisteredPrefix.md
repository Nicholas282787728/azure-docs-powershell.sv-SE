---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270106"
---
# <span data-ttu-id="47b88-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="47b88-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="47b88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47b88-102">SYNOPSIS</span></span>
<span data-ttu-id="47b88-103">Skapa registrerade prefix för peering-objekt.</span><span class="sxs-lookup"><span data-stu-id="47b88-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="47b88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47b88-104">SYNTAX</span></span>

### <span data-ttu-id="47b88-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="47b88-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b88-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="47b88-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b88-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="47b88-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b88-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47b88-108">DESCRIPTION</span></span>
<span data-ttu-id="47b88-109">Skapa registrerade prefix för peering-objekt.</span><span class="sxs-lookup"><span data-stu-id="47b88-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="47b88-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47b88-110">EXAMPLES</span></span>

### <span data-ttu-id="47b88-111">Använda peering och skapa ett registrerat prefix</span><span class="sxs-lookup"><span data-stu-id="47b88-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="47b88-112">Skaffa den peering du vill lägga till ett registrerat prefix.</span><span class="sxs-lookup"><span data-stu-id="47b88-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="47b88-113">Överför sedan till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47b88-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="47b88-114">Använda peering resourceId för att skapa ett registrerat ASN</span><span class="sxs-lookup"><span data-stu-id="47b88-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="47b88-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47b88-115">PARAMETERS</span></span>

### <span data-ttu-id="47b88-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47b88-116">-AsJob</span></span>
<span data-ttu-id="47b88-117">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="47b88-117">Run in the background.</span></span>

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

### <span data-ttu-id="47b88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b88-118">-DefaultProfile</span></span>
<span data-ttu-id="47b88-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47b88-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b88-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b88-120">-InputObject</span></span>
<span data-ttu-id="47b88-121">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="47b88-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="47b88-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="47b88-122">-Name</span></span>
<span data-ttu-id="47b88-123">Prefixets namn.</span><span class="sxs-lookup"><span data-stu-id="47b88-123">The name of prefix.</span></span>

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

### <span data-ttu-id="47b88-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="47b88-124">-PeeringName</span></span>
<span data-ttu-id="47b88-125">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="47b88-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="47b88-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="47b88-126">-Prefix</span></span>
<span data-ttu-id="47b88-127">Prefix för session IPv4</span><span class="sxs-lookup"><span data-stu-id="47b88-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="47b88-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b88-128">-ResourceGroupName</span></span>
<span data-ttu-id="47b88-129">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="47b88-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="47b88-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47b88-130">-ResourceId</span></span>
<span data-ttu-id="47b88-131">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="47b88-131">The resource id string name.</span></span>

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

### <span data-ttu-id="47b88-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47b88-132">-Confirm</span></span>
<span data-ttu-id="47b88-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47b88-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b88-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b88-134">-WhatIf</span></span>
<span data-ttu-id="47b88-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47b88-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b88-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47b88-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b88-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b88-137">CommonParameters</span></span>
<span data-ttu-id="47b88-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b88-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b88-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b88-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b88-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47b88-140">INPUTS</span></span>

### <span data-ttu-id="47b88-141">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="47b88-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="47b88-142">System. String</span><span class="sxs-lookup"><span data-stu-id="47b88-142">System.String</span></span>

## <span data-ttu-id="47b88-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47b88-143">OUTPUTS</span></span>

### <span data-ttu-id="47b88-144">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="47b88-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="47b88-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47b88-145">NOTES</span></span>

## <span data-ttu-id="47b88-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47b88-146">RELATED LINKS</span></span>