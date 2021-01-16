---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424875"
---
# <span data-ttu-id="1146f-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="1146f-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="1146f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1146f-102">SYNOPSIS</span></span>
<span data-ttu-id="1146f-103">Ta bort ett registrerat ASN från den överordnade peering-resursen.</span><span class="sxs-lookup"><span data-stu-id="1146f-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="1146f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1146f-104">SYNTAX</span></span>

### <span data-ttu-id="1146f-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1146f-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1146f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1146f-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1146f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1146f-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1146f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1146f-108">DESCRIPTION</span></span>
<span data-ttu-id="1146f-109">Tillåter borttagning av registrerade ASN från överordnad peering-resurs.</span><span class="sxs-lookup"><span data-stu-id="1146f-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="1146f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1146f-110">EXAMPLES</span></span>

### <span data-ttu-id="1146f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1146f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="1146f-112">Ta bort ett register-ID.</span><span class="sxs-lookup"><span data-stu-id="1146f-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="1146f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1146f-113">PARAMETERS</span></span>

### <span data-ttu-id="1146f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1146f-114">-AsJob</span></span>
<span data-ttu-id="1146f-115">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="1146f-115">Run in the background.</span></span>

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

### <span data-ttu-id="1146f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1146f-116">-DefaultProfile</span></span>
<span data-ttu-id="1146f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1146f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1146f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1146f-118">-Force</span></span>
<span data-ttu-id="1146f-119">Tvinga åtgärden att slutföra</span><span class="sxs-lookup"><span data-stu-id="1146f-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="1146f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1146f-120">-InputObject</span></span>
<span data-ttu-id="1146f-121">Använda en Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="1146f-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="1146f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1146f-122">-Name</span></span>
<span data-ttu-id="1146f-123">Namnet på det registrerade ASN</span><span class="sxs-lookup"><span data-stu-id="1146f-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="1146f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1146f-124">-PassThru</span></span>
<span data-ttu-id="1146f-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1146f-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1146f-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="1146f-126">-PeeringName</span></span>
<span data-ttu-id="1146f-127">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1146f-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1146f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1146f-128">-ResourceGroupName</span></span>
<span data-ttu-id="1146f-129">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="1146f-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1146f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1146f-130">-ResourceId</span></span>
<span data-ttu-id="1146f-131">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1146f-131">The resource id string name.</span></span>

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

### <span data-ttu-id="1146f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1146f-132">-Confirm</span></span>
<span data-ttu-id="1146f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1146f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1146f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1146f-134">-WhatIf</span></span>
<span data-ttu-id="1146f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1146f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1146f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1146f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1146f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1146f-137">CommonParameters</span></span>
<span data-ttu-id="1146f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1146f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1146f-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1146f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1146f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1146f-140">INPUTS</span></span>

### <span data-ttu-id="1146f-141">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="1146f-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="1146f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1146f-142">System.String</span></span>

## <span data-ttu-id="1146f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1146f-143">OUTPUTS</span></span>

### <span data-ttu-id="1146f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1146f-144">System.Boolean</span></span>

## <span data-ttu-id="1146f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1146f-145">NOTES</span></span>

## <span data-ttu-id="1146f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1146f-146">RELATED LINKS</span></span>
