---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581412"
---
# <span data-ttu-id="58bad-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="58bad-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="58bad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58bad-102">SYNOPSIS</span></span>
<span data-ttu-id="58bad-103">Tar bort ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="58bad-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58bad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58bad-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58bad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58bad-105">DESCRIPTION</span></span>
<span data-ttu-id="58bad-106">Cmdleten **Remove-AzureRmIntegrationAccountAgreement** tar bort ett integrerings konto avtal från en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58bad-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="58bad-107">Ange integrerings konto namn, resurs grupps namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="58bad-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="58bad-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="58bad-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="58bad-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="58bad-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="58bad-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="58bad-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="58bad-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="58bad-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="58bad-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58bad-112">EXAMPLES</span></span>

### <span data-ttu-id="58bad-113">Exempel 1: ta bort ett integrerings konto avtal efter namn</span><span class="sxs-lookup"><span data-stu-id="58bad-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="58bad-114">Det här kommandot tar bort integrerings konto avtalet som heter IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="58bad-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="58bad-115">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="58bad-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="58bad-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58bad-116">PARAMETERS</span></span>

### <span data-ttu-id="58bad-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="58bad-117">-AgreementName</span></span>
<span data-ttu-id="58bad-118">Anger namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="58bad-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="58bad-119">-Force</span><span class="sxs-lookup"><span data-stu-id="58bad-119">-Force</span></span>
<span data-ttu-id="58bad-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="58bad-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58bad-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="58bad-121">-Name</span></span>
<span data-ttu-id="58bad-122">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="58bad-122">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="58bad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58bad-123">-ResourceGroupName</span></span>
<span data-ttu-id="58bad-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58bad-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="58bad-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58bad-125">-Confirm</span></span>
<span data-ttu-id="58bad-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58bad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58bad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58bad-127">-WhatIf</span></span>
<span data-ttu-id="58bad-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58bad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58bad-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58bad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58bad-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bad-130">-DefaultProfile</span></span>
<span data-ttu-id="58bad-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58bad-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58bad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bad-132">CommonParameters</span></span>
<span data-ttu-id="58bad-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58bad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bad-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58bad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bad-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58bad-135">INPUTS</span></span>

## <span data-ttu-id="58bad-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58bad-136">OUTPUTS</span></span>

## <span data-ttu-id="58bad-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58bad-137">NOTES</span></span>

## <span data-ttu-id="58bad-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58bad-138">RELATED LINKS</span></span>

[<span data-ttu-id="58bad-139">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="58bad-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="58bad-140">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="58bad-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="58bad-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="58bad-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)

