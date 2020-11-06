---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: 5a47676a7c01052f44acba6362bd24eb65e4c05f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582843"
---
# <span data-ttu-id="f7e32-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="f7e32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7e32-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e32-103">Hämtar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="f7e32-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7e32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7e32-104">SYNTAX</span></span>

### <span data-ttu-id="f7e32-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="f7e32-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7e32-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="f7e32-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7e32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7e32-107">DESCRIPTION</span></span>
<span data-ttu-id="f7e32-108">Cmdleten **Get-AzureRmAutomationRunbook** får Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="f7e32-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="f7e32-109">Ange namnet på en viss Runbook.</span><span class="sxs-lookup"><span data-stu-id="f7e32-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="f7e32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7e32-110">EXAMPLES</span></span>

### <span data-ttu-id="f7e32-111">Exempel 1: Hämta alla Runbooks</span><span class="sxs-lookup"><span data-stu-id="f7e32-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f7e32-112">Det här kommandot får alla Runbooks i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f7e32-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f7e32-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7e32-113">PARAMETERS</span></span>

### <span data-ttu-id="f7e32-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7e32-114">-AutomationAccountName</span></span>
<span data-ttu-id="f7e32-115">Anger namnet på ett Automation-konto där denna cmdlet får Runbooks.</span><span class="sxs-lookup"><span data-stu-id="f7e32-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="f7e32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e32-116">-DefaultProfile</span></span>
<span data-ttu-id="f7e32-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f7e32-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7e32-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7e32-118">-Name</span></span>
<span data-ttu-id="f7e32-119">Anger namnet på en Runbook som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="f7e32-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f7e32-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e32-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7e32-121">Anger namnet på den resurs grupp för vilken denna cmdlet får Runbooks.</span><span class="sxs-lookup"><span data-stu-id="f7e32-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="f7e32-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e32-122">CommonParameters</span></span>
<span data-ttu-id="f7e32-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e32-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e32-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7e32-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e32-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7e32-125">INPUTS</span></span>

### <span data-ttu-id="f7e32-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f7e32-126">System.String</span></span>

## <span data-ttu-id="f7e32-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7e32-127">OUTPUTS</span></span>

### <span data-ttu-id="f7e32-128">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f7e32-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7e32-129">NOTES</span></span>

## <span data-ttu-id="f7e32-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7e32-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7e32-131">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-131">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-132">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-132">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-133">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-134">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-135">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-135">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-136">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-136">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-137">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-137">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f7e32-138">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7e32-138">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


