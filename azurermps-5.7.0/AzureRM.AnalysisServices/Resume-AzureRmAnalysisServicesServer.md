---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756519"
---
# <span data-ttu-id="2d4c7-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d4c7-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="2d4c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4c7-103">Återupptar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="2d4c7-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d4c7-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d4c7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4c7-106">Resume-AzureRmAnalysisServicesServer cmdleten återupptar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="2d4c7-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="2d4c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d4c7-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4c7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2d4c7-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="2d4c7-109">Det här kommandot återupptar en pausad server med namnet testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="2d4c7-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2d4c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d4c7-110">PARAMETERS</span></span>

### <span data-ttu-id="2d4c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4c7-111">-DefaultProfile</span></span>
<span data-ttu-id="2d4c7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d4c7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d4c7-113">-Name</span></span>
<span data-ttu-id="2d4c7-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="2d4c7-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2d4c7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4c7-115">-PassThru</span></span>
<span data-ttu-id="2d4c7-116">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="2d4c7-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2d4c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d4c7-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="2d4c7-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2d4c7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d4c7-119">-Confirm</span></span>
<span data-ttu-id="2d4c7-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="2d4c7-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2d4c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4c7-121">-WhatIf</span></span>
<span data-ttu-id="2d4c7-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="2d4c7-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2d4c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4c7-123">CommonParameters</span></span>
<span data-ttu-id="2d4c7-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4c7-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4c7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4c7-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d4c7-126">INPUTS</span></span>

### <span data-ttu-id="2d4c7-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="2d4c7-127">None</span></span>
<span data-ttu-id="2d4c7-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d4c7-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d4c7-129">OUTPUTS</span></span>

### <span data-ttu-id="2d4c7-130">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d4c7-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2d4c7-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d4c7-131">NOTES</span></span>
<span data-ttu-id="2d4c7-132">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="2d4c7-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="2d4c7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d4c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="2d4c7-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d4c7-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="2d4c7-135">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2d4c7-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
