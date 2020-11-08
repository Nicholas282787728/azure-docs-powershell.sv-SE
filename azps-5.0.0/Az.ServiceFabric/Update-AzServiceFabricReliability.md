---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: a63bcfe0f807f36ffae5c10e644322b1fb612325
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269078"
---
# <span data-ttu-id="2cf38-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2cf38-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="2cf38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cf38-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf38-103">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2cf38-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="2cf38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cf38-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cf38-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf38-106">Använd **Update-AzServiceFabricReliability** för att uppdatera tillförlitligheten för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="2cf38-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="2cf38-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cf38-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf38-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2cf38-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="2cf38-109">Det här kommandot ändrar Tillförlitlighets nivån för den primära nodtypen till silver.</span><span class="sxs-lookup"><span data-stu-id="2cf38-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="2cf38-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cf38-110">PARAMETERS</span></span>

### <span data-ttu-id="2cf38-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="2cf38-111">-AutoAddNode</span></span>
<span data-ttu-id="2cf38-112">Lägga till antal regioner automatiskt när du ändrar pålitlighet</span><span class="sxs-lookup"><span data-stu-id="2cf38-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf38-113">-DefaultProfile</span></span>
<span data-ttu-id="2cf38-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf38-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2cf38-115">-Name</span></span>
<span data-ttu-id="2cf38-116">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="2cf38-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="2cf38-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="2cf38-117">-ReliabilityLevel</span></span>
<span data-ttu-id="2cf38-118">Tillförlitlighets nivå</span><span class="sxs-lookup"><span data-stu-id="2cf38-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf38-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf38-119">-ResourceGroupName</span></span>
<span data-ttu-id="2cf38-120">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2cf38-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2cf38-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2cf38-121">-Confirm</span></span>
<span data-ttu-id="2cf38-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2cf38-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf38-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf38-123">-WhatIf</span></span>
<span data-ttu-id="2cf38-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2cf38-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf38-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2cf38-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf38-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf38-126">CommonParameters</span></span>
<span data-ttu-id="2cf38-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf38-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf38-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cf38-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf38-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cf38-129">INPUTS</span></span>

### <span data-ttu-id="2cf38-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf38-130">System.String</span></span>

### <span data-ttu-id="2cf38-131">Microsoft. Azure. commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="2cf38-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="2cf38-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cf38-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2cf38-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cf38-133">OUTPUTS</span></span>

### <span data-ttu-id="2cf38-134">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2cf38-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2cf38-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cf38-135">NOTES</span></span>

## <span data-ttu-id="2cf38-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cf38-136">RELATED LINKS</span></span>
