---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 6fa6b5b9bd7d73c0a2f5ea42b7878e9ce00cf6ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586408"
---
# <span data-ttu-id="00e40-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="00e40-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="00e40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00e40-102">SYNOPSIS</span></span>
<span data-ttu-id="00e40-103">Hämtar DSC-noder från Automation.</span><span class="sxs-lookup"><span data-stu-id="00e40-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00e40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00e40-104">SYNTAX</span></span>

### <span data-ttu-id="00e40-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="00e40-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00e40-106">ById</span><span class="sxs-lookup"><span data-stu-id="00e40-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00e40-107">ByName</span><span class="sxs-lookup"><span data-stu-id="00e40-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00e40-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="00e40-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00e40-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="00e40-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00e40-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00e40-110">DESCRIPTION</span></span>
<span data-ttu-id="00e40-111">Cmdleten **Get-AzureRmAutomationDscNode** får AP-noder (Desired State Configuration) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="00e40-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="00e40-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00e40-112">EXAMPLES</span></span>

### <span data-ttu-id="00e40-113">Exempel 1: Hämta alla DSC-noder</span><span class="sxs-lookup"><span data-stu-id="00e40-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="00e40-114">Det här kommandot får metadata för alla DSC-noder i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00e40-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="00e40-115">Exempel 2: Hämta alla DSC-noder för en DSC-konfiguration</span><span class="sxs-lookup"><span data-stu-id="00e40-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="00e40-116">Det här kommandot får metadata för alla DSC-noder i Automation-kontot med namnet Contoso17 som mappats till en DSC-noduppsättning som genererades av DSC Configuration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="00e40-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="00e40-117">Exempel 3: Hämta en DSC-nod efter ID</span><span class="sxs-lookup"><span data-stu-id="00e40-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="00e40-118">Det här kommandot får metadata på en DSC-nod med angivet ID i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00e40-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="00e40-119">Exempel 4: Hämta en DSC-nod efter namn</span><span class="sxs-lookup"><span data-stu-id="00e40-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="00e40-120">Det här kommandot får metadata på en DSC-nod med namnet Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00e40-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="00e40-121">Exempel 5: Hämta alla DSC-noder som mappats till en DSC-nodkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="00e40-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="00e40-122">Det här kommandot får metadata på alla DSC-noder i Automation-kontot som heter Contoso17 och som har mappats till en DSC-nodadress med namnet ContosoConfiguration. webserver.</span><span class="sxs-lookup"><span data-stu-id="00e40-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="00e40-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00e40-123">PARAMETERS</span></span>

### <span data-ttu-id="00e40-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00e40-124">-AutomationAccountName</span></span>
<span data-ttu-id="00e40-125">Anger namnet på det Automation-konto som innehåller de DSC-noder som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="00e40-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00e40-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="00e40-126">-ConfigurationName</span></span>
<span data-ttu-id="00e40-127">Anger namnet på en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="00e40-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="00e40-128">Denna cmdlet får DSC-noder som matchar de nodkonfigurationer som genereras från den konfiguration som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="00e40-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e40-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e40-129">-DefaultProfile</span></span>
<span data-ttu-id="00e40-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00e40-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00e40-131">-ID</span><span class="sxs-lookup"><span data-stu-id="00e40-131">-Id</span></span>
<span data-ttu-id="00e40-132">Anger det unika ID: t för DSC-noden som denna cmdlet hämtar.</span><span class="sxs-lookup"><span data-stu-id="00e40-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e40-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="00e40-133">-Name</span></span>
<span data-ttu-id="00e40-134">Anger namnet på en DSC-nod som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="00e40-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e40-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="00e40-135">-NodeConfigurationName</span></span>
<span data-ttu-id="00e40-136">Anger namnet på en noduppsättning som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="00e40-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e40-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e40-137">-ResourceGroupName</span></span>
<span data-ttu-id="00e40-138">Anger namnet på en resurs grupp där denna cmdlet får DSC-noder.</span><span class="sxs-lookup"><span data-stu-id="00e40-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="00e40-139">-Status</span><span class="sxs-lookup"><span data-stu-id="00e40-139">-Status</span></span>
<span data-ttu-id="00e40-140">Anger statusen för de DSC-noder som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="00e40-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="00e40-141">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="00e40-141">Valid values are:</span></span> 

- <span data-ttu-id="00e40-142">Villkor</span><span class="sxs-lookup"><span data-stu-id="00e40-142">Compliant</span></span> 
- <span data-ttu-id="00e40-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="00e40-143">NotCompliant</span></span>
- <span data-ttu-id="00e40-144">Startade</span><span class="sxs-lookup"><span data-stu-id="00e40-144">Failed</span></span>
- <span data-ttu-id="00e40-145">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="00e40-145">Pending</span></span> 
- <span data-ttu-id="00e40-146">Leverans</span><span class="sxs-lookup"><span data-stu-id="00e40-146">Received</span></span>
- <span data-ttu-id="00e40-147">Svara</span><span class="sxs-lookup"><span data-stu-id="00e40-147">Unresponsive</span></span>

```yaml
Type: DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases: 
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e40-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e40-148">CommonParameters</span></span>
<span data-ttu-id="00e40-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e40-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e40-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e40-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e40-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00e40-151">INPUTS</span></span>

### <span data-ttu-id="00e40-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="00e40-152">None</span></span>
<span data-ttu-id="00e40-153">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="00e40-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00e40-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00e40-154">OUTPUTS</span></span>

### <span data-ttu-id="00e40-155">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="00e40-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="00e40-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00e40-156">NOTES</span></span>

## <span data-ttu-id="00e40-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00e40-157">RELATED LINKS</span></span>

[<span data-ttu-id="00e40-158">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="00e40-158">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="00e40-159">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="00e40-159">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="00e40-160">Avregistrera-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="00e40-160">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


