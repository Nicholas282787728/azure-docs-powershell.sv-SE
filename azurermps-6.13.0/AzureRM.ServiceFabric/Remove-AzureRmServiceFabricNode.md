---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583480"
---
# <span data-ttu-id="2eb58-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2eb58-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="2eb58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eb58-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb58-103">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2eb58-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eb58-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eb58-105">DESCRIPTION</span></span>
<span data-ttu-id="2eb58-106">Använd **Remove-AzureRmServiceFabricNode** för att ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2eb58-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="2eb58-107">Borttagningen fortsätter bara om den uppfyller kluster hälso måtten.</span><span class="sxs-lookup"><span data-stu-id="2eb58-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="2eb58-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eb58-108">EXAMPLES</span></span>

### <span data-ttu-id="2eb58-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2eb58-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="2eb58-110">Det här kommandot tar bort två noder från NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="2eb58-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="2eb58-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eb58-111">PARAMETERS</span></span>

### <span data-ttu-id="2eb58-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb58-112">-DefaultProfile</span></span>
<span data-ttu-id="2eb58-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb58-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eb58-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2eb58-114">-Name</span></span>
<span data-ttu-id="2eb58-115">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="2eb58-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2eb58-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2eb58-116">-NodeType</span></span>
<span data-ttu-id="2eb58-117">Namn på nodtyp.</span><span class="sxs-lookup"><span data-stu-id="2eb58-117">Node type name.</span></span>

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

### <span data-ttu-id="2eb58-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="2eb58-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="2eb58-119">Antalet noder som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2eb58-119">Number of nodes to remove.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb58-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb58-120">-ResourceGroupName</span></span>
<span data-ttu-id="2eb58-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2eb58-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2eb58-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2eb58-122">-Confirm</span></span>
<span data-ttu-id="2eb58-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2eb58-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb58-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb58-124">-WhatIf</span></span>
<span data-ttu-id="2eb58-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2eb58-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2eb58-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2eb58-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb58-127">CommonParameters</span></span>
<span data-ttu-id="2eb58-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb58-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb58-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb58-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eb58-130">INPUTS</span></span>

### <span data-ttu-id="2eb58-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2eb58-131">System.Int32</span></span>
<span data-ttu-id="2eb58-132">Parametrar: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2eb58-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="2eb58-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb58-133">System.String</span></span>
<span data-ttu-id="2eb58-134">Parametrar: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2eb58-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="2eb58-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eb58-135">OUTPUTS</span></span>

### <span data-ttu-id="2eb58-136">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2eb58-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2eb58-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eb58-137">NOTES</span></span>

## <span data-ttu-id="2eb58-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eb58-138">RELATED LINKS</span></span>

[<span data-ttu-id="2eb58-139">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2eb58-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
