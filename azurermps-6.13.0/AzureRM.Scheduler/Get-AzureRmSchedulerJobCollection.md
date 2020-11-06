---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 402bb79dbd3b767cbc285600b9c81e27f244141e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583948"
---
# <span data-ttu-id="cb5b3-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb5b3-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="cb5b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5b3-103">Hämtar jobb samlingar.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb5b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb5b3-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb5b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb5b3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5b3-106">Cmdleten **Get-AzureRmSchedulerJobCollection** hämtar jobb samlingar i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="cb5b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb5b3-107">EXAMPLES</span></span>

## <span data-ttu-id="cb5b3-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb5b3-108">PARAMETERS</span></span>

### <span data-ttu-id="cb5b3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5b3-109">-DefaultProfile</span></span>
<span data-ttu-id="cb5b3-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb5b3-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="cb5b3-111">-JobCollectionName</span></span>
<span data-ttu-id="cb5b3-112">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5b3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5b3-113">-ResourceGroupName</span></span>
<span data-ttu-id="cb5b3-114">Anger resurs gruppen som den här cmdleten hämtar jobb samlingar från.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5b3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5b3-115">CommonParameters</span></span>
<span data-ttu-id="cb5b3-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5b3-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5b3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5b3-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb5b3-118">INPUTS</span></span>

### <span data-ttu-id="cb5b3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="cb5b3-119">System.String</span></span>

## <span data-ttu-id="cb5b3-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb5b3-120">OUTPUTS</span></span>

### <span data-ttu-id="cb5b3-121">Microsoft. Azure. commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="cb5b3-121">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="cb5b3-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb5b3-122">NOTES</span></span>

## <span data-ttu-id="cb5b3-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb5b3-123">RELATED LINKS</span></span>

[<span data-ttu-id="cb5b3-124">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb5b3-124">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cb5b3-125">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb5b3-125">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cb5b3-126">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb5b3-126">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cb5b3-127">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb5b3-127">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cb5b3-128">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb5b3-128">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


