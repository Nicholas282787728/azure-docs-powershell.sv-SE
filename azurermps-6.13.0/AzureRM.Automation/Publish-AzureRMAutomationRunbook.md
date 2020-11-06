---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: e3d60cf277402ac23764b538ba6492ef5c424219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579064"
---
# <span data-ttu-id="85ac1-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="85ac1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="85ac1-103">Publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="85ac1-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85ac1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85ac1-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85ac1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="85ac1-106">Cmdleten **Publishing-AzureRmAutomationRunbook** publicerar en Runbook för användning i produktions miljön för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="85ac1-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="85ac1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="85ac1-108">Exempel 1: publicera en Runbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="85ac1-109">Det här kommandot publicerar Runbook-flödet med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="85ac1-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="85ac1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85ac1-110">PARAMETERS</span></span>

### <span data-ttu-id="85ac1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="85ac1-111">-AutomationAccountName</span></span>
<span data-ttu-id="85ac1-112">Anger namnet på det Automation-konto som denna cmdlet publicerar en Runbook i.</span><span class="sxs-lookup"><span data-stu-id="85ac1-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="85ac1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ac1-113">-DefaultProfile</span></span>
<span data-ttu-id="85ac1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="85ac1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85ac1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="85ac1-115">-Name</span></span>
<span data-ttu-id="85ac1-116">Anger namnet på den Runbook som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="85ac1-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="85ac1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ac1-117">-ResourceGroupName</span></span>
<span data-ttu-id="85ac1-118">Anger namnet på den resurs grupp för vilken denna cmdlet publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="85ac1-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="85ac1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ac1-119">CommonParameters</span></span>
<span data-ttu-id="85ac1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85ac1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ac1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85ac1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ac1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85ac1-122">INPUTS</span></span>

### <span data-ttu-id="85ac1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="85ac1-123">System.String</span></span>

## <span data-ttu-id="85ac1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85ac1-124">OUTPUTS</span></span>

### <span data-ttu-id="85ac1-125">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="85ac1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85ac1-126">NOTES</span></span>

## <span data-ttu-id="85ac1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85ac1-127">RELATED LINKS</span></span>

[<span data-ttu-id="85ac1-128">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-128">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-129">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-129">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-130">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-130">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-131">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-132">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-133">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-133">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-134">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-134">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85ac1-135">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85ac1-135">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


