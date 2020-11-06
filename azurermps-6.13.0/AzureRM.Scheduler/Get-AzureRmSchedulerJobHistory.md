---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 5bf5745270db8cea076ccac9cff2d4e9b7a4bc06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583947"
---
# <span data-ttu-id="69119-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="69119-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="69119-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69119-102">SYNOPSIS</span></span>
<span data-ttu-id="69119-103">Hämtar jobb historiken.</span><span class="sxs-lookup"><span data-stu-id="69119-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69119-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69119-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69119-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69119-105">DESCRIPTION</span></span>
<span data-ttu-id="69119-106">Cmdleten **Get-AzureRmSchedulerJobHistory** hämtar historik för ett Azure Scheduler-jobb.</span><span class="sxs-lookup"><span data-stu-id="69119-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="69119-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69119-107">EXAMPLES</span></span>

## <span data-ttu-id="69119-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69119-108">PARAMETERS</span></span>

### <span data-ttu-id="69119-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69119-109">-DefaultProfile</span></span>
<span data-ttu-id="69119-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69119-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69119-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="69119-111">-JobCollectionName</span></span>
<span data-ttu-id="69119-112">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="69119-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="69119-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="69119-113">-JobExecutionStatus</span></span>
<span data-ttu-id="69119-114">Anger statusen för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="69119-114">Specifies the status of a job.</span></span>
<span data-ttu-id="69119-115">Denna cmdlet får historik som matchar den status som du anger.</span><span class="sxs-lookup"><span data-stu-id="69119-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="69119-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="69119-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69119-117">Rätta</span><span class="sxs-lookup"><span data-stu-id="69119-117">Completed</span></span> 
- <span data-ttu-id="69119-118">Startade</span><span class="sxs-lookup"><span data-stu-id="69119-118">Failed</span></span> 
- <span data-ttu-id="69119-119">Sköts</span><span class="sxs-lookup"><span data-stu-id="69119-119">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69119-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="69119-120">-JobName</span></span>
<span data-ttu-id="69119-121">Anger namnet på ett jobb som denna cmdlet hämtar historik för.</span><span class="sxs-lookup"><span data-stu-id="69119-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="69119-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69119-122">-ResourceGroupName</span></span>
<span data-ttu-id="69119-123">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="69119-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="69119-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69119-124">CommonParameters</span></span>
<span data-ttu-id="69119-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69119-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69119-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69119-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69119-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69119-127">INPUTS</span></span>

### <span data-ttu-id="69119-128">System. String</span><span class="sxs-lookup"><span data-stu-id="69119-128">System.String</span></span>

## <span data-ttu-id="69119-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69119-129">OUTPUTS</span></span>

### <span data-ttu-id="69119-130">Microsoft. Azure. commands. Scheduler. Models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="69119-130">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="69119-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69119-131">NOTES</span></span>

## <span data-ttu-id="69119-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69119-132">RELATED LINKS</span></span>

[<span data-ttu-id="69119-133">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="69119-133">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


