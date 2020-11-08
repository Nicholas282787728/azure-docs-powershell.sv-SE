---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260402"
---
# <span data-ttu-id="c4732-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4732-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c4732-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4732-102">SYNOPSIS</span></span>
<span data-ttu-id="c4732-103">Återupptar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c4732-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="c4732-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4732-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4732-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4732-105">DESCRIPTION</span></span>
<span data-ttu-id="c4732-106">Resume-AzAnalysisServicesServer cmdleten återupptar en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c4732-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="c4732-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4732-107">EXAMPLES</span></span>

### <span data-ttu-id="c4732-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4732-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c4732-109">Det här kommandot återupptar en pausad server med namnet testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="c4732-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c4732-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4732-110">PARAMETERS</span></span>

### <span data-ttu-id="c4732-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4732-111">-DefaultProfile</span></span>
<span data-ttu-id="c4732-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4732-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4732-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4732-113">-Name</span></span>
<span data-ttu-id="c4732-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c4732-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c4732-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4732-115">-PassThru</span></span>
<span data-ttu-id="c4732-116">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="c4732-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c4732-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4732-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4732-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="c4732-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="c4732-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4732-119">-Confirm</span></span>
<span data-ttu-id="c4732-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="c4732-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c4732-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4732-121">-WhatIf</span></span>
<span data-ttu-id="c4732-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="c4732-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c4732-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4732-123">CommonParameters</span></span>
<span data-ttu-id="c4732-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4732-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4732-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4732-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4732-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4732-126">INPUTS</span></span>

### <span data-ttu-id="c4732-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c4732-127">System.String</span></span>

## <span data-ttu-id="c4732-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4732-128">OUTPUTS</span></span>

### <span data-ttu-id="c4732-129">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4732-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c4732-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4732-130">NOTES</span></span>
<span data-ttu-id="c4732-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="c4732-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="c4732-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4732-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4732-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4732-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c4732-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c4732-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
