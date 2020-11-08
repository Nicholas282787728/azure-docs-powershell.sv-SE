---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 96706ef98a0b21bab06e2c6e8fae947dcd205271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089398"
---
# <span data-ttu-id="2540d-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2540d-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="2540d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2540d-102">SYNOPSIS</span></span>
<span data-ttu-id="2540d-103">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2540d-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="2540d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2540d-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2540d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2540d-105">DESCRIPTION</span></span>
<span data-ttu-id="2540d-106">Använd **Remove-AzServiceFabricNode** för att ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2540d-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="2540d-107">Borttagningen fortsätter bara om den uppfyller kluster hälso måtten.</span><span class="sxs-lookup"><span data-stu-id="2540d-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="2540d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2540d-108">EXAMPLES</span></span>

### <span data-ttu-id="2540d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2540d-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="2540d-110">Det här kommandot tar bort två noder från NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="2540d-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="2540d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2540d-111">PARAMETERS</span></span>

### <span data-ttu-id="2540d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2540d-112">-DefaultProfile</span></span>
<span data-ttu-id="2540d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2540d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2540d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2540d-114">-Name</span></span>
<span data-ttu-id="2540d-115">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="2540d-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="2540d-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2540d-116">-NodeType</span></span>
<span data-ttu-id="2540d-117">Namn på nodtyp</span><span class="sxs-lookup"><span data-stu-id="2540d-117">Node type name</span></span>

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

### <span data-ttu-id="2540d-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="2540d-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="2540d-119">Antalet noder att lägga till</span><span class="sxs-lookup"><span data-stu-id="2540d-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="2540d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2540d-120">-ResourceGroupName</span></span>
<span data-ttu-id="2540d-121">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2540d-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2540d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2540d-122">-Confirm</span></span>
<span data-ttu-id="2540d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2540d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2540d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2540d-124">-WhatIf</span></span>
<span data-ttu-id="2540d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2540d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2540d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2540d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2540d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2540d-127">CommonParameters</span></span>
<span data-ttu-id="2540d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2540d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2540d-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2540d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2540d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2540d-130">INPUTS</span></span>

### <span data-ttu-id="2540d-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2540d-131">System.Int32</span></span>

### <span data-ttu-id="2540d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2540d-132">System.String</span></span>

## <span data-ttu-id="2540d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2540d-133">OUTPUTS</span></span>

### <span data-ttu-id="2540d-134">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2540d-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2540d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2540d-135">NOTES</span></span>

## <span data-ttu-id="2540d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2540d-136">RELATED LINKS</span></span>

[<span data-ttu-id="2540d-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2540d-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
