---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: 747ffdb9df955609a38718016af50bb5434c0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756723"
---
# <span data-ttu-id="bda17-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="bda17-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="bda17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bda17-102">SYNOPSIS</span></span>
<span data-ttu-id="bda17-103">Hämtar rapporter som skickas från en DSC-nod till Automation.</span><span class="sxs-lookup"><span data-stu-id="bda17-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bda17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bda17-104">SYNTAX</span></span>

### <span data-ttu-id="bda17-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="bda17-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bda17-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="bda17-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bda17-107">ById</span><span class="sxs-lookup"><span data-stu-id="bda17-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bda17-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bda17-108">DESCRIPTION</span></span>
<span data-ttu-id="bda17-109">Cmdleten **Get-AzureRmAutomationDscNodeReport** hämtar rapporter som skickas från en APS-nod med önskad tillstånds konfiguration (DSC) till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bda17-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="bda17-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bda17-110">EXAMPLES</span></span>

### <span data-ttu-id="bda17-111">Exempel 1: Hämta alla rapporter för en DSC-nod</span><span class="sxs-lookup"><span data-stu-id="bda17-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="bda17-112">Det första kommandot får DSC-noden för den dator som heter Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bda17-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="bda17-113">Kommandot lagrar det här objektet i $Node variabel.</span><span class="sxs-lookup"><span data-stu-id="bda17-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="bda17-114">Det andra kommandot får metadata för alla rapporter som skickas från DSC-noden med namnet Computer14 till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bda17-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="bda17-115">Kommandot anger noden genom att använda egenskapen ID för $Node **-** objektet.</span><span class="sxs-lookup"><span data-stu-id="bda17-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="bda17-116">Exempel 2: Hämta en rapport för en DSC-nod efter rapport-ID</span><span class="sxs-lookup"><span data-stu-id="bda17-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="bda17-117">Det första kommandot får DSC-noden för den dator som heter Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bda17-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="bda17-118">Kommandot lagrar det här objektet i $Node variabel.</span><span class="sxs-lookup"><span data-stu-id="bda17-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="bda17-119">Det andra kommandot får metadata för den rapport som identifieras av angivet ID som skickas från DSC-noden med namnet Computer14 till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bda17-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bda17-120">Exempel 3: hämta den senaste rapporten för en DSC-nod</span><span class="sxs-lookup"><span data-stu-id="bda17-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="bda17-121">Det första kommandot får DSC-noden för den dator som heter Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bda17-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="bda17-122">Kommandot lagrar det här objektet i $Node variabel.</span><span class="sxs-lookup"><span data-stu-id="bda17-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="bda17-123">Det andra kommandot får metadata för den senaste rapporten som skickas från DSC-noden med namnet Computer14 till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bda17-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bda17-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bda17-124">PARAMETERS</span></span>

### <span data-ttu-id="bda17-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bda17-125">-AutomationAccountName</span></span>
<span data-ttu-id="bda17-126">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="bda17-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="bda17-127">Denna cmdlet exporterar rapporter för en DSC-nod som tillhör kontot som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bda17-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="bda17-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda17-128">-DefaultProfile</span></span>
<span data-ttu-id="bda17-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bda17-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bda17-130">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="bda17-130">-EndTime</span></span>
<span data-ttu-id="bda17-131">Anger en slut tid.</span><span class="sxs-lookup"><span data-stu-id="bda17-131">Specifies an end time.</span></span>
<span data-ttu-id="bda17-132">Denna cmdlet hämtar rapporter som automatiserats före denna tid.</span><span class="sxs-lookup"><span data-stu-id="bda17-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda17-133">-ID</span><span class="sxs-lookup"><span data-stu-id="bda17-133">-Id</span></span>
<span data-ttu-id="bda17-134">Anger det unika ID: t för den aktuella cmdleten för DSC-noden.</span><span class="sxs-lookup"><span data-stu-id="bda17-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda17-135">-Senaste</span><span class="sxs-lookup"><span data-stu-id="bda17-135">-Latest</span></span>
<span data-ttu-id="bda17-136">Anger att denna cmdlet endast får den senaste DSC-rapporten för angiven nod.</span><span class="sxs-lookup"><span data-stu-id="bda17-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda17-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="bda17-137">-NodeId</span></span>
<span data-ttu-id="bda17-138">Anger det unika ID: t för DSC-noden för vilken denna cmdlet hämtar rapporter.</span><span class="sxs-lookup"><span data-stu-id="bda17-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda17-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda17-139">-ResourceGroupName</span></span>
<span data-ttu-id="bda17-140">Anger namnet på en resurs grupp som innehåller DSC-noden för vilken denna cmdlet hämtar rapporter.</span><span class="sxs-lookup"><span data-stu-id="bda17-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="bda17-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bda17-141">-StartTime</span></span>
<span data-ttu-id="bda17-142">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="bda17-142">Specifies a start time.</span></span>
<span data-ttu-id="bda17-143">Denna cmdlet får rapporter som automatiseras efter den här tiden.</span><span class="sxs-lookup"><span data-stu-id="bda17-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda17-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda17-144">CommonParameters</span></span>
<span data-ttu-id="bda17-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda17-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda17-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda17-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda17-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bda17-147">INPUTS</span></span>

### <span data-ttu-id="bda17-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bda17-148">System.Guid</span></span>

### <span data-ttu-id="bda17-149">System. Nullable ' 1 [[system. DateTimeOffset, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bda17-149">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bda17-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bda17-150">System.String</span></span>

## <span data-ttu-id="bda17-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bda17-151">OUTPUTS</span></span>

### <span data-ttu-id="bda17-152">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="bda17-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="bda17-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bda17-153">NOTES</span></span>

## <span data-ttu-id="bda17-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bda17-154">RELATED LINKS</span></span>

[<span data-ttu-id="bda17-155">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="bda17-155">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="bda17-156">Exportera-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="bda17-156">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

