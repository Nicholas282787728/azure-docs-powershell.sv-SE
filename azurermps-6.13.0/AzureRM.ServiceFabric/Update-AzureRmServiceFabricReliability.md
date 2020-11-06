---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 15dfc29703e2d331920a1751bcd6671e77d84171
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577872"
---
# <span data-ttu-id="fa511-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="fa511-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="fa511-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa511-102">SYNOPSIS</span></span>
<span data-ttu-id="fa511-103">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fa511-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa511-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa511-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa511-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa511-105">DESCRIPTION</span></span>
<span data-ttu-id="fa511-106">Använd **Update-AzureRmServiceFabricReliability** för att uppdatera tillförlitligheten för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fa511-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="fa511-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa511-107">EXAMPLES</span></span>

### <span data-ttu-id="fa511-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa511-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="fa511-109">Det här kommandot ändrar Tillförlitlighets nivån för den primära nodtypen till silver.</span><span class="sxs-lookup"><span data-stu-id="fa511-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="fa511-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa511-110">PARAMETERS</span></span>

### <span data-ttu-id="fa511-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="fa511-111">-AutoAddNode</span></span>
<span data-ttu-id="fa511-112">Lägg till antal regioner automatiskt när du ändrar pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="fa511-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="fa511-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa511-113">-DefaultProfile</span></span>
<span data-ttu-id="fa511-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa511-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa511-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa511-115">-Name</span></span>
<span data-ttu-id="fa511-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="fa511-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fa511-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="fa511-117">-ReliabilityLevel</span></span>
<span data-ttu-id="fa511-118">Tillförlitlighets nivå.</span><span class="sxs-lookup"><span data-stu-id="fa511-118">Reliability tier.</span></span>

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

### <span data-ttu-id="fa511-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa511-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa511-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fa511-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fa511-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa511-121">-Confirm</span></span>
<span data-ttu-id="fa511-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa511-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa511-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa511-123">-WhatIf</span></span>
<span data-ttu-id="fa511-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa511-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa511-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa511-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa511-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa511-126">CommonParameters</span></span>
<span data-ttu-id="fa511-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa511-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa511-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa511-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa511-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa511-129">INPUTS</span></span>

### <span data-ttu-id="fa511-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fa511-130">System.String</span></span>

### <span data-ttu-id="fa511-131">Microsoft. Azure. commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="fa511-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="fa511-132">Parametrar: ReliabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa511-132">Parameters: ReliabilityLevel (ByValue)</span></span>

### <span data-ttu-id="fa511-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa511-133">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="fa511-134">Parametrar: AutoAddNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa511-134">Parameters: AutoAddNode (ByValue)</span></span>

## <span data-ttu-id="fa511-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa511-135">OUTPUTS</span></span>

### <span data-ttu-id="fa511-136">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fa511-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fa511-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa511-137">NOTES</span></span>

## <span data-ttu-id="fa511-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa511-138">RELATED LINKS</span></span>
