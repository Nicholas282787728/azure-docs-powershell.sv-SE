---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 35b8788c67098a45f6a5373e90b7a93fbcbc4703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573786"
---
# <span data-ttu-id="331e3-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="331e3-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="331e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="331e3-102">SYNOPSIS</span></span>
<span data-ttu-id="331e3-103">Inaktive ras en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="331e3-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="331e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="331e3-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="331e3-105">DESCRIPTION</span></span>
<span data-ttu-id="331e3-106">Suspend-AzureRmAnalysisServicesServer cmdlet inaktiverar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="331e3-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="331e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="331e3-107">EXAMPLES</span></span>

### <span data-ttu-id="331e3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="331e3-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="331e3-109">Det här kommandot avaktiverar en aktiv server som heter testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="331e3-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="331e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="331e3-110">PARAMETERS</span></span>

### <span data-ttu-id="331e3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="331e3-111">-Name</span></span>
<span data-ttu-id="331e3-112">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="331e3-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="331e3-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="331e3-113">-PassThru</span></span>
<span data-ttu-id="331e3-114">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="331e3-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="331e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="331e3-116">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="331e3-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="331e3-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="331e3-117">-Confirm</span></span>
<span data-ttu-id="331e3-118">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="331e3-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="331e3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="331e3-119">-WhatIf</span></span>
<span data-ttu-id="331e3-120">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="331e3-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="331e3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331e3-121">CommonParameters</span></span>
<span data-ttu-id="331e3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331e3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331e3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="331e3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331e3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="331e3-124">INPUTS</span></span>

## <span data-ttu-id="331e3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="331e3-125">OUTPUTS</span></span>

### <span data-ttu-id="331e3-126">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="331e3-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="331e3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="331e3-127">NOTES</span></span>
<span data-ttu-id="331e3-128">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="331e3-128">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="331e3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="331e3-129">RELATED LINKS</span></span>

[<span data-ttu-id="331e3-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="331e3-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="331e3-131">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="331e3-131">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

