---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521814"
---
# <span data-ttu-id="d1057-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="d1057-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1057-102">SYNOPSIS</span></span>
<span data-ttu-id="d1057-103">Uppdaterar en CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="d1057-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1057-104">SYNTAX</span></span>

### <span data-ttu-id="d1057-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1057-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1057-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1057-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1057-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1057-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1057-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1057-108">DESCRIPTION</span></span>
<span data-ttu-id="d1057-109">Med cmdleten **Update-AzCustomIpPrefix** kan användaren antingen provision eller prosig deras CustomIpPrefix eller redigera taggarna för resursen.</span><span class="sxs-lookup"><span data-stu-id="d1057-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="d1057-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1057-110">EXAMPLES</span></span>

### <span data-ttu-id="d1057-111">Exempel 1: provision The CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="d1057-112">Kommandot ovan kommer att inleda CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d1057-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="d1057-113">Exempel 2: avprovision CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="d1057-114">Med kommandot ovan kommer den första processen för CustomIpPrefix att starta.</span><span class="sxs-lookup"><span data-stu-id="d1057-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="d1057-115">Exempel 3: uppdatera taggar för CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="d1057-116">Kommandot ovan uppdaterar taggarna för CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d1057-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="d1057-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1057-117">PARAMETERS</span></span>

### <span data-ttu-id="d1057-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1057-118">-AsJob</span></span>
<span data-ttu-id="d1057-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d1057-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-120">-Provision</span><span class="sxs-lookup"><span data-stu-id="d1057-120">-Commission</span></span>
<span data-ttu-id="d1057-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d1057-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="d1057-122">-Decomission</span></span>
<span data-ttu-id="d1057-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d1057-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1057-124">-DefaultProfile</span></span>
<span data-ttu-id="d1057-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1057-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1057-126">-InputObject</span></span>
<span data-ttu-id="d1057-127">CustomIpPrefix ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="d1057-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1057-128">-Name</span></span>
<span data-ttu-id="d1057-129">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d1057-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1057-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1057-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d1057-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1057-132">-ResourceId</span></span>
<span data-ttu-id="d1057-133">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d1057-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d1057-134">-Tag</span></span>
<span data-ttu-id="d1057-135">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d1057-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1057-136">-Confirm</span></span>
<span data-ttu-id="d1057-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1057-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1057-138">-WhatIf</span></span>
<span data-ttu-id="d1057-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1057-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1057-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1057-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1057-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1057-141">CommonParameters</span></span>
<span data-ttu-id="d1057-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1057-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1057-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1057-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1057-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1057-144">INPUTS</span></span>

### <span data-ttu-id="d1057-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d1057-145">System.String</span></span>

### <span data-ttu-id="d1057-146">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="d1057-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d1057-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d1057-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1057-148">OUTPUTS</span></span>

### <span data-ttu-id="d1057-149">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="d1057-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1057-150">NOTES</span></span>

## <span data-ttu-id="d1057-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1057-151">RELATED LINKS</span></span>

[<span data-ttu-id="d1057-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="d1057-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="d1057-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d1057-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)