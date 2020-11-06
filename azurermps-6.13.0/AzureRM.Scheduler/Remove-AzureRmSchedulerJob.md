---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 6a15f51290efec856494737881693c3d1fae0620
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575094"
---
# <span data-ttu-id="9d3a4-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="9d3a4-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="9d3a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3a4-103">Tar bort ett jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d3a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d3a4-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d3a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d3a4-105">DESCRIPTION</span></span>
<span data-ttu-id="9d3a4-106">Cmdleten **Remove-AzureRmSchedulerJob** tar bort ett Azure Scheduler-jobb.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="9d3a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d3a4-107">EXAMPLES</span></span>

## <span data-ttu-id="9d3a4-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d3a4-108">PARAMETERS</span></span>

### <span data-ttu-id="9d3a4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3a4-109">-DefaultProfile</span></span>
<span data-ttu-id="9d3a4-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d3a4-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9d3a4-111">-JobCollectionName</span></span>
<span data-ttu-id="9d3a4-112">Anger namnet på en jobb samling som innehåller jobbet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-112">Specifies the name of a job collection that contains the job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3a4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="9d3a4-113">-JobName</span></span>
<span data-ttu-id="9d3a4-114">Anger namnet på det jobb som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-114">Specifies the name of a job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3a4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d3a4-115">-PassThru</span></span>
<span data-ttu-id="9d3a4-116">Anger att denna cmdlet returnerar ett lyckat resultat.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="9d3a4-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d3a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="9d3a4-119">Anger resurs gruppen för jobbet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-119">Specifies the resource group of the job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3a4-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d3a4-120">-Confirm</span></span>
<span data-ttu-id="9d3a4-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3a4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d3a4-122">-WhatIf</span></span>
<span data-ttu-id="9d3a4-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d3a4-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3a4-125">CommonParameters</span></span>
<span data-ttu-id="9d3a4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d3a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3a4-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d3a4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3a4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d3a4-128">INPUTS</span></span>

### <span data-ttu-id="9d3a4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9d3a4-129">System.String</span></span>

## <span data-ttu-id="9d3a4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d3a4-130">OUTPUTS</span></span>

### <span data-ttu-id="9d3a4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9d3a4-131">System.String</span></span>

## <span data-ttu-id="9d3a4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d3a4-132">NOTES</span></span>

## <span data-ttu-id="9d3a4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d3a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d3a4-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="9d3a4-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


