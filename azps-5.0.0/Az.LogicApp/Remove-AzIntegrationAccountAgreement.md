---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273363"
---
# <span data-ttu-id="c3def-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c3def-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="c3def-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3def-102">SYNOPSIS</span></span>
<span data-ttu-id="c3def-103">Tar bort ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="c3def-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="c3def-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3def-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3def-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3def-105">DESCRIPTION</span></span>
<span data-ttu-id="c3def-106">Cmdleten **Remove-AzIntegrationAccountAgreement** tar bort ett integrerings konto avtal från en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c3def-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="c3def-107">Ange integrerings konto namn, resurs grupps namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="c3def-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="c3def-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="c3def-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c3def-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="c3def-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c3def-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="c3def-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c3def-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="c3def-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c3def-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3def-112">EXAMPLES</span></span>

### <span data-ttu-id="c3def-113">Exempel 1: ta bort ett integrerings konto avtal efter namn</span><span class="sxs-lookup"><span data-stu-id="c3def-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="c3def-114">Det här kommandot tar bort integrerings konto avtalet som heter IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="c3def-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="c3def-115">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c3def-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c3def-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3def-116">PARAMETERS</span></span>

### <span data-ttu-id="c3def-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c3def-117">-AgreementName</span></span>
<span data-ttu-id="c3def-118">Anger namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="c3def-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="c3def-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3def-119">-DefaultProfile</span></span>
<span data-ttu-id="c3def-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c3def-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3def-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c3def-121">-Force</span></span>
<span data-ttu-id="c3def-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c3def-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3def-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3def-123">-Name</span></span>
<span data-ttu-id="c3def-124">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="c3def-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c3def-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3def-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3def-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c3def-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c3def-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3def-127">-Confirm</span></span>
<span data-ttu-id="c3def-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3def-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3def-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3def-129">-WhatIf</span></span>
<span data-ttu-id="c3def-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3def-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3def-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3def-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3def-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3def-132">CommonParameters</span></span>
<span data-ttu-id="c3def-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3def-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3def-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3def-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3def-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3def-135">INPUTS</span></span>

### <span data-ttu-id="c3def-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c3def-136">System.String</span></span>

## <span data-ttu-id="c3def-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3def-137">OUTPUTS</span></span>

### <span data-ttu-id="c3def-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="c3def-138">System.Void</span></span>

## <span data-ttu-id="c3def-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3def-139">NOTES</span></span>

## <span data-ttu-id="c3def-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3def-140">RELATED LINKS</span></span>

[<span data-ttu-id="c3def-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c3def-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="c3def-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c3def-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="c3def-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c3def-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


