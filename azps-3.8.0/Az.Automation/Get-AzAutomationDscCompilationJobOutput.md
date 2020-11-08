---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090431"
---
# <span data-ttu-id="a487e-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a487e-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="a487e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a487e-102">SYNOPSIS</span></span>
<span data-ttu-id="a487e-103">Hämtar loggnings strömmar för ett Automation DSC Compilation-jobb.</span><span class="sxs-lookup"><span data-stu-id="a487e-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="a487e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a487e-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a487e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a487e-105">DESCRIPTION</span></span>
<span data-ttu-id="a487e-106">Cmdleten **Get-AzAutomationDscCompilationJobOutput** hämtar strömmarna för ett AP-kompilator jobb i en APS-Configuration-konfiguration (DSC) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a487e-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="a487e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a487e-107">EXAMPLES</span></span>

### <span data-ttu-id="a487e-108">Exempel 1: Hämta loggar för ett DSC Compilation-jobb</span><span class="sxs-lookup"><span data-stu-id="a487e-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="a487e-109">Det första kommandot hämtar de Compilation Jobs i Automation-kontot som heter Contoso17 med hjälp av Get-AzAutomationDscCompilationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a487e-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="a487e-110">Kommandot lagrar objekten i $Jobs variabel.</span><span class="sxs-lookup"><span data-stu-id="a487e-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="a487e-111">Det andra kommandot får utdata för kompileringen för alla strömmar för den första medlemmen i $Jobs-matrisen.</span><span class="sxs-lookup"><span data-stu-id="a487e-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="a487e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a487e-112">PARAMETERS</span></span>

### <span data-ttu-id="a487e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a487e-113">-AutomationAccountName</span></span>
<span data-ttu-id="a487e-114">Anger namnet på Automation-kontot som innehåller DSC Compilation-jobbet.</span><span class="sxs-lookup"><span data-stu-id="a487e-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a487e-115">-DefaultProfile</span></span>
<span data-ttu-id="a487e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a487e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a487e-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a487e-117">-Id</span></span>
<span data-ttu-id="a487e-118">Anger det unika ID: t för det DSC Compilation-jobb som denna cmdlet ska skriva ut.</span><span class="sxs-lookup"><span data-stu-id="a487e-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a487e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a487e-120">Anger namnet på den resurs grupp som innehåller det DSC Compilation-jobb som denna cmdlet hämtar data ström för.</span><span class="sxs-lookup"><span data-stu-id="a487e-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="a487e-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a487e-121">-StartTime</span></span>
<span data-ttu-id="a487e-122">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="a487e-122">Specifies a start time.</span></span>
<span data-ttu-id="a487e-123">Denna cmdlet hämtar data flödes poster som ska skickas från DSC-kompilatorn efter denna tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="a487e-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487e-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="a487e-124">-Stream</span></span>
<span data-ttu-id="a487e-125">Anger den typ av ström för utdata som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a487e-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="a487e-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a487e-126">Valid values are:</span></span> 
- <span data-ttu-id="a487e-127">Eventuell</span><span class="sxs-lookup"><span data-stu-id="a487e-127">Any</span></span> 
- <span data-ttu-id="a487e-128">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="a487e-128">Warning</span></span> 
- <span data-ttu-id="a487e-129">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="a487e-129">Error</span></span> 
- <span data-ttu-id="a487e-130">Utförlig</span><span class="sxs-lookup"><span data-stu-id="a487e-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a487e-131">CommonParameters</span></span>
<span data-ttu-id="a487e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a487e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a487e-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a487e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a487e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a487e-134">INPUTS</span></span>

### <span data-ttu-id="a487e-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a487e-135">System.Guid</span></span>

### <span data-ttu-id="a487e-136">Microsoft. Azure. commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="a487e-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="a487e-137">System. Nullable ' 1 [[system. DateTimeOffset, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a487e-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a487e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a487e-138">System.String</span></span>

## <span data-ttu-id="a487e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a487e-139">OUTPUTS</span></span>

### <span data-ttu-id="a487e-140">Microsoft. Azure. commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="a487e-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="a487e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a487e-141">NOTES</span></span>

## <span data-ttu-id="a487e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a487e-142">RELATED LINKS</span></span>

[<span data-ttu-id="a487e-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a487e-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="a487e-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a487e-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


