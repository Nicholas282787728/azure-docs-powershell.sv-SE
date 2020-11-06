---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: eaa1195e5cb853111b6e75efbff7e37bc8ff6881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572960"
---
# <span data-ttu-id="11e49-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="11e49-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="11e49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11e49-102">SYNOPSIS</span></span>
<span data-ttu-id="11e49-103">Ändrar den noduppsättning som en DSC-nod är mappad till.</span><span class="sxs-lookup"><span data-stu-id="11e49-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11e49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11e49-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11e49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11e49-105">DESCRIPTION</span></span>
<span data-ttu-id="11e49-106">Cmdleten **set-AzureRmAutomationDscNode** ändrar en konfiguration för DSC-nodkonfigurationer (önskad konfiguration för en APS).</span><span class="sxs-lookup"><span data-stu-id="11e49-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="11e49-107">Azure Automation lagrar DSC-nodkonfigurationer som ett MOF-konfigurationsobjekt (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="11e49-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="11e49-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11e49-108">EXAMPLES</span></span>

### <span data-ttu-id="11e49-109">Exempel 1: ändra mappning av Nodinstans</span><span class="sxs-lookup"><span data-stu-id="11e49-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="11e49-110">Det här kommandot tilldelar noduppsättningen namnet contoso. NodeConfiguration01 till noden med angiven GUID.</span><span class="sxs-lookup"><span data-stu-id="11e49-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="11e49-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11e49-111">PARAMETERS</span></span>

### <span data-ttu-id="11e49-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11e49-112">-AutomationAccountName</span></span>
<span data-ttu-id="11e49-113">Anger namnet på det Automation-konto som innehåller DSC-noden för vilken denna cmdlet ändrar konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="11e49-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="11e49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e49-114">-DefaultProfile</span></span>
<span data-ttu-id="11e49-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="11e49-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11e49-116">-Force</span><span class="sxs-lookup"><span data-stu-id="11e49-116">-Force</span></span>
<span data-ttu-id="11e49-117">ps_force kommandot för att köra utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="11e49-117">ps_force the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e49-118">-ID</span><span class="sxs-lookup"><span data-stu-id="11e49-118">-Id</span></span>
<span data-ttu-id="11e49-119">Anger det unika ID: t för DSC-noden för vilken denna cmdlet ändrar konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="11e49-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e49-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="11e49-120">-NodeConfigurationName</span></span>
<span data-ttu-id="11e49-121">Anger namnet på den nod som den här cmdleten mappar till för att mappa noden.</span><span class="sxs-lookup"><span data-stu-id="11e49-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e49-122">-ResourceGroupName</span></span>
<span data-ttu-id="11e49-123">Anger namnet på en resurs grupp där denna cmdlet ändrar en DSC-noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="11e49-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="11e49-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11e49-124">-Confirm</span></span>
<span data-ttu-id="11e49-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11e49-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e49-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e49-126">-WhatIf</span></span>
<span data-ttu-id="11e49-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11e49-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e49-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11e49-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e49-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e49-129">CommonParameters</span></span>
<span data-ttu-id="11e49-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e49-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e49-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e49-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e49-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11e49-132">INPUTS</span></span>

### <span data-ttu-id="11e49-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="11e49-133">System.Guid</span></span>

### <span data-ttu-id="11e49-134">System. String</span><span class="sxs-lookup"><span data-stu-id="11e49-134">System.String</span></span>

## <span data-ttu-id="11e49-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11e49-135">OUTPUTS</span></span>

### <span data-ttu-id="11e49-136">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="11e49-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="11e49-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11e49-137">NOTES</span></span>

## <span data-ttu-id="11e49-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11e49-138">RELATED LINKS</span></span>

[<span data-ttu-id="11e49-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="11e49-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="11e49-140">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="11e49-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="11e49-141">Avregistrera-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="11e49-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


