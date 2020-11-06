---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 409a1eca9083c51f501293e4ca37150ce0c328e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578520"
---
# <span data-ttu-id="33dd6-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="33dd6-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="33dd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="33dd6-103">Tar bort en typ av Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="33dd6-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33dd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33dd6-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33dd6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="33dd6-106">Cmdleten **Remove-AzureRmAutomationConnectionType** tar bort en Anslutnings typ från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="33dd6-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="33dd6-107">Alla anslutningar som är kopplade till den Anslutnings typ du tar bort blir oanvändbara.</span><span class="sxs-lookup"><span data-stu-id="33dd6-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="33dd6-108">Ta bort dem, såvida du inte skapar en ny Anslutnings typ som uppfyller följande villkor:</span><span class="sxs-lookup"><span data-stu-id="33dd6-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="33dd6-109">Typen har samma namn som den ursprungliga anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="33dd6-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="33dd6-110">Typen har samma fält definitioner som den ursprungliga anslutnings typen.</span><span class="sxs-lookup"><span data-stu-id="33dd6-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="33dd6-111">Den kan innehålla ytterligare fält.</span><span class="sxs-lookup"><span data-stu-id="33dd6-111">It can have additional fields.</span></span>

## <span data-ttu-id="33dd6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33dd6-112">EXAMPLES</span></span>

### <span data-ttu-id="33dd6-113">Exempel 1: ta bort en Anslutnings typ</span><span class="sxs-lookup"><span data-stu-id="33dd6-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="33dd6-114">Det här kommandot tar bort en Anslutnings typ med namnet ContosoConnectionType i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="33dd6-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="33dd6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33dd6-115">PARAMETERS</span></span>

### <span data-ttu-id="33dd6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33dd6-116">-AutomationAccountName</span></span>
<span data-ttu-id="33dd6-117">Anger namnet på det Automation-konto som denna cmdlet tar bort en Anslutnings typ för.</span><span class="sxs-lookup"><span data-stu-id="33dd6-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="33dd6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="33dd6-118">-Force</span></span>
<span data-ttu-id="33dd6-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="33dd6-119">ps_force</span></span>

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

### <span data-ttu-id="33dd6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="33dd6-120">-Name</span></span>
<span data-ttu-id="33dd6-121">Anger namnet på den typ av Automation-anslutning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="33dd6-121">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="33dd6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33dd6-122">-ResourceGroupName</span></span>
<span data-ttu-id="33dd6-123">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en typ av Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="33dd6-123">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="33dd6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33dd6-124">-Confirm</span></span>
<span data-ttu-id="33dd6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33dd6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33dd6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33dd6-126">-WhatIf</span></span>
<span data-ttu-id="33dd6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33dd6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33dd6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33dd6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33dd6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dd6-129">-DefaultProfile</span></span>
<span data-ttu-id="33dd6-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33dd6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33dd6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dd6-131">CommonParameters</span></span>
<span data-ttu-id="33dd6-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33dd6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dd6-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33dd6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dd6-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33dd6-134">INPUTS</span></span>

## <span data-ttu-id="33dd6-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33dd6-135">OUTPUTS</span></span>

## <span data-ttu-id="33dd6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33dd6-136">NOTES</span></span>

## <span data-ttu-id="33dd6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33dd6-137">RELATED LINKS</span></span>

[<span data-ttu-id="33dd6-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="33dd6-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


