---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406419"
---
# <span data-ttu-id="c9628-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9628-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c9628-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9628-102">SYNOPSIS</span></span>
<span data-ttu-id="c9628-103">Tar bort en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c9628-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="c9628-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9628-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9628-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9628-105">DESCRIPTION</span></span>
<span data-ttu-id="c9628-106">Remove-AzAnalysisServicesServer-cmdleten tar bort en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c9628-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="c9628-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9628-107">EXAMPLES</span></span>

### <span data-ttu-id="c9628-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9628-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c9628-109">Det här kommandot tar bort servern med namnet testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="c9628-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c9628-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9628-110">PARAMETERS</span></span>

### <span data-ttu-id="c9628-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9628-111">-DefaultProfile</span></span>
<span data-ttu-id="c9628-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9628-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9628-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9628-113">-Name</span></span>
<span data-ttu-id="c9628-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c9628-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c9628-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9628-115">-PassThru</span></span>
<span data-ttu-id="c9628-116">Returnerar den borttagna Server informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="c9628-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c9628-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9628-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9628-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="c9628-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="c9628-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9628-119">-Confirm</span></span>
<span data-ttu-id="c9628-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="c9628-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c9628-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9628-121">-WhatIf</span></span>
<span data-ttu-id="c9628-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="c9628-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c9628-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9628-123">CommonParameters</span></span>
<span data-ttu-id="c9628-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9628-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9628-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9628-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9628-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9628-126">INPUTS</span></span>

### <span data-ttu-id="c9628-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c9628-127">System.String</span></span>

## <span data-ttu-id="c9628-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9628-128">OUTPUTS</span></span>

### <span data-ttu-id="c9628-129">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9628-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c9628-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9628-130">NOTES</span></span>
<span data-ttu-id="c9628-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="c9628-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="c9628-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9628-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9628-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9628-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c9628-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9628-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
