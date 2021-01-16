---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396488"
---
# <span data-ttu-id="46fe8-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="46fe8-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="46fe8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="46fe8-103">Tar bort ett nytt peering service-prefix</span><span class="sxs-lookup"><span data-stu-id="46fe8-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="46fe8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46fe8-104">SYNTAX</span></span>

### <span data-ttu-id="46fe8-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="46fe8-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46fe8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="46fe8-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46fe8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46fe8-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46fe8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="46fe8-109">Tar bort ett peering service-prefix från en peering-tjänst.</span><span class="sxs-lookup"><span data-stu-id="46fe8-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="46fe8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46fe8-110">EXAMPLES</span></span>

### <span data-ttu-id="46fe8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46fe8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="46fe8-112">Ta bort ett prefix från ett peering service-objekt</span><span class="sxs-lookup"><span data-stu-id="46fe8-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="46fe8-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="46fe8-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="46fe8-114">Ta bort ett prefix från ett resurs-ID för peering service.</span><span class="sxs-lookup"><span data-stu-id="46fe8-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="46fe8-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="46fe8-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="46fe8-116">Ta bort ett prefix från ett resurs grupp namn och namn för peering service</span><span class="sxs-lookup"><span data-stu-id="46fe8-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="46fe8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46fe8-117">PARAMETERS</span></span>

### <span data-ttu-id="46fe8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46fe8-118">-AsJob</span></span>
<span data-ttu-id="46fe8-119">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="46fe8-119">Run in the background.</span></span>

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

### <span data-ttu-id="46fe8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46fe8-120">-DefaultProfile</span></span>
<span data-ttu-id="46fe8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46fe8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46fe8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="46fe8-122">-Force</span></span>
<span data-ttu-id="46fe8-123">Tvinga åtgärden att slutföra</span><span class="sxs-lookup"><span data-stu-id="46fe8-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="46fe8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46fe8-124">-InputObject</span></span>
<span data-ttu-id="46fe8-125">Använda en Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="46fe8-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46fe8-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="46fe8-126">-Name</span></span>
<span data-ttu-id="46fe8-127">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="46fe8-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="46fe8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46fe8-128">-PassThru</span></span>
<span data-ttu-id="46fe8-129">Returnerar sant för lyckades eller falskt för misslyckad.</span><span class="sxs-lookup"><span data-stu-id="46fe8-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="46fe8-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="46fe8-130">-PrefixName</span></span>
<span data-ttu-id="46fe8-131">Prefixets namn.</span><span class="sxs-lookup"><span data-stu-id="46fe8-131">The name of prefix.</span></span>

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

### <span data-ttu-id="46fe8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46fe8-132">-ResourceGroupName</span></span>
<span data-ttu-id="46fe8-133">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="46fe8-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="46fe8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46fe8-134">-ResourceId</span></span>
<span data-ttu-id="46fe8-135">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="46fe8-135">The resource id string name.</span></span>

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

### <span data-ttu-id="46fe8-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46fe8-136">-Confirm</span></span>
<span data-ttu-id="46fe8-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46fe8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46fe8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46fe8-138">-WhatIf</span></span>
<span data-ttu-id="46fe8-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46fe8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46fe8-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46fe8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46fe8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fe8-141">CommonParameters</span></span>
<span data-ttu-id="46fe8-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46fe8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fe8-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46fe8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fe8-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46fe8-144">INPUTS</span></span>

### <span data-ttu-id="46fe8-145">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="46fe8-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="46fe8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="46fe8-146">System.String</span></span>

## <span data-ttu-id="46fe8-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46fe8-147">OUTPUTS</span></span>

### <span data-ttu-id="46fe8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46fe8-148">System.Boolean</span></span>

## <span data-ttu-id="46fe8-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46fe8-149">NOTES</span></span>

## <span data-ttu-id="46fe8-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46fe8-150">RELATED LINKS</span></span>
