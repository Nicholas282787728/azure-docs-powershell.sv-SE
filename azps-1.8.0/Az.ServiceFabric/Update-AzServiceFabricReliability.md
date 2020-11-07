---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: b0630a1d7fee588716c4db493f9c5ead2003165c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746825"
---
# <span data-ttu-id="8abde-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="8abde-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="8abde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8abde-102">SYNOPSIS</span></span>
<span data-ttu-id="8abde-103">Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="8abde-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="8abde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8abde-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8abde-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8abde-105">DESCRIPTION</span></span>
<span data-ttu-id="8abde-106">Använd **Update-AzServiceFabricReliability** för att uppdatera tillförlitligheten för den primära nodtypen i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="8abde-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="8abde-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8abde-107">EXAMPLES</span></span>

### <span data-ttu-id="8abde-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8abde-108">Example 1</span></span>
```
PS c:> Add-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="8abde-109">Det här kommandot ändrar Tillförlitlighets nivån för den primära nodtypen till silver.</span><span class="sxs-lookup"><span data-stu-id="8abde-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="8abde-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8abde-110">PARAMETERS</span></span>

### <span data-ttu-id="8abde-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="8abde-111">-AutoAddNode</span></span>
<span data-ttu-id="8abde-112">Lägg till antal regioner automatiskt när du ändrar pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="8abde-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="8abde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8abde-113">-DefaultProfile</span></span>
<span data-ttu-id="8abde-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8abde-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8abde-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8abde-115">-Name</span></span>
<span data-ttu-id="8abde-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="8abde-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8abde-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="8abde-117">-ReliabilityLevel</span></span>
<span data-ttu-id="8abde-118">Tillförlitlighets nivå.</span><span class="sxs-lookup"><span data-stu-id="8abde-118">Reliability tier.</span></span>

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

### <span data-ttu-id="8abde-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8abde-119">-ResourceGroupName</span></span>
<span data-ttu-id="8abde-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8abde-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8abde-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8abde-121">-Confirm</span></span>
<span data-ttu-id="8abde-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8abde-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8abde-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8abde-123">-WhatIf</span></span>
<span data-ttu-id="8abde-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8abde-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8abde-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8abde-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8abde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abde-126">CommonParameters</span></span>
<span data-ttu-id="8abde-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8abde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abde-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8abde-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abde-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8abde-129">INPUTS</span></span>

### <span data-ttu-id="8abde-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8abde-130">System.String</span></span>

### <span data-ttu-id="8abde-131">Microsoft. Azure. commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="8abde-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="8abde-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8abde-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8abde-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8abde-133">OUTPUTS</span></span>

### <span data-ttu-id="8abde-134">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="8abde-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8abde-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8abde-135">NOTES</span></span>

## <span data-ttu-id="8abde-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8abde-136">RELATED LINKS</span></span>
