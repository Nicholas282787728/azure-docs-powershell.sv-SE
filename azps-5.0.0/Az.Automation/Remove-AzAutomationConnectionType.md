---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321816"
---
# <span data-ttu-id="cb964-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="cb964-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="cb964-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb964-102">SYNOPSIS</span></span>
<span data-ttu-id="cb964-103">Tar bort en typ av Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="cb964-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="cb964-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb964-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb964-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb964-105">DESCRIPTION</span></span>
<span data-ttu-id="cb964-106">Cmdleten **Remove-AzAutomationConnectionType** tar bort en Anslutnings typ från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cb964-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="cb964-107">Alla anslutningar som är kopplade till den Anslutnings typ du tar bort blir oanvändbara.</span><span class="sxs-lookup"><span data-stu-id="cb964-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="cb964-108">Ta bort dem, såvida du inte skapar en ny Anslutnings typ som uppfyller följande villkor:</span><span class="sxs-lookup"><span data-stu-id="cb964-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="cb964-109">Typen har samma namn som den ursprungliga anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="cb964-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="cb964-110">Typen har samma fält definitioner som den ursprungliga anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="cb964-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="cb964-111">Den kan innehålla ytterligare fält.</span><span class="sxs-lookup"><span data-stu-id="cb964-111">It can have additional fields.</span></span>

## <span data-ttu-id="cb964-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb964-112">EXAMPLES</span></span>

### <span data-ttu-id="cb964-113">Exempel 1: ta bort en Anslutnings typ</span><span class="sxs-lookup"><span data-stu-id="cb964-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cb964-114">Det här kommandot tar bort en Anslutnings typ med namnet ContosoConnectionType i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cb964-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cb964-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb964-115">PARAMETERS</span></span>

### <span data-ttu-id="cb964-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb964-116">-AutomationAccountName</span></span>
<span data-ttu-id="cb964-117">Anger namnet på det Automation-konto som denna cmdlet tar bort en Anslutnings typ för.</span><span class="sxs-lookup"><span data-stu-id="cb964-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="cb964-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb964-118">-DefaultProfile</span></span>
<span data-ttu-id="cb964-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cb964-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb964-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cb964-120">-Force</span></span>
<span data-ttu-id="cb964-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="cb964-121">ps_force</span></span>

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

### <span data-ttu-id="cb964-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb964-122">-Name</span></span>
<span data-ttu-id="cb964-123">Anger namnet på den typ av Automation-anslutning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cb964-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cb964-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb964-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb964-125">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en typ av Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="cb964-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="cb964-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb964-126">-Confirm</span></span>
<span data-ttu-id="cb964-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb964-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb964-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb964-128">-WhatIf</span></span>
<span data-ttu-id="cb964-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb964-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb964-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb964-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb964-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb964-131">CommonParameters</span></span>
<span data-ttu-id="cb964-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb964-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb964-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb964-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb964-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb964-134">INPUTS</span></span>

### <span data-ttu-id="cb964-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cb964-135">System.String</span></span>

## <span data-ttu-id="cb964-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb964-136">OUTPUTS</span></span>

### <span data-ttu-id="cb964-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="cb964-137">System.Void</span></span>

## <span data-ttu-id="cb964-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb964-138">NOTES</span></span>

## <span data-ttu-id="cb964-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb964-139">RELATED LINKS</span></span>

[<span data-ttu-id="cb964-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cb964-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)

