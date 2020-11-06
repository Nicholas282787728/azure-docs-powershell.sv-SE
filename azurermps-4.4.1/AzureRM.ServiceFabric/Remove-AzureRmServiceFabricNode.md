---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575828"
---
# <span data-ttu-id="867a4-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="867a4-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="867a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="867a4-102">SYNOPSIS</span></span>
<span data-ttu-id="867a4-103">Ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="867a4-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="867a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="867a4-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="867a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="867a4-105">DESCRIPTION</span></span>
<span data-ttu-id="867a4-106">Använd **Remove-AzureRmServiceFabricNode** för att ta bort noder från en viss nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="867a4-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="867a4-107">Borttagningen fortsätter bara om den uppfyller kluster hälso måtten.</span><span class="sxs-lookup"><span data-stu-id="867a4-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="867a4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="867a4-108">EXAMPLES</span></span>

### <span data-ttu-id="867a4-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="867a4-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="867a4-110">Det här kommandot tar bort två noder från NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="867a4-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="867a4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="867a4-111">PARAMETERS</span></span>

### <span data-ttu-id="867a4-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="867a4-112">-Name</span></span>
<span data-ttu-id="867a4-113">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="867a4-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="867a4-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="867a4-114">-NodeType</span></span>
<span data-ttu-id="867a4-115">Namn på nodtyp.</span><span class="sxs-lookup"><span data-stu-id="867a4-115">Node type name.</span></span>

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

### <span data-ttu-id="867a4-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="867a4-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="867a4-117">Antalet noder som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="867a4-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="867a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="867a4-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="867a4-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="867a4-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="867a4-120">-Confirm</span></span>
<span data-ttu-id="867a4-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="867a4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867a4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867a4-122">-WhatIf</span></span>
<span data-ttu-id="867a4-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="867a4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="867a4-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="867a4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867a4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867a4-125">-DefaultProfile</span></span>
<span data-ttu-id="867a4-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="867a4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="867a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867a4-127">CommonParameters</span></span>
<span data-ttu-id="867a4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867a4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="867a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867a4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="867a4-130">INPUTS</span></span>

### <span data-ttu-id="867a4-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="867a4-131">System.Int32</span></span>
<span data-ttu-id="867a4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="867a4-132">System.String</span></span>

## <span data-ttu-id="867a4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="867a4-133">OUTPUTS</span></span>

### <span data-ttu-id="867a4-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="867a4-134">System.Object</span></span>

## <span data-ttu-id="867a4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="867a4-135">NOTES</span></span>

## <span data-ttu-id="867a4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="867a4-136">RELATED LINKS</span></span>

[<span data-ttu-id="867a4-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="867a4-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
