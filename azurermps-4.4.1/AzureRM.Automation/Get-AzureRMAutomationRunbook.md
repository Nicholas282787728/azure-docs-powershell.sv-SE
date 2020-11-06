---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: e543a7da3ce5502e0f78619ca4fbb455b29b82d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574748"
---
# <span data-ttu-id="475a4-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="475a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="475a4-102">SYNOPSIS</span></span>
<span data-ttu-id="475a4-103">Hämtar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="475a4-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="475a4-104">SYNTAX</span></span>

### <span data-ttu-id="475a4-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="475a4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475a4-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="475a4-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="475a4-107">DESCRIPTION</span></span>
<span data-ttu-id="475a4-108">Cmdleten **Get-AzureRmAutomationRunbook** får Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="475a4-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="475a4-109">Ange namnet på en viss Runbook.</span><span class="sxs-lookup"><span data-stu-id="475a4-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="475a4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="475a4-110">EXAMPLES</span></span>

### <span data-ttu-id="475a4-111">Exempel 1: Hämta alla Runbooks</span><span class="sxs-lookup"><span data-stu-id="475a4-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="475a4-112">Det här kommandot får alla Runbooks i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="475a4-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="475a4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="475a4-113">PARAMETERS</span></span>

### <span data-ttu-id="475a4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="475a4-114">-AutomationAccountName</span></span>
<span data-ttu-id="475a4-115">Anger namnet på ett Automation-konto där denna cmdlet får Runbooks.</span><span class="sxs-lookup"><span data-stu-id="475a4-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="475a4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="475a4-116">-Name</span></span>
<span data-ttu-id="475a4-117">Anger namnet på en Runbook som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="475a4-117">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="475a4-119">Anger namnet på den resurs grupp för vilken denna cmdlet får Runbooks.</span><span class="sxs-lookup"><span data-stu-id="475a4-119">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="475a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475a4-120">-DefaultProfile</span></span>
<span data-ttu-id="475a4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="475a4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475a4-122">CommonParameters</span></span>
<span data-ttu-id="475a4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475a4-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475a4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475a4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="475a4-125">INPUTS</span></span>

## <span data-ttu-id="475a4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="475a4-126">OUTPUTS</span></span>

### <span data-ttu-id="475a4-127">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="475a4-127">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="475a4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="475a4-128">NOTES</span></span>

## <span data-ttu-id="475a4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="475a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="475a4-130">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-130">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-131">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-132">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-133">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-134">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-134">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-135">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-135">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-136">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-136">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="475a4-137">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="475a4-137">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


