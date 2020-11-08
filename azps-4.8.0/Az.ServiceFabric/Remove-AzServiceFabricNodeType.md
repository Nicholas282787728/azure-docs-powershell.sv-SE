---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259104"
---
# <span data-ttu-id="fc0af-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fc0af-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="fc0af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc0af-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0af-103">Ta bort en fullständig nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fc0af-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="fc0af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc0af-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc0af-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0af-106">Använd **Remove-AzServiceFabricNodeType** för att ta bort alla noder från en viss nodtyp och nodtypen från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fc0af-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="fc0af-107">Det går inte att använda det här kommandot för att ta bort typen primär nodtyp.</span><span class="sxs-lookup"><span data-stu-id="fc0af-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="fc0af-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc0af-108">EXAMPLES</span></span>

### <span data-ttu-id="fc0af-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc0af-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="fc0af-110">Det här kommandot tar bort NodeType ' NT1 ' från klustret.</span><span class="sxs-lookup"><span data-stu-id="fc0af-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="fc0af-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc0af-111">PARAMETERS</span></span>

### <span data-ttu-id="fc0af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0af-112">-DefaultProfile</span></span>
<span data-ttu-id="fc0af-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0af-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc0af-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc0af-114">-Name</span></span>
<span data-ttu-id="fc0af-115">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="fc0af-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fc0af-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="fc0af-116">-NodeType</span></span>
<span data-ttu-id="fc0af-117">Namnet på nodtypen</span><span class="sxs-lookup"><span data-stu-id="fc0af-117">The node type name</span></span>

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

### <span data-ttu-id="fc0af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0af-118">-ResourceGroupName</span></span>
<span data-ttu-id="fc0af-119">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fc0af-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fc0af-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc0af-120">-Confirm</span></span>
<span data-ttu-id="fc0af-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc0af-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0af-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0af-122">-WhatIf</span></span>
<span data-ttu-id="fc0af-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc0af-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc0af-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc0af-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0af-125">CommonParameters</span></span>
<span data-ttu-id="fc0af-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0af-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc0af-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0af-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc0af-128">INPUTS</span></span>

### <span data-ttu-id="fc0af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fc0af-129">System.String</span></span>

## <span data-ttu-id="fc0af-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc0af-130">OUTPUTS</span></span>

### <span data-ttu-id="fc0af-131">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fc0af-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fc0af-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc0af-132">NOTES</span></span>

## <span data-ttu-id="fc0af-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc0af-133">RELATED LINKS</span></span>
