---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: c754b7e30fdec3a179beefdf48292a781ec083db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576416"
---
# <span data-ttu-id="70353-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70353-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="70353-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70353-102">SYNOPSIS</span></span>
<span data-ttu-id="70353-103">Inaktiverar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="70353-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70353-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70353-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70353-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70353-105">DESCRIPTION</span></span>
<span data-ttu-id="70353-106">Cmdleten **disable-AzureRmSchedulerJobCollection** inaktiverar en jobb samling i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="70353-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="70353-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70353-107">EXAMPLES</span></span>

## <span data-ttu-id="70353-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70353-108">PARAMETERS</span></span>

### <span data-ttu-id="70353-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70353-109">-DefaultProfile</span></span>
<span data-ttu-id="70353-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70353-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70353-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="70353-111">-JobCollectionName</span></span>
<span data-ttu-id="70353-112">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="70353-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="70353-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70353-113">-PassThru</span></span>
<span data-ttu-id="70353-114">Anger att denna cmdlet returnerar ett lyckat resultat.</span><span class="sxs-lookup"><span data-stu-id="70353-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="70353-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="70353-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70353-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70353-116">-ResourceGroupName</span></span>
<span data-ttu-id="70353-117">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="70353-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="70353-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70353-118">-Confirm</span></span>
<span data-ttu-id="70353-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70353-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70353-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70353-120">-WhatIf</span></span>
<span data-ttu-id="70353-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70353-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70353-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70353-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70353-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70353-123">CommonParameters</span></span>
<span data-ttu-id="70353-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70353-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70353-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70353-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70353-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70353-126">INPUTS</span></span>

### <span data-ttu-id="70353-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="70353-127">None</span></span>
<span data-ttu-id="70353-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="70353-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70353-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70353-129">OUTPUTS</span></span>

## <span data-ttu-id="70353-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70353-130">NOTES</span></span>

## <span data-ttu-id="70353-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70353-131">RELATED LINKS</span></span>

[<span data-ttu-id="70353-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70353-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="70353-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70353-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="70353-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70353-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="70353-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70353-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="70353-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70353-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


