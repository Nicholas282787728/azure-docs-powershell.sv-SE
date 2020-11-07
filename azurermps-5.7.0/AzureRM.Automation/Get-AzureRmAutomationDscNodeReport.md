---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758343"
---
# <span data-ttu-id="119bc-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="119bc-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="119bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="119bc-102">SYNOPSIS</span></span>
<span data-ttu-id="119bc-103">Hämtar rapporter som skickas från en DSC-nod till Automation.</span><span class="sxs-lookup"><span data-stu-id="119bc-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="119bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="119bc-104">SYNTAX</span></span>

### <span data-ttu-id="119bc-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="119bc-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="119bc-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="119bc-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="119bc-107">ById</span><span class="sxs-lookup"><span data-stu-id="119bc-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="119bc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="119bc-108">DESCRIPTION</span></span>
<span data-ttu-id="119bc-109">Cmdleten **Get-AzureRmAutomationDscNodeReport** hämtar rapporter som skickas från en APS-nod med önskad tillstånds konfiguration (DSC) till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="119bc-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="119bc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="119bc-110">EXAMPLES</span></span>

### <span data-ttu-id="119bc-111">Exempel 1: Hämta alla rapporter för en DSC-nod</span><span class="sxs-lookup"><span data-stu-id="119bc-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="119bc-112">Det första kommandot får DSC-noden för den dator som heter Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="119bc-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="119bc-113">Kommandot lagrar det här objektet i $Node variabel.</span><span class="sxs-lookup"><span data-stu-id="119bc-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="119bc-114">Det andra kommandot får metadata för alla rapporter som skickas från DSC-noden med namnet Computer14 till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="119bc-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="119bc-115">Kommandot anger noden genom att använda egenskapen ID för $Node **-** objektet.</span><span class="sxs-lookup"><span data-stu-id="119bc-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="119bc-116">Exempel 2: Hämta en rapport för en DSC-nod efter rapport-ID</span><span class="sxs-lookup"><span data-stu-id="119bc-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="119bc-117">Det första kommandot får DSC-noden för den dator som heter Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="119bc-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="119bc-118">Kommandot lagrar det här objektet i $Node variabel.</span><span class="sxs-lookup"><span data-stu-id="119bc-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="119bc-119">Det andra kommandot får metadata för den rapport som identifieras av angivet ID som skickas från DSC-noden med namnet Computer14 till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="119bc-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="119bc-120">Exempel 3: hämta den senaste rapporten för en DSC-nod</span><span class="sxs-lookup"><span data-stu-id="119bc-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="119bc-121">Det första kommandot får DSC-noden för den dator som heter Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="119bc-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="119bc-122">Kommandot lagrar det här objektet i $Node variabel.</span><span class="sxs-lookup"><span data-stu-id="119bc-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="119bc-123">Det andra kommandot får metadata för den senaste rapporten som skickas från DSC-noden med namnet Computer14 till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="119bc-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="119bc-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="119bc-124">PARAMETERS</span></span>

### <span data-ttu-id="119bc-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="119bc-125">-AutomationAccountName</span></span>
<span data-ttu-id="119bc-126">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="119bc-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="119bc-127">Denna cmdlet exporterar rapporter för en DSC-nod som tillhör kontot som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="119bc-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="119bc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="119bc-128">-DefaultProfile</span></span>
<span data-ttu-id="119bc-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="119bc-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="119bc-130">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="119bc-130">-EndTime</span></span>
<span data-ttu-id="119bc-131">Anger en slut tid.</span><span class="sxs-lookup"><span data-stu-id="119bc-131">Specifies an end time.</span></span>
<span data-ttu-id="119bc-132">Denna cmdlet hämtar rapporter som automatiserats före denna tid.</span><span class="sxs-lookup"><span data-stu-id="119bc-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="119bc-133">-ID</span><span class="sxs-lookup"><span data-stu-id="119bc-133">-Id</span></span>
<span data-ttu-id="119bc-134">Anger det unika ID: t för den aktuella cmdleten för DSC-noden.</span><span class="sxs-lookup"><span data-stu-id="119bc-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="119bc-135">-Senaste</span><span class="sxs-lookup"><span data-stu-id="119bc-135">-Latest</span></span>
<span data-ttu-id="119bc-136">Anger att denna cmdlet endast får den senaste DSC-rapporten för angiven nod.</span><span class="sxs-lookup"><span data-stu-id="119bc-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="119bc-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="119bc-137">-NodeId</span></span>
<span data-ttu-id="119bc-138">Anger det unika ID: t för DSC-noden för vilken denna cmdlet hämtar rapporter.</span><span class="sxs-lookup"><span data-stu-id="119bc-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="119bc-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="119bc-139">-ResourceGroupName</span></span>
<span data-ttu-id="119bc-140">Anger namnet på en resurs grupp som innehåller DSC-noden för vilken denna cmdlet hämtar rapporter.</span><span class="sxs-lookup"><span data-stu-id="119bc-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="119bc-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="119bc-141">-StartTime</span></span>
<span data-ttu-id="119bc-142">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="119bc-142">Specifies a start time.</span></span>
<span data-ttu-id="119bc-143">Denna cmdlet får rapporter som automatiseras efter den här tiden.</span><span class="sxs-lookup"><span data-stu-id="119bc-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="119bc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119bc-144">CommonParameters</span></span>
<span data-ttu-id="119bc-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="119bc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119bc-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="119bc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119bc-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="119bc-147">INPUTS</span></span>

### <span data-ttu-id="119bc-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="119bc-148">None</span></span>
<span data-ttu-id="119bc-149">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="119bc-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="119bc-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="119bc-150">OUTPUTS</span></span>

### <span data-ttu-id="119bc-151">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="119bc-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="119bc-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="119bc-152">NOTES</span></span>

## <span data-ttu-id="119bc-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="119bc-153">RELATED LINKS</span></span>

[<span data-ttu-id="119bc-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="119bc-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="119bc-155">Exportera-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="119bc-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


