---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757561"
---
# <span data-ttu-id="189c1-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="189c1-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="189c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="189c1-102">SYNOPSIS</span></span>
<span data-ttu-id="189c1-103">Tar bort ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="189c1-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="189c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="189c1-104">SYNTAX</span></span>

### <span data-ttu-id="189c1-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="189c1-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="189c1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="189c1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="189c1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="189c1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="189c1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="189c1-108">DESCRIPTION</span></span>
<span data-ttu-id="189c1-109">Med \* \* Remove-AzureRmPublicIpPrefix cmdlet tas ett prefix för Azure Public IP bort så länge det inte finns några offentliga IP-adresser tilldelade till sig.</span><span class="sxs-lookup"><span data-stu-id="189c1-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="189c1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="189c1-110">EXAMPLES</span></span>

### <span data-ttu-id="189c1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="189c1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="189c1-112">Tar bort det offentliga IP-prefixet med namnet $prefixName från resurs gruppen $rgName</span><span class="sxs-lookup"><span data-stu-id="189c1-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="189c1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="189c1-113">PARAMETERS</span></span>

### <span data-ttu-id="189c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="189c1-114">-AsJob</span></span>
<span data-ttu-id="189c1-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="189c1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="189c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189c1-116">-DefaultProfile</span></span>
<span data-ttu-id="189c1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="189c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189c1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="189c1-118">-Force</span></span>
<span data-ttu-id="189c1-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="189c1-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="189c1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="189c1-120">-InputObject</span></span>
<span data-ttu-id="189c1-121">Ett PublicIpPrefix-objekt</span><span class="sxs-lookup"><span data-stu-id="189c1-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="189c1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="189c1-122">-Name</span></span>
<span data-ttu-id="189c1-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="189c1-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="189c1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="189c1-124">-PassThru</span></span>
<span data-ttu-id="189c1-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="189c1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="189c1-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="189c1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="189c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="189c1-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="189c1-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="189c1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="189c1-129">-ResourceId</span></span>
<span data-ttu-id="189c1-130">ResourceId för resursen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="189c1-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="189c1-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="189c1-131">-Confirm</span></span>
<span data-ttu-id="189c1-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="189c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189c1-133">-WhatIf</span></span>
<span data-ttu-id="189c1-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="189c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189c1-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="189c1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189c1-136">CommonParameters</span></span>
<span data-ttu-id="189c1-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="189c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="189c1-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="189c1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189c1-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="189c1-139">INPUTS</span></span>

### <span data-ttu-id="189c1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="189c1-140">System.String</span></span>
<span data-ttu-id="189c1-141">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="189c1-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="189c1-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="189c1-142">OUTPUTS</span></span>

### <span data-ttu-id="189c1-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="189c1-143">System.Object</span></span>

## <span data-ttu-id="189c1-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="189c1-144">NOTES</span></span>

## <span data-ttu-id="189c1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="189c1-145">RELATED LINKS</span></span>
