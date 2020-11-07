---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: fdcc8946070994cd172514f8da1578328ae61db2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919174"
---
# <span data-ttu-id="7bdf0-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7bdf0-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="7bdf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdf0-103">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="7bdf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bdf0-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bdf0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bdf0-105">DESCRIPTION</span></span>
<span data-ttu-id="7bdf0-106">Använd **Add-AzServiceFabricNode** för att lägga till noder till den specifika nodtypen.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="7bdf0-107">Du behöver bara ange antalet noder som du vill lägga till i en nodtyp.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="7bdf0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bdf0-108">EXAMPLES</span></span>

### <span data-ttu-id="7bdf0-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7bdf0-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="7bdf0-110">Det här kommandot lägger till 2 noder till nodtypen ' N1 '.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="7bdf0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bdf0-111">PARAMETERS</span></span>

### <span data-ttu-id="7bdf0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdf0-112">-DefaultProfile</span></span>
<span data-ttu-id="7bdf0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bdf0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bdf0-114">-Name</span></span>
<span data-ttu-id="7bdf0-115">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="7bdf0-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="7bdf0-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7bdf0-116">-NodeType</span></span>
<span data-ttu-id="7bdf0-117">Namn på nodtyp</span><span class="sxs-lookup"><span data-stu-id="7bdf0-117">Node type name</span></span>

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

### <span data-ttu-id="7bdf0-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="7bdf0-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="7bdf0-119">Antalet noder att lägga till</span><span class="sxs-lookup"><span data-stu-id="7bdf0-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="7bdf0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bdf0-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bdf0-121">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7bdf0-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bdf0-122">-Confirm</span></span>
<span data-ttu-id="7bdf0-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bdf0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bdf0-124">-WhatIf</span></span>
<span data-ttu-id="7bdf0-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bdf0-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bdf0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdf0-127">CommonParameters</span></span>
<span data-ttu-id="7bdf0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bdf0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdf0-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bdf0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdf0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bdf0-130">INPUTS</span></span>

### <span data-ttu-id="7bdf0-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7bdf0-131">System.Int32</span></span>

### <span data-ttu-id="7bdf0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7bdf0-132">System.String</span></span>

## <span data-ttu-id="7bdf0-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bdf0-133">OUTPUTS</span></span>

### <span data-ttu-id="7bdf0-134">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7bdf0-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7bdf0-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bdf0-135">NOTES</span></span>

## <span data-ttu-id="7bdf0-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bdf0-136">RELATED LINKS</span></span>

[<span data-ttu-id="7bdf0-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7bdf0-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
