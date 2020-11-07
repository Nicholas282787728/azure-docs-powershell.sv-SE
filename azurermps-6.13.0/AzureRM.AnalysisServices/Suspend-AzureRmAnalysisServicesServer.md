---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756747"
---
# <span data-ttu-id="36ae6-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="36ae6-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="36ae6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="36ae6-103">Inaktive ras en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="36ae6-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36ae6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36ae6-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ae6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="36ae6-106">Suspend-AzureRmAnalysisServicesServer cmdlet inaktiverar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="36ae6-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="36ae6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="36ae6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36ae6-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="36ae6-109">Det här kommandot avaktiverar en aktiv server som heter testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="36ae6-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="36ae6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="36ae6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ae6-111">-DefaultProfile</span></span>
<span data-ttu-id="36ae6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36ae6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ae6-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="36ae6-113">-Name</span></span>
<span data-ttu-id="36ae6-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="36ae6-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="36ae6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36ae6-115">-PassThru</span></span>
<span data-ttu-id="36ae6-116">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="36ae6-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="36ae6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ae6-117">-ResourceGroupName</span></span>
<span data-ttu-id="36ae6-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="36ae6-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ae6-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36ae6-119">-Confirm</span></span>
<span data-ttu-id="36ae6-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="36ae6-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="36ae6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ae6-121">-WhatIf</span></span>
<span data-ttu-id="36ae6-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="36ae6-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="36ae6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ae6-123">CommonParameters</span></span>
<span data-ttu-id="36ae6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ae6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ae6-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ae6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ae6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36ae6-126">INPUTS</span></span>

### <span data-ttu-id="36ae6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="36ae6-127">System.String</span></span>

## <span data-ttu-id="36ae6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36ae6-128">OUTPUTS</span></span>

### <span data-ttu-id="36ae6-129">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="36ae6-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="36ae6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36ae6-130">NOTES</span></span>
<span data-ttu-id="36ae6-131">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="36ae6-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="36ae6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36ae6-132">RELATED LINKS</span></span>

[<span data-ttu-id="36ae6-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="36ae6-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="36ae6-134">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="36ae6-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

