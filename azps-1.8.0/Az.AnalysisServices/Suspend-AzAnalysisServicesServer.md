---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: ecd9e83607da048246ec996188fd9a31d231ff32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743447"
---
# <span data-ttu-id="dce8d-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dce8d-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="dce8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dce8d-102">SYNOPSIS</span></span>
<span data-ttu-id="dce8d-103">Inaktive ras en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="dce8d-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="dce8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dce8d-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dce8d-105">DESCRIPTION</span></span>
<span data-ttu-id="dce8d-106">Suspend-AzAnalysisServicesServer cmdlet inaktiverar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="dce8d-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="dce8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dce8d-107">EXAMPLES</span></span>

### <span data-ttu-id="dce8d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dce8d-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="dce8d-109">Det här kommandot avaktiverar en aktiv server som heter testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="dce8d-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="dce8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dce8d-110">PARAMETERS</span></span>

### <span data-ttu-id="dce8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce8d-111">-DefaultProfile</span></span>
<span data-ttu-id="dce8d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dce8d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce8d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="dce8d-113">-Name</span></span>
<span data-ttu-id="dce8d-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="dce8d-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="dce8d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dce8d-115">-PassThru</span></span>
<span data-ttu-id="dce8d-116">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="dce8d-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="dce8d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce8d-117">-ResourceGroupName</span></span>
<span data-ttu-id="dce8d-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="dce8d-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="dce8d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dce8d-119">-Confirm</span></span>
<span data-ttu-id="dce8d-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="dce8d-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="dce8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce8d-121">-WhatIf</span></span>
<span data-ttu-id="dce8d-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="dce8d-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="dce8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce8d-123">CommonParameters</span></span>
<span data-ttu-id="dce8d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce8d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce8d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce8d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dce8d-126">INPUTS</span></span>

### <span data-ttu-id="dce8d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dce8d-127">System.String</span></span>

## <span data-ttu-id="dce8d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dce8d-128">OUTPUTS</span></span>

### <span data-ttu-id="dce8d-129">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dce8d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="dce8d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dce8d-130">NOTES</span></span>
<span data-ttu-id="dce8d-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="dce8d-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="dce8d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dce8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="dce8d-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dce8d-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="dce8d-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dce8d-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

