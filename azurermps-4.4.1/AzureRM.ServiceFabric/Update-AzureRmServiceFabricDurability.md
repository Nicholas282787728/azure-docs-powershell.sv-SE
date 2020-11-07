---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 1c62c637324f19088dfffcfb4c8defae0a056b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575822"
---
# <span data-ttu-id="4de89-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="4de89-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="4de89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4de89-102">SYNOPSIS</span></span>
<span data-ttu-id="4de89-103">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="4de89-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4de89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4de89-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de89-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4de89-105">DESCRIPTION</span></span>
<span data-ttu-id="4de89-106">Använd **Update-AzureRmServiceFabricDurability** för att uppdatera hållbarhet eller SKU för klustret.</span><span class="sxs-lookup"><span data-stu-id="4de89-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="4de89-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4de89-107">EXAMPLES</span></span>

### <span data-ttu-id="4de89-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4de89-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="4de89-109">Det här kommandot ändrar tåligheten för NodeType ' NT1 ' till silver.</span><span class="sxs-lookup"><span data-stu-id="4de89-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="4de89-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4de89-110">PARAMETERS</span></span>

### <span data-ttu-id="4de89-111">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="4de89-111">-DurabilityLevel</span></span>
<span data-ttu-id="4de89-112">Ange hållbarheten.</span><span class="sxs-lookup"><span data-stu-id="4de89-112">Specify durability level.</span></span>

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

### <span data-ttu-id="4de89-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4de89-113">-Name</span></span>
<span data-ttu-id="4de89-114">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="4de89-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4de89-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4de89-115">-NodeType</span></span>
<span data-ttu-id="4de89-116">Ange namnet på tjänst strukturens nodtyp.</span><span class="sxs-lookup"><span data-stu-id="4de89-116">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="4de89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de89-117">-ResourceGroupName</span></span>
<span data-ttu-id="4de89-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4de89-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4de89-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="4de89-119">-Sku</span></span>
<span data-ttu-id="4de89-120">Ange typen SKU för nodtypen.</span><span class="sxs-lookup"><span data-stu-id="4de89-120">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="4de89-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4de89-121">-Confirm</span></span>
<span data-ttu-id="4de89-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4de89-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de89-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de89-123">-WhatIf</span></span>
<span data-ttu-id="4de89-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4de89-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4de89-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4de89-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de89-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de89-126">-DefaultProfile</span></span>
<span data-ttu-id="4de89-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4de89-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de89-128">CommonParameters</span></span>
<span data-ttu-id="4de89-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de89-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de89-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de89-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4de89-131">INPUTS</span></span>

### <span data-ttu-id="4de89-132">Microsoft. Azure. commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="4de89-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="4de89-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4de89-133">System.String</span></span>

## <span data-ttu-id="4de89-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4de89-134">OUTPUTS</span></span>

### <span data-ttu-id="4de89-135">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="4de89-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="4de89-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4de89-136">NOTES</span></span>

## <span data-ttu-id="4de89-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4de89-137">RELATED LINKS</span></span>
