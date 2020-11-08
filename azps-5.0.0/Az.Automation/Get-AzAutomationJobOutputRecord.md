---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272346"
---
# <span data-ttu-id="1a827-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="1a827-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="1a827-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a827-102">SYNOPSIS</span></span>
<span data-ttu-id="1a827-103">Får fullständig utskrift av en utdataström för en automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="1a827-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="1a827-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a827-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a827-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a827-105">DESCRIPTION</span></span>
<span data-ttu-id="1a827-106">Cmdleten **Get-AzAutomationJobOutputRecord** får hela utdata från en output-post.</span><span class="sxs-lookup"><span data-stu-id="1a827-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="1a827-107">Även om cmdleten **Get-AzAutomationJobOutput** innehåller en eller flera utgångs poster returneras bara en sammanfattning, som en sträng, för värdet för en output-post.</span><span class="sxs-lookup"><span data-stu-id="1a827-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="1a827-108">Det returnerar inte det fulla värdet för en utmatnings posts utgångs datum i den ursprungliga typen.</span><span class="sxs-lookup"><span data-stu-id="1a827-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="1a827-109">Dessutom har sammanfattningen maximal längd, vilket är det fulla värdet som denna cmdlet matar ut.</span><span class="sxs-lookup"><span data-stu-id="1a827-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="1a827-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a827-110">EXAMPLES</span></span>

### <span data-ttu-id="1a827-111">Exempel 1: få full till gång till ett automatiserings jobb</span><span class="sxs-lookup"><span data-stu-id="1a827-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="1a827-112">Det här kommandot får hela utdata från jobbet som har angivet jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="1a827-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="1a827-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a827-113">PARAMETERS</span></span>

### <span data-ttu-id="1a827-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a827-114">-AutomationAccountName</span></span>
<span data-ttu-id="1a827-115">Anger namnet på ett Automation-konto som den här cmdleten får en output-post för.</span><span class="sxs-lookup"><span data-stu-id="1a827-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="1a827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a827-116">-DefaultProfile</span></span>
<span data-ttu-id="1a827-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1a827-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a827-118">-ID</span><span class="sxs-lookup"><span data-stu-id="1a827-118">-Id</span></span>
<span data-ttu-id="1a827-119">Anger ID för en output-post för den här cmdleten som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1a827-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="1a827-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="1a827-120">-JobId</span></span>
<span data-ttu-id="1a827-121">Anger ID för ett jobb som denna cmdlet hämtar en utdatafil till.</span><span class="sxs-lookup"><span data-stu-id="1a827-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="1a827-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a827-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a827-123">Anger namnet på en resurs grupp för vilken denna cmdlet får en output-post.</span><span class="sxs-lookup"><span data-stu-id="1a827-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="1a827-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a827-124">CommonParameters</span></span>
<span data-ttu-id="1a827-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a827-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a827-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a827-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a827-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a827-127">INPUTS</span></span>

### <span data-ttu-id="1a827-128">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1a827-128">System.Guid</span></span>

### <span data-ttu-id="1a827-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1a827-129">System.String</span></span>

## <span data-ttu-id="1a827-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a827-130">OUTPUTS</span></span>

### <span data-ttu-id="1a827-131">Microsoft. Azure. commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="1a827-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="1a827-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a827-132">NOTES</span></span>

## <span data-ttu-id="1a827-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a827-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a827-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1a827-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


