---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 5b88342a91f015cd58da36f9b04d3a8a325ae239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574161"
---
# <span data-ttu-id="94461-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="94461-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="94461-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94461-102">SYNOPSIS</span></span>
<span data-ttu-id="94461-103">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="94461-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94461-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94461-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94461-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94461-105">DESCRIPTION</span></span>
<span data-ttu-id="94461-106">Använd **Update-AzureRmServiceFabricReliability** för att uppdatera tillförlitligheten för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="94461-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="94461-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94461-107">EXAMPLES</span></span>

### <span data-ttu-id="94461-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="94461-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="94461-109">Det här kommandot ändrar Tillförlitlighets nivån för den primära nodtypen till silver.</span><span class="sxs-lookup"><span data-stu-id="94461-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="94461-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94461-110">PARAMETERS</span></span>

### <span data-ttu-id="94461-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="94461-111">-AutoAddNode</span></span>
<span data-ttu-id="94461-112">Lägg till antal regioner automatiskt när du ändrar pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="94461-112">Add node count automatically when changing reliability.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94461-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94461-113">-DefaultProfile</span></span>
<span data-ttu-id="94461-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94461-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94461-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="94461-115">-Name</span></span>
<span data-ttu-id="94461-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="94461-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="94461-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="94461-117">-ReliabilityLevel</span></span>
<span data-ttu-id="94461-118">Tillförlitlighets nivå.</span><span class="sxs-lookup"><span data-stu-id="94461-118">Reliability tier.</span></span>

```yaml
Type: ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94461-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94461-119">-ResourceGroupName</span></span>
<span data-ttu-id="94461-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="94461-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="94461-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94461-121">-Confirm</span></span>
<span data-ttu-id="94461-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94461-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94461-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94461-123">-WhatIf</span></span>
<span data-ttu-id="94461-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94461-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94461-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94461-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94461-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94461-126">CommonParameters</span></span>
<span data-ttu-id="94461-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94461-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94461-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94461-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94461-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94461-129">INPUTS</span></span>

### <span data-ttu-id="94461-130">Microsoft. Azure. commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="94461-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="94461-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94461-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="94461-132">System. String</span><span class="sxs-lookup"><span data-stu-id="94461-132">System.String</span></span>

## <span data-ttu-id="94461-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94461-133">OUTPUTS</span></span>

### <span data-ttu-id="94461-134">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="94461-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="94461-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94461-135">NOTES</span></span>

## <span data-ttu-id="94461-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94461-136">RELATED LINKS</span></span>

