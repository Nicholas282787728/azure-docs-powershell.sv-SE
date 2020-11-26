---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259541"
---
# <span data-ttu-id="04246-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="04246-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="04246-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04246-102">SYNOPSIS</span></span>
<span data-ttu-id="04246-103">Tar bort en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="04246-103">Removes an integration account map.</span></span>

## <span data-ttu-id="04246-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04246-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04246-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04246-105">DESCRIPTION</span></span>
<span data-ttu-id="04246-106">Cmdleten **Remove-AzIntegrationAccountMap** tar bort en integrerings konto översikt från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="04246-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="04246-107">Ange integrerings konto namnet, resurs gruppens namn och kartans namn.</span><span class="sxs-lookup"><span data-stu-id="04246-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="04246-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="04246-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="04246-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="04246-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="04246-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="04246-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="04246-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="04246-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="04246-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04246-112">EXAMPLES</span></span>

### <span data-ttu-id="04246-113">Exempel 1: ta bort en integrerings konto karta</span><span class="sxs-lookup"><span data-stu-id="04246-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="04246-114">Det här kommandot tar bort integrerings konto översikten med namnet IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="04246-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="04246-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04246-115">PARAMETERS</span></span>

### <span data-ttu-id="04246-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04246-116">-DefaultProfile</span></span>
<span data-ttu-id="04246-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="04246-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04246-118">-Force</span><span class="sxs-lookup"><span data-stu-id="04246-118">-Force</span></span>
<span data-ttu-id="04246-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="04246-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04246-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="04246-120">-MapName</span></span>
<span data-ttu-id="04246-121">Anger namnet på integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="04246-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04246-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="04246-122">-Name</span></span>
<span data-ttu-id="04246-123">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="04246-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04246-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04246-124">-ResourceGroupName</span></span>
<span data-ttu-id="04246-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="04246-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="04246-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04246-126">-Confirm</span></span>
<span data-ttu-id="04246-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04246-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04246-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04246-128">-WhatIf</span></span>
<span data-ttu-id="04246-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04246-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04246-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04246-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04246-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04246-131">CommonParameters</span></span>
<span data-ttu-id="04246-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04246-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04246-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04246-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04246-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04246-134">INPUTS</span></span>

### <span data-ttu-id="04246-135">System. String</span><span class="sxs-lookup"><span data-stu-id="04246-135">System.String</span></span>

## <span data-ttu-id="04246-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04246-136">OUTPUTS</span></span>

### <span data-ttu-id="04246-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="04246-137">System.Void</span></span>

## <span data-ttu-id="04246-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04246-138">NOTES</span></span>

## <span data-ttu-id="04246-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04246-139">RELATED LINKS</span></span>

[<span data-ttu-id="04246-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="04246-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="04246-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="04246-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="04246-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="04246-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)

