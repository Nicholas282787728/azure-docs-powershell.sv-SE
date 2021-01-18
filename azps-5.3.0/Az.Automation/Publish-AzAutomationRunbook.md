---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524911"
---
# <span data-ttu-id="d97f9-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="d97f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d97f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d97f9-103">Publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="d97f9-103">Publishes a runbook.</span></span>

## <span data-ttu-id="d97f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d97f9-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d97f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d97f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d97f9-106">Cmdleten **Publishing-AzAutomationRunbook** publicerar en Runbook för användning i produktions miljön för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d97f9-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="d97f9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d97f9-107">EXAMPLES</span></span>

### <span data-ttu-id="d97f9-108">Exempel 1: publicera en Runbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d97f9-109">Det här kommandot publicerar Runbook-flödet med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d97f9-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d97f9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d97f9-110">PARAMETERS</span></span>

### <span data-ttu-id="d97f9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d97f9-111">-AutomationAccountName</span></span>
<span data-ttu-id="d97f9-112">Anger namnet på det Automation-konto som denna cmdlet publicerar en Runbook i.</span><span class="sxs-lookup"><span data-stu-id="d97f9-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="d97f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97f9-113">-DefaultProfile</span></span>
<span data-ttu-id="d97f9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d97f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d97f9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d97f9-115">-Name</span></span>
<span data-ttu-id="d97f9-116">Anger namnet på den Runbook som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="d97f9-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97f9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97f9-117">-ResourceGroupName</span></span>
<span data-ttu-id="d97f9-118">Anger namnet på den resurs grupp för vilken denna cmdlet publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="d97f9-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="d97f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97f9-119">CommonParameters</span></span>
<span data-ttu-id="d97f9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97f9-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97f9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97f9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d97f9-122">INPUTS</span></span>

### <span data-ttu-id="d97f9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d97f9-123">System.String</span></span>

## <span data-ttu-id="d97f9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d97f9-124">OUTPUTS</span></span>

### <span data-ttu-id="d97f9-125">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d97f9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d97f9-126">NOTES</span></span>

## <span data-ttu-id="d97f9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d97f9-127">RELATED LINKS</span></span>

[<span data-ttu-id="d97f9-128">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="d97f9-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d97f9-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


