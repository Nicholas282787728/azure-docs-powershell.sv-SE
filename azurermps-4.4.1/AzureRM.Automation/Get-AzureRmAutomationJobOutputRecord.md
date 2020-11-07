---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: d9ef76273d89f243f5a8d13543442aba16f7a9d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578575"
---
# <span data-ttu-id="8d9e4-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="8d9e4-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="8d9e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9e4-103">Får fullständig utskrift av en utdataström för en automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d9e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d9e4-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d9e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d9e4-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9e4-106">Cmdleten **Get-AzureRmAutomationJobOutputRecord** får hela utdata från en output-post.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="8d9e4-107">Även om cmdleten **Get-AzureRmAutomationJobOutput** innehåller en eller flera utgångs poster returneras bara en sammanfattning, som en sträng, för värdet för en output-post.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="8d9e4-108">Det returnerar inte det fulla värdet för en utmatnings posts utgångs datum i den ursprungliga typen.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="8d9e4-109">Dessutom har sammanfattningen maximal längd, vilket är det fulla värdet som denna cmdlet matar ut.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="8d9e4-110">Till skillnad från **Get-AzureRmAutomationJobOutput** returnerar den här cmdleten det fullständiga värdet i den ursprungligen returnerade typen, för eventuell utdataström.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="8d9e4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d9e4-111">EXAMPLES</span></span>

### <span data-ttu-id="8d9e4-112">Exempel 1: få full till gång till ett automatiserings jobb</span><span class="sxs-lookup"><span data-stu-id="8d9e4-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="8d9e4-113">Det här kommandot får hela utdata från jobbet som har angivet jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="8d9e4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d9e4-114">PARAMETERS</span></span>

### <span data-ttu-id="8d9e4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8d9e4-115">-AutomationAccountName</span></span>
<span data-ttu-id="8d9e4-116">Anger namnet på ett Automation-konto som den här cmdleten får en output-post för.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="8d9e4-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8d9e4-117">-Id</span></span>
<span data-ttu-id="8d9e4-118">Anger ID för en output-post för den här cmdleten som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-118">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="8d9e4-119">-JobId</span><span class="sxs-lookup"><span data-stu-id="8d9e4-119">-JobId</span></span>
<span data-ttu-id="8d9e4-120">Anger ID för ett jobb som denna cmdlet hämtar en utdatafil till.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-120">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="8d9e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d9e4-122">Anger namnet på en resurs grupp för vilken denna cmdlet får en output-post.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-122">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="8d9e4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9e4-123">-DefaultProfile</span></span>
<span data-ttu-id="8d9e4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9e4-125">CommonParameters</span></span>
<span data-ttu-id="8d9e4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9e4-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9e4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9e4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d9e4-128">INPUTS</span></span>

## <span data-ttu-id="8d9e4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d9e4-129">OUTPUTS</span></span>

### <span data-ttu-id="8d9e4-130">Microsoft. Azure. commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="8d9e4-130">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="8d9e4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d9e4-131">NOTES</span></span>

## <span data-ttu-id="8d9e4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d9e4-132">RELATED LINKS</span></span>

[<span data-ttu-id="8d9e4-133">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="8d9e4-133">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

