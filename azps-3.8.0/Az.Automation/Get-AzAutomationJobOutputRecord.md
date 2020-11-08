---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: e43cb76db410752aef0a0cffc72d3d5bb6f8e28f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090401"
---
# <span data-ttu-id="0b7e7-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="0b7e7-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="0b7e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7e7-103">Får fullständig utskrift av en utdataström för en automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="0b7e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b7e7-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b7e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b7e7-105">DESCRIPTION</span></span>
<span data-ttu-id="0b7e7-106">Cmdleten **Get-AzAutomationJobOutputRecord** får hela utdata från en output-post.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="0b7e7-107">Även om cmdleten **Get-AzAutomationJobOutput** innehåller en eller flera utgångs poster returneras bara en sammanfattning, som en sträng, för värdet för en output-post.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="0b7e7-108">Det returnerar inte det fulla värdet för en utmatnings posts utgångs datum i den ursprungliga typen.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="0b7e7-109">Dessutom har sammanfattningen maximal längd, vilket är det fulla värdet som denna cmdlet matar ut.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="0b7e7-110">Till skillnad från **Get-AzAutomationJobOutput** returnerar den här cmdleten det fullständiga värdet i den ursprungligen returnerade typen, för eventuell utdataström.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="0b7e7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b7e7-111">EXAMPLES</span></span>

### <span data-ttu-id="0b7e7-112">Exempel 1: få full till gång till ett automatiserings jobb</span><span class="sxs-lookup"><span data-stu-id="0b7e7-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="0b7e7-113">Det här kommandot får hela utdata från jobbet som har angivet jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="0b7e7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b7e7-114">PARAMETERS</span></span>

### <span data-ttu-id="0b7e7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0b7e7-115">-AutomationAccountName</span></span>
<span data-ttu-id="0b7e7-116">Anger namnet på ett Automation-konto som den här cmdleten får en output-post för.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="0b7e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7e7-117">-DefaultProfile</span></span>
<span data-ttu-id="0b7e7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0b7e7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b7e7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0b7e7-119">-Id</span></span>
<span data-ttu-id="0b7e7-120">Anger ID för en output-post för den här cmdleten som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e7-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="0b7e7-121">-JobId</span></span>
<span data-ttu-id="0b7e7-122">Anger ID för ett jobb som denna cmdlet hämtar en utdatafil till.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b7e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="0b7e7-124">Anger namnet på en resurs grupp för vilken denna cmdlet får en output-post.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="0b7e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7e7-125">CommonParameters</span></span>
<span data-ttu-id="0b7e7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7e7-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b7e7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7e7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b7e7-128">INPUTS</span></span>

### <span data-ttu-id="0b7e7-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0b7e7-129">System.Guid</span></span>

### <span data-ttu-id="0b7e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0b7e7-130">System.String</span></span>

## <span data-ttu-id="0b7e7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b7e7-131">OUTPUTS</span></span>

### <span data-ttu-id="0b7e7-132">Microsoft. Azure. commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="0b7e7-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="0b7e7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b7e7-133">NOTES</span></span>

## <span data-ttu-id="0b7e7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b7e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b7e7-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0b7e7-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

