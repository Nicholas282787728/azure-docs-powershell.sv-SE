---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424864"
---
# <span data-ttu-id="c2f27-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c2f27-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="c2f27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2f27-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f27-103">Ta bort ett registrerat prefix från den överordnade peering-resursen.</span><span class="sxs-lookup"><span data-stu-id="c2f27-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="c2f27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2f27-104">SYNTAX</span></span>

### <span data-ttu-id="c2f27-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="c2f27-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2f27-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f27-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f27-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2f27-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f27-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2f27-108">DESCRIPTION</span></span>
<span data-ttu-id="c2f27-109">Tillåter borttagning av registrerat prefix från överordnad peering-resurs.</span><span class="sxs-lookup"><span data-stu-id="c2f27-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="c2f27-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2f27-110">EXAMPLES</span></span>

### <span data-ttu-id="c2f27-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2f27-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="c2f27-112">Ta bort ett registrerat prefix efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c2f27-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="c2f27-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2f27-113">PARAMETERS</span></span>

### <span data-ttu-id="c2f27-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2f27-114">-AsJob</span></span>
<span data-ttu-id="c2f27-115">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="c2f27-115">Run in the background.</span></span>

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

### <span data-ttu-id="c2f27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f27-116">-DefaultProfile</span></span>
<span data-ttu-id="c2f27-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f27-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f27-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c2f27-118">-Force</span></span>
<span data-ttu-id="c2f27-119">Tvinga åtgärden att slutföra</span><span class="sxs-lookup"><span data-stu-id="c2f27-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="c2f27-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f27-120">-InputObject</span></span>
<span data-ttu-id="c2f27-121">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c2f27-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f27-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2f27-122">-Name</span></span>
<span data-ttu-id="c2f27-123">Prefixets namn.</span><span class="sxs-lookup"><span data-stu-id="c2f27-123">The name of prefix.</span></span>

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

### <span data-ttu-id="c2f27-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2f27-124">-PassThru</span></span>
<span data-ttu-id="c2f27-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c2f27-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c2f27-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="c2f27-126">-PeeringName</span></span>
<span data-ttu-id="c2f27-127">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c2f27-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f27-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f27-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2f27-129">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="c2f27-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c2f27-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2f27-130">-ResourceId</span></span>
<span data-ttu-id="c2f27-131">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c2f27-131">The resource id string name.</span></span>

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

### <span data-ttu-id="c2f27-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2f27-132">-Confirm</span></span>
<span data-ttu-id="c2f27-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2f27-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f27-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f27-134">-WhatIf</span></span>
<span data-ttu-id="c2f27-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2f27-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f27-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2f27-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f27-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f27-137">CommonParameters</span></span>
<span data-ttu-id="c2f27-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f27-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f27-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2f27-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f27-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2f27-140">INPUTS</span></span>

### <span data-ttu-id="c2f27-141">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c2f27-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="c2f27-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c2f27-142">System.String</span></span>

## <span data-ttu-id="c2f27-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2f27-143">OUTPUTS</span></span>

### <span data-ttu-id="c2f27-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2f27-144">System.Boolean</span></span>

## <span data-ttu-id="c2f27-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2f27-145">NOTES</span></span>

## <span data-ttu-id="c2f27-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2f27-146">RELATED LINKS</span></span>
