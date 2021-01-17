---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415971"
---
# <span data-ttu-id="263c2-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="263c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="263c2-102">SYNOPSIS</span></span>
<span data-ttu-id="263c2-103">Uppdaterar en CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="263c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="263c2-104">SYNTAX</span></span>

### <span data-ttu-id="263c2-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="263c2-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="263c2-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="263c2-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="263c2-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="263c2-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="263c2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="263c2-108">DESCRIPTION</span></span>
<span data-ttu-id="263c2-109">Med cmdleten **Update-AzCustomIpPrefix** kan användaren antingen provision eller prosig deras CustomIpPrefix eller redigera taggarna för resursen.</span><span class="sxs-lookup"><span data-stu-id="263c2-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="263c2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="263c2-110">EXAMPLES</span></span>

### <span data-ttu-id="263c2-111">Exempel 1: provision The CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="263c2-112">Kommandot ovan kommer att inleda CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="263c2-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="263c2-113">Exempel 2: avprovision CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="263c2-114">Med kommandot ovan kommer den första processen för CustomIpPrefix att starta.</span><span class="sxs-lookup"><span data-stu-id="263c2-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="263c2-115">Exempel 3: uppdatera taggar för CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="263c2-116">Kommandot ovan uppdaterar taggarna för CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="263c2-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="263c2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="263c2-117">PARAMETERS</span></span>

### <span data-ttu-id="263c2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="263c2-118">-AsJob</span></span>
<span data-ttu-id="263c2-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="263c2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="263c2-120">-Provision</span><span class="sxs-lookup"><span data-stu-id="263c2-120">-Commission</span></span>
<span data-ttu-id="263c2-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="263c2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="263c2-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="263c2-122">-Decomission</span></span>
<span data-ttu-id="263c2-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="263c2-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="263c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263c2-124">-DefaultProfile</span></span>
<span data-ttu-id="263c2-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="263c2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="263c2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="263c2-126">-InputObject</span></span>
<span data-ttu-id="263c2-127">CustomIpPrefix ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="263c2-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="263c2-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="263c2-128">-Name</span></span>
<span data-ttu-id="263c2-129">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="263c2-129">The resource name.</span></span>

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

### <span data-ttu-id="263c2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263c2-130">-ResourceGroupName</span></span>
<span data-ttu-id="263c2-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="263c2-131">The resource group name.</span></span>

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

### <span data-ttu-id="263c2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="263c2-132">-ResourceId</span></span>
<span data-ttu-id="263c2-133">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="263c2-133">The resource Id.</span></span>

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

### <span data-ttu-id="263c2-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="263c2-134">-Tag</span></span>
<span data-ttu-id="263c2-135">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="263c2-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="263c2-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="263c2-136">-Confirm</span></span>
<span data-ttu-id="263c2-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="263c2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="263c2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="263c2-138">-WhatIf</span></span>
<span data-ttu-id="263c2-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="263c2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="263c2-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="263c2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="263c2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263c2-141">CommonParameters</span></span>
<span data-ttu-id="263c2-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263c2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263c2-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="263c2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263c2-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="263c2-144">INPUTS</span></span>

### <span data-ttu-id="263c2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="263c2-145">System.String</span></span>

### <span data-ttu-id="263c2-146">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="263c2-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="263c2-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="263c2-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="263c2-148">OUTPUTS</span></span>

### <span data-ttu-id="263c2-149">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="263c2-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="263c2-150">NOTES</span></span>

## <span data-ttu-id="263c2-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="263c2-151">RELATED LINKS</span></span>

[<span data-ttu-id="263c2-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="263c2-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="263c2-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="263c2-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)