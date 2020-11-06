---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 56a6afff6551ae0191ac1f17d3a52c47940e045a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577871"
---
# <span data-ttu-id="731a8-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="731a8-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="731a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="731a8-102">SYNOPSIS</span></span>
<span data-ttu-id="731a8-103">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="731a8-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="731a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="731a8-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="731a8-105">DESCRIPTION</span></span>
<span data-ttu-id="731a8-106">Använd **Update-AzureRmServiceFabricDurability** för att uppdatera hållbarhet eller SKU för klustret.</span><span class="sxs-lookup"><span data-stu-id="731a8-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="731a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="731a8-107">EXAMPLES</span></span>

### <span data-ttu-id="731a8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="731a8-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="731a8-109">Det här kommandot ändrar tåligheten för NodeType ' NT1 ' till silver.</span><span class="sxs-lookup"><span data-stu-id="731a8-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="731a8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="731a8-110">PARAMETERS</span></span>

### <span data-ttu-id="731a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731a8-111">-DefaultProfile</span></span>
<span data-ttu-id="731a8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="731a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="731a8-113">-DurabilityLevel</span></span>
<span data-ttu-id="731a8-114">Ange hållbarheten.</span><span class="sxs-lookup"><span data-stu-id="731a8-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="731a8-115">-Name</span></span>
<span data-ttu-id="731a8-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="731a8-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="731a8-117">-NodeType</span></span>
<span data-ttu-id="731a8-118">Ange namnet på tjänst strukturens nodtyp.</span><span class="sxs-lookup"><span data-stu-id="731a8-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="731a8-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="731a8-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="731a8-121">-Sku</span></span>
<span data-ttu-id="731a8-122">Ange typen SKU för nodtypen.</span><span class="sxs-lookup"><span data-stu-id="731a8-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="731a8-123">-Confirm</span></span>
<span data-ttu-id="731a8-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="731a8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731a8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731a8-125">-WhatIf</span></span>
<span data-ttu-id="731a8-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="731a8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="731a8-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="731a8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731a8-128">CommonParameters</span></span>
<span data-ttu-id="731a8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731a8-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731a8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731a8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="731a8-131">INPUTS</span></span>

### <span data-ttu-id="731a8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="731a8-132">System.String</span></span>
<span data-ttu-id="731a8-133">Parametrar: NodeType (ByValue), SKU (ByValue)</span><span class="sxs-lookup"><span data-stu-id="731a8-133">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="731a8-134">Microsoft. Azure. commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="731a8-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="731a8-135">Parametrar: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="731a8-135">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="731a8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="731a8-136">OUTPUTS</span></span>

### <span data-ttu-id="731a8-137">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="731a8-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="731a8-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="731a8-138">NOTES</span></span>

## <span data-ttu-id="731a8-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="731a8-139">RELATED LINKS</span></span>
