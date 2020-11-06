---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 3078bddfe82fa1280e7f3288f86c572c44a99148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577491"
---
# <span data-ttu-id="d62ea-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d62ea-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d62ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d62ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d62ea-103">Inaktiverar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="d62ea-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d62ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d62ea-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d62ea-105">DESCRIPTION</span></span>
<span data-ttu-id="d62ea-106">Cmdleten **disable-AzureRmSchedulerJobCollection** inaktiverar en jobb samling i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d62ea-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d62ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d62ea-107">EXAMPLES</span></span>

## <span data-ttu-id="d62ea-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d62ea-108">PARAMETERS</span></span>

### <span data-ttu-id="d62ea-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d62ea-109">-JobCollectionName</span></span>
<span data-ttu-id="d62ea-110">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="d62ea-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="d62ea-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d62ea-111">-PassThru</span></span>
<span data-ttu-id="d62ea-112">Anger att denna cmdlet returnerar ett lyckat resultat.</span><span class="sxs-lookup"><span data-stu-id="d62ea-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="d62ea-113">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d62ea-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d62ea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d62ea-114">-ResourceGroupName</span></span>
<span data-ttu-id="d62ea-115">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="d62ea-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="d62ea-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d62ea-116">-Confirm</span></span>
<span data-ttu-id="d62ea-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d62ea-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d62ea-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62ea-118">-WhatIf</span></span>
<span data-ttu-id="d62ea-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d62ea-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d62ea-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d62ea-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d62ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62ea-121">-DefaultProfile</span></span>
<span data-ttu-id="d62ea-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d62ea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d62ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62ea-123">CommonParameters</span></span>
<span data-ttu-id="d62ea-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62ea-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62ea-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d62ea-126">INPUTS</span></span>

## <span data-ttu-id="d62ea-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d62ea-127">OUTPUTS</span></span>

## <span data-ttu-id="d62ea-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d62ea-128">NOTES</span></span>

## <span data-ttu-id="d62ea-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d62ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="d62ea-130">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d62ea-130">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d62ea-131">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d62ea-131">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d62ea-132">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d62ea-132">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d62ea-133">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d62ea-133">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d62ea-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d62ea-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


