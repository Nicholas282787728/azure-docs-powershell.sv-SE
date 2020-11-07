---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b4ff486bac10c79a544761c1946fd3e34dce69a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756776"
---
# <span data-ttu-id="b728a-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b728a-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="b728a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b728a-102">SYNOPSIS</span></span>
<span data-ttu-id="b728a-103">Tar bort en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="b728a-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b728a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b728a-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b728a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b728a-105">DESCRIPTION</span></span>
<span data-ttu-id="b728a-106">Cmdleten **Remove-AzureRmSchedulerJobCollection** tar bort en jobb samling i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b728a-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="b728a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b728a-107">EXAMPLES</span></span>

## <span data-ttu-id="b728a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b728a-108">PARAMETERS</span></span>

### <span data-ttu-id="b728a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b728a-109">-DefaultProfile</span></span>
<span data-ttu-id="b728a-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b728a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b728a-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b728a-111">-JobCollectionName</span></span>
<span data-ttu-id="b728a-112">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="b728a-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b728a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b728a-113">-PassThru</span></span>
<span data-ttu-id="b728a-114">Anger att denna cmdlet returnerar ett lyckat resultat.</span><span class="sxs-lookup"><span data-stu-id="b728a-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="b728a-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b728a-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b728a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b728a-116">-ResourceGroupName</span></span>
<span data-ttu-id="b728a-117">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="b728a-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b728a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b728a-118">-Confirm</span></span>
<span data-ttu-id="b728a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b728a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b728a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b728a-120">-WhatIf</span></span>
<span data-ttu-id="b728a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b728a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b728a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b728a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b728a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b728a-123">CommonParameters</span></span>
<span data-ttu-id="b728a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b728a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b728a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b728a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b728a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b728a-126">INPUTS</span></span>

### <span data-ttu-id="b728a-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="b728a-127">None</span></span>
<span data-ttu-id="b728a-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b728a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b728a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b728a-129">OUTPUTS</span></span>

## <span data-ttu-id="b728a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b728a-130">NOTES</span></span>

## <span data-ttu-id="b728a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b728a-131">RELATED LINKS</span></span>

[<span data-ttu-id="b728a-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b728a-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b728a-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b728a-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b728a-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b728a-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b728a-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b728a-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b728a-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b728a-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


