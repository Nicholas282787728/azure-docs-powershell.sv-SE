---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 9673c236886feb801d6e4078bfccbf82e2339811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576092"
---
# <span data-ttu-id="b8308-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b8308-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="b8308-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8308-102">SYNOPSIS</span></span>
<span data-ttu-id="b8308-103">Inaktiverar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="b8308-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8308-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8308-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8308-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8308-105">DESCRIPTION</span></span>
<span data-ttu-id="b8308-106">Cmdleten **disable-AzureRmSchedulerJobCollection** inaktiverar en jobb samling i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b8308-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="b8308-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8308-107">EXAMPLES</span></span>

## <span data-ttu-id="b8308-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8308-108">PARAMETERS</span></span>

### <span data-ttu-id="b8308-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8308-109">-DefaultProfile</span></span>
<span data-ttu-id="b8308-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8308-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8308-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b8308-111">-JobCollectionName</span></span>
<span data-ttu-id="b8308-112">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="b8308-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="b8308-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8308-113">-PassThru</span></span>
<span data-ttu-id="b8308-114">Anger att denna cmdlet returnerar ett lyckat resultat.</span><span class="sxs-lookup"><span data-stu-id="b8308-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="b8308-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b8308-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b8308-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8308-116">-ResourceGroupName</span></span>
<span data-ttu-id="b8308-117">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="b8308-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="b8308-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8308-118">-Confirm</span></span>
<span data-ttu-id="b8308-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8308-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8308-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8308-120">-WhatIf</span></span>
<span data-ttu-id="b8308-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8308-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8308-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8308-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8308-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8308-123">CommonParameters</span></span>
<span data-ttu-id="b8308-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8308-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8308-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8308-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8308-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8308-126">INPUTS</span></span>

### <span data-ttu-id="b8308-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b8308-127">System.String</span></span>

## <span data-ttu-id="b8308-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8308-128">OUTPUTS</span></span>

### <span data-ttu-id="b8308-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8308-129">System.String</span></span>

## <span data-ttu-id="b8308-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8308-130">NOTES</span></span>

## <span data-ttu-id="b8308-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8308-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8308-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b8308-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b8308-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b8308-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b8308-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b8308-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b8308-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b8308-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b8308-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b8308-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

