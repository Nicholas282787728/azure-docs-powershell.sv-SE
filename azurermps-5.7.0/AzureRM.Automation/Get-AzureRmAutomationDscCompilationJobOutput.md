---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: e7093f04cfd7b51f00dcc5cbcd6ad3cb98f54bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586416"
---
# <span data-ttu-id="86a02-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="86a02-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="86a02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86a02-102">SYNOPSIS</span></span>
<span data-ttu-id="86a02-103">Hämtar loggnings strömmar för ett Automation DSC Compilation-jobb.</span><span class="sxs-lookup"><span data-stu-id="86a02-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86a02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86a02-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86a02-105">DESCRIPTION</span></span>
<span data-ttu-id="86a02-106">Cmdleten **Get-AzureRmAutomationDscCompilationJobOutput** hämtar strömmarna för ett AP-kompilator jobb i en APS-Configuration-konfiguration (DSC) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="86a02-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="86a02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86a02-107">EXAMPLES</span></span>

### <span data-ttu-id="86a02-108">Exempel 1: Hämta loggar för ett DSC Compilation-jobb</span><span class="sxs-lookup"><span data-stu-id="86a02-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="86a02-109">Det första kommandot hämtar de Compilation Jobs i Automation-kontot som heter Contoso17 med hjälp av Get-AzureRmAutomationDscCompilationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a02-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="86a02-110">Kommandot lagrar objekten i $Jobs variabel.</span><span class="sxs-lookup"><span data-stu-id="86a02-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="86a02-111">Det andra kommandot får utdata för kompileringen för alla strömmar för den första medlemmen i $Jobs-matrisen.</span><span class="sxs-lookup"><span data-stu-id="86a02-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="86a02-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86a02-112">PARAMETERS</span></span>

### <span data-ttu-id="86a02-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="86a02-113">-AutomationAccountName</span></span>
<span data-ttu-id="86a02-114">Anger namnet på Automation-kontot som innehåller DSC Compilation-jobbet.</span><span class="sxs-lookup"><span data-stu-id="86a02-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a02-115">-DefaultProfile</span></span>
<span data-ttu-id="86a02-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="86a02-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86a02-117">-ID</span><span class="sxs-lookup"><span data-stu-id="86a02-117">-Id</span></span>
<span data-ttu-id="86a02-118">Anger det unika ID: t för det DSC Compilation-jobb som denna cmdlet ska skriva ut.</span><span class="sxs-lookup"><span data-stu-id="86a02-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a02-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a02-119">-ResourceGroupName</span></span>
<span data-ttu-id="86a02-120">Anger namnet på den resurs grupp som innehåller det DSC Compilation-jobb som denna cmdlet hämtar data ström för.</span><span class="sxs-lookup"><span data-stu-id="86a02-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="86a02-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="86a02-121">-StartTime</span></span>
<span data-ttu-id="86a02-122">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="86a02-122">Specifies a start time.</span></span>
<span data-ttu-id="86a02-123">Denna cmdlet hämtar data flödes poster som ska skickas från DSC-kompilatorn efter denna tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="86a02-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a02-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="86a02-124">-Stream</span></span>
<span data-ttu-id="86a02-125">Anger den typ av ström för utdata som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="86a02-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="86a02-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="86a02-126">Valid values are:</span></span> 

- <span data-ttu-id="86a02-127">Eventuell</span><span class="sxs-lookup"><span data-stu-id="86a02-127">Any</span></span> 
- <span data-ttu-id="86a02-128">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="86a02-128">Warning</span></span> 
- <span data-ttu-id="86a02-129">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="86a02-129">Error</span></span> 
- <span data-ttu-id="86a02-130">Utförlig</span><span class="sxs-lookup"><span data-stu-id="86a02-130">Verbose</span></span>

```yaml
Type: CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a02-131">CommonParameters</span></span>
<span data-ttu-id="86a02-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a02-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a02-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a02-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86a02-134">INPUTS</span></span>

### <span data-ttu-id="86a02-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="86a02-135">None</span></span>
<span data-ttu-id="86a02-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="86a02-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86a02-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86a02-137">OUTPUTS</span></span>

### <span data-ttu-id="86a02-138">Microsoft. Azure. commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="86a02-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="86a02-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86a02-139">NOTES</span></span>

## <span data-ttu-id="86a02-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86a02-140">RELATED LINKS</span></span>

[<span data-ttu-id="86a02-141">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="86a02-141">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="86a02-142">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="86a02-142">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


