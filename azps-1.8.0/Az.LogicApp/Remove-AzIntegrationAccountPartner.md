---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: d630a88134b2910a38b21ff964db9748db5cbeeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915997"
---
# <span data-ttu-id="62726-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="62726-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="62726-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62726-102">SYNOPSIS</span></span>
<span data-ttu-id="62726-103">Tar bort en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="62726-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="62726-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62726-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62726-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62726-105">DESCRIPTION</span></span>
<span data-ttu-id="62726-106">Cmdleten **Remove-AzIntegrationAccountPartner** tar bort en integrerings konto partner från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62726-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="62726-107">Ange integrerings konto namn, resurs grupps namn och partner namn.</span><span class="sxs-lookup"><span data-stu-id="62726-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="62726-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="62726-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="62726-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="62726-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="62726-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="62726-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="62726-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="62726-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="62726-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62726-112">EXAMPLES</span></span>

### <span data-ttu-id="62726-113">Exempel 1: ta bort en integrerings konto partner</span><span class="sxs-lookup"><span data-stu-id="62726-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="62726-114">Det här kommandot tar bort integrerings konto partnern med namnet IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="62726-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="62726-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62726-115">PARAMETERS</span></span>

### <span data-ttu-id="62726-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62726-116">-DefaultProfile</span></span>
<span data-ttu-id="62726-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62726-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62726-118">-Force</span><span class="sxs-lookup"><span data-stu-id="62726-118">-Force</span></span>
<span data-ttu-id="62726-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="62726-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62726-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="62726-120">-Name</span></span>
<span data-ttu-id="62726-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="62726-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="62726-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="62726-122">-PartnerName</span></span>
<span data-ttu-id="62726-123">Anger namnet på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="62726-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="62726-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62726-124">-ResourceGroupName</span></span>
<span data-ttu-id="62726-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62726-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="62726-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62726-126">-Confirm</span></span>
<span data-ttu-id="62726-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62726-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62726-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62726-128">-WhatIf</span></span>
<span data-ttu-id="62726-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62726-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62726-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62726-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62726-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62726-131">CommonParameters</span></span>
<span data-ttu-id="62726-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62726-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62726-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62726-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62726-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62726-134">INPUTS</span></span>

### <span data-ttu-id="62726-135">System. String</span><span class="sxs-lookup"><span data-stu-id="62726-135">System.String</span></span>

## <span data-ttu-id="62726-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62726-136">OUTPUTS</span></span>

### <span data-ttu-id="62726-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="62726-137">System.Void</span></span>

## <span data-ttu-id="62726-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62726-138">NOTES</span></span>

## <span data-ttu-id="62726-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62726-139">RELATED LINKS</span></span>

[<span data-ttu-id="62726-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="62726-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="62726-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="62726-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="62726-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="62726-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


