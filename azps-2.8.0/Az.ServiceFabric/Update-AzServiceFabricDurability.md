---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 283ca228ba44d2ec87cd926d23e0217eb67434eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919148"
---
# <span data-ttu-id="11e17-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="11e17-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="11e17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11e17-102">SYNOPSIS</span></span>
<span data-ttu-id="11e17-103">Uppdatera livs längden eller VmSku för en nodtyp i klustret.</span><span class="sxs-lookup"><span data-stu-id="11e17-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="11e17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11e17-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e17-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11e17-105">DESCRIPTION</span></span>
<span data-ttu-id="11e17-106">Använd **Update-AzServiceFabricDurability** för att uppdatera hållbarhet eller SKU för klustret.</span><span class="sxs-lookup"><span data-stu-id="11e17-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="11e17-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11e17-107">EXAMPLES</span></span>

### <span data-ttu-id="11e17-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11e17-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="11e17-109">Det här kommandot ändrar tåligheten för NodeType ' NT1 ' till silver.</span><span class="sxs-lookup"><span data-stu-id="11e17-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="11e17-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11e17-110">PARAMETERS</span></span>

### <span data-ttu-id="11e17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e17-111">-DefaultProfile</span></span>
<span data-ttu-id="11e17-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11e17-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e17-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="11e17-113">-DurabilityLevel</span></span>
<span data-ttu-id="11e17-114">Ange hållbarheten.</span><span class="sxs-lookup"><span data-stu-id="11e17-114">Specify durability level.</span></span>

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

### <span data-ttu-id="11e17-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="11e17-115">-Name</span></span>
<span data-ttu-id="11e17-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="11e17-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="11e17-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="11e17-117">-NodeType</span></span>
<span data-ttu-id="11e17-118">Ange namnet på tjänst strukturens nodtyp.</span><span class="sxs-lookup"><span data-stu-id="11e17-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="11e17-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e17-119">-ResourceGroupName</span></span>
<span data-ttu-id="11e17-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="11e17-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="11e17-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="11e17-121">-Sku</span></span>
<span data-ttu-id="11e17-122">Ange typen SKU för nodtypen.</span><span class="sxs-lookup"><span data-stu-id="11e17-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="11e17-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11e17-123">-Confirm</span></span>
<span data-ttu-id="11e17-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11e17-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e17-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e17-125">-WhatIf</span></span>
<span data-ttu-id="11e17-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11e17-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11e17-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11e17-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e17-128">CommonParameters</span></span>
<span data-ttu-id="11e17-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e17-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e17-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e17-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11e17-131">INPUTS</span></span>

### <span data-ttu-id="11e17-132">System. String</span><span class="sxs-lookup"><span data-stu-id="11e17-132">System.String</span></span>

### <span data-ttu-id="11e17-133">Microsoft. Azure. commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="11e17-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="11e17-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11e17-134">OUTPUTS</span></span>

### <span data-ttu-id="11e17-135">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="11e17-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="11e17-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11e17-136">NOTES</span></span>

## <span data-ttu-id="11e17-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11e17-137">RELATED LINKS</span></span>
