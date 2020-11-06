---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575042"
---
# <span data-ttu-id="4a8f7-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="4a8f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8f7-103">Ändrar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a8f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a8f7-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a8f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a8f7-105">DESCRIPTION</span></span>
<span data-ttu-id="4a8f7-106">Cmdleten **set-AzureRmAutomationRunbook** ändrar konfigurationen för en Azure Automation-RUNBOOK i APS.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="4a8f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a8f7-107">EXAMPLES</span></span>

### <span data-ttu-id="4a8f7-108">Exempel 1: Aktivera utförlig loggning för en Runbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4a8f7-109">Det här kommandot aktiverar utförlig loggning för jobben i angiven Runbook i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4a8f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a8f7-110">PARAMETERS</span></span>

### <span data-ttu-id="4a8f7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a8f7-111">-AutomationAccountName</span></span>
<span data-ttu-id="4a8f7-112">Anger namnet på det Automation-konto som denna cmdlet ändrar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="4a8f7-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4a8f7-113">-Description</span></span>
<span data-ttu-id="4a8f7-114">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-114">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8f7-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="4a8f7-115">-LogProgress</span></span>
<span data-ttu-id="4a8f7-116">Anger om Runbook loggar status.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-116">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8f7-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="4a8f7-117">-LogVerbose</span></span>
<span data-ttu-id="4a8f7-118">Anger om loggning innehåller detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-118">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8f7-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a8f7-119">-Name</span></span>
<span data-ttu-id="4a8f7-120">Anger namnet på den Runbook som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4a8f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a8f7-122">Anger namnet på den resurs grupp för vilken denna cmdlet ändrar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="4a8f7-123">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4a8f7-123">-Tags</span></span>
<span data-ttu-id="4a8f7-124">Anger en ord lista med taggar som ersätter de aktuella taggarna för den ändrade Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8f7-125">-DefaultProfile</span></span>
<span data-ttu-id="4a8f7-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a8f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8f7-127">CommonParameters</span></span>
<span data-ttu-id="4a8f7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8f7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a8f7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8f7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a8f7-130">INPUTS</span></span>

## <span data-ttu-id="4a8f7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a8f7-131">OUTPUTS</span></span>

### <span data-ttu-id="4a8f7-132">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="4a8f7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a8f7-133">NOTES</span></span>

## <span data-ttu-id="4a8f7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a8f7-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a8f7-135">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-140">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-141">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a8f7-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a8f7-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


