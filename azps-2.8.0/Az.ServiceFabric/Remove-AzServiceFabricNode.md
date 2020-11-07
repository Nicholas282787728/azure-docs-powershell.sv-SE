---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 10adef91eab42f49459ba6fb9ad9130b42d74e01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919156"
---
# <span data-ttu-id="0e7ba-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0e7ba-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="0e7ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7ba-103">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="0e7ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e7ba-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e7ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="0e7ba-106">Använd **Remove-AzServiceFabricNode** för att ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="0e7ba-107">Borttagningen fortsätter bara om den uppfyller kluster hälso måtten.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="0e7ba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e7ba-108">EXAMPLES</span></span>

### <span data-ttu-id="0e7ba-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e7ba-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="0e7ba-110">Det här kommandot tar bort två noder från NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="0e7ba-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e7ba-111">PARAMETERS</span></span>

### <span data-ttu-id="0e7ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7ba-112">-DefaultProfile</span></span>
<span data-ttu-id="0e7ba-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7ba-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e7ba-114">-Name</span></span>
<span data-ttu-id="0e7ba-115">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="0e7ba-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0e7ba-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0e7ba-116">-NodeType</span></span>
<span data-ttu-id="0e7ba-117">Namn på nodtyp</span><span class="sxs-lookup"><span data-stu-id="0e7ba-117">Node type name</span></span>

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

### <span data-ttu-id="0e7ba-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="0e7ba-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="0e7ba-119">Antalet noder att lägga till</span><span class="sxs-lookup"><span data-stu-id="0e7ba-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="0e7ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e7ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e7ba-121">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0e7ba-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e7ba-122">-Confirm</span></span>
<span data-ttu-id="0e7ba-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e7ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e7ba-124">-WhatIf</span></span>
<span data-ttu-id="0e7ba-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e7ba-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e7ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7ba-127">CommonParameters</span></span>
<span data-ttu-id="0e7ba-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e7ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7ba-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e7ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7ba-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e7ba-130">INPUTS</span></span>

### <span data-ttu-id="0e7ba-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0e7ba-131">System.Int32</span></span>

### <span data-ttu-id="0e7ba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0e7ba-132">System.String</span></span>

## <span data-ttu-id="0e7ba-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e7ba-133">OUTPUTS</span></span>

### <span data-ttu-id="0e7ba-134">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0e7ba-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0e7ba-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e7ba-135">NOTES</span></span>

## <span data-ttu-id="0e7ba-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e7ba-136">RELATED LINKS</span></span>

[<span data-ttu-id="0e7ba-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0e7ba-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
