---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: aca27be11fde78df8abad1d7cdcfeff4232b60d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756845"
---
# <span data-ttu-id="11655-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="11655-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="11655-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11655-102">SYNOPSIS</span></span>
<span data-ttu-id="11655-103">Lägga till noder till den specifika nodtypen i klustret.</span><span class="sxs-lookup"><span data-stu-id="11655-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11655-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11655-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToAdd <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11655-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11655-105">DESCRIPTION</span></span>
<span data-ttu-id="11655-106">Använd **Add-AzureRmServiceFabricNode** för att lägga till noder till den specifika nodtypen.</span><span class="sxs-lookup"><span data-stu-id="11655-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="11655-107">Du behöver bara ange antalet noder som du vill lägga till i en nodtyp.</span><span class="sxs-lookup"><span data-stu-id="11655-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="11655-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11655-108">EXAMPLES</span></span>

### <span data-ttu-id="11655-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11655-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="11655-110">Det här kommandot lägger till 2 noder till nodtypen ' N1 '.</span><span class="sxs-lookup"><span data-stu-id="11655-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="11655-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11655-111">PARAMETERS</span></span>

### <span data-ttu-id="11655-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="11655-112">-Name</span></span>
<span data-ttu-id="11655-113">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="11655-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="11655-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="11655-114">-NodeType</span></span>
<span data-ttu-id="11655-115">Namn på nodtyp.</span><span class="sxs-lookup"><span data-stu-id="11655-115">Node type name.</span></span>

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

### <span data-ttu-id="11655-116">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="11655-116">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="11655-117">VM-instansnamn.</span><span class="sxs-lookup"><span data-stu-id="11655-117">VM instance number.</span></span>

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

### <span data-ttu-id="11655-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11655-118">-ResourceGroupName</span></span>
<span data-ttu-id="11655-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="11655-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="11655-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11655-120">-Confirm</span></span>
<span data-ttu-id="11655-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11655-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11655-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11655-122">-WhatIf</span></span>
<span data-ttu-id="11655-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11655-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11655-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11655-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11655-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11655-125">-DefaultProfile</span></span>
<span data-ttu-id="11655-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11655-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11655-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11655-127">CommonParameters</span></span>
<span data-ttu-id="11655-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11655-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11655-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11655-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11655-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11655-130">INPUTS</span></span>

### <span data-ttu-id="11655-131">System. String</span><span class="sxs-lookup"><span data-stu-id="11655-131">System.String</span></span>

## <span data-ttu-id="11655-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11655-132">OUTPUTS</span></span>

### <span data-ttu-id="11655-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="11655-133">System.Object</span></span>

## <span data-ttu-id="11655-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11655-134">NOTES</span></span>

## <span data-ttu-id="11655-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11655-135">RELATED LINKS</span></span>

[<span data-ttu-id="11655-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="11655-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
