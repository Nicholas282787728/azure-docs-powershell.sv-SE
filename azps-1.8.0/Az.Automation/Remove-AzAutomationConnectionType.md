---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: ab8d51b4a1b7a66e90a61fa4903d9373dd98eb9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754767"
---
# <span data-ttu-id="45def-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="45def-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="45def-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45def-102">SYNOPSIS</span></span>
<span data-ttu-id="45def-103">Tar bort en typ av Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="45def-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="45def-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45def-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45def-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45def-105">DESCRIPTION</span></span>
<span data-ttu-id="45def-106">Cmdleten **Remove-AzAutomationConnectionType** tar bort en Anslutnings typ från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="45def-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="45def-107">Alla anslutningar som är kopplade till den Anslutnings typ du tar bort blir oanvändbara.</span><span class="sxs-lookup"><span data-stu-id="45def-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="45def-108">Ta bort dem, såvida du inte skapar en ny Anslutnings typ som uppfyller följande villkor:</span><span class="sxs-lookup"><span data-stu-id="45def-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="45def-109">Typen har samma namn som den ursprungliga anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="45def-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="45def-110">Typen har samma fält definitioner som den ursprungliga anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="45def-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="45def-111">Den kan innehålla ytterligare fält.</span><span class="sxs-lookup"><span data-stu-id="45def-111">It can have additional fields.</span></span>

## <span data-ttu-id="45def-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45def-112">EXAMPLES</span></span>

### <span data-ttu-id="45def-113">Exempel 1: ta bort en Anslutnings typ</span><span class="sxs-lookup"><span data-stu-id="45def-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="45def-114">Det här kommandot tar bort en Anslutnings typ med namnet ContosoConnectionType i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="45def-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="45def-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45def-115">PARAMETERS</span></span>

### <span data-ttu-id="45def-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="45def-116">-AutomationAccountName</span></span>
<span data-ttu-id="45def-117">Anger namnet på det Automation-konto som denna cmdlet tar bort en Anslutnings typ för.</span><span class="sxs-lookup"><span data-stu-id="45def-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="45def-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45def-118">-DefaultProfile</span></span>
<span data-ttu-id="45def-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="45def-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45def-120">-Force</span><span class="sxs-lookup"><span data-stu-id="45def-120">-Force</span></span>
<span data-ttu-id="45def-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="45def-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45def-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="45def-122">-Name</span></span>
<span data-ttu-id="45def-123">Anger namnet på den typ av Automation-anslutning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="45def-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45def-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45def-124">-ResourceGroupName</span></span>
<span data-ttu-id="45def-125">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en typ av Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="45def-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="45def-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45def-126">-Confirm</span></span>
<span data-ttu-id="45def-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45def-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45def-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45def-128">-WhatIf</span></span>
<span data-ttu-id="45def-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45def-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45def-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45def-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45def-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45def-131">CommonParameters</span></span>
<span data-ttu-id="45def-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45def-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45def-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45def-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45def-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45def-134">INPUTS</span></span>

### <span data-ttu-id="45def-135">System. String</span><span class="sxs-lookup"><span data-stu-id="45def-135">System.String</span></span>

## <span data-ttu-id="45def-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45def-136">OUTPUTS</span></span>

### <span data-ttu-id="45def-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="45def-137">System.Void</span></span>

## <span data-ttu-id="45def-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45def-138">NOTES</span></span>

## <span data-ttu-id="45def-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45def-139">RELATED LINKS</span></span>

[<span data-ttu-id="45def-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="45def-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


