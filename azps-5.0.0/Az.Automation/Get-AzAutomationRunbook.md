---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272944"
---
# <span data-ttu-id="aa9d7-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="aa9d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9d7-103">Hämtar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-103">Gets a runbook.</span></span>

## <span data-ttu-id="aa9d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa9d7-104">SYNTAX</span></span>

### <span data-ttu-id="aa9d7-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="aa9d7-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa9d7-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="aa9d7-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa9d7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa9d7-107">DESCRIPTION</span></span>
<span data-ttu-id="aa9d7-108">Cmdleten **Get-AzAutomationRunbook** får Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="aa9d7-109">Ange namnet på en viss Runbook.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="aa9d7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa9d7-110">EXAMPLES</span></span>

### <span data-ttu-id="aa9d7-111">Exempel 1: Hämta alla Runbooks</span><span class="sxs-lookup"><span data-stu-id="aa9d7-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa9d7-112">Det här kommandot får alla Runbooks i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="aa9d7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa9d7-113">PARAMETERS</span></span>

### <span data-ttu-id="aa9d7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa9d7-114">-AutomationAccountName</span></span>
<span data-ttu-id="aa9d7-115">Anger namnet på ett Automation-konto där denna cmdlet får Runbooks.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="aa9d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9d7-116">-DefaultProfile</span></span>
<span data-ttu-id="aa9d7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa9d7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa9d7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa9d7-118">-Name</span></span>
<span data-ttu-id="aa9d7-119">Anger namnet på en Runbook som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aa9d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa9d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa9d7-121">Anger namnet på den resurs grupp för vilken denna cmdlet får Runbooks.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="aa9d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9d7-122">CommonParameters</span></span>
<span data-ttu-id="aa9d7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa9d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9d7-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa9d7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9d7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa9d7-125">INPUTS</span></span>

### <span data-ttu-id="aa9d7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="aa9d7-126">System.String</span></span>

## <span data-ttu-id="aa9d7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa9d7-127">OUTPUTS</span></span>

### <span data-ttu-id="aa9d7-128">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="aa9d7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa9d7-129">NOTES</span></span>

## <span data-ttu-id="aa9d7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa9d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa9d7-131">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-135">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="aa9d7-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="aa9d7-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

