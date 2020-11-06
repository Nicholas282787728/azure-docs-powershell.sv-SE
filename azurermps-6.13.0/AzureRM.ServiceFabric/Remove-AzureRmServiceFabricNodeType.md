---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 36cad62f67be4273d363277e52f4dc8d2c91373c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583476"
---
# <span data-ttu-id="1b5b6-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1b5b6-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="1b5b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5b6-103">Ta bort en fullständig nodtyp från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b5b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b5b6-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b5b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="1b5b6-106">Använd **Remove-AzureRmServiceFabricNodeType** för att ta bort alla noder från en viss nodtyp och nodtypen från ett kluster.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="1b5b6-107">Det går inte att använda det här kommandot för att ta bort typen primär nodtyp.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="1b5b6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b5b6-108">EXAMPLES</span></span>

### <span data-ttu-id="1b5b6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b5b6-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="1b5b6-110">Det här kommandot tar bort NodeType ' NT1 ' från klustret.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="1b5b6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b5b6-111">PARAMETERS</span></span>

### <span data-ttu-id="1b5b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5b6-112">-DefaultProfile</span></span>
<span data-ttu-id="1b5b6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b5b6-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b5b6-114">-Name</span></span>
<span data-ttu-id="1b5b6-115">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1b5b6-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1b5b6-116">-NodeType</span></span>
<span data-ttu-id="1b5b6-117">Namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-117">The node type name.</span></span>

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

### <span data-ttu-id="1b5b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b5b6-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1b5b6-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b5b6-120">-Confirm</span></span>
<span data-ttu-id="1b5b6-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b5b6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b5b6-122">-WhatIf</span></span>
<span data-ttu-id="1b5b6-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b5b6-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b5b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5b6-125">CommonParameters</span></span>
<span data-ttu-id="1b5b6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b5b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5b6-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b5b6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5b6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b5b6-128">INPUTS</span></span>

### <span data-ttu-id="1b5b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1b5b6-129">System.String</span></span>
<span data-ttu-id="1b5b6-130">Parametrar: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b5b6-130">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="1b5b6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b5b6-131">OUTPUTS</span></span>

### <span data-ttu-id="1b5b6-132">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1b5b6-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1b5b6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b5b6-133">NOTES</span></span>

## <span data-ttu-id="1b5b6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b5b6-134">RELATED LINKS</span></span>
