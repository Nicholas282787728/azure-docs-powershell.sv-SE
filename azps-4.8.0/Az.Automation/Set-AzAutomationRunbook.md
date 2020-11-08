---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101739"
---
# <span data-ttu-id="34e47-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="34e47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34e47-102">SYNOPSIS</span></span>
<span data-ttu-id="34e47-103">Ändrar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="34e47-103">Modifies a runbook.</span></span>

## <span data-ttu-id="34e47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34e47-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34e47-105">DESCRIPTION</span></span>
<span data-ttu-id="34e47-106">Cmdleten **set-AzAutomationRunbook** ändrar konfigurationen för en Azure Automation-RUNBOOK i APS.</span><span class="sxs-lookup"><span data-stu-id="34e47-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="34e47-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34e47-107">EXAMPLES</span></span>

### <span data-ttu-id="34e47-108">Exempel 1: Aktivera utförlig loggning för en Runbook</span><span class="sxs-lookup"><span data-stu-id="34e47-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="34e47-109">Det här kommandot aktiverar utförlig loggning för jobben i angiven Runbook i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="34e47-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="34e47-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34e47-110">PARAMETERS</span></span>

### <span data-ttu-id="34e47-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34e47-111">-AutomationAccountName</span></span>
<span data-ttu-id="34e47-112">Anger namnet på det Automation-konto som denna cmdlet ändrar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="34e47-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="34e47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e47-113">-DefaultProfile</span></span>
<span data-ttu-id="34e47-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34e47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34e47-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="34e47-115">-Description</span></span>
<span data-ttu-id="34e47-116">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="34e47-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="34e47-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="34e47-117">-LogProgress</span></span>
<span data-ttu-id="34e47-118">Anger om Runbook loggar status.</span><span class="sxs-lookup"><span data-stu-id="34e47-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="34e47-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="34e47-119">-LogVerbose</span></span>
<span data-ttu-id="34e47-120">Anger om loggning innehåller detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="34e47-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="34e47-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="34e47-121">-Name</span></span>
<span data-ttu-id="34e47-122">Anger namnet på den Runbook som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="34e47-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="34e47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e47-123">-ResourceGroupName</span></span>
<span data-ttu-id="34e47-124">Anger namnet på den resurs grupp för vilken denna cmdlet ändrar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="34e47-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="34e47-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="34e47-125">-Tag</span></span>
<span data-ttu-id="34e47-126">Runbook-taggarna.</span><span class="sxs-lookup"><span data-stu-id="34e47-126">The runbook tags.</span></span>

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

### <span data-ttu-id="34e47-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e47-127">CommonParameters</span></span>
<span data-ttu-id="34e47-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e47-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e47-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e47-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e47-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34e47-130">INPUTS</span></span>

### <span data-ttu-id="34e47-131">System. String</span><span class="sxs-lookup"><span data-stu-id="34e47-131">System.String</span></span>

### <span data-ttu-id="34e47-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="34e47-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="34e47-133">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34e47-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="34e47-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34e47-134">OUTPUTS</span></span>

### <span data-ttu-id="34e47-135">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="34e47-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="34e47-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34e47-136">NOTES</span></span>

## <span data-ttu-id="34e47-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34e47-137">RELATED LINKS</span></span>

[<span data-ttu-id="34e47-138">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-143">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="34e47-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34e47-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


