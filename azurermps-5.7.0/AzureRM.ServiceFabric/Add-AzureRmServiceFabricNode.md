---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: af8f5d38777674d761b8b55c649b048c933f2c66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576412"
---
# <span data-ttu-id="6734d-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6734d-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="6734d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6734d-102">SYNOPSIS</span></span>
<span data-ttu-id="6734d-103">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="6734d-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6734d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6734d-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6734d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6734d-105">DESCRIPTION</span></span>
<span data-ttu-id="6734d-106">Använd **Add-AzureRmServiceFabricNode** för att lägga till noder till den specifika nodtypen.</span><span class="sxs-lookup"><span data-stu-id="6734d-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="6734d-107">Du behöver bara ange antalet noder som du vill lägga till i en nodtyp.</span><span class="sxs-lookup"><span data-stu-id="6734d-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="6734d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6734d-108">EXAMPLES</span></span>

### <span data-ttu-id="6734d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6734d-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="6734d-110">Det här kommandot lägger till 2 noder till nodtypen ' N1 '.</span><span class="sxs-lookup"><span data-stu-id="6734d-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="6734d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6734d-111">PARAMETERS</span></span>

### <span data-ttu-id="6734d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6734d-112">-DefaultProfile</span></span>
<span data-ttu-id="6734d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6734d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6734d-114">-Name</span></span>
<span data-ttu-id="6734d-115">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="6734d-115">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6734d-116">-NodeType</span></span>
<span data-ttu-id="6734d-117">Namn på nodtyp.</span><span class="sxs-lookup"><span data-stu-id="6734d-117">Node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="6734d-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="6734d-119">VM-instansnamn.</span><span class="sxs-lookup"><span data-stu-id="6734d-119">VM instance number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6734d-120">-ResourceGroupName</span></span>
<span data-ttu-id="6734d-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6734d-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6734d-122">-Confirm</span></span>
<span data-ttu-id="6734d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6734d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6734d-124">-WhatIf</span></span>
<span data-ttu-id="6734d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6734d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6734d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6734d-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6734d-127">CommonParameters</span></span>
<span data-ttu-id="6734d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6734d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6734d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6734d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6734d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6734d-130">INPUTS</span></span>

### <span data-ttu-id="6734d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6734d-131">System.String</span></span>

## <span data-ttu-id="6734d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6734d-132">OUTPUTS</span></span>

### <span data-ttu-id="6734d-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="6734d-133">System.Object</span></span>

## <span data-ttu-id="6734d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6734d-134">NOTES</span></span>

## <span data-ttu-id="6734d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6734d-135">RELATED LINKS</span></span>

[<span data-ttu-id="6734d-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6734d-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
