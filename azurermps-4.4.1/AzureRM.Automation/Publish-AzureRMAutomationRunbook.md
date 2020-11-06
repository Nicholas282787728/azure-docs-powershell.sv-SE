---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581532"
---
# <span data-ttu-id="7ecf4-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="7ecf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ecf4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ecf4-103">Publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ecf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ecf4-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ecf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ecf4-105">DESCRIPTION</span></span>
<span data-ttu-id="7ecf4-106">Cmdleten **Publishing-AzureRmAutomationRunbook** publicerar en Runbook för användning i produktions miljön för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="7ecf4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ecf4-107">EXAMPLES</span></span>

### <span data-ttu-id="7ecf4-108">Exempel 1: publicera en Runbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ecf4-109">Det här kommandot publicerar Runbook-flödet med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7ecf4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ecf4-110">PARAMETERS</span></span>

### <span data-ttu-id="7ecf4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ecf4-111">-AutomationAccountName</span></span>
<span data-ttu-id="7ecf4-112">Anger namnet på det Automation-konto som denna cmdlet publicerar en Runbook i.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="7ecf4-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ecf4-113">-Name</span></span>
<span data-ttu-id="7ecf4-114">Anger namnet på den Runbook som denna cmdlet publicerar.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-114">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="7ecf4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ecf4-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ecf4-116">Anger namnet på den resurs grupp för vilken denna cmdlet publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-116">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="7ecf4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ecf4-117">-DefaultProfile</span></span>
<span data-ttu-id="7ecf4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ecf4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ecf4-119">CommonParameters</span></span>
<span data-ttu-id="7ecf4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ecf4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ecf4-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ecf4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ecf4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ecf4-122">INPUTS</span></span>

## <span data-ttu-id="7ecf4-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ecf4-123">OUTPUTS</span></span>

### <span data-ttu-id="7ecf4-124">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-124">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="7ecf4-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ecf4-125">NOTES</span></span>

## <span data-ttu-id="7ecf4-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ecf4-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ecf4-127">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-127">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-128">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-128">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-129">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-129">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-130">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-130">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-131">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-132">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-132">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-133">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-133">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7ecf4-134">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ecf4-134">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


