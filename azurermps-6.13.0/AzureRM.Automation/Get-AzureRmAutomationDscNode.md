---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: a902c88c53736f1e0db238cdb53ea381e5e887a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572996"
---
# <span data-ttu-id="54d00-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="54d00-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="54d00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54d00-102">SYNOPSIS</span></span>
<span data-ttu-id="54d00-103">Hämtar DSC-noder från Automation.</span><span class="sxs-lookup"><span data-stu-id="54d00-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54d00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54d00-104">SYNTAX</span></span>

### <span data-ttu-id="54d00-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="54d00-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54d00-106">ById</span><span class="sxs-lookup"><span data-stu-id="54d00-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54d00-107">ByName</span><span class="sxs-lookup"><span data-stu-id="54d00-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54d00-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="54d00-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54d00-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="54d00-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54d00-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54d00-110">DESCRIPTION</span></span>
<span data-ttu-id="54d00-111">Cmdleten **Get-AzureRmAutomationDscNode** får AP-noder (Desired State Configuration) från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="54d00-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="54d00-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54d00-112">EXAMPLES</span></span>

### <span data-ttu-id="54d00-113">Exempel 1: Hämta alla DSC-noder</span><span class="sxs-lookup"><span data-stu-id="54d00-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="54d00-114">Det här kommandot får metadata för alla DSC-noder i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54d00-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="54d00-115">Exempel 2: Hämta alla DSC-noder för en DSC-konfiguration</span><span class="sxs-lookup"><span data-stu-id="54d00-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="54d00-116">Det här kommandot får metadata för alla DSC-noder i Automation-kontot med namnet Contoso17 som mappats till en DSC-noduppsättning som genererades av DSC Configuration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="54d00-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="54d00-117">Exempel 3: Hämta en DSC-nod efter ID</span><span class="sxs-lookup"><span data-stu-id="54d00-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="54d00-118">Det här kommandot får metadata på en DSC-nod med angivet ID i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54d00-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="54d00-119">Exempel 4: Hämta en DSC-nod efter namn</span><span class="sxs-lookup"><span data-stu-id="54d00-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="54d00-120">Det här kommandot får metadata på en DSC-nod med namnet Computer14 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54d00-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="54d00-121">Exempel 5: Hämta alla DSC-noder som mappats till en DSC-nodkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="54d00-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="54d00-122">Det här kommandot får metadata på alla DSC-noder i Automation-kontot som heter Contoso17 och som har mappats till en DSC-nodadress med namnet ContosoConfiguration. webserver.</span><span class="sxs-lookup"><span data-stu-id="54d00-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="54d00-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54d00-123">PARAMETERS</span></span>

### <span data-ttu-id="54d00-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54d00-124">-AutomationAccountName</span></span>
<span data-ttu-id="54d00-125">Anger namnet på det Automation-konto som innehåller de DSC-noder som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="54d00-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="54d00-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="54d00-126">-ConfigurationName</span></span>
<span data-ttu-id="54d00-127">Anger namnet på en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="54d00-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="54d00-128">Denna cmdlet får DSC-noder som matchar de nodkonfigurationer som genereras från den konfiguration som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="54d00-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d00-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d00-129">-DefaultProfile</span></span>
<span data-ttu-id="54d00-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54d00-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54d00-131">-ID</span><span class="sxs-lookup"><span data-stu-id="54d00-131">-Id</span></span>
<span data-ttu-id="54d00-132">Anger det unika ID: t för DSC-noden som denna cmdlet hämtar.</span><span class="sxs-lookup"><span data-stu-id="54d00-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54d00-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="54d00-133">-Name</span></span>
<span data-ttu-id="54d00-134">Anger namnet på en DSC-nod som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="54d00-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54d00-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="54d00-135">-NodeConfigurationName</span></span>
<span data-ttu-id="54d00-136">Anger namnet på en noduppsättning som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="54d00-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d00-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d00-137">-ResourceGroupName</span></span>
<span data-ttu-id="54d00-138">Anger namnet på en resurs grupp där denna cmdlet får DSC-noder.</span><span class="sxs-lookup"><span data-stu-id="54d00-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="54d00-139">-Status</span><span class="sxs-lookup"><span data-stu-id="54d00-139">-Status</span></span>
<span data-ttu-id="54d00-140">Anger statusen för de DSC-noder som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="54d00-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="54d00-141">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="54d00-141">Valid values are:</span></span> 
- <span data-ttu-id="54d00-142">Villkor</span><span class="sxs-lookup"><span data-stu-id="54d00-142">Compliant</span></span> 
- <span data-ttu-id="54d00-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="54d00-143">NotCompliant</span></span>
- <span data-ttu-id="54d00-144">Startade</span><span class="sxs-lookup"><span data-stu-id="54d00-144">Failed</span></span>
- <span data-ttu-id="54d00-145">OAvsluta</span><span class="sxs-lookup"><span data-stu-id="54d00-145">Pending</span></span> 
- <span data-ttu-id="54d00-146">Leverans</span><span class="sxs-lookup"><span data-stu-id="54d00-146">Received</span></span>
- <span data-ttu-id="54d00-147">Svara</span><span class="sxs-lookup"><span data-stu-id="54d00-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d00-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d00-148">CommonParameters</span></span>
<span data-ttu-id="54d00-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d00-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d00-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d00-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d00-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54d00-151">INPUTS</span></span>

### <span data-ttu-id="54d00-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="54d00-152">System.Guid</span></span>

### <span data-ttu-id="54d00-153">System. String</span><span class="sxs-lookup"><span data-stu-id="54d00-153">System.String</span></span>

## <span data-ttu-id="54d00-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54d00-154">OUTPUTS</span></span>

### <span data-ttu-id="54d00-155">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="54d00-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="54d00-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54d00-156">NOTES</span></span>

## <span data-ttu-id="54d00-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54d00-157">RELATED LINKS</span></span>

[<span data-ttu-id="54d00-158">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="54d00-158">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="54d00-159">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="54d00-159">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="54d00-160">Avregistrera-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="54d00-160">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


