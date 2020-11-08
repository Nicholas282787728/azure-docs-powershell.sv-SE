---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262074"
---
# <span data-ttu-id="ce15e-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce15e-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="ce15e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce15e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce15e-103">Tar bort en CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce15e-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="ce15e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce15e-104">SYNTAX</span></span>

### <span data-ttu-id="ce15e-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ce15e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce15e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce15e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce15e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce15e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce15e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce15e-108">DESCRIPTION</span></span>
<span data-ttu-id="ce15e-109">Cmdleten **Remove-AzCustomIpPrefix** tar bort en CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="ce15e-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="ce15e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce15e-110">EXAMPLES</span></span>

### <span data-ttu-id="ce15e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce15e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="ce15e-112">Tar bort CustomIpPrefix med namnet $prefixName från resurs gruppen $rgName</span><span class="sxs-lookup"><span data-stu-id="ce15e-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="ce15e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce15e-113">PARAMETERS</span></span>

### <span data-ttu-id="ce15e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce15e-114">-AsJob</span></span>
<span data-ttu-id="ce15e-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ce15e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce15e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce15e-116">-DefaultProfile</span></span>
<span data-ttu-id="ce15e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce15e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce15e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce15e-118">-Force</span></span>
<span data-ttu-id="ce15e-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ce15e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ce15e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce15e-120">-InputObject</span></span>
<span data-ttu-id="ce15e-121">Ett customIpPrefix-objekt.</span><span class="sxs-lookup"><span data-stu-id="ce15e-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce15e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce15e-122">-Name</span></span>
<span data-ttu-id="ce15e-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ce15e-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce15e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce15e-124">-PassThru</span></span>
<span data-ttu-id="ce15e-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ce15e-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce15e-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ce15e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce15e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce15e-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce15e-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ce15e-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce15e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce15e-129">-ResourceId</span></span>
<span data-ttu-id="ce15e-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ce15e-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce15e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce15e-131">-Confirm</span></span>
<span data-ttu-id="ce15e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce15e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce15e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce15e-133">-WhatIf</span></span>
<span data-ttu-id="ce15e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce15e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce15e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce15e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce15e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce15e-136">CommonParameters</span></span>
<span data-ttu-id="ce15e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce15e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce15e-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce15e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce15e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce15e-139">INPUTS</span></span>

### <span data-ttu-id="ce15e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ce15e-140">System.String</span></span>

### <span data-ttu-id="ce15e-141">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce15e-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="ce15e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce15e-142">OUTPUTS</span></span>

### <span data-ttu-id="ce15e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce15e-143">System.Boolean</span></span>

## <span data-ttu-id="ce15e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce15e-144">NOTES</span></span>

## <span data-ttu-id="ce15e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce15e-145">RELATED LINKS</span></span>

[<span data-ttu-id="ce15e-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce15e-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="ce15e-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce15e-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="ce15e-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce15e-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)