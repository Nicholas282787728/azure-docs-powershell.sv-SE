---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582127"
---
# <span data-ttu-id="85602-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="85602-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85602-102">SYNOPSIS</span></span>
<span data-ttu-id="85602-103">Ändrar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="85602-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85602-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85602-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85602-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85602-105">DESCRIPTION</span></span>
<span data-ttu-id="85602-106">Cmdleten **set-AzureRmAutomationRunbook** ändrar konfigurationen för en Azure Automation-RUNBOOK i APS.</span><span class="sxs-lookup"><span data-stu-id="85602-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="85602-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85602-107">EXAMPLES</span></span>

### <span data-ttu-id="85602-108">Exempel 1: Aktivera utförlig loggning för en Runbook</span><span class="sxs-lookup"><span data-stu-id="85602-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="85602-109">Det här kommandot aktiverar utförlig loggning för jobben i angiven Runbook i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="85602-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="85602-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85602-110">PARAMETERS</span></span>

### <span data-ttu-id="85602-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="85602-111">-AutomationAccountName</span></span>
<span data-ttu-id="85602-112">Anger namnet på det Automation-konto som denna cmdlet ändrar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="85602-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="85602-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85602-113">-DefaultProfile</span></span>
<span data-ttu-id="85602-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="85602-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85602-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="85602-115">-Description</span></span>
<span data-ttu-id="85602-116">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="85602-116">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85602-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="85602-117">-LogProgress</span></span>
<span data-ttu-id="85602-118">Anger om Runbook loggar status.</span><span class="sxs-lookup"><span data-stu-id="85602-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85602-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="85602-119">-LogVerbose</span></span>
<span data-ttu-id="85602-120">Anger om loggning innehåller detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="85602-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85602-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="85602-121">-Name</span></span>
<span data-ttu-id="85602-122">Anger namnet på den Runbook som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="85602-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85602-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85602-123">-ResourceGroupName</span></span>
<span data-ttu-id="85602-124">Anger namnet på den resurs grupp för vilken denna cmdlet ändrar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="85602-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="85602-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="85602-125">-Tag</span></span>
<span data-ttu-id="85602-126">Runbook-taggarna.</span><span class="sxs-lookup"><span data-stu-id="85602-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85602-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85602-127">CommonParameters</span></span>
<span data-ttu-id="85602-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85602-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85602-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85602-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85602-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85602-130">INPUTS</span></span>

### <span data-ttu-id="85602-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="85602-131">None</span></span>
<span data-ttu-id="85602-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="85602-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85602-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85602-133">OUTPUTS</span></span>

### <span data-ttu-id="85602-134">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="85602-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="85602-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85602-135">NOTES</span></span>

## <span data-ttu-id="85602-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85602-136">RELATED LINKS</span></span>

[<span data-ttu-id="85602-137">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-138">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-139">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-140">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-141">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-142">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-143">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="85602-144">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="85602-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


